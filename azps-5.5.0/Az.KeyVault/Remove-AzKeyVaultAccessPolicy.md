---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: e19565aa8ae249acf61fce67f0a2b54e20143758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118956"
---
# <span data-ttu-id="3b6a1-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b6a1-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="3b6a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="3b6a1-103">Remove todas as permissões de um usuário ou aplicativo de um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="3b6a1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b6a1-104">SYNTAX</span></span>

### <span data-ttu-id="3b6a1-105">ByUserPrincipalName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3b6a1-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="3b6a1-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b6a1-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="3b6a1-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="3b6a1-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="3b6a1-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b6a1-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b6a1-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="3b6a1-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="3b6a1-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="3b6a1-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b6a1-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b6a1-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="3b6a1-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6a1-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="3b6a1-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b6a1-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b6a1-120">DESCRIPTION</span></span>
<span data-ttu-id="3b6a1-121">O cmdlet **Remove-AzKeyVaultAccessPolicy** remove todas as permissões de um usuário ou aplicativo ou para todos os usuários e aplicativos de um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="3b6a1-122">Mesmo que você remova todas as permissões, o proprietário da assinatura do Azure que contém o cofre de chaves poderá adicionar permissões ao cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="3b6a1-123">Observe que, embora especificar o grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="3b6a1-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b6a1-124">EXAMPLES</span></span>

### <span data-ttu-id="3b6a1-125">Exemplo 1: Remover permissões de um usuário</span><span class="sxs-lookup"><span data-stu-id="3b6a1-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

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

<span data-ttu-id="3b6a1-126">Esse comando remove todas as permissões que um usuário tem PattiFuller@contoso.com no cofre de teclas chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="3b6a1-127">Se -PassThru for especificado, o objeto KeyVault será retornado.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="3b6a1-128">Exemplo 2: Remover permissões para um aplicativo</span><span class="sxs-lookup"><span data-stu-id="3b6a1-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="3b6a1-129">Esse comando remove todas as permissões que um aplicativo tem no cofre de teclas chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="3b6a1-130">Este exemplo identifica o aplicativo usando o nome da entidade de serviço registrado no Azure Active `http://payroll.contoso.com` Directory.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="3b6a1-131">Exemplo 3: remover permissões para um aplicativo usando sua ID de objeto</span><span class="sxs-lookup"><span data-stu-id="3b6a1-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="3b6a1-132">Esse comando remove todas as permissões que um aplicativo tem no cofre de teclas chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="3b6a1-133">Este exemplo identifica o aplicativo pela ID do objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="3b6a1-134">Exemplo 4: Remover permissões para o provedor de recursos Microsoft.Compute</span><span class="sxs-lookup"><span data-stu-id="3b6a1-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="3b6a1-135">Este comando remove a permissão do provedor de recursos Microsoft.Compute para obter segredos da Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="3b6a1-136">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b6a1-136">PARAMETERS</span></span>

### <span data-ttu-id="3b6a1-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3b6a1-137">-ApplicationId</span></span>
<span data-ttu-id="3b6a1-138">Especifica a ID do aplicativo cujas permissões devem ser removidas</span><span class="sxs-lookup"><span data-stu-id="3b6a1-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="3b6a1-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b6a1-139">-DefaultProfile</span></span>
<span data-ttu-id="3b6a1-140">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3b6a1-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b6a1-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="3b6a1-141">-EmailAddress</span></span>
<span data-ttu-id="3b6a1-142">Especifica o endereço de email do usuário cujo acesso você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-142">Specifies the user email address of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="3b6a1-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="3b6a1-143">-EnabledForDeployment</span></span>
<span data-ttu-id="3b6a1-144">Se especificado, desabilita a recuperação de segredos desse cofre de chave pelo provedor de recursos Microsoft.Compute quando referenciado na criação de recursos.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="3b6a1-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="3b6a1-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="3b6a1-146">Se especificado, desabilita a recuperação de segredos deste cofre de chaves pela Criptografia de Disco do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="3b6a1-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="3b6a1-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="3b6a1-148">Se especificado, desabilita a recuperação de segredos desse cofre de chaves pelo Gerenciador de Recursos do Azure quando referenciado em modelos.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="3b6a1-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b6a1-149">-InputObject</span></span>
<span data-ttu-id="3b6a1-150">Objeto do Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-150">Key Vault object.</span></span>

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

### <span data-ttu-id="3b6a1-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3b6a1-151">-ObjectId</span></span>
<span data-ttu-id="3b6a1-152">Especifica a ID do objeto da entidade de usuário ou serviço no Azure Active Directory para a qual remover permissões.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="3b6a1-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b6a1-153">-PassThru</span></span>
<span data-ttu-id="3b6a1-154">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3b6a1-155">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3b6a1-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b6a1-156">-ResourceGroupName</span></span>
<span data-ttu-id="3b6a1-157">Especifica o nome do grupo de recursos associado ao cofre de chave cuja política de acesso está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="3b6a1-158">Se não especificado, este cmdlet pesquisa o cofre de chave na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="3b6a1-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b6a1-159">-ResourceId</span></span>
<span data-ttu-id="3b6a1-160">ID do Recurso KeyVault.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-160">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="3b6a1-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b6a1-161">-ServicePrincipalName</span></span>
<span data-ttu-id="3b6a1-162">Especifica o nome da entidade de serviço do aplicativo cujas permissões você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="3b6a1-163">Especifique a ID do aplicativo, também conhecida como ID do cliente, registrada para o aplicativo no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="3b6a1-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b6a1-164">-UserPrincipalName</span></span>
<span data-ttu-id="3b6a1-165">Especifica o nome principal do usuário cujo acesso você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="3b6a1-166">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="3b6a1-166">-VaultName</span></span>
<span data-ttu-id="3b6a1-167">Especifica o nome do cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="3b6a1-168">Este cmdlet remove permissões para o cofre de teclas especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="3b6a1-169">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3b6a1-169">-Confirm</span></span>
<span data-ttu-id="3b6a1-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b6a1-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b6a1-171">-WhatIf</span></span>
<span data-ttu-id="3b6a1-172">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b6a1-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b6a1-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b6a1-174">CommonParameters</span></span>
<span data-ttu-id="3b6a1-175">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b6a1-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b6a1-176">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b6a1-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b6a1-177">Entradas</span><span class="sxs-lookup"><span data-stu-id="3b6a1-177">INPUTS</span></span>

### <span data-ttu-id="3b6a1-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3b6a1-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3b6a1-179">System.String</span><span class="sxs-lookup"><span data-stu-id="3b6a1-179">System.String</span></span>

## <span data-ttu-id="3b6a1-180">Saídas</span><span class="sxs-lookup"><span data-stu-id="3b6a1-180">OUTPUTS</span></span>

### <span data-ttu-id="3b6a1-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3b6a1-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="3b6a1-182">Notas</span><span class="sxs-lookup"><span data-stu-id="3b6a1-182">NOTES</span></span>

## <span data-ttu-id="3b6a1-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b6a1-183">RELATED LINKS</span></span>

[<span data-ttu-id="3b6a1-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b6a1-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

