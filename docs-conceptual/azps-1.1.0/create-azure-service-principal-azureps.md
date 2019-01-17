---
title: Criar uma entidade de serviço do Azure com o Azure PowerShell
description: Saiba como criar uma entidade de serviço para seu aplicativo ou serviço com o Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54341870"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Criar uma entidade de serviço do Azure com o Azure PowerShell

Se você planeja gerenciar seu aplicativo ou serviço com o Azure PowerShell, execute-o em uma entidade de serviço do Azure Active Directory (AAD), em vez de suas próprias credenciais. Este artigo serve de guia para você criar uma entidade de segurança com o Azure PowerShell.

## <a name="what-is-a-service-principal"></a>O que é uma entidade de serviço?

Uma entidade de serviço do Azure é uma identidade de segurança usada por aplicativos criados pelo usuário, serviços e ferramentas de automação para acessar recursos específicos do Azure. As entidades de serviço recebem permissões específicas relacionadas às suas tarefas, dando a você um melhor controle de segurança. Isso é diferente de uma identidade de usuário geral, que geralmente está autorizada a fazer alterações.

## <a name="verify-your-own-permission-level"></a>Verificar seu próprio nível de permissão

Primeiro, você deve ter permissões suficientes no Azure Active Directory e em sua assinatura do Azure. Você deve ser capaz de criar um aplicativo no Active Directory e atribuir uma função à entidade de serviço.

A maneira mais fácil de verificar se a sua conta tem as permissões certas é por meio do portal. Consulte [Verificar permissão necessária no portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Criar uma entidade de serviço para seu aplicativo

Após entrar na sua conta do Azure, você poderá criar a entidade de serviço. Você deve ter uma das maneiras a seguir para identificar seu aplicativo implantado:

* O nome exclusivo do seu aplicativo implantado, como "MyDemoWebApp" nos exemplos a seguir
* A ID do Aplicativo, o GUID exclusivo associado ao seu aplicativo, serviço ou objeto implantado

### <a name="get-information-about-your-application"></a>Obter informações sobre seu aplicativo

O cmdlet `Get-AzADApplication` pode ser usado para obter informações sobre seu aplicativo.

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a>Criar uma entidade de serviço para seu aplicativo

O cmdlet `New-AzADServicePrincipal` é usado para criar a entidade de serviço.

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

A partir daqui, você pode também usar diretamente a propriedade `$servicePrincipal.Secret` como um argumento para `Connect-AzAccount` (confira "Entrar usando a entidade de serviço"), ou você pode converter esta `SecureString` para uma cadeia de caracteres de texto sem formatação:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a>Entrar usando a entidade de serviço

Agora você pode entrar como a nova entidade de serviço para seu aplicativo usando a `appId` que você forneceu e a `password` que foi  
gerada. Você também precisa da ID do Locatário para a entidade de serviço. Sua ID do Locatário é exibida quando você entra no Azure com suas credenciais pessoais. Para entrar com uma entidade de serviço, use os comandos:

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Após conseguir entrar, você verá um resultado do tipo:

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

Parabéns! Você pode usar essas credenciais para executar seu aplicativo. Em seguida, será necessário ajustar as permissões da entidade de serviço.

## <a name="managing-roles"></a>Gerenciamento de funções

> [!NOTE]
> O RBAC (Controle de Acesso do Azure Baseado em Função) é um modelo para definir e gerenciar funções para entidades de usuário e de serviço. As funções têm conjuntos de permissões associados a elas, que determinam os recursos que uma entidade pode ler, acessar, gravar ou gerenciar. Para saber mais sobre RBAC e funções, veja [RBAC: Funções internas](/azure/active-directory/role-based-access-built-in-roles).

O Azure PowerShell fornece os seguintes cmdlets para gerenciar atribuições de função:

* [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
* [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
* [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

A função padrão para uma entidade de serviço é **Colaborador**. Pode não ser a melhor opção, dependendo do escopo das interações do seu aplicativo com os serviços do Azure, dadas suas permissões amplas.
A função **Leitor** é mais restritiva e pode ser uma boa opção para aplicativos somente leitura. Você pode exibir detalhes sobre as permissões específicas de função ou criar conectores personalizados por meio do portal do Azure.

Neste exemplo, adicionamos a função **Leitor** ao nosso exemplo anterior e excluímos a função **Colaborador**:

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

Para exibir as funções atuais atribuídas:

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

Outros cmdlets do Azure PowerShell para gerenciamento de funções:

* [Get-AzRoleDefinition](/powershell/module/az.resources/Get-azRoleDefinition)
* [New-AzRoleDefinition](/powershell/module/az.resources/New-azRoleDefinition)
* [Remove-AzRoleDefinition](/powershell/module/az.resources/Remove-azRoleDefinition)
* [Set-AzRoleDefinition](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Alterar as credenciais da entidade de segurança

É uma boa prática de segurança examinar as permissões e atualizar a senha regularmente. Talvez você queira gerenciar e modificar as credenciais de segurança à medida que seu aplicativo muda. Por exemplo, podemos alterar a senha da entidade de serviço criando uma nova senha e removendo a antiga.

### <a name="add-a-new-password-for-the-service-principal"></a>Adicionar uma nova senha para a entidade de serviço

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>Obter uma lista de credenciais para a entidade de serviço

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>Remover a senha antiga da entidade de serviço

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>Verificar a lista de credenciais para a entidade de serviço

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a>Obter informações sobre a entidade de serviço

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
