---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 343cea9eb3d708e802d1e06f555fd13ab1cd8c13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430223"
---
# <span data-ttu-id="21e68-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="21e68-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="21e68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21e68-102">SYNOPSIS</span></span>
<span data-ttu-id="21e68-103">Remove todas as permissões de um usuário ou aplicativo de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="21e68-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21e68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21e68-104">SYNTAX</span></span>

### <span data-ttu-id="21e68-105">ByUserPrincipalName (padrão)</span><span class="sxs-lookup"><span data-stu-id="21e68-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21e68-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="21e68-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21e68-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="21e68-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21e68-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="21e68-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e68-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="21e68-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e68-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="21e68-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e68-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="21e68-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e68-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="21e68-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e68-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="21e68-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e68-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="21e68-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e68-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="21e68-115">ResourceIdByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e68-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="21e68-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e68-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="21e68-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e68-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="21e68-118">ResourceIdByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e68-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="21e68-119">ResourceIdForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21e68-120">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21e68-120">DESCRIPTION</span></span>
<span data-ttu-id="21e68-121">O cmdlet **Remove-AzureRmKeyVaultAccessPolicy** remove todas as permissões para um usuário ou aplicativo ou para todos os usuários e aplicativos de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="21e68-121">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="21e68-122">Mesmo que você remova todas as permissões, o proprietário da assinatura do Azure que contém o cofre de chaves pode adicionar permissões ao cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="21e68-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="21e68-123">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="21e68-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="21e68-124">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21e68-124">EXAMPLES</span></span>

### <span data-ttu-id="21e68-125">Exemplo 1: remover permissões de um usuário</span><span class="sxs-lookup"><span data-stu-id="21e68-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     :
                                   Permissions to Certificates                : get, create
                                   Permissions to (Key Vault Managed) Storage :


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="21e68-126">Esse comando Remove todas as permissões que um usuário PattiFuller@contoso.com tem no cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="21e68-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="21e68-127">Se-PassThru for especificado, o objeto do keyvault será retornado.</span><span class="sxs-lookup"><span data-stu-id="21e68-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="21e68-128">Exemplo 2: remover as permissões de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="21e68-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="21e68-129">Esse comando Remove todas as permissões que um aplicativo tem no cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="21e68-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="21e68-130">Este exemplo identifica o aplicativo usando o nome principal do serviço registrado no Azure Active Directory http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="21e68-130">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="21e68-131">Exemplo 3: remover as permissões de um aplicativo usando sua ID de objeto</span><span class="sxs-lookup"><span data-stu-id="21e68-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="21e68-132">Esse comando Remove todas as permissões que um aplicativo tem no cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="21e68-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="21e68-133">Este exemplo identifica o aplicativo pela ID de objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="21e68-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="21e68-134">Exemplo 4: remover permissões para o provedor de recursos Microsoft. Compute</span><span class="sxs-lookup"><span data-stu-id="21e68-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="21e68-135">Esse comando Remove a permissão do provedor de recursos Microsoft. COMPUTE para obter os segredos da Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="21e68-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="21e68-136">OS</span><span class="sxs-lookup"><span data-stu-id="21e68-136">PARAMETERS</span></span>

### <span data-ttu-id="21e68-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="21e68-137">-ApplicationId</span></span>
<span data-ttu-id="21e68-138">Especifica a ID do aplicativo cujas permissões devem ser removidas</span><span class="sxs-lookup"><span data-stu-id="21e68-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="21e68-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e68-139">-DefaultProfile</span></span>
<span data-ttu-id="21e68-140">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="21e68-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e68-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="21e68-141">-EmailAddress</span></span>
<span data-ttu-id="21e68-142">Especifica o endereço de email do usuário do qual o acesso você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="21e68-142">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail, InputObjectByEmail, ResourceIdByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e68-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="21e68-143">-EnabledForDeployment</span></span>
<span data-ttu-id="21e68-144">Se especificado, desabilita a recuperação de segredos deste cofre de chaves pelo provedor de recursos Microsoft. Compute quando referenciado na criação de recursos.</span><span class="sxs-lookup"><span data-stu-id="21e68-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="21e68-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="21e68-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="21e68-146">Se especificado, desabilita a recuperação de segredos deste cofre de chaves por criptografia de disco do Azure.</span><span class="sxs-lookup"><span data-stu-id="21e68-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="21e68-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="21e68-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="21e68-148">Se especificado, desabilita a recuperação de segredos deste cofre de chaves pelo Azure Resource Manager quando referenciado nos modelos.</span><span class="sxs-lookup"><span data-stu-id="21e68-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="21e68-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21e68-149">-InputObject</span></span>
<span data-ttu-id="21e68-150">Objeto do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="21e68-150">Key Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21e68-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="21e68-151">-ObjectId</span></span>
<span data-ttu-id="21e68-152">Especifica a ID de objeto da entidade de usuário ou serviço do Azure Active Directory para a qual as permissões são removidas.</span><span class="sxs-lookup"><span data-stu-id="21e68-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="21e68-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21e68-153">-PassThru</span></span>
<span data-ttu-id="21e68-154">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="21e68-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="21e68-155">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="21e68-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="21e68-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21e68-156">-ResourceGroupName</span></span>
<span data-ttu-id="21e68-157">Especifica o nome do grupo de recursos associado ao cofre de chaves cuja política de acesso está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="21e68-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="21e68-158">Se não for especificado, esse cmdlet pesquisará o cofre de chaves na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="21e68-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e68-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21e68-159">-ResourceId</span></span>
<span data-ttu-id="21e68-160">ID do recurso do keyvault.</span><span class="sxs-lookup"><span data-stu-id="21e68-160">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmail, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21e68-161">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="21e68-161">-ServicePrincipalName</span></span>
<span data-ttu-id="21e68-162">Especifica o nome principal do serviço do aplicativo cujas permissões você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="21e68-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="21e68-163">Especifique a identificação do aplicativo, também conhecida como ID do cliente, registrada para o aplicativo no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="21e68-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="21e68-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="21e68-164">-UserPrincipalName</span></span>
<span data-ttu-id="21e68-165">Especifica o nome UPN do usuário cujo acesso você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="21e68-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="21e68-166">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="21e68-166">-VaultName</span></span>
<span data-ttu-id="21e68-167">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="21e68-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="21e68-168">Esse cmdlet Remove permissões para o cofre de chaves que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="21e68-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e68-169">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21e68-169">-Confirm</span></span>
<span data-ttu-id="21e68-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21e68-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21e68-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21e68-171">-WhatIf</span></span>
<span data-ttu-id="21e68-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21e68-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21e68-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21e68-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21e68-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e68-174">CommonParameters</span></span>
<span data-ttu-id="21e68-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21e68-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e68-176">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21e68-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e68-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21e68-177">INPUTS</span></span>

### <span data-ttu-id="21e68-178">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="21e68-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="21e68-179">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="21e68-179">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="21e68-180">System. String</span><span class="sxs-lookup"><span data-stu-id="21e68-180">System.String</span></span>

## <span data-ttu-id="21e68-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21e68-181">OUTPUTS</span></span>

### <span data-ttu-id="21e68-182">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="21e68-182">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="21e68-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21e68-183">NOTES</span></span>

## <span data-ttu-id="21e68-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21e68-184">RELATED LINKS</span></span>

[<span data-ttu-id="21e68-185">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="21e68-185">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)
