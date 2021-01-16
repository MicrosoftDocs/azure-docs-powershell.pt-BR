---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: eeaea44ec387dc7739a97b5026054186ff817ab3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262741"
---
# <span data-ttu-id="68f6a-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68f6a-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="68f6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="68f6a-103">Concede ou modifica permissões existentes para um usuário, aplicativo ou grupo de segurança para executar operações com um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="68f6a-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="68f6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68f6a-104">SYNTAX</span></span>

### <span data-ttu-id="68f6a-105">ByUserPrincipalName (padrão)</span><span class="sxs-lookup"><span data-stu-id="68f6a-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68f6a-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="68f6a-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f6a-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="68f6a-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68f6a-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="68f6a-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68f6a-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="68f6a-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f6a-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="68f6a-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f6a-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="68f6a-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68f6a-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="68f6a-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68f6a-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="68f6a-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68f6a-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="68f6a-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f6a-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="68f6a-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f6a-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="68f6a-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68f6a-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="68f6a-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f6a-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="68f6a-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f6a-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="68f6a-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68f6a-120">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68f6a-120">DESCRIPTION</span></span>
<span data-ttu-id="68f6a-121">O cmdlet **set-AzKeyVaultAccessPolicy** concede ou modifica permissões existentes para um usuário, aplicativo ou grupo de segurança para executar as operações especificadas com um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="68f6a-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="68f6a-122">Ele não modifica as permissões que outros usuários, aplicativos ou grupos de segurança têm no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="68f6a-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="68f6a-123">Se você estiver definindo permissões para um grupo de segurança, essa operação afetará apenas os usuários desse grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="68f6a-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="68f6a-124">Todos os diretórios a seguir devem ser do mesmo diretório do Azure:</span><span class="sxs-lookup"><span data-stu-id="68f6a-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="68f6a-125">O diretório padrão da assinatura do Azure em que o cofre de chaves reside.</span><span class="sxs-lookup"><span data-stu-id="68f6a-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="68f6a-126">O diretório do Azure que contém o usuário ou o grupo de aplicativos aos quais você está concedendo permissões.</span><span class="sxs-lookup"><span data-stu-id="68f6a-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="68f6a-127">Exemplos de cenários quando essas condições não são atendidas e esse cmdlet não funcionará:</span><span class="sxs-lookup"><span data-stu-id="68f6a-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="68f6a-128">Autorizar um usuário de outra organização a gerenciar seu cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="68f6a-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="68f6a-129">Cada organização tem seu próprio diretório.</span><span class="sxs-lookup"><span data-stu-id="68f6a-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="68f6a-130">Sua conta do Azure tem vários diretórios.</span><span class="sxs-lookup"><span data-stu-id="68f6a-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="68f6a-131">Se você registrar um aplicativo em um diretório diferente do diretório padrão, não poderá autorizar esse aplicativo a usar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="68f6a-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="68f6a-132">O aplicativo deve estar no diretório padrão.</span><span class="sxs-lookup"><span data-stu-id="68f6a-132">The application must be in the default directory.</span></span>
<span data-ttu-id="68f6a-133">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="68f6a-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="68f6a-134">Ao usar uma entidade de serviço para conceder permissões de política de acesso, você deve usar o `-BypassObjectIdValidation` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="68f6a-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="68f6a-135">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68f6a-135">EXAMPLES</span></span>

### <span data-ttu-id="68f6a-136">Exemplo 1: conceder permissões a um usuário para um cofre de chaves e modificar as permissões</span><span class="sxs-lookup"><span data-stu-id="68f6a-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="68f6a-137">O primeiro comando concede permissões para um usuário em seu Active Directory do Azure, PattiFuller@contoso.com para executar operações em chaves e segredos com um cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="68f6a-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="68f6a-138">O parâmetro *PassThru* resulta no objeto atualizado sendo retornado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68f6a-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="68f6a-139">O segundo comando modifica as permissões que foram concedidas ao PattiFuller@contoso.com primeiro comando, a fim de permitir a obtenção de segredos, além de definir e excluir essas permissões.</span><span class="sxs-lookup"><span data-stu-id="68f6a-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="68f6a-140">As permissões para operações de chave permanecem inalteradas após esse comando.</span><span class="sxs-lookup"><span data-stu-id="68f6a-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="68f6a-141">O último comando modifica as permissões existentes para PattiFuller@contoso.com remover todas as permissões para operações de chave.</span><span class="sxs-lookup"><span data-stu-id="68f6a-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="68f6a-142">As permissões para operações secretas permanecem inalteradas após esse comando.</span><span class="sxs-lookup"><span data-stu-id="68f6a-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="68f6a-143">Exemplo 2: conceder permissões para uma entidade de serviço de aplicativo para ler e gravar segredos</span><span class="sxs-lookup"><span data-stu-id="68f6a-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="68f6a-144">Esse comando concede permissões para um aplicativo para um cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="68f6a-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="68f6a-145">O parâmetro *servicePrincipalName* especifica o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68f6a-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="68f6a-146">O aplicativo deve ser registrado no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="68f6a-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="68f6a-147">*O valor do parâmetro servicePrincipalName* deve ser o nome principal do aplicativo ou o GUID da ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68f6a-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="68f6a-148">Este exemplo especifica o nome principal do serviço `http://payroll.contoso.com` , e o comando concede as permissões do aplicativo para ler e gravar segredos.</span><span class="sxs-lookup"><span data-stu-id="68f6a-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="68f6a-149">Exemplo 3: conceder permissões para um aplicativo usando sua ID de objeto</span><span class="sxs-lookup"><span data-stu-id="68f6a-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="68f6a-150">Esse comando concede as permissões do aplicativo para ler e gravar segredos.</span><span class="sxs-lookup"><span data-stu-id="68f6a-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="68f6a-151">Este exemplo especifica o aplicativo que usa a ID de objeto da entidade de serviço do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68f6a-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="68f6a-152">Exemplo 4: conceder permissões para um nome de usuário principal</span><span class="sxs-lookup"><span data-stu-id="68f6a-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="68f6a-153">Esse comando concede a obter, listar e definir permissões para o nome principal do usuário especificado para acessar os segredos.</span><span class="sxs-lookup"><span data-stu-id="68f6a-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="68f6a-154">Exemplo 5: habilitar os segredos para serem recuperados de um cofre de chaves pelo provedor de recursos Microsoft. Compute</span><span class="sxs-lookup"><span data-stu-id="68f6a-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="68f6a-155">Esse comando concede as permissões para que os segredos sejam recuperados do cofre da chave Contoso03Vault pelo provedor de recursos Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="68f6a-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="68f6a-156">Exemplo 6: conceder permissões a um grupo de segurança</span><span class="sxs-lookup"><span data-stu-id="68f6a-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="68f6a-157">O primeiro comando usa o cmdlet Get-AzADGroup para obter todos os grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="68f6a-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="68f6a-158">Na saída, você verá 3 grupos retornados, chamados **grupo1**, **group2** e **Group3**.</span><span class="sxs-lookup"><span data-stu-id="68f6a-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="68f6a-159">Vários grupos podem ter o mesmo nome, mas sempre têm um ObjectId exclusivo.</span><span class="sxs-lookup"><span data-stu-id="68f6a-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="68f6a-160">Quando mais de um grupo com o mesmo nome for retornado, use o ObjectId na saída para identificar o que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="68f6a-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="68f6a-161">Em seguida, você usa a saída desse comando com Set-AzKeyVaultAccessPolicy para conceder permissões a group2 para o seu cofre de chaves, chamado **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="68f6a-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="68f6a-162">Este exemplo enumera os grupos chamados "group2" embutidos na mesma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="68f6a-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="68f6a-163">Pode haver vários grupos na lista retornada com o nome "group2".</span><span class="sxs-lookup"><span data-stu-id="68f6a-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="68f6a-164">Este exemplo escolhe o primeiro, indicado pelo índice \[ 0 \] na lista retornada.</span><span class="sxs-lookup"><span data-stu-id="68f6a-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="68f6a-165">Exemplo 7: conceder ao Azure acesso à proteção de informações à chave locatário gerenciada pelo cliente (BYOK)</span><span class="sxs-lookup"><span data-stu-id="68f6a-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="68f6a-166">Esse comando autoriza a proteção de informações do Azure a usar uma chave gerenciada pelo cliente (a traga sua própria chave ou o cenário "BYOK") como a chave locatário do Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="68f6a-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="68f6a-167">Ao executar esse comando, especifique seu próprio nome do cofre de chaves, mas você deve especificar o parâmetro *servicePrincipalName* com o GUID **00000012-0000-0000-C000-000000000000** e especificar as permissões no exemplo.</span><span class="sxs-lookup"><span data-stu-id="68f6a-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="68f6a-168">OS</span><span class="sxs-lookup"><span data-stu-id="68f6a-168">PARAMETERS</span></span>

### <span data-ttu-id="68f6a-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="68f6a-169">-ApplicationId</span></span>
<span data-ttu-id="68f6a-170">Para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="68f6a-170">For future use.</span></span>

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

### <span data-ttu-id="68f6a-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="68f6a-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="68f6a-172">Permite que você especifique uma ID de objeto sem validar que o objeto existe no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="68f6a-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="68f6a-173">Use esse parâmetro somente se você quiser conceder acesso ao seu cofre de chaves a uma ID de objeto que se refere a um grupo de segurança delegado de outro locatário do Azure.</span><span class="sxs-lookup"><span data-stu-id="68f6a-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="68f6a-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f6a-174">-DefaultProfile</span></span>
<span data-ttu-id="68f6a-175">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="68f6a-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68f6a-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="68f6a-176">-EmailAddress</span></span>
<span data-ttu-id="68f6a-177">Especifica o endereço de email do usuário para o qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="68f6a-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="68f6a-178">Esse endereço de email deve existir no diretório associado à assinatura atual e ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="68f6a-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="68f6a-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="68f6a-179">-EnabledForDeployment</span></span>
<span data-ttu-id="68f6a-180">Habilita o provedor de recursos Microsoft. Compute a recuperar segredos deste cofre de chaves quando esse cofre de chaves é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="68f6a-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="68f6a-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="68f6a-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="68f6a-182">Habilita o serviço de criptografia de disco do Azure a obter segredos e a desencapsulação de chaves deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="68f6a-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="68f6a-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="68f6a-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="68f6a-184">Permite que o Azure Resource Manager obtenha os segredos deste cofre de chaves quando esse cofre de chaves é referenciado em uma implantação de modelo.</span><span class="sxs-lookup"><span data-stu-id="68f6a-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="68f6a-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68f6a-185">-InputObject</span></span>
<span data-ttu-id="68f6a-186">Objeto do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="68f6a-186">Key Vault Object</span></span>

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

### <span data-ttu-id="68f6a-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="68f6a-187">-ObjectId</span></span>
<span data-ttu-id="68f6a-188">Especifica a ID de objeto da entidade de usuário ou serviço do Azure Active Directory para a qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="68f6a-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="68f6a-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68f6a-189">-PassThru</span></span>
<span data-ttu-id="68f6a-190">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="68f6a-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="68f6a-191">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="68f6a-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="68f6a-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="68f6a-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="68f6a-193">Especifica uma matriz de permissões de certificado a serem concedidas a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="68f6a-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="68f6a-194">Os valores aceitáveis para esse parâmetro:</span><span class="sxs-lookup"><span data-stu-id="68f6a-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="68f6a-195">Todo</span><span class="sxs-lookup"><span data-stu-id="68f6a-195">All</span></span>
- <span data-ttu-id="68f6a-196">Obter</span><span class="sxs-lookup"><span data-stu-id="68f6a-196">Get</span></span>
- <span data-ttu-id="68f6a-197">Programação</span><span class="sxs-lookup"><span data-stu-id="68f6a-197">List</span></span>
- <span data-ttu-id="68f6a-198">Remover</span><span class="sxs-lookup"><span data-stu-id="68f6a-198">Delete</span></span>
- <span data-ttu-id="68f6a-199">Criados</span><span class="sxs-lookup"><span data-stu-id="68f6a-199">Create</span></span>
- <span data-ttu-id="68f6a-200">Importações</span><span class="sxs-lookup"><span data-stu-id="68f6a-200">Import</span></span>
- <span data-ttu-id="68f6a-201">Atualização</span><span class="sxs-lookup"><span data-stu-id="68f6a-201">Update</span></span>
- <span data-ttu-id="68f6a-202">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="68f6a-202">Managecontacts</span></span>
- <span data-ttu-id="68f6a-203">Emissors</span><span class="sxs-lookup"><span data-stu-id="68f6a-203">Getissuers</span></span>
- <span data-ttu-id="68f6a-204">Listissuers</span><span class="sxs-lookup"><span data-stu-id="68f6a-204">Listissuers</span></span>
- <span data-ttu-id="68f6a-205">Emissores</span><span class="sxs-lookup"><span data-stu-id="68f6a-205">Setissuers</span></span>
- <span data-ttu-id="68f6a-206">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="68f6a-206">Deleteissuers</span></span>
- <span data-ttu-id="68f6a-207">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="68f6a-207">Manageissuers</span></span>
- <span data-ttu-id="68f6a-208">Gravação</span><span class="sxs-lookup"><span data-stu-id="68f6a-208">Recover</span></span>
- <span data-ttu-id="68f6a-209">Fazer</span><span class="sxs-lookup"><span data-stu-id="68f6a-209">Backup</span></span>
- <span data-ttu-id="68f6a-210">Restaurar</span><span class="sxs-lookup"><span data-stu-id="68f6a-210">Restore</span></span>
- <span data-ttu-id="68f6a-211">Purga</span><span class="sxs-lookup"><span data-stu-id="68f6a-211">Purge</span></span>

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

### <span data-ttu-id="68f6a-212">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="68f6a-212">-PermissionsToKeys</span></span>
<span data-ttu-id="68f6a-213">Especifica uma matriz de permissões de operações de chave a serem concedidas a um usuário ou serviço principal.</span><span class="sxs-lookup"><span data-stu-id="68f6a-213">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="68f6a-214">Os valores aceitáveis para esse parâmetro:</span><span class="sxs-lookup"><span data-stu-id="68f6a-214">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="68f6a-215">Todo</span><span class="sxs-lookup"><span data-stu-id="68f6a-215">All</span></span>
- <span data-ttu-id="68f6a-216">Criptografá</span><span class="sxs-lookup"><span data-stu-id="68f6a-216">Decrypt</span></span>
- <span data-ttu-id="68f6a-217">Com</span><span class="sxs-lookup"><span data-stu-id="68f6a-217">Encrypt</span></span>
- <span data-ttu-id="68f6a-218">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="68f6a-218">UnwrapKey</span></span>
- <span data-ttu-id="68f6a-219">WrapKey</span><span class="sxs-lookup"><span data-stu-id="68f6a-219">WrapKey</span></span>
- <span data-ttu-id="68f6a-220">Verificar</span><span class="sxs-lookup"><span data-stu-id="68f6a-220">Verify</span></span>
- <span data-ttu-id="68f6a-221">Designa</span><span class="sxs-lookup"><span data-stu-id="68f6a-221">Sign</span></span>
- <span data-ttu-id="68f6a-222">Obter</span><span class="sxs-lookup"><span data-stu-id="68f6a-222">Get</span></span>
- <span data-ttu-id="68f6a-223">Programação</span><span class="sxs-lookup"><span data-stu-id="68f6a-223">List</span></span>
- <span data-ttu-id="68f6a-224">Atualização</span><span class="sxs-lookup"><span data-stu-id="68f6a-224">Update</span></span>
- <span data-ttu-id="68f6a-225">Criados</span><span class="sxs-lookup"><span data-stu-id="68f6a-225">Create</span></span>
- <span data-ttu-id="68f6a-226">Importações</span><span class="sxs-lookup"><span data-stu-id="68f6a-226">Import</span></span>
- <span data-ttu-id="68f6a-227">Remover</span><span class="sxs-lookup"><span data-stu-id="68f6a-227">Delete</span></span>
- <span data-ttu-id="68f6a-228">Fazer</span><span class="sxs-lookup"><span data-stu-id="68f6a-228">Backup</span></span>
- <span data-ttu-id="68f6a-229">Restaurar</span><span class="sxs-lookup"><span data-stu-id="68f6a-229">Restore</span></span>
- <span data-ttu-id="68f6a-230">Gravação</span><span class="sxs-lookup"><span data-stu-id="68f6a-230">Recover</span></span>
- <span data-ttu-id="68f6a-231">Purga</span><span class="sxs-lookup"><span data-stu-id="68f6a-231">Purge</span></span>

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

### <span data-ttu-id="68f6a-232">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="68f6a-232">-PermissionsToSecrets</span></span>
<span data-ttu-id="68f6a-233">Especifica uma matriz de permissões de operação secreta a serem concedidas a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="68f6a-233">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="68f6a-234">Os valores aceitáveis para esse parâmetro:</span><span class="sxs-lookup"><span data-stu-id="68f6a-234">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="68f6a-235">Todo</span><span class="sxs-lookup"><span data-stu-id="68f6a-235">All</span></span>
- <span data-ttu-id="68f6a-236">Obter</span><span class="sxs-lookup"><span data-stu-id="68f6a-236">Get</span></span>
- <span data-ttu-id="68f6a-237">Programação</span><span class="sxs-lookup"><span data-stu-id="68f6a-237">List</span></span>
- <span data-ttu-id="68f6a-238">Configurar</span><span class="sxs-lookup"><span data-stu-id="68f6a-238">Set</span></span>
- <span data-ttu-id="68f6a-239">Remover</span><span class="sxs-lookup"><span data-stu-id="68f6a-239">Delete</span></span>
- <span data-ttu-id="68f6a-240">Fazer</span><span class="sxs-lookup"><span data-stu-id="68f6a-240">Backup</span></span>
- <span data-ttu-id="68f6a-241">Restaurar</span><span class="sxs-lookup"><span data-stu-id="68f6a-241">Restore</span></span>
- <span data-ttu-id="68f6a-242">Gravação</span><span class="sxs-lookup"><span data-stu-id="68f6a-242">Recover</span></span>
- <span data-ttu-id="68f6a-243">Purga</span><span class="sxs-lookup"><span data-stu-id="68f6a-243">Purge</span></span>

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

### <span data-ttu-id="68f6a-244">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="68f6a-244">-PermissionsToStorage</span></span>
<span data-ttu-id="68f6a-245">Especifica as permissões da conta de armazenamento gerenciado e da operação de definição SaS a serem concedidas a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="68f6a-245">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="68f6a-246">Os valores aceitáveis para esse parâmetro:</span><span class="sxs-lookup"><span data-stu-id="68f6a-246">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="68f6a-247">todo</span><span class="sxs-lookup"><span data-stu-id="68f6a-247">all</span></span>
- <span data-ttu-id="68f6a-248">Obter</span><span class="sxs-lookup"><span data-stu-id="68f6a-248">get</span></span>
- <span data-ttu-id="68f6a-249">programação</span><span class="sxs-lookup"><span data-stu-id="68f6a-249">list</span></span>
- <span data-ttu-id="68f6a-250">remover</span><span class="sxs-lookup"><span data-stu-id="68f6a-250">delete</span></span>
- <span data-ttu-id="68f6a-251">configurar</span><span class="sxs-lookup"><span data-stu-id="68f6a-251">set</span></span>
- <span data-ttu-id="68f6a-252">atualização</span><span class="sxs-lookup"><span data-stu-id="68f6a-252">update</span></span>
- <span data-ttu-id="68f6a-253">regeneratekey</span><span class="sxs-lookup"><span data-stu-id="68f6a-253">regeneratekey</span></span>
- <span data-ttu-id="68f6a-254">Gets</span><span class="sxs-lookup"><span data-stu-id="68f6a-254">getsas</span></span>
- <span data-ttu-id="68f6a-255">listas de</span><span class="sxs-lookup"><span data-stu-id="68f6a-255">listsas</span></span>
- <span data-ttu-id="68f6a-256">exclusões</span><span class="sxs-lookup"><span data-stu-id="68f6a-256">deletesas</span></span>
- <span data-ttu-id="68f6a-257">conjuntos de valores</span><span class="sxs-lookup"><span data-stu-id="68f6a-257">setsas</span></span>
- <span data-ttu-id="68f6a-258">gravação</span><span class="sxs-lookup"><span data-stu-id="68f6a-258">recover</span></span>
- <span data-ttu-id="68f6a-259">fazer</span><span class="sxs-lookup"><span data-stu-id="68f6a-259">backup</span></span>
- <span data-ttu-id="68f6a-260">restaurar</span><span class="sxs-lookup"><span data-stu-id="68f6a-260">restore</span></span>
- <span data-ttu-id="68f6a-261">purga</span><span class="sxs-lookup"><span data-stu-id="68f6a-261">purge</span></span>

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

### <span data-ttu-id="68f6a-262">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f6a-262">-ResourceGroupName</span></span>
<span data-ttu-id="68f6a-263">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="68f6a-263">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="68f6a-264">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68f6a-264">-ResourceId</span></span>
<span data-ttu-id="68f6a-265">ID do recurso do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="68f6a-265">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="68f6a-266">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="68f6a-266">-ServicePrincipalName</span></span>
<span data-ttu-id="68f6a-267">Especifica o nome principal do serviço do aplicativo para o qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="68f6a-267">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="68f6a-268">Especifique o ID do aplicativo, também conhecido como ID do cliente, registrado para o aplicativo no diretório AzureActive.</span><span class="sxs-lookup"><span data-stu-id="68f6a-268">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="68f6a-269">O aplicativo com o nome da entidade de serviço que esse parâmetro especifica deve ser registrado no diretório do Azure que contém sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="68f6a-269">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="68f6a-270">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="68f6a-270">-UserPrincipalName</span></span>
<span data-ttu-id="68f6a-271">Especifica o nome UPN do usuário a quem conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="68f6a-271">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="68f6a-272">Este nome de usuário principal deve existir no diretório associado à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="68f6a-272">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="68f6a-273">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="68f6a-273">-VaultName</span></span>
<span data-ttu-id="68f6a-274">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="68f6a-274">Specifies the name of a key vault.</span></span>
<span data-ttu-id="68f6a-275">Esse cmdlet modifica a política de acesso para o cofre de chaves que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="68f6a-275">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="68f6a-276">-Confirme</span><span class="sxs-lookup"><span data-stu-id="68f6a-276">-Confirm</span></span>
<span data-ttu-id="68f6a-277">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68f6a-277">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68f6a-278">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68f6a-278">-WhatIf</span></span>
<span data-ttu-id="68f6a-279">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68f6a-279">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68f6a-280">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68f6a-280">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68f6a-281">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f6a-281">CommonParameters</span></span>
<span data-ttu-id="68f6a-282">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68f6a-282">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f6a-283">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68f6a-283">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f6a-284">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68f6a-284">INPUTS</span></span>

### <span data-ttu-id="68f6a-285">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="68f6a-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="68f6a-286">System. String</span><span class="sxs-lookup"><span data-stu-id="68f6a-286">System.String</span></span>

## <span data-ttu-id="68f6a-287">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68f6a-287">OUTPUTS</span></span>

### <span data-ttu-id="68f6a-288">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="68f6a-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="68f6a-289">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68f6a-289">NOTES</span></span>

## <span data-ttu-id="68f6a-290">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68f6a-290">RELATED LINKS</span></span>

[<span data-ttu-id="68f6a-291">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="68f6a-291">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="68f6a-292">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68f6a-292">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

