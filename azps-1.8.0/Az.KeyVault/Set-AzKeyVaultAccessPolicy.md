---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 55cdc385c5cdf291db15399f4fd587b9b10ce308
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93786620"
---
# <span data-ttu-id="24fc1-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24fc1-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="24fc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="24fc1-103">Concede ou modifica permissões existentes para um usuário, aplicativo ou grupo de segurança para executar operações com um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="24fc1-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="24fc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24fc1-104">SYNTAX</span></span>

### <span data-ttu-id="24fc1-105">ByUserPrincipalName (padrão)</span><span class="sxs-lookup"><span data-stu-id="24fc1-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24fc1-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="24fc1-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fc1-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="24fc1-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24fc1-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="24fc1-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24fc1-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="24fc1-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fc1-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="24fc1-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fc1-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="24fc1-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24fc1-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="24fc1-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24fc1-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="24fc1-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24fc1-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="24fc1-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fc1-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="24fc1-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fc1-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="24fc1-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24fc1-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="24fc1-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fc1-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="24fc1-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fc1-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="24fc1-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24fc1-120">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24fc1-120">DESCRIPTION</span></span>
<span data-ttu-id="24fc1-121">O cmdlet **set-AzKeyVaultAccessPolicy** concede ou modifica permissões existentes para um usuário, aplicativo ou grupo de segurança para executar as operações especificadas com um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="24fc1-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="24fc1-122">Ele não modifica as permissões que outros usuários, aplicativos ou grupos de segurança têm no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="24fc1-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="24fc1-123">Se você estiver definindo permissões para um grupo de segurança, essa operação afetará apenas os usuários desse grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="24fc1-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="24fc1-124">Todos os diretórios a seguir devem ser do mesmo diretório do Azure:</span><span class="sxs-lookup"><span data-stu-id="24fc1-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="24fc1-125">O diretório padrão da assinatura do Azure em que o cofre de chaves reside.</span><span class="sxs-lookup"><span data-stu-id="24fc1-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="24fc1-126">O diretório do Azure que contém o usuário ou o grupo de aplicativos aos quais você está concedendo permissões.</span><span class="sxs-lookup"><span data-stu-id="24fc1-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="24fc1-127">Exemplos de cenários quando essas condições não são atendidas e esse cmdlet não funcionará:</span><span class="sxs-lookup"><span data-stu-id="24fc1-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="24fc1-128">Autorizar um usuário de outra organização a gerenciar seu cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="24fc1-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="24fc1-129">Cada organização tem seu próprio diretório.</span><span class="sxs-lookup"><span data-stu-id="24fc1-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="24fc1-130">Sua conta do Azure tem vários diretórios.</span><span class="sxs-lookup"><span data-stu-id="24fc1-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="24fc1-131">Se você registrar um aplicativo em um diretório diferente do diretório padrão, não poderá autorizar esse aplicativo a usar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="24fc1-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="24fc1-132">O aplicativo deve estar no diretório padrão.</span><span class="sxs-lookup"><span data-stu-id="24fc1-132">The application must be in the default directory.</span></span>
<span data-ttu-id="24fc1-133">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="24fc1-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="24fc1-134">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24fc1-134">EXAMPLES</span></span>

### <span data-ttu-id="24fc1-135">Exemplo 1: conceder permissões a um usuário para um cofre de chaves e modificar as permissões</span><span class="sxs-lookup"><span data-stu-id="24fc1-135">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

<span data-ttu-id="24fc1-136">O primeiro comando concede permissões para um usuário em seu Active Directory do Azure, PattiFuller@contoso.com para executar operações em chaves e segredos com um cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="24fc1-136">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="24fc1-137">O parâmetro *PassThru* resulta no objeto atualizado sendo retornado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24fc1-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="24fc1-138">O segundo comando modifica as permissões que foram concedidas ao PattiFuller@contoso.com primeiro comando, a fim de permitir a obtenção de segredos, além de definir e excluir essas permissões.</span><span class="sxs-lookup"><span data-stu-id="24fc1-138">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="24fc1-139">As permissões para operações de chave permanecem inalteradas após esse comando.</span><span class="sxs-lookup"><span data-stu-id="24fc1-139">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="24fc1-140">O último comando modifica as permissões existentes para PattiFuller@contoso.com remover todas as permissões para operações de chave.</span><span class="sxs-lookup"><span data-stu-id="24fc1-140">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="24fc1-141">As permissões para operações secretas permanecem inalteradas após esse comando.</span><span class="sxs-lookup"><span data-stu-id="24fc1-141">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="24fc1-142">Exemplo 2: conceder permissões para uma entidade de serviço de aplicativo para ler e gravar segredos</span><span class="sxs-lookup"><span data-stu-id="24fc1-142">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="24fc1-143">Esse comando concede permissões para um aplicativo para um cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="24fc1-143">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="24fc1-144">O parâmetro *servicePrincipalName* especifica o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24fc1-144">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="24fc1-145">O aplicativo deve ser registrado no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24fc1-145">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="24fc1-146">*O valor do parâmetro servicePrincipalName* deve ser o nome principal do aplicativo ou o GUID da ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24fc1-146">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="24fc1-147">Este exemplo especifica o nome principal do serviço `http://payroll.contoso.com` , e o comando concede as permissões do aplicativo para ler e gravar segredos.</span><span class="sxs-lookup"><span data-stu-id="24fc1-147">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="24fc1-148">Exemplo 3: conceder permissões para um aplicativo usando sua ID de objeto</span><span class="sxs-lookup"><span data-stu-id="24fc1-148">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="24fc1-149">Esse comando concede as permissões do aplicativo para ler e gravar segredos.</span><span class="sxs-lookup"><span data-stu-id="24fc1-149">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="24fc1-150">Este exemplo especifica o aplicativo que usa a ID de objeto da entidade de serviço do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24fc1-150">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="24fc1-151">Exemplo 4: conceder permissões para um nome de usuário principal</span><span class="sxs-lookup"><span data-stu-id="24fc1-151">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="24fc1-152">Esse comando concede a obter, listar e definir permissões para o nome principal do usuário especificado para acessar os segredos.</span><span class="sxs-lookup"><span data-stu-id="24fc1-152">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="24fc1-153">Exemplo 5: habilitar os segredos para serem recuperados de um cofre de chaves pelo provedor de recursos Microsoft. Compute</span><span class="sxs-lookup"><span data-stu-id="24fc1-153">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="24fc1-154">Esse comando concede as permissões para que os segredos sejam recuperados do cofre da chave Contoso03Vault pelo provedor de recursos Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="24fc1-154">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="24fc1-155">Exemplo 6: conceder permissões a um grupo de segurança</span><span class="sxs-lookup"><span data-stu-id="24fc1-155">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="24fc1-156">O primeiro comando usa o cmdlet Get-AzADGroup para obter todos os grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24fc1-156">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="24fc1-157">Na saída, você verá 3 grupos retornados, chamados **grupo1** , **group2** e **Group3**.</span><span class="sxs-lookup"><span data-stu-id="24fc1-157">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="24fc1-158">Vários grupos podem ter o mesmo nome, mas sempre têm um ObjectId exclusivo.</span><span class="sxs-lookup"><span data-stu-id="24fc1-158">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="24fc1-159">Quando mais de um grupo com o mesmo nome for retornado, use o ObjectId na saída para identificar o que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="24fc1-159">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="24fc1-160">Em seguida, você usa a saída desse comando com Set-AzKeyVaultAccessPolicy para conceder permissões a group2 para o seu cofre de chaves, chamado **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="24fc1-160">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="24fc1-161">Este exemplo enumera os grupos chamados "group2" embutidos na mesma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="24fc1-161">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="24fc1-162">Pode haver vários grupos na lista retornada com o nome "group2".</span><span class="sxs-lookup"><span data-stu-id="24fc1-162">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="24fc1-163">Este exemplo escolhe o primeiro, indicado pelo índice \[ 0 \] na lista retornada.</span><span class="sxs-lookup"><span data-stu-id="24fc1-163">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="24fc1-164">Exemplo 7: conceder ao Azure acesso à proteção de informações à chave locatário gerenciada pelo cliente (BYOK)</span><span class="sxs-lookup"><span data-stu-id="24fc1-164">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="24fc1-165">Esse comando autoriza a proteção de informações do Azure a usar uma chave gerenciada pelo cliente (a traga sua própria chave ou o cenário "BYOK") como a chave locatário do Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="24fc1-165">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="24fc1-166">Ao executar esse comando, especifique seu próprio nome do cofre de chaves, mas você deve especificar o parâmetro *servicePrincipalName* com o GUID **00000012-0000-0000-C000-000000000000** e especificar as permissões no exemplo.</span><span class="sxs-lookup"><span data-stu-id="24fc1-166">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="24fc1-167">OS</span><span class="sxs-lookup"><span data-stu-id="24fc1-167">PARAMETERS</span></span>

### <span data-ttu-id="24fc1-168">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="24fc1-168">-ApplicationId</span></span>
<span data-ttu-id="24fc1-169">Para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="24fc1-169">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-170">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="24fc1-170">-BypassObjectIdValidation</span></span>
<span data-ttu-id="24fc1-171">Permite que você especifique uma ID de objeto sem validar que o objeto existe no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24fc1-171">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="24fc1-172">Use esse parâmetro somente se você quiser conceder acesso ao seu cofre de chaves a uma ID de objeto que se refere a um grupo de segurança delegado de outro locatário do Azure.</span><span class="sxs-lookup"><span data-stu-id="24fc1-172">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24fc1-173">-DefaultProfile</span></span>
<span data-ttu-id="24fc1-174">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="24fc1-174">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-175">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="24fc1-175">-EmailAddress</span></span>
<span data-ttu-id="24fc1-176">Especifica o endereço de email do usuário para o qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="24fc1-176">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="24fc1-177">Esse endereço de email deve existir no diretório associado à assinatura atual e ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="24fc1-177">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-178">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="24fc1-178">-EnabledForDeployment</span></span>
<span data-ttu-id="24fc1-179">Habilita o provedor de recursos Microsoft. Compute a recuperar segredos deste cofre de chaves quando esse cofre de chaves é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="24fc1-179">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-180">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="24fc1-180">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="24fc1-181">Habilita o serviço de criptografia de disco do Azure a obter segredos e a desencapsulação de chaves deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="24fc1-181">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-182">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="24fc1-182">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="24fc1-183">Permite que o Azure Resource Manager obtenha os segredos deste cofre de chaves quando esse cofre de chaves é referenciado em uma implantação de modelo.</span><span class="sxs-lookup"><span data-stu-id="24fc1-183">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-184">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24fc1-184">-InputObject</span></span>
<span data-ttu-id="24fc1-185">Objeto do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="24fc1-185">Key Vault Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-186">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="24fc1-186">-ObjectId</span></span>
<span data-ttu-id="24fc1-187">Especifica a ID de objeto da entidade de usuário ou serviço do Azure Active Directory para a qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="24fc1-187">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-188">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24fc1-188">-PassThru</span></span>
<span data-ttu-id="24fc1-189">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="24fc1-189">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="24fc1-190">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="24fc1-190">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-191">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="24fc1-191">-PermissionsToCertificates</span></span>
<span data-ttu-id="24fc1-192">Especifica uma matriz de permissões de certificado a serem concedidas a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="24fc1-192">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="24fc1-193">Os valores aceitáveis para esse parâmetro:</span><span class="sxs-lookup"><span data-stu-id="24fc1-193">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="24fc1-194">Obter</span><span class="sxs-lookup"><span data-stu-id="24fc1-194">Get</span></span>
- <span data-ttu-id="24fc1-195">Programação</span><span class="sxs-lookup"><span data-stu-id="24fc1-195">List</span></span>
- <span data-ttu-id="24fc1-196">Remover</span><span class="sxs-lookup"><span data-stu-id="24fc1-196">Delete</span></span>
- <span data-ttu-id="24fc1-197">Criados</span><span class="sxs-lookup"><span data-stu-id="24fc1-197">Create</span></span>
- <span data-ttu-id="24fc1-198">Importações</span><span class="sxs-lookup"><span data-stu-id="24fc1-198">Import</span></span>
- <span data-ttu-id="24fc1-199">Atualização</span><span class="sxs-lookup"><span data-stu-id="24fc1-199">Update</span></span>
- <span data-ttu-id="24fc1-200">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="24fc1-200">Managecontacts</span></span>
- <span data-ttu-id="24fc1-201">Emissors</span><span class="sxs-lookup"><span data-stu-id="24fc1-201">Getissuers</span></span>
- <span data-ttu-id="24fc1-202">Listissuers</span><span class="sxs-lookup"><span data-stu-id="24fc1-202">Listissuers</span></span>
- <span data-ttu-id="24fc1-203">Emissores</span><span class="sxs-lookup"><span data-stu-id="24fc1-203">Setissuers</span></span>
- <span data-ttu-id="24fc1-204">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="24fc1-204">Deleteissuers</span></span>
- <span data-ttu-id="24fc1-205">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="24fc1-205">Manageissuers</span></span>
- <span data-ttu-id="24fc1-206">Gravação</span><span class="sxs-lookup"><span data-stu-id="24fc1-206">Recover</span></span>
- <span data-ttu-id="24fc1-207">Fazer</span><span class="sxs-lookup"><span data-stu-id="24fc1-207">Backup</span></span>
- <span data-ttu-id="24fc1-208">Restaurar</span><span class="sxs-lookup"><span data-stu-id="24fc1-208">Restore</span></span>
- <span data-ttu-id="24fc1-209">Purga</span><span class="sxs-lookup"><span data-stu-id="24fc1-209">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-210">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="24fc1-210">-PermissionsToKeys</span></span>
<span data-ttu-id="24fc1-211">Especifica uma matriz de permissões de operações de chave a serem concedidas a um usuário ou serviço principal.</span><span class="sxs-lookup"><span data-stu-id="24fc1-211">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="24fc1-212">Os valores aceitáveis para esse parâmetro:</span><span class="sxs-lookup"><span data-stu-id="24fc1-212">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="24fc1-213">Criptografá</span><span class="sxs-lookup"><span data-stu-id="24fc1-213">Decrypt</span></span>
- <span data-ttu-id="24fc1-214">Com</span><span class="sxs-lookup"><span data-stu-id="24fc1-214">Encrypt</span></span>
- <span data-ttu-id="24fc1-215">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="24fc1-215">UnwrapKey</span></span>
- <span data-ttu-id="24fc1-216">WrapKey</span><span class="sxs-lookup"><span data-stu-id="24fc1-216">WrapKey</span></span>
- <span data-ttu-id="24fc1-217">Verificar</span><span class="sxs-lookup"><span data-stu-id="24fc1-217">Verify</span></span>
- <span data-ttu-id="24fc1-218">Designa</span><span class="sxs-lookup"><span data-stu-id="24fc1-218">Sign</span></span>
- <span data-ttu-id="24fc1-219">Obter</span><span class="sxs-lookup"><span data-stu-id="24fc1-219">Get</span></span>
- <span data-ttu-id="24fc1-220">Programação</span><span class="sxs-lookup"><span data-stu-id="24fc1-220">List</span></span>
- <span data-ttu-id="24fc1-221">Atualização</span><span class="sxs-lookup"><span data-stu-id="24fc1-221">Update</span></span>
- <span data-ttu-id="24fc1-222">Criados</span><span class="sxs-lookup"><span data-stu-id="24fc1-222">Create</span></span>
- <span data-ttu-id="24fc1-223">Importações</span><span class="sxs-lookup"><span data-stu-id="24fc1-223">Import</span></span>
- <span data-ttu-id="24fc1-224">Remover</span><span class="sxs-lookup"><span data-stu-id="24fc1-224">Delete</span></span>
- <span data-ttu-id="24fc1-225">Fazer</span><span class="sxs-lookup"><span data-stu-id="24fc1-225">Backup</span></span>
- <span data-ttu-id="24fc1-226">Restaurar</span><span class="sxs-lookup"><span data-stu-id="24fc1-226">Restore</span></span>
- <span data-ttu-id="24fc1-227">Gravação</span><span class="sxs-lookup"><span data-stu-id="24fc1-227">Recover</span></span>
- <span data-ttu-id="24fc1-228">Purga</span><span class="sxs-lookup"><span data-stu-id="24fc1-228">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-229">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="24fc1-229">-PermissionsToSecrets</span></span>
<span data-ttu-id="24fc1-230">Especifica uma matriz de permissões de operação secreta a serem concedidas a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="24fc1-230">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="24fc1-231">Os valores aceitáveis para esse parâmetro:</span><span class="sxs-lookup"><span data-stu-id="24fc1-231">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="24fc1-232">Obter</span><span class="sxs-lookup"><span data-stu-id="24fc1-232">Get</span></span>
- <span data-ttu-id="24fc1-233">Programação</span><span class="sxs-lookup"><span data-stu-id="24fc1-233">List</span></span>
- <span data-ttu-id="24fc1-234">Configurar</span><span class="sxs-lookup"><span data-stu-id="24fc1-234">Set</span></span>
- <span data-ttu-id="24fc1-235">Remover</span><span class="sxs-lookup"><span data-stu-id="24fc1-235">Delete</span></span>
- <span data-ttu-id="24fc1-236">Fazer</span><span class="sxs-lookup"><span data-stu-id="24fc1-236">Backup</span></span>
- <span data-ttu-id="24fc1-237">Restaurar</span><span class="sxs-lookup"><span data-stu-id="24fc1-237">Restore</span></span>
- <span data-ttu-id="24fc1-238">Gravação</span><span class="sxs-lookup"><span data-stu-id="24fc1-238">Recover</span></span>
- <span data-ttu-id="24fc1-239">Purga</span><span class="sxs-lookup"><span data-stu-id="24fc1-239">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-240">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="24fc1-240">-PermissionsToStorage</span></span>
<span data-ttu-id="24fc1-241">Especifica as permissões da conta de armazenamento gerenciado e da operação de definição SaS a serem concedidas a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="24fc1-241">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-242">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24fc1-242">-ResourceGroupName</span></span>
<span data-ttu-id="24fc1-243">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24fc1-243">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-244">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24fc1-244">-ResourceId</span></span>
<span data-ttu-id="24fc1-245">ID do recurso do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="24fc1-245">Key Vault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-246">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="24fc1-246">-ServicePrincipalName</span></span>
<span data-ttu-id="24fc1-247">Especifica o nome principal do serviço do aplicativo para o qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="24fc1-247">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="24fc1-248">Especifique o ID do aplicativo, também conhecido como ID do cliente, registrado para o aplicativo no diretório AzureActive.</span><span class="sxs-lookup"><span data-stu-id="24fc1-248">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="24fc1-249">O aplicativo com o nome da entidade de serviço que esse parâmetro especifica deve ser registrado no diretório do Azure que contém sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="24fc1-249">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-250">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="24fc1-250">-UserPrincipalName</span></span>
<span data-ttu-id="24fc1-251">Especifica o nome UPN do usuário a quem conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="24fc1-251">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="24fc1-252">Este nome de usuário principal deve existir no diretório associado à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="24fc1-252">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-253">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="24fc1-253">-VaultName</span></span>
<span data-ttu-id="24fc1-254">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="24fc1-254">Specifies the name of a key vault.</span></span>
<span data-ttu-id="24fc1-255">Esse cmdlet modifica a política de acesso para o cofre de chaves que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="24fc1-255">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-256">-Confirme</span><span class="sxs-lookup"><span data-stu-id="24fc1-256">-Confirm</span></span>
<span data-ttu-id="24fc1-257">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24fc1-257">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24fc1-258">-WhatIf</span></span>
<span data-ttu-id="24fc1-259">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24fc1-259">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24fc1-260">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24fc1-260">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fc1-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24fc1-261">CommonParameters</span></span>
<span data-ttu-id="24fc1-262">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24fc1-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24fc1-263">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24fc1-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24fc1-264">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24fc1-264">INPUTS</span></span>

### <span data-ttu-id="24fc1-265">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="24fc1-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="24fc1-266">System. String</span><span class="sxs-lookup"><span data-stu-id="24fc1-266">System.String</span></span>

## <span data-ttu-id="24fc1-267">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24fc1-267">OUTPUTS</span></span>

### <span data-ttu-id="24fc1-268">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="24fc1-268">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="24fc1-269">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24fc1-269">NOTES</span></span>

## <span data-ttu-id="24fc1-270">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24fc1-270">RELATED LINKS</span></span>

[<span data-ttu-id="24fc1-271">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="24fc1-271">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="24fc1-272">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24fc1-272">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

