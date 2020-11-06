---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 6fe6f6345f9208a524e1162fb317b88c450f3909
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601194"
---
# <span data-ttu-id="4301b-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4301b-101">Update-AzVmss</span></span>

## <span data-ttu-id="4301b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4301b-102">SYNOPSIS</span></span>
<span data-ttu-id="4301b-103">Atualiza o estado de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="4301b-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="4301b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4301b-104">SYNTAX</span></span>

### <span data-ttu-id="4301b-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="4301b-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-BootDiagnosticsEnabled <Boolean>] [-Tag <Hashtable>]
 [-UpgradePolicyMode <UpgradeMode>] [-DisablePasswordAuthentication <Boolean>]
 [-ManagedDiskStorageAccountType <String>] [-AutomaticOSUpgrade <Boolean>] [-SkuTier <String>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-SinglePlacementGroup <Boolean>] [-PlanPublisher <String>]
 [-BootDiagnosticsStorageUri <String>] [-Overprovision <Boolean>] [-DisableAutoRollback <Boolean>]
 [-TimeZone <String>] [-PlanPromotionCode <String>] [-MaxBatchInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-ImageReferenceSku <String>]
 [-VhdContainer <String[]>] [-MaxUnhealthyInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-SkuName <String>] [-ImageReferenceVersion <String>]
 [-PauseTimeBetweenBatches <String>] [-ImageUri <String>] [-PlanName <String>] [-PlanProduct <String>]
 [-ImageReferenceId <String>] [-EnableAutomaticUpdate <Boolean>] [-CustomData <String>] [-LicenseType <String>]
 [-OsDiskCaching <CachingTypes>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4301b-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4301b-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-BootDiagnosticsEnabled <Boolean>] [-Tag <Hashtable>]
 [-UpgradePolicyMode <UpgradeMode>] [-DisablePasswordAuthentication <Boolean>]
 -IdentityType <ResourceIdentityType> [-ManagedDiskStorageAccountType <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SkuTier <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-SinglePlacementGroup <Boolean>]
 [-PlanPublisher <String>] [-BootDiagnosticsStorageUri <String>] [-Overprovision <Boolean>]
 [-DisableAutoRollback <Boolean>] [-TimeZone <String>] [-PlanPromotionCode <String>]
 [-MaxBatchInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-ImageReferenceSku <String>] [-VhdContainer <String[]>]
 [-MaxUnhealthyInstancePercent <Int32>] [-ImageReferencePublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-SkuName <String>] [-ImageReferenceVersion <String>] [-PauseTimeBetweenBatches <String>] [-ImageUri <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-ImageReferenceId <String>] [-EnableAutomaticUpdate <Boolean>]
 [-CustomData <String>] [-LicenseType <String>] [-OsDiskCaching <CachingTypes>] [-IdentityId <String[]>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4301b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4301b-107">DESCRIPTION</span></span>
<span data-ttu-id="4301b-108">O cmdlet **Update-AzVmss** atualiza o estado de um VMSS (conjunto de dimensionamento de máquina virtual) para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="4301b-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="4301b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4301b-109">EXAMPLES</span></span>

### <span data-ttu-id="4301b-110">Exemplo 1: Atualize o estado de um VMSS para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="4301b-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="4301b-111">Esse comando atualiza o estado do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001 para o estado de um objeto VMSS local, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="4301b-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="4301b-112">OS</span><span class="sxs-lookup"><span data-stu-id="4301b-112">PARAMETERS</span></span>

### <span data-ttu-id="4301b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4301b-113">-AsJob</span></span>
<span data-ttu-id="4301b-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="4301b-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4301b-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="4301b-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="4301b-116">Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias do conjunto de escala de forma contínua quando uma versão mais recente da imagem se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="4301b-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="4301b-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="4301b-118">Se o diagnóstico de inicialização deve ser habilitado no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4301b-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="4301b-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="4301b-120">URL da conta de armazenamento a ser usada para colocar a captura de tela e a saída do console.</span><span class="sxs-lookup"><span data-stu-id="4301b-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="4301b-121">-CustomData</span></span>
<span data-ttu-id="4301b-122">Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.</span><span class="sxs-lookup"><span data-stu-id="4301b-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="4301b-123">Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4301b-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="4301b-124">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="4301b-124">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4301b-125">-DefaultProfile</span></span>
<span data-ttu-id="4301b-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4301b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4301b-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="4301b-127">-DisableAutoRollback</span></span>
<span data-ttu-id="4301b-128">Desabilitar a reversão automática para a política de atualização automática de so</span><span class="sxs-lookup"><span data-stu-id="4301b-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="4301b-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="4301b-130">Indica que esse cmdlet desabilita a autenticação de senha para o SO Linux.</span><span class="sxs-lookup"><span data-stu-id="4301b-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="4301b-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="4301b-132">Indica se as máquinas virtuais do Windows no VMSS estão habilitadas para atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="4301b-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-133">-Identityid</span><span class="sxs-lookup"><span data-stu-id="4301b-133">-IdentityId</span></span>
<span data-ttu-id="4301b-134">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4301b-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="4301b-135">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="4301b-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4301b-136">-IdentityType</span></span>
<span data-ttu-id="4301b-137">Especifica o tipo de identidade usado para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4301b-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="4301b-138">O tipo ' SystemAssignedUserAssigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="4301b-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="4301b-139">O tipo ' nenhum ' removerá todas as identidades do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4301b-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="4301b-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4301b-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4301b-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="4301b-141">SystemAssigned</span></span>
- <span data-ttu-id="4301b-142">Userassigned</span><span class="sxs-lookup"><span data-stu-id="4301b-142">UserAssigned</span></span>
- <span data-ttu-id="4301b-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="4301b-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="4301b-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4301b-144">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="4301b-145">-ImageReferenceId</span></span>
<span data-ttu-id="4301b-146">Especifica a ID de referência da imagem.</span><span class="sxs-lookup"><span data-stu-id="4301b-146">Specifies the image reference ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="4301b-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="4301b-148">Especifica o tipo de oferta da máquina virtual da máquina (VMImage).</span><span class="sxs-lookup"><span data-stu-id="4301b-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="4301b-149">Para obter uma oferta de imagem, use o cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="4301b-149">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="4301b-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="4301b-151">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="4301b-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="4301b-152">Para obter um fornecedor, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="4301b-152">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="4301b-153">-ImageReferenceSku</span></span>
<span data-ttu-id="4301b-154">Especifica o SKU da VMImage.</span><span class="sxs-lookup"><span data-stu-id="4301b-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="4301b-155">Para obter os SKUs, use o cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="4301b-155">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="4301b-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="4301b-157">Especifica a versão da VMImage.</span><span class="sxs-lookup"><span data-stu-id="4301b-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="4301b-158">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="4301b-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="4301b-159">-ImageUri</span></span>
<span data-ttu-id="4301b-160">Especifica o URI do blob para a imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="4301b-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="4301b-161">O VMSS cria um disco do sistema operacional no mesmo contêiner da imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="4301b-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4301b-162">-LicenseType</span></span>
<span data-ttu-id="4301b-163">Especifique o tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="4301b-163">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4301b-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="4301b-165">Especifica o tipo de conta de armazenamento para o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4301b-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="4301b-166">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4301b-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4301b-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="4301b-167">StandardLRS</span></span>
- <span data-ttu-id="4301b-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="4301b-168">PremiumLRS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="4301b-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="4301b-170">A porcentagem máxima do total de instâncias da máquina virtual que serão atualizadas simultaneamente pela atualização sem interrupção em um lote.</span><span class="sxs-lookup"><span data-stu-id="4301b-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="4301b-171">Como se trata de um valor máximo, instâncias não íntegras em lotes anteriores ou futuros podem fazer com que a porcentagem de instâncias em um lote seja reduzida para garantir maior confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="4301b-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="4301b-172">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="4301b-172">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-173">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="4301b-173">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="4301b-174">A porcentagem máxima do total de instâncias da máquina virtual no conjunto de escala que podem ser simultaneamente não íntegras, como resultado da atualização ou por estar em um estado não íntegro pelas verificações de integridade da máquina virtual antes de anular a atualização sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="4301b-174">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="4301b-175">Esta restrição será verificada antes de iniciar qualquer lote.</span><span class="sxs-lookup"><span data-stu-id="4301b-175">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="4301b-176">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="4301b-176">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-177">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="4301b-177">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="4301b-178">A porcentagem máxima de instâncias da máquina virtual atualizadas que podem ser encontradas em um estado não íntegro.</span><span class="sxs-lookup"><span data-stu-id="4301b-178">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="4301b-179">Essa verificação ocorrerá após a atualização de cada lote.</span><span class="sxs-lookup"><span data-stu-id="4301b-179">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="4301b-180">Se essa porcentagem já tiver sido excedida, a atualização sem interrupção será anulada.</span><span class="sxs-lookup"><span data-stu-id="4301b-180">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="4301b-181">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="4301b-181">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-182">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="4301b-182">-OsDiskCaching</span></span>
<span data-ttu-id="4301b-183">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4301b-183">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="4301b-184">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4301b-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4301b-185">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4301b-185">None</span></span>
- <span data-ttu-id="4301b-186">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4301b-186">ReadOnly</span></span>
- <span data-ttu-id="4301b-187">ReadWrite o valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="4301b-187">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="4301b-188">Se você alterar o valor de cache, o cmdlet reiniciará a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4301b-188">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="4301b-189">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="4301b-189">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-190">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="4301b-190">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="4301b-191">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4301b-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-192">-Superprovisionamento</span><span class="sxs-lookup"><span data-stu-id="4301b-192">-Overprovision</span></span>
<span data-ttu-id="4301b-193">Indica se o cmdlet está supervisionando o VMSS.</span><span class="sxs-lookup"><span data-stu-id="4301b-193">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-194">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="4301b-194">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="4301b-195">O tempo de espera entre concluir a atualização de todas as máquinas virtuais em um lote e iniciar o próximo lote.</span><span class="sxs-lookup"><span data-stu-id="4301b-195">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="4301b-196">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="4301b-196">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="4301b-197">O valor padrão é 0 segundos (PT0S).</span><span class="sxs-lookup"><span data-stu-id="4301b-197">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-198">-PlanName</span><span class="sxs-lookup"><span data-stu-id="4301b-198">-PlanName</span></span>
<span data-ttu-id="4301b-199">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="4301b-199">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-200">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="4301b-200">-PlanProduct</span></span>
<span data-ttu-id="4301b-201">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="4301b-201">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-202">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="4301b-202">-PlanPromotionCode</span></span>
<span data-ttu-id="4301b-203">Especifica o código promocional do plano.</span><span class="sxs-lookup"><span data-stu-id="4301b-203">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-204">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="4301b-204">-PlanPublisher</span></span>
<span data-ttu-id="4301b-205">Especifica o fornecedor do plano.</span><span class="sxs-lookup"><span data-stu-id="4301b-205">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-206">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="4301b-206">-ProvisionVMAgent</span></span>
<span data-ttu-id="4301b-207">Indica se o agente da máquina virtual deve ser provisionado nas máquinas virtuais do Windows no VMSS.</span><span class="sxs-lookup"><span data-stu-id="4301b-207">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-208">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4301b-208">-ResourceGroupName</span></span>
<span data-ttu-id="4301b-209">Especifica o nome do grupo de recursos ao qual o VMSS pertence.</span><span class="sxs-lookup"><span data-stu-id="4301b-209">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="4301b-210">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="4301b-210">-SinglePlacementGroup</span></span>
<span data-ttu-id="4301b-211">Especifica o grupo de posicionamento único.</span><span class="sxs-lookup"><span data-stu-id="4301b-211">Specifies the single placement group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-212">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4301b-212">-SkuCapacity</span></span>
<span data-ttu-id="4301b-213">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="4301b-213">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-214">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4301b-214">-SkuName</span></span>
<span data-ttu-id="4301b-215">Especifica o tamanho de todas as instâncias de VMSS.</span><span class="sxs-lookup"><span data-stu-id="4301b-215">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-216">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4301b-216">-SkuTier</span></span>
<span data-ttu-id="4301b-217">Especifica o nível de VMSS.</span><span class="sxs-lookup"><span data-stu-id="4301b-217">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="4301b-218">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4301b-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4301b-219">Oficial</span><span class="sxs-lookup"><span data-stu-id="4301b-219">Standard</span></span>
- <span data-ttu-id="4301b-220">Basic</span><span class="sxs-lookup"><span data-stu-id="4301b-220">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-221">-Marca</span><span class="sxs-lookup"><span data-stu-id="4301b-221">-Tag</span></span>
<span data-ttu-id="4301b-222">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4301b-222">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4301b-223">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4301b-223">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-224">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="4301b-224">-TimeZone</span></span>
<span data-ttu-id="4301b-225">Especifica o fuso horário para o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="4301b-225">Specifies the time zone for Windows OS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-226">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="4301b-226">-UltraSSDEnabled</span></span>
<span data-ttu-id="4301b-227">O sinalizador que habilita ou desabilita uma funcionalidade para ter um ou mais discos de dados gerenciados com o tipo de conta de armazenamento UltraSSD_LRS no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4301b-227">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="4301b-228">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a um VMSS somente se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="4301b-228">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="4301b-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="4301b-230">Especificou o modo de uma atualização para máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="4301b-230">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="4301b-231">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4301b-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4301b-232">Automático</span><span class="sxs-lookup"><span data-stu-id="4301b-232">Automatic</span></span>
- <span data-ttu-id="4301b-233">Manual</span><span class="sxs-lookup"><span data-stu-id="4301b-233">Manual</span></span>
- <span data-ttu-id="4301b-234">Implantação</span><span class="sxs-lookup"><span data-stu-id="4301b-234">Rolling</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-235">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="4301b-235">-VhdContainer</span></span>
<span data-ttu-id="4301b-236">Especifica as URLs de contêiner usadas para armazenar discos do sistema operacional para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="4301b-236">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-237">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4301b-237">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4301b-238">Especifica um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="4301b-238">Specifies a local VMSS object.</span></span>
<span data-ttu-id="4301b-239">Para obter um objeto VMSS, use o cmdlet Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4301b-239">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="4301b-240">Esse objeto da máquina virtual contém o estado atualizado para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="4301b-240">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-241">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4301b-241">-VMScaleSetName</span></span>
<span data-ttu-id="4301b-242">Especifica o nome do VMSS que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="4301b-242">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-243">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4301b-243">-Confirm</span></span>
<span data-ttu-id="4301b-244">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4301b-244">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4301b-245">-WhatIf</span></span>
<span data-ttu-id="4301b-246">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4301b-246">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4301b-247">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4301b-247">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4301b-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4301b-248">CommonParameters</span></span>
<span data-ttu-id="4301b-249">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4301b-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4301b-250">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4301b-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4301b-251">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4301b-251">INPUTS</span></span>

### <span data-ttu-id="4301b-252">System. String</span><span class="sxs-lookup"><span data-stu-id="4301b-252">System.String</span></span>

### <span data-ttu-id="4301b-253">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4301b-253">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4301b-254">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4301b-254">System.Boolean</span></span>

## <span data-ttu-id="4301b-255">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4301b-255">OUTPUTS</span></span>

### <span data-ttu-id="4301b-256">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4301b-256">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4301b-257">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4301b-257">NOTES</span></span>

## <span data-ttu-id="4301b-258">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4301b-258">RELATED LINKS</span></span>

[<span data-ttu-id="4301b-259">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4301b-259">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="4301b-260">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4301b-260">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="4301b-261">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4301b-261">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="4301b-262">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4301b-262">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="4301b-263">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4301b-263">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="4301b-264">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4301b-264">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="4301b-265">Parar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4301b-265">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


