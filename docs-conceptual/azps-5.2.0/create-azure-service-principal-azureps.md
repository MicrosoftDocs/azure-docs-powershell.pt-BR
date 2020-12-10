---
title: Usar as entidades de serviço do Azure com o Azure PowerShell
description: Saiba como criar e usar entidades de serviço com o Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.service: azure-powershell
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: a5640ded6fc8c6478084374f7808450f6a99d6e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856110"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Criar uma entidade de serviço do Azure com o Azure PowerShell

Ferramentas automatizadas que usam os serviços do Azure devem sempre ter permissões restritas. Em vez de os aplicativos entrarem como um usuário com privilégio total, o Azure oferece as entidades de serviço.

Uma entidade de serviço do Azure é uma identidade criada para uso com aplicativos, serviços hospedados e ferramentas automatizadas para acessar os recursos do Azure. Esse acesso é restrito pelas funções atribuídas à entidade de serviço, oferecendo a você o controle sobre quais recursos poderão ser acessados e em qual nível. Por motivos de segurança, é sempre recomendado usar entidades de serviço com ferramentas automatizadas em vez de permitir a entrada com uma identidade de usuário.

Este artigo mostra as etapas para criar, obter informações e redefinir uma entidade de serviço com o Azure PowerShell.

> [!WARNING]
> Quando você cria uma entidade de serviço usando o comando [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal), a saída inclui as credenciais que você precisa proteger. Lembre-se de não incluir essas credenciais em seu código ou de verificar as credenciais em seu controle do código-fonte. Como alternativa, considere usar [identidades gerenciadas](/azure/active-directory/managed-identities-azure-resources/overview) para evitar a necessidade de usar credenciais.
>
> Por padrão, [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) atribui a função [Colaborador](/azure/role-based-access-control/built-in-roles#contributor) à entidade de serviço no escopo da assinatura. Para reduzir o risco de uma entidade de serviço comprometida, atribua uma função mais específica e restrinja o escopo a um recurso ou grupo de recursos. Confira [Etapas para adicionar uma atribuição de função](/azure/role-based-access-control/role-assignments-steps) para obter mais informações.

## <a name="create-a-service-principal"></a>Criar uma entidade de serviço

Criar uma entidade de serviço com o cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal). Ao criar uma entidade de serviço, você pode escolher o tipo de autenticação de entrada usada.

> [!NOTE]
> Se a sua conta não tiver permissão para criar uma entidade de serviço, `New-AzADServicePrincipal` retornará a mensagem de erro "Privilégios insuficientes para concluir a operação".
> Entre em contato com o administrador do Azure Active Directory para criar uma entidade de serviço.

Há dois tipos de autenticação disponíveis para as entidades de serviço: A autenticação baseada em senha e em certificado.

### <a name="password-based-authentication"></a>Autenticação baseada em senha

> [!IMPORTANT]
> A função padrão de uma entidade de serviço de autenticação baseada em senha é **Colaborador**. Essa função tem permissões completas para ler e gravar em uma conta do Azure. Para obter informações sobre como gerenciar atribuições de função, confira [Gerenciar funções de entidade de serviço](#manage-service-principal-roles).

Sem outros parâmetros de autenticação, usa-se a autenticação baseada em senha, com uma senha aleatória criada para você. Caso queira uma autenticação baseada em senha, esse método é recomendado.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

O objeto retornado contém o membro `Secret`, que é um `SecureString` que contém a senha gerada. Armazene esse valor em algum lugar seguro para autenticar com a entidade de serviço. Seu valor _não_ será exibido na saída do console. Se você perder a senha, [redefina as credenciais da entidade de serviço](#reset-credentials).

O código a seguir permitirá que você exporte o segredo:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

Para senhas fornecidas pelo usuário, o argumento `-PasswordCredential` usa os objetos `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`. Esses objetos devem ter uma validade `StartDate` e `EndDate`, além de usar um texto sem formatação `Password`. Quando criar uma senha, certifique-se de seguir as [Regras e restrições de senha do Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).
Não use uma senha fraca, nem reutilize uma senha.

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

O objeto retornado por `New-AzADServicePrincipal` contém os membros `Id` e `DisplayName`, os quais podem ser usados para entrar com a entidade de serviço.

> [!IMPORTANT]
> Para entrar com uma entidade de serviço é preciso ter a ID do locatário que serviu de base para a criação da entidade de serviço. Para obter o locatário ativo de quando a entidade de serviço foi criada, execute o comando seguinte _imediatamente após_ a criação da entidade de serviço:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a>Autenticação baseada em certificado

> [!IMPORTANT]
> Não há nenhuma função padrão atribuída ao criar uma entidade de serviço de autenticação baseada em certificado. Para obter informações sobre como gerenciar atribuições de função, confira [Gerenciar funções de entidade de serviço](#manage-service-principal-roles).

As entidades de serviço que usam a autenticação baseada em certificado são criadas com o parâmetro `-CertValue`. Esse parâmetro usa uma cadeia de caracteres ASCII codificada em base64 do certificado público. Isso é representado por um arquivo PEM ou por um CRT ou CER com texto codificado. Não há suporte para codificações binárias do certificado público. Essas instruções pressupõem que você já tenha um certificado disponível.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

Você também pode usar o parâmetro `-KeyCredential`, que usa objetos `PSADKeyCredential`. Esses objetos devem ter um `StartDate` e `EndDate` válidos, além do membro `CertValue` definido como uma cadeia de caracteres ASCII codificada com base64 do certificado público.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

O objeto retornado por `New-AzADServicePrincipal` contém os membros `Id` e `DisplayName`, os quais podem ser usados para entrar com a entidade de serviço. Os clientes que entram com a entidade de serviço também precisam acessar a chave privada do certificado.

> [!IMPORTANT]
> Para entrar com uma entidade de serviço é preciso ter a ID do locatário que serviu de base para a criação da entidade de serviço. Para obter o locatário ativo de quando a entidade de serviço foi criada, execute o comando seguinte _imediatamente após_ a criação da entidade de serviço:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a>Obter uma entidade de serviço existente

Uma lista de entidades de serviço do locatário ativo pode ser recuperada com [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal). Por padrão, esse comando retorna _todas_ as entidades de serviço em um locatário. Para grandes organizações, pode levar muito tempo para retornar resultados. Em vez disso, recomenda-se usar um dos argumentos de filtragem opcionais do lado do servidor:

- `-DisplayNameBeginsWith` solicita entidades de serviço que tenham um _prefixo_ que corresponda ao valor fornecido. O nome de exibição de uma entidade de serviço é o valor definido com `-DisplayName` durante a criação.
- `-DisplayName` solicita uma _correspondência exata_ de um nome da entidade de serviço.

## <a name="manage-service-principal-roles"></a>Gerenciar funções da entidade de serviço

O Azure PowerShell tem os seguintes cmdlets para gerenciar atribuições de função:

- [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
- [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
- [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

A função padrão de uma entidade de serviço de autenticação baseada em senha é **Colaborador**. Essa função tem permissões completas para ler e gravar em uma conta do Azure. A função **Leitor** é mais restritiva, com acesso somente leitura. Para obter mais informações sobre o Controle de Acesso Baseado em Função (RBAC) e funções, confira [RBAC: funções internas](/azure/active-directory/role-based-access-built-in-roles).

Esse exemplo adiciona a função **Leitor** e exclui a função **Colaborador**:

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> Os cmdlets de atribuição de função não usam a ID de objeto da entidade de serviço. Eles usam a ID do aplicativo associado, que é gerada no momento da criação. Para obter a ID do aplicativo para uma entidade de serviço, use `Get-AzADServicePrincipal`.

> [!NOTE]
> Caso sua conta não tenha permissão para atribuir uma função, você verá uma mensagem de erro informando que a sua conta "não tem autorização para executar a ação 'Microsoft.Authorization/roleAssignments/write'". Entre em contato com o administrador do Azure Active Directory para gerenciar funções.

Adicionar uma função _não_ restringe as permissões atribuídas anteriormente. Ao restringir as permissões da entidade de serviço, a função **Colaborador** deverá ser removida.

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
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

Para obter instruções sobre como importar um certificado em um armazenamento de credenciais acessível pelo PowerShell, confira [Entrar com o Azure PowerShell](authenticate-azureps.md#sp-signin)

## <a name="reset-credentials"></a>Redefinir credenciais

Se você esquecer as credenciais de uma entidade de serviço, use o comando [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) para adicionar uma nova credencial com uma senha aleatória. Esse cmdlet não dá suporte a credenciais definidas pelo usuário ao redefinir a senha.

> [!IMPORTANT]
> Antes de atribuir quaisquer novas credenciais, talvez seja interessante remover as credenciais existentes para evitar entrar com elas. Para fazer isso, use o cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a>Solução de problemas

Se você receber o erro: _"New-AzADServicePrincipal: Outro objeto com o mesmo valor para a propriedade identifierUris já existe."_ Verifique se não existe uma entidade de serviço com o mesmo nome.

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Se a entidade de serviço existente não for mais necessária, você poderá removê-la usando o exemplo a seguir.

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Esse erro também pode ocorrer quando você criou uma entidade de serviço anteriormente para um aplicativo do Azure Active Directory. Se você remover a entidade de serviço, o aplicativo ainda estará disponível. Esse aplicativo impede que você crie outra entidade de serviço com o mesmo nome.

Você pode usar o seguinte exemplo para verificar se não existe um aplicativo do Azure Active Directory com o mesmo nome:

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

Se um aplicativo com o mesmo nome existir e não for mais necessário, ele poderá ser removido usando o exemplo a seguir.

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

Caso contrário, escolha um nome alternativo para a entidade de serviço que você está tentando criar.
