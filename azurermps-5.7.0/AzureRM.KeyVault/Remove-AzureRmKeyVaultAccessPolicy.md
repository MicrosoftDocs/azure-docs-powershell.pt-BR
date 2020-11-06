---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: ca175d0873b74d8b13d1755f3d0986580c5853ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431669"
---
# <span data-ttu-id="8a01f-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8a01f-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="8a01f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a01f-102">SYNOPSIS</span></span>
<span data-ttu-id="8a01f-103">Remove todas as permissões de um usuário ou aplicativo de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8a01f-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a01f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a01f-104">SYNTAX</span></span>

### <span data-ttu-id="8a01f-105">ByUserPrincipalName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8a01f-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a01f-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="8a01f-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a01f-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a01f-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a01f-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="8a01f-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a01f-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="8a01f-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a01f-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="8a01f-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a01f-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a01f-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a01f-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a01f-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a01f-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="8a01f-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a01f-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="8a01f-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a01f-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a01f-115">DESCRIPTION</span></span>
<span data-ttu-id="8a01f-116">O cmdlet **Remove-AzureRmKeyVaultAccessPolicy** remove todas as permissões para um usuário ou aplicativo ou para todos os usuários e aplicativos de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8a01f-116">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="8a01f-117">Mesmo que você remova todas as permissões, o proprietário da assinatura do Azure que contém o cofre de chaves pode adicionar permissões ao cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8a01f-117">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="8a01f-118">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="8a01f-118">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="8a01f-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a01f-119">EXAMPLES</span></span>

### <span data-ttu-id="8a01f-120">Exemplo 1: remover permissões de um usuário</span><span class="sxs-lookup"><span data-stu-id="8a01f-120">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="8a01f-121">Esse comando Remove todas as permissões que um usuário PattiFuller@contoso.com tem no cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8a01f-121">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="8a01f-122">Exemplo 2: remover as permissões de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="8a01f-122">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="8a01f-123">Esse comando Remove todas as permissões que um aplicativo tem no cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8a01f-123">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="8a01f-124">Este exemplo identifica o aplicativo usando o nome principal do serviço registrado no Azure Active Directory http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="8a01f-124">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="8a01f-125">Exemplo 3: remover as permissões de um aplicativo usando sua ID de objeto</span><span class="sxs-lookup"><span data-stu-id="8a01f-125">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="8a01f-126">Esse comando Remove todas as permissões que um aplicativo tem no cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8a01f-126">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="8a01f-127">Este exemplo identifica o aplicativo pela ID de objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="8a01f-127">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="8a01f-128">Exemplo 4: remover permissões para o provedor de recursos Microsoft. Compute</span><span class="sxs-lookup"><span data-stu-id="8a01f-128">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="8a01f-129">Esse comando Remove a permissão do provedor de recursos Microsoft. COMPUTE para obter os segredos da Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8a01f-129">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="8a01f-130">OS</span><span class="sxs-lookup"><span data-stu-id="8a01f-130">PARAMETERS</span></span>

### <span data-ttu-id="8a01f-131">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8a01f-131">-ApplicationId</span></span>
<span data-ttu-id="8a01f-132">Especifica a ID do aplicativo cujas permissões devem ser removidas</span><span class="sxs-lookup"><span data-stu-id="8a01f-132">Specifies the ID of application whose permissions should be removed</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a01f-133">-DefaultProfile</span></span>
<span data-ttu-id="8a01f-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8a01f-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-135">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8a01f-135">-EmailAddress</span></span>
<span data-ttu-id="8a01f-136">Especifica o endereço de email do usuário do qual o acesso você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="8a01f-136">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail, InputObjectByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-137">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="8a01f-137">-EnabledForDeployment</span></span>
<span data-ttu-id="8a01f-138">Se especificado, desabilita a recuperação de segredos deste cofre de chaves pelo provedor de recursos Microsoft. Compute quando referenciado na criação de recursos.</span><span class="sxs-lookup"><span data-stu-id="8a01f-138">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-139">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="8a01f-139">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="8a01f-140">Se especificado, desabilita a recuperação de segredos deste cofre de chaves por criptografia de disco do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a01f-140">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-141">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="8a01f-141">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="8a01f-142">Se especificado, desabilita a recuperação de segredos deste cofre de chaves pelo Azure Resource Manager quando referenciado nos modelos.</span><span class="sxs-lookup"><span data-stu-id="8a01f-142">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a01f-143">-InputObject</span></span>
<span data-ttu-id="8a01f-144">Objeto do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8a01f-144">Key Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-145">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8a01f-145">-ObjectId</span></span>
<span data-ttu-id="8a01f-146">Especifica a ID de objeto da entidade de usuário ou serviço do Azure Active Directory para a qual as permissões são removidas.</span><span class="sxs-lookup"><span data-stu-id="8a01f-146">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a01f-147">-PassThru</span></span>
<span data-ttu-id="8a01f-148">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8a01f-148">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8a01f-149">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8a01f-149">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a01f-150">-ResourceGroupName</span></span>
<span data-ttu-id="8a01f-151">Especifica o nome do grupo de recursos associado ao cofre de chaves cuja política de acesso está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="8a01f-151">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="8a01f-152">Se não for especificado, esse cmdlet pesquisará o cofre de chaves na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8a01f-152">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-153">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="8a01f-153">-ServicePrincipalName</span></span>
<span data-ttu-id="8a01f-154">Especifica o nome principal do serviço do aplicativo cujas permissões você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="8a01f-154">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="8a01f-155">Especifique a identificação do aplicativo, também conhecida como ID do cliente, registrada para o aplicativo no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8a01f-155">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-156">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a01f-156">-UserPrincipalName</span></span>
<span data-ttu-id="8a01f-157">Especifica o nome UPN do usuário cujo acesso você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="8a01f-157">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-158">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="8a01f-158">-VaultName</span></span>
<span data-ttu-id="8a01f-159">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8a01f-159">Specifies the name of the key vault.</span></span>
<span data-ttu-id="8a01f-160">Esse cmdlet Remove permissões para o cofre de chaves que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="8a01f-160">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8a01f-161">-Confirm</span></span>
<span data-ttu-id="8a01f-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a01f-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a01f-163">-WhatIf</span></span>
<span data-ttu-id="8a01f-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8a01f-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a01f-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8a01f-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a01f-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a01f-166">CommonParameters</span></span>
<span data-ttu-id="8a01f-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a01f-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a01f-168">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a01f-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a01f-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a01f-169">INPUTS</span></span>

### <span data-ttu-id="8a01f-170">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8a01f-170">None</span></span>
<span data-ttu-id="8a01f-171">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8a01f-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a01f-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a01f-172">OUTPUTS</span></span>

### <span data-ttu-id="8a01f-173">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8a01f-173">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8a01f-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a01f-174">NOTES</span></span>

## <span data-ttu-id="8a01f-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a01f-175">RELATED LINKS</span></span>

[<span data-ttu-id="8a01f-176">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8a01f-176">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

