---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://go.microsoft.com/fwlink/?LinkId=690164
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 4e46c100984a9e50794130b3de6e30ce5f664ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439931"
---
# <span data-ttu-id="8bb3c-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bb3c-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="8bb3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bb3c-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb3c-103">Remove todas as permissões de um usuário ou aplicativo de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bb3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bb3c-104">SYNTAX</span></span>

### <span data-ttu-id="8bb3c-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8bb3c-105">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bb3c-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8bb3c-106">ByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bb3c-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="8bb3c-107">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bb3c-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="8bb3c-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bb3c-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="8bb3c-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bb3c-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bb3c-110">DESCRIPTION</span></span>
<span data-ttu-id="8bb3c-111">O cmdlet **Remove-AzureRmKeyVaultAccessPolicy** remove todas as permissões para um usuário ou aplicativo ou para todos os usuários e aplicativos de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-111">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="8bb3c-112">Mesmo que você remova todas as permissões, o proprietário da assinatura do Azure que contém o cofre de chaves pode adicionar permissões ao cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-112">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="8bb3c-113">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-113">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="8bb3c-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bb3c-114">EXAMPLES</span></span>

### <span data-ttu-id="8bb3c-115">Exemplo 1: remover permissões de um usuário</span><span class="sxs-lookup"><span data-stu-id="8bb3c-115">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="8bb3c-116">Esse comando Remove todas as permissões que um usuário PattiFuller@contoso.com tem no cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-116">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="8bb3c-117">Exemplo 2: remover as permissões de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="8bb3c-117">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="8bb3c-118">Esse comando Remove todas as permissões que um aplicativo tem no cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-118">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="8bb3c-119">Este exemplo identifica o aplicativo usando o nome principal do serviço registrado no Azure Active Directory http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="8bb3c-119">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="8bb3c-120">Exemplo 3: remover as permissões de um aplicativo usando sua ID de objeto</span><span class="sxs-lookup"><span data-stu-id="8bb3c-120">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="8bb3c-121">Esse comando Remove todas as permissões que um aplicativo tem no cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-121">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="8bb3c-122">Este exemplo identifica o aplicativo pela ID de objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-122">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="8bb3c-123">Exemplo 4: remover permissões para o provedor de recursos Microsoft. Compute</span><span class="sxs-lookup"><span data-stu-id="8bb3c-123">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="8bb3c-124">Esse comando Remove a permissão do provedor de recursos Microsoft. COMPUTE para obter os segredos da Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-124">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="8bb3c-125">OS</span><span class="sxs-lookup"><span data-stu-id="8bb3c-125">PARAMETERS</span></span>

### <span data-ttu-id="8bb3c-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8bb3c-126">-ApplicationId</span></span>
<span data-ttu-id="8bb3c-127">Para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-127">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb3c-128">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8bb3c-128">-EmailAddress</span></span>
<span data-ttu-id="8bb3c-129">Especifica o endereço de email do usuário do qual o acesso você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-129">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb3c-130">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="8bb3c-130">-EnabledForDeployment</span></span>
<span data-ttu-id="8bb3c-131">Habilita o provedor de recursos Microsoft. Compute a recuperar segredos deste cofre de chaves quando esse cofre de chaves é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-131">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb3c-132">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="8bb3c-132">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="8bb3c-133">Habilita o serviço de criptografia de disco do Azure a obter segredos e a desencapsulação de chaves deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-133">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb3c-134">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="8bb3c-134">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="8bb3c-135">Permite que o Azure Resource Manager obtenha os segredos deste cofre de chaves quando esse cofre de chaves é referenciado em uma implantação de modelo.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-135">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb3c-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8bb3c-136">-ObjectId</span></span>
<span data-ttu-id="8bb3c-137">Especifica a ID de objeto da entidade de usuário ou serviço do Azure Active Directory para a qual as permissões são removidas.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-137">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb3c-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bb3c-138">-PassThru</span></span>
<span data-ttu-id="8bb3c-139">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-139">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8bb3c-140">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-140">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8bb3c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bb3c-141">-ResourceGroupName</span></span>
<span data-ttu-id="8bb3c-142">Especifica o nome do grupo de recursos associado ao cofre de chaves cuja política de acesso está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-142">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="8bb3c-143">Se não for especificado, esse cmdlet pesquisará o cofre de chaves na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-143">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb3c-144">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="8bb3c-144">-ServicePrincipalName</span></span>
<span data-ttu-id="8bb3c-145">Especifica o nome principal do serviço do aplicativo cujas permissões você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-145">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="8bb3c-146">Especifique a identificação do aplicativo, também conhecida como ID do cliente, registrada para o aplicativo no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-146">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb3c-147">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8bb3c-147">-UserPrincipalName</span></span>
<span data-ttu-id="8bb3c-148">Especifica o nome UPN do usuário cujo acesso você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-148">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb3c-149">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="8bb3c-149">-VaultName</span></span>
<span data-ttu-id="8bb3c-150">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-150">Specifies the name of the key vault.</span></span>
<span data-ttu-id="8bb3c-151">Esse cmdlet Remove permissões para o cofre de chaves que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-151">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb3c-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8bb3c-152">-Confirm</span></span>
<span data-ttu-id="8bb3c-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bb3c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bb3c-154">-WhatIf</span></span>
<span data-ttu-id="8bb3c-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bb3c-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bb3c-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb3c-157">-DefaultProfile</span></span>
<span data-ttu-id="8bb3c-158">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bb3c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb3c-159">CommonParameters</span></span>
<span data-ttu-id="8bb3c-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb3c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb3c-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bb3c-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb3c-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bb3c-162">INPUTS</span></span>

## <span data-ttu-id="8bb3c-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bb3c-163">OUTPUTS</span></span>

### <span data-ttu-id="8bb3c-164">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="8bb3c-164">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="8bb3c-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bb3c-165">NOTES</span></span>

## <span data-ttu-id="8bb3c-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bb3c-166">RELATED LINKS</span></span>

[<span data-ttu-id="8bb3c-167">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bb3c-167">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

