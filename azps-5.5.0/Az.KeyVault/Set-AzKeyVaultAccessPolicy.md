---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: eeaea44ec387dc7739a97b5026054186ff817ab3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113095"
---
# <span data-ttu-id="279ad-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="279ad-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="279ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="279ad-102">SYNOPSIS</span></span>
<span data-ttu-id="279ad-103">Concede ou modifica permissões existentes para que um usuário, aplicativo ou grupo de segurança execute operações com um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="279ad-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="279ad-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="279ad-104">SYNTAX</span></span>

### <span data-ttu-id="279ad-105">ByUserPrincipalName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="279ad-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="279ad-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="279ad-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279ad-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="279ad-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="279ad-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="279ad-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="279ad-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="279ad-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279ad-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="279ad-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279ad-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="279ad-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="279ad-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="279ad-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="279ad-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="279ad-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="279ad-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="279ad-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279ad-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="279ad-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279ad-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="279ad-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="279ad-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="279ad-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279ad-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="279ad-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279ad-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="279ad-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="279ad-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="279ad-120">DESCRIPTION</span></span>
<span data-ttu-id="279ad-121">O cmdlet **Set-AzKeyVaultAccessPolicy** concede ou modifica permissões existentes para que um usuário, aplicativo ou grupo de segurança execute as operações especificadas com um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="279ad-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="279ad-122">Ele não modifica as permissões que outros usuários, aplicativos ou grupos de segurança têm no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="279ad-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="279ad-123">Se você estiver definindo permissões para um grupo de segurança, essa operação afetará apenas os usuários desse grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="279ad-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="279ad-124">Os diretórios a seguir devem ser todos do mesmo diretório do Azure:</span><span class="sxs-lookup"><span data-stu-id="279ad-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="279ad-125">O diretório padrão da assinatura do Azure no qual reside o cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="279ad-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="279ad-126">O diretório do Azure que contém o usuário ou o grupo de aplicativos ao qual você está concedendo permissões.</span><span class="sxs-lookup"><span data-stu-id="279ad-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="279ad-127">Exemplos de cenários quando essas condições não são atendidas e este cmdlet não funcionará são:</span><span class="sxs-lookup"><span data-stu-id="279ad-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="279ad-128">Autorizar um usuário de uma organização diferente para gerenciar seu cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="279ad-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="279ad-129">Cada organização tem seu próprio diretório.</span><span class="sxs-lookup"><span data-stu-id="279ad-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="279ad-130">Sua conta do Azure tem vários diretórios.</span><span class="sxs-lookup"><span data-stu-id="279ad-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="279ad-131">Se você registrar um aplicativo em um diretório diferente do diretório padrão, não poderá autorizar esse aplicativo a usar seu cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="279ad-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="279ad-132">O aplicativo deve estar no diretório padrão.</span><span class="sxs-lookup"><span data-stu-id="279ad-132">The application must be in the default directory.</span></span>
<span data-ttu-id="279ad-133">Observe que, embora especificar o grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="279ad-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="279ad-134">Ao usar uma entidade de serviço para conceder permissões de política de acesso, você deve usar o `-BypassObjectIdValidation` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="279ad-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="279ad-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="279ad-135">EXAMPLES</span></span>

### <span data-ttu-id="279ad-136">Exemplo 1: Conceder permissões a um usuário para um cofre de chave e modificar as permissões</span><span class="sxs-lookup"><span data-stu-id="279ad-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="279ad-137">O primeiro comando concede permissões a um usuário no Azure Active Directory para executar operações em chaves e segredos com um cofre de chave chamado PattiFuller@contoso.com Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="279ad-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="279ad-138">O *parâmetro PassThru* resulta no objeto atualizado que está sendo retornado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="279ad-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="279ad-139">O segundo comando modifica as permissões que foram concedidas no primeiro comando, para agora permitir a criação de segredos além de PattiFuller@contoso.com defini-las e excluí-las.</span><span class="sxs-lookup"><span data-stu-id="279ad-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="279ad-140">As permissões para operações de tecla permanecem inalteradas após esse comando.</span><span class="sxs-lookup"><span data-stu-id="279ad-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="279ad-141">O comando final modifica ainda mais as permissões existentes para PattiFuller@contoso.com remover todas as permissões para operações de chave.</span><span class="sxs-lookup"><span data-stu-id="279ad-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="279ad-142">As permissões para operações secretas permanecem inalteradas após esse comando.</span><span class="sxs-lookup"><span data-stu-id="279ad-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="279ad-143">Exemplo 2: Conceder permissões para uma entidade de serviço de aplicativos ler e escrever segredos</span><span class="sxs-lookup"><span data-stu-id="279ad-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="279ad-144">Este comando concede permissões para um aplicativo para um cofre de chave chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="279ad-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="279ad-145">O *parâmetro ServicePrincipalName* especifica o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="279ad-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="279ad-146">O aplicativo deve ser registrado no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="279ad-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="279ad-147">O valor do parâmetro *ServicePrincipalName* deve ser o nome principal do serviço do aplicativo ou o GUID de ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="279ad-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="279ad-148">Este exemplo especifica o nome da entidade de serviço e o comando concede às permissões do aplicativo `http://payroll.contoso.com` para ler e escrever segredos.</span><span class="sxs-lookup"><span data-stu-id="279ad-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="279ad-149">Exemplo 3: Conceder permissões para um aplicativo usando sua ID de objeto</span><span class="sxs-lookup"><span data-stu-id="279ad-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="279ad-150">Esse comando concede aos aplicativos permissões de leitura e gravação de segredos.</span><span class="sxs-lookup"><span data-stu-id="279ad-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="279ad-151">Este exemplo especifica o aplicativo usando a ID de objeto da entidade de serviço do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="279ad-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="279ad-152">Exemplo 4: Conceder permissões para um nome de entidade de usuário</span><span class="sxs-lookup"><span data-stu-id="279ad-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="279ad-153">Esse comando concede permissões de obter, listar e definir permissões para o nome de usuário principal especificado para acesso a segredos.</span><span class="sxs-lookup"><span data-stu-id="279ad-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="279ad-154">Exemplo 5: Habilitar a recuperação de segredos de um cofre de chave pelo provedor de recursos Microsoft.Compute</span><span class="sxs-lookup"><span data-stu-id="279ad-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="279ad-155">Esse comando concede as permissões para que os segredos sejam recuperados do cofre de chave Contoso03Vault pelo provedor de recursos Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="279ad-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="279ad-156">Exemplo 6: Conceder permissões a um grupo de segurança</span><span class="sxs-lookup"><span data-stu-id="279ad-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="279ad-157">O primeiro comando usa o Get-AzADGroup cmdlet para obter todos os grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="279ad-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="279ad-158">Na saída, você vê três grupos retornados, **denominados grupo1,** **grupo2** e **grupo3.**</span><span class="sxs-lookup"><span data-stu-id="279ad-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="279ad-159">Vários grupos podem ter o mesmo nome, mas sempre têm uma ObjectId exclusiva.</span><span class="sxs-lookup"><span data-stu-id="279ad-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="279ad-160">Quando mais de um grupo que tem o mesmo nome for retornado, use a ObjectId na saída para identificar o que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="279ad-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="279ad-161">Em seguida, use a saída deste comando com o Set-AzKeyVaultAccessPolicy para conceder permissões ao grupo2 para o seu cofre de chaves, chamado **myownvault.**</span><span class="sxs-lookup"><span data-stu-id="279ad-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="279ad-162">Este exemplo enumera os grupos denominados "grupo2" em linha na mesma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="279ad-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="279ad-163">Pode haver vários grupos na lista retornada que são chamados de "grupo2".</span><span class="sxs-lookup"><span data-stu-id="279ad-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="279ad-164">Este exemplo escolhe o primeiro, indicado pelo índice \[ 0 \] na lista retornada.</span><span class="sxs-lookup"><span data-stu-id="279ad-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="279ad-165">Exemplo 7: Conceder acesso à Proteção de Informações do Azure à chave de locatário gerenciada pelo cliente (BYOK)</span><span class="sxs-lookup"><span data-stu-id="279ad-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="279ad-166">Este comando autoriza a Proteção de Informações do Azure a usar uma chave gerenciada pelo cliente (o cenário trazer sua própria chave ou "BYOK") como a chave de locatário da Proteção de Informações do Azure.</span><span class="sxs-lookup"><span data-stu-id="279ad-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="279ad-167">Ao executar esse comando, especifique seu próprio nome de cofre de chave, mas você deve especificar o parâmetro *ServicePrincipalName* com o GUID **00000012-0000-0000-c000-00000000000** e especificar as permissões no exemplo.</span><span class="sxs-lookup"><span data-stu-id="279ad-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="279ad-168">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="279ad-168">PARAMETERS</span></span>

### <span data-ttu-id="279ad-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="279ad-169">-ApplicationId</span></span>
<span data-ttu-id="279ad-170">Para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="279ad-170">For future use.</span></span>

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

### <span data-ttu-id="279ad-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="279ad-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="279ad-172">Permite especificar uma ID de objeto sem validar que o objeto existe no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="279ad-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="279ad-173">Use esse parâmetro somente se você quiser conceder acesso ao seu cofre de chave para uma ID de objeto que se refere a um grupo de segurança delegado de outro locatário do Azure.</span><span class="sxs-lookup"><span data-stu-id="279ad-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="279ad-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279ad-174">-DefaultProfile</span></span>
<span data-ttu-id="279ad-175">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="279ad-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="279ad-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="279ad-176">-EmailAddress</span></span>
<span data-ttu-id="279ad-177">Especifica o endereço de email do usuário ao qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="279ad-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="279ad-178">Esse endereço de email deve existir no diretório associado à assinatura atual e ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="279ad-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="279ad-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="279ad-179">-EnabledForDeployment</span></span>
<span data-ttu-id="279ad-180">Permite que o provedor de recursos Microsoft.Compute recupere segredos desse cofre-chave quando esse cofre de chave é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="279ad-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="279ad-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="279ad-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="279ad-182">Habilita o serviço de criptografia de disco do Azure a obter segredos e desembrulhar chaves deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="279ad-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="279ad-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="279ad-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="279ad-184">Permite que o Gerenciador de Recursos do Azure receba segredos desse cofre de chave quando esse cofre de chave for referenciado em uma implantação de modelo.</span><span class="sxs-lookup"><span data-stu-id="279ad-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="279ad-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="279ad-185">-InputObject</span></span>
<span data-ttu-id="279ad-186">Objeto do Cofre de Teclas</span><span class="sxs-lookup"><span data-stu-id="279ad-186">Key Vault Object</span></span>

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

### <span data-ttu-id="279ad-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="279ad-187">-ObjectId</span></span>
<span data-ttu-id="279ad-188">Especifica a ID do objeto da entidade de usuário ou serviço no Azure Active Directory para a qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="279ad-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="279ad-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="279ad-189">-PassThru</span></span>
<span data-ttu-id="279ad-190">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="279ad-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="279ad-191">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="279ad-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="279ad-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="279ad-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="279ad-193">Especifica uma matriz de permissões de certificado para conceder a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="279ad-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="279ad-194">Os valores aceitáveis para este parâmetro:</span><span class="sxs-lookup"><span data-stu-id="279ad-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="279ad-195">Todos</span><span class="sxs-lookup"><span data-stu-id="279ad-195">All</span></span>
- <span data-ttu-id="279ad-196">Obter</span><span class="sxs-lookup"><span data-stu-id="279ad-196">Get</span></span>
- <span data-ttu-id="279ad-197">Lista</span><span class="sxs-lookup"><span data-stu-id="279ad-197">List</span></span>
- <span data-ttu-id="279ad-198">Excluir</span><span class="sxs-lookup"><span data-stu-id="279ad-198">Delete</span></span>
- <span data-ttu-id="279ad-199">Criar</span><span class="sxs-lookup"><span data-stu-id="279ad-199">Create</span></span>
- <span data-ttu-id="279ad-200">Importação</span><span class="sxs-lookup"><span data-stu-id="279ad-200">Import</span></span>
- <span data-ttu-id="279ad-201">Atualização</span><span class="sxs-lookup"><span data-stu-id="279ad-201">Update</span></span>
- <span data-ttu-id="279ad-202">Gerenciar contatos</span><span class="sxs-lookup"><span data-stu-id="279ad-202">Managecontacts</span></span>
- <span data-ttu-id="279ad-203">Getissuers</span><span class="sxs-lookup"><span data-stu-id="279ad-203">Getissuers</span></span>
- <span data-ttu-id="279ad-204">Listissuers</span><span class="sxs-lookup"><span data-stu-id="279ad-204">Listissuers</span></span>
- <span data-ttu-id="279ad-205">Setissuers</span><span class="sxs-lookup"><span data-stu-id="279ad-205">Setissuers</span></span>
- <span data-ttu-id="279ad-206">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="279ad-206">Deleteissuers</span></span>
- <span data-ttu-id="279ad-207">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="279ad-207">Manageissuers</span></span>
- <span data-ttu-id="279ad-208">Recuperar</span><span class="sxs-lookup"><span data-stu-id="279ad-208">Recover</span></span>
- <span data-ttu-id="279ad-209">Backup</span><span class="sxs-lookup"><span data-stu-id="279ad-209">Backup</span></span>
- <span data-ttu-id="279ad-210">Restaurar</span><span class="sxs-lookup"><span data-stu-id="279ad-210">Restore</span></span>
- <span data-ttu-id="279ad-211">Purga</span><span class="sxs-lookup"><span data-stu-id="279ad-211">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279ad-212">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="279ad-212">-PermissionsToKeys</span></span>
<span data-ttu-id="279ad-213">Especifica uma matriz de permissões de operação chave para conceder a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="279ad-213">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="279ad-214">Os valores aceitáveis para este parâmetro:</span><span class="sxs-lookup"><span data-stu-id="279ad-214">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="279ad-215">Todos</span><span class="sxs-lookup"><span data-stu-id="279ad-215">All</span></span>
- <span data-ttu-id="279ad-216">Descriptografar</span><span class="sxs-lookup"><span data-stu-id="279ad-216">Decrypt</span></span>
- <span data-ttu-id="279ad-217">Criptografar</span><span class="sxs-lookup"><span data-stu-id="279ad-217">Encrypt</span></span>
- <span data-ttu-id="279ad-218">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="279ad-218">UnwrapKey</span></span>
- <span data-ttu-id="279ad-219">WrapKey</span><span class="sxs-lookup"><span data-stu-id="279ad-219">WrapKey</span></span>
- <span data-ttu-id="279ad-220">Verificar</span><span class="sxs-lookup"><span data-stu-id="279ad-220">Verify</span></span>
- <span data-ttu-id="279ad-221">Sinal</span><span class="sxs-lookup"><span data-stu-id="279ad-221">Sign</span></span>
- <span data-ttu-id="279ad-222">Obter</span><span class="sxs-lookup"><span data-stu-id="279ad-222">Get</span></span>
- <span data-ttu-id="279ad-223">Lista</span><span class="sxs-lookup"><span data-stu-id="279ad-223">List</span></span>
- <span data-ttu-id="279ad-224">Atualização</span><span class="sxs-lookup"><span data-stu-id="279ad-224">Update</span></span>
- <span data-ttu-id="279ad-225">Criar</span><span class="sxs-lookup"><span data-stu-id="279ad-225">Create</span></span>
- <span data-ttu-id="279ad-226">Importação</span><span class="sxs-lookup"><span data-stu-id="279ad-226">Import</span></span>
- <span data-ttu-id="279ad-227">Excluir</span><span class="sxs-lookup"><span data-stu-id="279ad-227">Delete</span></span>
- <span data-ttu-id="279ad-228">Backup</span><span class="sxs-lookup"><span data-stu-id="279ad-228">Backup</span></span>
- <span data-ttu-id="279ad-229">Restaurar</span><span class="sxs-lookup"><span data-stu-id="279ad-229">Restore</span></span>
- <span data-ttu-id="279ad-230">Recuperar</span><span class="sxs-lookup"><span data-stu-id="279ad-230">Recover</span></span>
- <span data-ttu-id="279ad-231">Purga</span><span class="sxs-lookup"><span data-stu-id="279ad-231">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279ad-232">-PermissionsToSecsecções</span><span class="sxs-lookup"><span data-stu-id="279ad-232">-PermissionsToSecrets</span></span>
<span data-ttu-id="279ad-233">Especifica uma matriz de permissões de operação secreta para conceder a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="279ad-233">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="279ad-234">Os valores aceitáveis para este parâmetro:</span><span class="sxs-lookup"><span data-stu-id="279ad-234">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="279ad-235">Todos</span><span class="sxs-lookup"><span data-stu-id="279ad-235">All</span></span>
- <span data-ttu-id="279ad-236">Obter</span><span class="sxs-lookup"><span data-stu-id="279ad-236">Get</span></span>
- <span data-ttu-id="279ad-237">Lista</span><span class="sxs-lookup"><span data-stu-id="279ad-237">List</span></span>
- <span data-ttu-id="279ad-238">Definir</span><span class="sxs-lookup"><span data-stu-id="279ad-238">Set</span></span>
- <span data-ttu-id="279ad-239">Excluir</span><span class="sxs-lookup"><span data-stu-id="279ad-239">Delete</span></span>
- <span data-ttu-id="279ad-240">Backup</span><span class="sxs-lookup"><span data-stu-id="279ad-240">Backup</span></span>
- <span data-ttu-id="279ad-241">Restaurar</span><span class="sxs-lookup"><span data-stu-id="279ad-241">Restore</span></span>
- <span data-ttu-id="279ad-242">Recuperar</span><span class="sxs-lookup"><span data-stu-id="279ad-242">Recover</span></span>
- <span data-ttu-id="279ad-243">Purga</span><span class="sxs-lookup"><span data-stu-id="279ad-243">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279ad-244">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="279ad-244">-PermissionsToStorage</span></span>
<span data-ttu-id="279ad-245">Especifica permissões de conta de armazenamento gerenciada e de operação de definição saS para conceder a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="279ad-245">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="279ad-246">Os valores aceitáveis para este parâmetro:</span><span class="sxs-lookup"><span data-stu-id="279ad-246">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="279ad-247">Todos</span><span class="sxs-lookup"><span data-stu-id="279ad-247">all</span></span>
- <span data-ttu-id="279ad-248">Obter</span><span class="sxs-lookup"><span data-stu-id="279ad-248">get</span></span>
- <span data-ttu-id="279ad-249">Lista</span><span class="sxs-lookup"><span data-stu-id="279ad-249">list</span></span>
- <span data-ttu-id="279ad-250">Excluir</span><span class="sxs-lookup"><span data-stu-id="279ad-250">delete</span></span>
- <span data-ttu-id="279ad-251">Definir</span><span class="sxs-lookup"><span data-stu-id="279ad-251">set</span></span>
- <span data-ttu-id="279ad-252">Atualização</span><span class="sxs-lookup"><span data-stu-id="279ad-252">update</span></span>
- <span data-ttu-id="279ad-253">regeneratekey</span><span class="sxs-lookup"><span data-stu-id="279ad-253">regeneratekey</span></span>
- <span data-ttu-id="279ad-254">getsas</span><span class="sxs-lookup"><span data-stu-id="279ad-254">getsas</span></span>
- <span data-ttu-id="279ad-255">listas</span><span class="sxs-lookup"><span data-stu-id="279ad-255">listsas</span></span>
- <span data-ttu-id="279ad-256">deletesas</span><span class="sxs-lookup"><span data-stu-id="279ad-256">deletesas</span></span>
- <span data-ttu-id="279ad-257">conjuntos</span><span class="sxs-lookup"><span data-stu-id="279ad-257">setsas</span></span>
- <span data-ttu-id="279ad-258">Recuperar</span><span class="sxs-lookup"><span data-stu-id="279ad-258">recover</span></span>
- <span data-ttu-id="279ad-259">Backup</span><span class="sxs-lookup"><span data-stu-id="279ad-259">backup</span></span>
- <span data-ttu-id="279ad-260">Restaurar</span><span class="sxs-lookup"><span data-stu-id="279ad-260">restore</span></span>
- <span data-ttu-id="279ad-261">Purga</span><span class="sxs-lookup"><span data-stu-id="279ad-261">purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279ad-262">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="279ad-262">-ResourceGroupName</span></span>
<span data-ttu-id="279ad-263">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="279ad-263">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="279ad-264">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="279ad-264">-ResourceId</span></span>
<span data-ttu-id="279ad-265">ID do Recurso do Cofre de Chave</span><span class="sxs-lookup"><span data-stu-id="279ad-265">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="279ad-266">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="279ad-266">-ServicePrincipalName</span></span>
<span data-ttu-id="279ad-267">Especifica o nome da entidade de serviço do aplicativo ao qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="279ad-267">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="279ad-268">Especifique a ID do aplicativo, também conhecida como ID do cliente, registrada para o aplicativo no Diretório AzureActive.</span><span class="sxs-lookup"><span data-stu-id="279ad-268">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="279ad-269">O aplicativo com o nome da entidade de serviço especificado por esse parâmetro deve ser registrado no diretório do Azure que contém sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="279ad-269">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="279ad-270">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="279ad-270">-UserPrincipalName</span></span>
<span data-ttu-id="279ad-271">Especifica o nome principal do usuário ao qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="279ad-271">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="279ad-272">Esse nome de entidade de usuário deve existir no diretório associado à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="279ad-272">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="279ad-273">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="279ad-273">-VaultName</span></span>
<span data-ttu-id="279ad-274">Especifica o nome de um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="279ad-274">Specifies the name of a key vault.</span></span>
<span data-ttu-id="279ad-275">Esse cmdlet modifica a política de acesso para o cofre de chave especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="279ad-275">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="279ad-276">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="279ad-276">-Confirm</span></span>
<span data-ttu-id="279ad-277">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="279ad-277">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="279ad-278">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="279ad-278">-WhatIf</span></span>
<span data-ttu-id="279ad-279">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="279ad-279">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="279ad-280">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="279ad-280">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="279ad-281">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279ad-281">CommonParameters</span></span>
<span data-ttu-id="279ad-282">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="279ad-282">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279ad-283">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="279ad-283">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279ad-284">Entradas</span><span class="sxs-lookup"><span data-stu-id="279ad-284">INPUTS</span></span>

### <span data-ttu-id="279ad-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="279ad-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="279ad-286">System.String</span><span class="sxs-lookup"><span data-stu-id="279ad-286">System.String</span></span>

## <span data-ttu-id="279ad-287">Saídas</span><span class="sxs-lookup"><span data-stu-id="279ad-287">OUTPUTS</span></span>

### <span data-ttu-id="279ad-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="279ad-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="279ad-289">Notas</span><span class="sxs-lookup"><span data-stu-id="279ad-289">NOTES</span></span>

## <span data-ttu-id="279ad-290">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="279ad-290">RELATED LINKS</span></span>

[<span data-ttu-id="279ad-291">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="279ad-291">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="279ad-292">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="279ad-292">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

