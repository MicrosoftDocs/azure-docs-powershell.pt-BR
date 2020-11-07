---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 544af56c5e1ff72a3b23c3dcf89af36f7d74eff2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785533"
---
# <span data-ttu-id="2121f-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2121f-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="2121f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2121f-102">SYNOPSIS</span></span>
<span data-ttu-id="2121f-103">Atualiza o estado de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="2121f-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2121f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2121f-104">SYNTAX</span></span>

### <span data-ttu-id="2121f-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="2121f-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2121f-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="2121f-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] -IdentityType <ResourceIdentityType>
 [-SkuName <String>] [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>]
 [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>]
 [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2121f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2121f-107">DESCRIPTION</span></span>
<span data-ttu-id="2121f-108">O cmdlet **Update-AzureRmVmss** atualiza o estado de um VMSS (conjunto de dimensionamento de máquina virtual) para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="2121f-108">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="2121f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2121f-109">EXAMPLES</span></span>

### <span data-ttu-id="2121f-110">Exemplo 1: Atualize o estado de um VMSS para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="2121f-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="2121f-111">Esse comando atualiza o estado do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001 para o estado de um objeto VMSS local, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="2121f-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="2121f-112">OS</span><span class="sxs-lookup"><span data-stu-id="2121f-112">PARAMETERS</span></span>

### <span data-ttu-id="2121f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2121f-113">-AsJob</span></span>
<span data-ttu-id="2121f-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="2121f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2121f-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="2121f-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="2121f-116">Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias do conjunto de escala de forma contínua quando uma versão mais recente da imagem se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="2121f-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="2121f-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="2121f-118">Se o diagnóstico de inicialização deve ser habilitado no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2121f-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="2121f-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="2121f-120">URL da conta de armazenamento a ser usada para colocar a captura de tela e a saída do console.</span><span class="sxs-lookup"><span data-stu-id="2121f-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="2121f-121">-CustomData</span></span>
<span data-ttu-id="2121f-122">Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.</span><span class="sxs-lookup"><span data-stu-id="2121f-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="2121f-123">Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2121f-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="2121f-124">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="2121f-124">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2121f-125">-DefaultProfile</span></span>
<span data-ttu-id="2121f-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2121f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2121f-127">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="2121f-127">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="2121f-128">Indica que esse cmdlet desabilita a autenticação de senha para o SO Linux.</span><span class="sxs-lookup"><span data-stu-id="2121f-128">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-129">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="2121f-129">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="2121f-130">Indica se as máquinas virtuais do Windows no VMSS estão habilitadas para atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="2121f-130">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-131">-Identityid</span><span class="sxs-lookup"><span data-stu-id="2121f-131">-IdentityId</span></span>
<span data-ttu-id="2121f-132">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2121f-132">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="2121f-133">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="2121f-133">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-134">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2121f-134">-IdentityType</span></span>
<span data-ttu-id="2121f-135">Especifica o tipo de identidade usado para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2121f-135">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="2121f-136">O tipo ' SystemAssignedUserAssigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="2121f-136">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="2121f-137">O tipo ' nenhum ' removerá todas as identidades do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2121f-137">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="2121f-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2121f-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2121f-139">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="2121f-139">SystemAssigned</span></span>
- <span data-ttu-id="2121f-140">Userassigned</span><span class="sxs-lookup"><span data-stu-id="2121f-140">UserAssigned</span></span>
- <span data-ttu-id="2121f-141">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="2121f-141">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="2121f-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2121f-142">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-143">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="2121f-143">-ImageReferenceId</span></span>
<span data-ttu-id="2121f-144">Especifica a ID de referência da imagem.</span><span class="sxs-lookup"><span data-stu-id="2121f-144">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-145">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="2121f-145">-ImageReferenceOffer</span></span>
<span data-ttu-id="2121f-146">Especifica o tipo de oferta da máquina virtual da máquina (VMImage).</span><span class="sxs-lookup"><span data-stu-id="2121f-146">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="2121f-147">Para obter uma oferta de imagem, use o cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="2121f-147">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-148">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="2121f-148">-ImageReferencePublisher</span></span>
<span data-ttu-id="2121f-149">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="2121f-149">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="2121f-150">Para obter um fornecedor, use o cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="2121f-150">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-151">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="2121f-151">-ImageReferenceSku</span></span>
<span data-ttu-id="2121f-152">Especifica o SKU da VMImage.</span><span class="sxs-lookup"><span data-stu-id="2121f-152">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="2121f-153">Para obter os SKUs, use o cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="2121f-153">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-154">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="2121f-154">-ImageReferenceVersion</span></span>
<span data-ttu-id="2121f-155">Especifica a versão da VMImage.</span><span class="sxs-lookup"><span data-stu-id="2121f-155">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="2121f-156">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="2121f-156">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-157">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="2121f-157">-ImageUri</span></span>
<span data-ttu-id="2121f-158">Especifica o URI do blob para a imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="2121f-158">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="2121f-159">O VMSS cria um disco do sistema operacional no mesmo contêiner da imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="2121f-159">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-160">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2121f-160">-LicenseType</span></span>
<span data-ttu-id="2121f-161">Especifique o tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="2121f-161">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-162">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2121f-162">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="2121f-163">Especifica o tipo de conta de armazenamento para o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="2121f-163">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="2121f-164">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2121f-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2121f-165">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="2121f-165">StandardLRS</span></span>
- <span data-ttu-id="2121f-166">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="2121f-166">PremiumLRS</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-167">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="2121f-167">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="2121f-168">A porcentagem máxima do total de instâncias da máquina virtual que serão atualizadas simultaneamente pela atualização sem interrupção em um lote.</span><span class="sxs-lookup"><span data-stu-id="2121f-168">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="2121f-169">Como se trata de um valor máximo, instâncias não íntegras em lotes anteriores ou futuros podem fazer com que a porcentagem de instâncias em um lote seja reduzida para garantir maior confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="2121f-169">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="2121f-170">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="2121f-170">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-171">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="2121f-171">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="2121f-172">A porcentagem máxima do total de instâncias da máquina virtual no conjunto de escala que podem ser simultaneamente não íntegras, como resultado da atualização ou por estar em um estado não íntegro pelas verificações de integridade da máquina virtual antes de anular a atualização sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="2121f-172">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="2121f-173">Esta restrição será verificada antes de iniciar qualquer lote.</span><span class="sxs-lookup"><span data-stu-id="2121f-173">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="2121f-174">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="2121f-174">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-175">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="2121f-175">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="2121f-176">A porcentagem máxima de instâncias da máquina virtual atualizadas que podem ser encontradas em um estado não íntegro.</span><span class="sxs-lookup"><span data-stu-id="2121f-176">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="2121f-177">Essa verificação ocorrerá após a atualização de cada lote.</span><span class="sxs-lookup"><span data-stu-id="2121f-177">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="2121f-178">Se essa porcentagem já tiver sido excedida, a atualização sem interrupção será anulada.</span><span class="sxs-lookup"><span data-stu-id="2121f-178">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="2121f-179">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="2121f-179">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-180">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="2121f-180">-OsDiskCaching</span></span>
<span data-ttu-id="2121f-181">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2121f-181">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="2121f-182">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2121f-182">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2121f-183">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2121f-183">None</span></span>
- <span data-ttu-id="2121f-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2121f-184">ReadOnly</span></span>
- <span data-ttu-id="2121f-185">Leitura</span><span class="sxs-lookup"><span data-stu-id="2121f-185">ReadWrite</span></span>

<span data-ttu-id="2121f-186">O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="2121f-186">The default value is ReadWrite.</span></span>
<span data-ttu-id="2121f-187">Se você alterar o valor de cache, o cmdlet reiniciará a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2121f-187">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="2121f-188">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="2121f-188">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-189">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="2121f-189">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="2121f-190">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2121f-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-191">-Superprovisionamento</span><span class="sxs-lookup"><span data-stu-id="2121f-191">-Overprovision</span></span>
<span data-ttu-id="2121f-192">Indica se o cmdlet está supervisionando o VMSS.</span><span class="sxs-lookup"><span data-stu-id="2121f-192">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-193">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="2121f-193">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="2121f-194">O tempo de espera entre concluir a atualização de todas as máquinas virtuais em um lote e iniciar o próximo lote.</span><span class="sxs-lookup"><span data-stu-id="2121f-194">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="2121f-195">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="2121f-195">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="2121f-196">O valor padrão é 0 segundos (PT0S).</span><span class="sxs-lookup"><span data-stu-id="2121f-196">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-197">-PlanName</span><span class="sxs-lookup"><span data-stu-id="2121f-197">-PlanName</span></span>
<span data-ttu-id="2121f-198">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="2121f-198">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-199">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="2121f-199">-PlanProduct</span></span>
<span data-ttu-id="2121f-200">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="2121f-200">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-201">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="2121f-201">-PlanPromotionCode</span></span>
<span data-ttu-id="2121f-202">Especifica o código promocional do plano.</span><span class="sxs-lookup"><span data-stu-id="2121f-202">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-203">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="2121f-203">-PlanPublisher</span></span>
<span data-ttu-id="2121f-204">Especifica o fornecedor do plano.</span><span class="sxs-lookup"><span data-stu-id="2121f-204">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-205">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="2121f-205">-ProvisionVMAgent</span></span>
<span data-ttu-id="2121f-206">Indica se o agente da máquina virtual deve ser provisionado nas máquinas virtuais do Windows no VMSS.</span><span class="sxs-lookup"><span data-stu-id="2121f-206">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2121f-207">-ResourceGroupName</span></span>
<span data-ttu-id="2121f-208">Especifica o nome do grupo de recursos ao qual o VMSS pertence.</span><span class="sxs-lookup"><span data-stu-id="2121f-208">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-209">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2121f-209">-SinglePlacementGroup</span></span>
<span data-ttu-id="2121f-210">Especifica o grupo de posicionamento único.</span><span class="sxs-lookup"><span data-stu-id="2121f-210">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-211">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2121f-211">-SkuCapacity</span></span>
<span data-ttu-id="2121f-212">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="2121f-212">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-213">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2121f-213">-SkuName</span></span>
<span data-ttu-id="2121f-214">Especifica o tamanho de todas as instâncias de VMSS.</span><span class="sxs-lookup"><span data-stu-id="2121f-214">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-215">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2121f-215">-SkuTier</span></span>
<span data-ttu-id="2121f-216">Especifica o nível de VMSS.</span><span class="sxs-lookup"><span data-stu-id="2121f-216">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="2121f-217">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2121f-217">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2121f-218">Oficial</span><span class="sxs-lookup"><span data-stu-id="2121f-218">Standard</span></span>
- <span data-ttu-id="2121f-219">Basic</span><span class="sxs-lookup"><span data-stu-id="2121f-219">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-220">-Marca</span><span class="sxs-lookup"><span data-stu-id="2121f-220">-Tag</span></span>
<span data-ttu-id="2121f-221">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2121f-221">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2121f-222">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="2121f-222">For example:</span></span>

<span data-ttu-id="2121f-223">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2121f-223">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-224">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="2121f-224">-TimeZone</span></span>
<span data-ttu-id="2121f-225">Especifica o fuso horário para o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="2121f-225">Specifies the time zone for Windows OS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-226">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="2121f-226">-UpgradePolicyMode</span></span>
<span data-ttu-id="2121f-227">Especificou o modo de uma atualização para máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="2121f-227">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="2121f-228">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2121f-228">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2121f-229">Automático</span><span class="sxs-lookup"><span data-stu-id="2121f-229">Automatic</span></span>
- <span data-ttu-id="2121f-230">Manual</span><span class="sxs-lookup"><span data-stu-id="2121f-230">Manual</span></span>
- <span data-ttu-id="2121f-231">Implantação</span><span class="sxs-lookup"><span data-stu-id="2121f-231">Rolling</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-232">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="2121f-232">-VhdContainer</span></span>
<span data-ttu-id="2121f-233">Especifica as URLs de contêiner usadas para armazenar discos do sistema operacional para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="2121f-233">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2121f-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2121f-235">Especifica um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="2121f-235">Specifies a local VMSS object.</span></span>
<span data-ttu-id="2121f-236">Para obter um objeto VMSS, use o cmdlet Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="2121f-236">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="2121f-237">Esse objeto da máquina virtual contém o estado atualizado para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="2121f-237">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-238">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2121f-238">-VMScaleSetName</span></span>
<span data-ttu-id="2121f-239">Especifica o nome do VMSS que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="2121f-239">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-240">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2121f-240">-Confirm</span></span>
<span data-ttu-id="2121f-241">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2121f-241">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-242">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2121f-242">-WhatIf</span></span>
<span data-ttu-id="2121f-243">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2121f-243">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2121f-244">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2121f-244">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2121f-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2121f-245">CommonParameters</span></span>
<span data-ttu-id="2121f-246">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2121f-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2121f-247">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2121f-247">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2121f-248">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2121f-248">INPUTS</span></span>

### <span data-ttu-id="2121f-249">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2121f-249">VirtualMachineScaleSet</span></span>
<span data-ttu-id="2121f-250">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2121f-250">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="2121f-251">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2121f-251">OUTPUTS</span></span>

### <span data-ttu-id="2121f-252">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2121f-252">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2121f-253">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2121f-253">NOTES</span></span>

## <span data-ttu-id="2121f-254">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2121f-254">RELATED LINKS</span></span>

[<span data-ttu-id="2121f-255">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2121f-255">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="2121f-256">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2121f-256">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="2121f-257">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2121f-257">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="2121f-258">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2121f-258">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="2121f-259">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2121f-259">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="2121f-260">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2121f-260">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="2121f-261">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2121f-261">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


