---
title: Usar as entidades de serviço do Azure com o Azure PowerShell
description: Saiba como criar e usar entidades de serviço com o Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: 4c47d2bac2c63f13ac0ebbccda3e2eed12cd658f
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062370"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Criar uma entidade de serviço do Azure com o Azure PowerShell

Ferramentas automatizadas que usam os serviços do Azure devem sempre ter permissões restritas. Em vez de os aplicativos entrarem como um usuário com privilégio total, o Azure oferece as entidades de serviço.

Uma entidade de serviço do Azure é uma identidade criada para uso com aplicativos, serviços hospedados e ferramentas automatizadas para acessar os recursos do Azure. Esse acesso é restrito pelas funções atribuídas à entidade de serviço, oferecendo a você o controle sobre quais recursos poderão ser acessados e em qual nível. Por motivos de segurança, é sempre recomendado usar entidades de serviço com ferramentas automatizadas em vez de permitir a entrada com uma identidade de usuário.

Este artigo mostra as etapas para criar, obter informações e redefinir uma entidade de serviço com o Azure PowerShell.

## <a name="create-a-service-principal"></a>Criar uma entidade de serviço

Criar uma entidade de serviço com o cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal). Ao criar uma entidade de serviço, você pode escolher o tipo de autenticação de entrada usada.

> [!NOTE]
>
> Se sua conta não tiver permissão para criar uma entidade de serviço, `New-AzADServicePrincipal` mostrará uma mensagem de erro “Privilégios insuficientes para concluir a operação”. Entre em contato com o administrador do Azure Active Directory para criar uma entidade de serviço.

Há dois tipos de autenticação disponíveis para as entidades de serviço: A autenticação baseada em senha e em certificado.

### <a name="password-based-authentication"></a>Autenticação baseada em senha

Sem outros parâmetros de autenticação, usa-se a autenticação baseada em senha, com uma senha aleatória criada para você. Caso queira uma autenticação baseada em senha, esse método é recomendado.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

O objeto retornado contém o membro `Secret`, que é um `SecureString` que contém a senha gerada. Armazene esse valor em algum lugar seguro para autenticar com a entidade de serviço. Seu valor __não__ será exibido na saída do console. Se você perder a senha, [redefina as credenciais da entidade de serviço](#reset-credentials).

O código a seguir permitirá que você exporte o segredo:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

Para senhas fornecidas pelo usuário, o argumento `-PasswordCredential` usa os objetos `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`. Esses objetos devem ter uma validade `StartDate` e `EndDate`, além de usar um texto sem formatação `Password`. Quando criar uma senha, certifique-se de seguir as [Regras e restrições de senha do Azure Active Directory](/azure/active-directory/active-directory-passwords-policy). Não use uma senha fraca, nem reutilize uma senha.

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

O objeto retornado por `New-AzADServicePrincipal` contém os membros `Id` e `DisplayName`, os quais podem ser usados para entrar com a entidade de serviço.

> [!IMPORTANT]
>
> Para entrar com uma entidade de serviço é preciso ter a ID do locatário que serviu de base para a criação da entidade de serviço. Para obter o locatário ativo de quando a entidade de serviço foi criada, execute o comando seguinte __imediatamente após__ a criação da entidade de serviço:
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a>Autenticação baseada em certificado

As entidades de serviço que usam a autenticação baseada em certificado são criadas com o parâmetro `-CertValue`. Esse parâmetro usa uma cadeia de caracteres ASCII codificada em base64 do certificado público. Isso é representado por um arquivo PEM ou por um CRT ou CER com texto codificado. Não há suporte para codificações binárias do certificado público. Essas instruções pressupõem que você já tenha um certificado disponível.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

Você também pode usar o parâmetro `-KeyCredential`, que usa objetos `PSADKeyCredential`. Esses objetos devem ter um `StartDate` e `EndDate` válidos, além do membro `CertValue` definido como uma cadeia de caracteres ASCII codificada com base64 do certificado público.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

O objeto retornado por `New-AzADServicePrincipal` contém os membros `Id` e `DisplayName`, os quais podem ser usados para entrar com a entidade de serviço. Os clientes que entram com a entidade de serviço também precisam acessar a chave privada do certificado.

> [!IMPORTANT]
>
> Para entrar com uma entidade de serviço é preciso ter a ID do locatário que serviu de base para a criação da entidade de serviço. Para obter o locatário ativo de quando a entidade de serviço foi criada, execute o comando seguinte __imediatamente após__ a criação da entidade de serviço:
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a>Obter uma entidade de serviço existente

Uma lista de entidades de serviço para o locatário ativo no momento pode ser recuperada com [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal). Por padrão, esse comando retorna __todas__ as entidades de serviço em um locatário, ou seja, para grandes organizações, pode demorar bastante para retornar resultados. Em vez disso, recomenda-se usar um dos argumentos de filtragem opcionais do lado do servidor:

* `-DisplayNameBeginsWith` solicita entidades de serviço que tenham um _prefixo_ que corresponda ao valor fornecido. O nome de exibição de uma entidade de serviço é o valor definido com `-DisplayName` durante a criação.
* `-DisplayName` solicita uma _correspondência exata_ de um nome da entidade de serviço.

## <a name="manage-service-principal-roles"></a>Gerenciar funções da entidade de serviço

O Azure PowerShell tem os seguintes cmdlets para gerenciar atribuições de função:

* [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
* [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
* [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

A função padrão para uma entidade de serviço é **Colaborador**. Essa função tem permissões completas para ler e gravar em uma conta do Azure. A função **Leitor** é mais restritiva, com acesso somente leitura.  Para obter mais informações sobre o Controle de Acesso Baseado em Função (RBAC) e funções, confira [RBAC: funções internas](/azure/active-directory/role-based-access-built-in-roles).

Esse exemplo adiciona a função **Leitor** e exclui a função **Colaborador**:

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> Os cmdlets de atribuição de função não usam a ID de objeto da entidade de serviço. Eles usam a ID do aplicativo associado, que é gerada no momento da criação. Para obter a ID do aplicativo para uma entidade de serviço, use `Get-AzADServicePrincipal`.

> [!NOTE]
> Caso sua conta não tenha permissão para atribuir uma função, você verá uma mensagem de erro informando que sua conta “não tem autorização para executar a ação ‘Microsoft.Authorization/roleAssignments/write’”. Entre em contato com o administrador do Azure Active Directory para gerenciar funções.

Adicionar uma função _não_ restringe as permissões atribuídas anteriormente. Ao restringir as permissões da entidade de serviço, a função __Colaborador__ deverá ser removida.

Para verificar as alterações, liste as funções atribuídas:

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a>Entrar usando uma entidade de serviço

Teste as novas credenciais e permissões da entidade de serviço iniciando a sessão. Para entrar com uma entidade de serviço, você precisa do valor `applicationId` associado a ela e do locatário com base no qual ela foi criada.

Para entrar com uma entidade de serviço usando a senha:

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

A autenticação baseada em certificado exige que o Azure PowerShell possa recuperar informações de um repositório de certificados local com base em uma impressão digital do certificado.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

Para obter instruções sobre como importar um certificado em um armazenamento de credenciais acessível pelo PowerShell, confira [Entrar com o Azure PowerShell](authenticate-azureps.md#sp-signin)

## <a name="reset-credentials"></a>Redefinir credenciais

Se você esquecer das credenciais de uma entidade de serviço, use o comando [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) para adicionar uma nova credencial. Esse cmdlet usa os mesmos argumentos e tipos de credencial que `New-AzADServicePrincipal`. Sem nenhum argumento de credencial, é criado um novo `PasswordCredential` com uma senha aleatória.

> [!IMPORTANT]
> Antes de atribuir quaisquer novas credenciais, talvez seja interessante remover as credenciais existentes para evitar entrar com elas. Para fazer isso, use o cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
