---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: c8a482c4d3021e1dd5de30582d2dad501a20ed41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597150"
---
# <span data-ttu-id="35475-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="35475-101">Update-AzVmss</span></span>

## <span data-ttu-id="35475-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35475-102">SYNOPSIS</span></span>
<span data-ttu-id="35475-103">Atualiza o estado de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="35475-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="35475-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35475-104">SYNTAX</span></span>

### <span data-ttu-id="35475-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="35475-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35475-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="35475-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-IdentityId <String[]>] -IdentityType <ResourceIdentityType> [-ImageReferenceId <String>]
 [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>]
 [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35475-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35475-107">DESCRIPTION</span></span>
<span data-ttu-id="35475-108">O cmdlet **Update-AzVmss** atualiza o estado de um VMSS (conjunto de dimensionamento de máquina virtual) para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="35475-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="35475-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35475-109">EXAMPLES</span></span>

### <span data-ttu-id="35475-110">Exemplo 1: Atualize o estado de um VMSS para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="35475-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="35475-111">Esse comando atualiza o estado do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001 para o estado de um objeto VMSS local, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="35475-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="35475-112">OS</span><span class="sxs-lookup"><span data-stu-id="35475-112">PARAMETERS</span></span>

### <span data-ttu-id="35475-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35475-113">-AsJob</span></span>
<span data-ttu-id="35475-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="35475-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="35475-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="35475-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="35475-116">Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias do conjunto de escala de forma contínua quando uma versão mais recente da imagem se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="35475-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="35475-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="35475-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="35475-118">Se o diagnóstico de inicialização deve ser habilitado no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35475-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="35475-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="35475-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="35475-120">URL da conta de armazenamento a ser usada para colocar a captura de tela e a saída do console.</span><span class="sxs-lookup"><span data-stu-id="35475-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="35475-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="35475-121">-CustomData</span></span>
<span data-ttu-id="35475-122">Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.</span><span class="sxs-lookup"><span data-stu-id="35475-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="35475-123">Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35475-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="35475-124">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="35475-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="35475-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35475-125">-DefaultProfile</span></span>
<span data-ttu-id="35475-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35475-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35475-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="35475-127">-DisableAutoRollback</span></span>
<span data-ttu-id="35475-128">Desabilitar a reversão automática para a política de atualização automática de so</span><span class="sxs-lookup"><span data-stu-id="35475-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="35475-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="35475-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="35475-130">Indica que esse cmdlet desabilita a autenticação de senha para o SO Linux.</span><span class="sxs-lookup"><span data-stu-id="35475-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="35475-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="35475-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="35475-132">Indica se as máquinas virtuais do Windows no VMSS estão habilitadas para atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="35475-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="35475-133">-Identityid</span><span class="sxs-lookup"><span data-stu-id="35475-133">-IdentityId</span></span>
<span data-ttu-id="35475-134">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35475-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="35475-135">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="35475-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="35475-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="35475-136">-IdentityType</span></span>
<span data-ttu-id="35475-137">Especifica o tipo de identidade usado para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35475-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="35475-138">O tipo ' SystemAssignedUserAssigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="35475-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="35475-139">O tipo ' nenhum ' removerá todas as identidades do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35475-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="35475-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35475-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35475-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="35475-141">SystemAssigned</span></span>
- <span data-ttu-id="35475-142">Userassigned</span><span class="sxs-lookup"><span data-stu-id="35475-142">UserAssigned</span></span>
- <span data-ttu-id="35475-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="35475-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="35475-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="35475-144">None</span></span>

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

### <span data-ttu-id="35475-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="35475-145">-ImageReferenceId</span></span>
<span data-ttu-id="35475-146">Especifica a ID de referência da imagem.</span><span class="sxs-lookup"><span data-stu-id="35475-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="35475-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="35475-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="35475-148">Especifica o tipo de oferta da máquina virtual da máquina (VMImage).</span><span class="sxs-lookup"><span data-stu-id="35475-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="35475-149">Para obter uma oferta de imagem, use o cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="35475-149">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="35475-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="35475-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="35475-151">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="35475-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="35475-152">Para obter um fornecedor, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="35475-152">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="35475-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="35475-153">-ImageReferenceSku</span></span>
<span data-ttu-id="35475-154">Especifica o SKU da VMImage.</span><span class="sxs-lookup"><span data-stu-id="35475-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="35475-155">Para obter os SKUs, use o cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="35475-155">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="35475-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="35475-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="35475-157">Especifica a versão da VMImage.</span><span class="sxs-lookup"><span data-stu-id="35475-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="35475-158">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="35475-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="35475-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="35475-159">-ImageUri</span></span>
<span data-ttu-id="35475-160">Especifica o URI do blob para a imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="35475-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="35475-161">O VMSS cria um disco do sistema operacional no mesmo contêiner da imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="35475-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="35475-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="35475-162">-LicenseType</span></span>
<span data-ttu-id="35475-163">Especifique o tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="35475-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="35475-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="35475-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="35475-165">Especifica o tipo de conta de armazenamento para o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="35475-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="35475-166">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35475-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35475-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="35475-167">StandardLRS</span></span>
- <span data-ttu-id="35475-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="35475-168">PremiumLRS</span></span>

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

### <span data-ttu-id="35475-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="35475-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="35475-170">A porcentagem máxima do total de instâncias da máquina virtual que serão atualizadas simultaneamente pela atualização sem interrupção em um lote.</span><span class="sxs-lookup"><span data-stu-id="35475-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="35475-171">Como se trata de um valor máximo, instâncias não íntegras em lotes anteriores ou futuros podem fazer com que a porcentagem de instâncias em um lote seja reduzida para garantir maior confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="35475-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="35475-172">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="35475-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="35475-173">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="35475-173">-MaxPrice</span></span>
<span data-ttu-id="35475-174">Especifica o preço máximo que você está disposto a pagar por uma VM/VMSS de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="35475-174">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="35475-175">Este preço está em dólares americanos.</span><span class="sxs-lookup"><span data-stu-id="35475-175">This price is in US Dollars.</span></span> <span data-ttu-id="35475-176">Esse preço será comparado com o preço de baixa prioridade atual para o tamanho da VM.</span><span class="sxs-lookup"><span data-stu-id="35475-176">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="35475-177">Além disso, os preços são comparados no momento da criação/atualização de VMs/VMSS de baixa prioridade e a operação será bem-sucedida apenas se o maxPrice for maior do que o preço de baixa prioridade atual.</span><span class="sxs-lookup"><span data-stu-id="35475-177">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="35475-178">O maxPrice também será usado para remover uma VM/VMSS de baixa prioridade se o preço atual de baixa prioridade vai além do maxPrice após a criação de VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="35475-178">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="35475-179">Os valores possíveis são: qualquer valor decimal maior do que zero.</span><span class="sxs-lookup"><span data-stu-id="35475-179">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="35475-180">Exemplo: 0, 1538.</span><span class="sxs-lookup"><span data-stu-id="35475-180">Example: 0.01538.</span></span>  <span data-ttu-id="35475-181">-1 indica que a VM de baixa prioridade/VMSS não deve ser removida por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="35475-181">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="35475-182">Além disso, o preço máximo padrão é-1 se não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="35475-182">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35475-183">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="35475-183">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="35475-184">A porcentagem máxima do total de instâncias da máquina virtual no conjunto de escala que podem ser simultaneamente não íntegras, como resultado da atualização ou por estar em um estado não íntegro pelas verificações de integridade da máquina virtual antes de anular a atualização sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="35475-184">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="35475-185">Esta restrição será verificada antes de iniciar qualquer lote.</span><span class="sxs-lookup"><span data-stu-id="35475-185">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="35475-186">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="35475-186">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="35475-187">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="35475-187">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="35475-188">A porcentagem máxima de instâncias da máquina virtual atualizadas que podem ser encontradas em um estado não íntegro.</span><span class="sxs-lookup"><span data-stu-id="35475-188">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="35475-189">Essa verificação ocorrerá após a atualização de cada lote.</span><span class="sxs-lookup"><span data-stu-id="35475-189">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="35475-190">Se essa porcentagem já tiver sido excedida, a atualização sem interrupção será anulada.</span><span class="sxs-lookup"><span data-stu-id="35475-190">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="35475-191">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="35475-191">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="35475-192">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="35475-192">-OsDiskCaching</span></span>
<span data-ttu-id="35475-193">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="35475-193">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="35475-194">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35475-194">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35475-195">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="35475-195">None</span></span>
- <span data-ttu-id="35475-196">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="35475-196">ReadOnly</span></span>
- <span data-ttu-id="35475-197">ReadWrite o valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="35475-197">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="35475-198">Se você alterar o valor de cache, o cmdlet reiniciará a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35475-198">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="35475-199">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="35475-199">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="35475-200">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="35475-200">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="35475-201">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="35475-201">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="35475-202">-Superprovisionamento</span><span class="sxs-lookup"><span data-stu-id="35475-202">-Overprovision</span></span>
<span data-ttu-id="35475-203">Indica se o cmdlet está supervisionando o VMSS.</span><span class="sxs-lookup"><span data-stu-id="35475-203">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="35475-204">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="35475-204">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="35475-205">O tempo de espera entre concluir a atualização de todas as máquinas virtuais em um lote e iniciar o próximo lote.</span><span class="sxs-lookup"><span data-stu-id="35475-205">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="35475-206">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="35475-206">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="35475-207">O valor padrão é 0 segundos (PT0S).</span><span class="sxs-lookup"><span data-stu-id="35475-207">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="35475-208">-PlanName</span><span class="sxs-lookup"><span data-stu-id="35475-208">-PlanName</span></span>
<span data-ttu-id="35475-209">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="35475-209">Specifies the plan name.</span></span>

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

### <span data-ttu-id="35475-210">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="35475-210">-PlanProduct</span></span>
<span data-ttu-id="35475-211">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="35475-211">Specifies the plan product.</span></span>

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

### <span data-ttu-id="35475-212">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="35475-212">-PlanPromotionCode</span></span>
<span data-ttu-id="35475-213">Especifica o código promocional do plano.</span><span class="sxs-lookup"><span data-stu-id="35475-213">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="35475-214">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="35475-214">-PlanPublisher</span></span>
<span data-ttu-id="35475-215">Especifica o fornecedor do plano.</span><span class="sxs-lookup"><span data-stu-id="35475-215">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="35475-216">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="35475-216">-ProvisionVMAgent</span></span>
<span data-ttu-id="35475-217">Indica se o agente da máquina virtual deve ser provisionado nas máquinas virtuais do Windows no VMSS.</span><span class="sxs-lookup"><span data-stu-id="35475-217">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="35475-218">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35475-218">-ResourceGroupName</span></span>
<span data-ttu-id="35475-219">Especifica o nome do grupo de recursos ao qual o VMSS pertence.</span><span class="sxs-lookup"><span data-stu-id="35475-219">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="35475-220">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="35475-220">-SinglePlacementGroup</span></span>
<span data-ttu-id="35475-221">Especifica o grupo de posicionamento único.</span><span class="sxs-lookup"><span data-stu-id="35475-221">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="35475-222">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="35475-222">-SkuCapacity</span></span>
<span data-ttu-id="35475-223">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="35475-223">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="35475-224">-SkuName</span><span class="sxs-lookup"><span data-stu-id="35475-224">-SkuName</span></span>
<span data-ttu-id="35475-225">Especifica o tamanho de todas as instâncias de VMSS.</span><span class="sxs-lookup"><span data-stu-id="35475-225">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="35475-226">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="35475-226">-SkuTier</span></span>
<span data-ttu-id="35475-227">Especifica o nível de VMSS.</span><span class="sxs-lookup"><span data-stu-id="35475-227">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="35475-228">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35475-228">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35475-229">Oficial</span><span class="sxs-lookup"><span data-stu-id="35475-229">Standard</span></span>
- <span data-ttu-id="35475-230">Basic</span><span class="sxs-lookup"><span data-stu-id="35475-230">Basic</span></span>

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

### <span data-ttu-id="35475-231">-Marca</span><span class="sxs-lookup"><span data-stu-id="35475-231">-Tag</span></span>
<span data-ttu-id="35475-232">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="35475-232">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="35475-233">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="35475-233">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="35475-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="35475-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="35475-235">Período de tempo configurável (em minutos) em que uma máquina virtual que está sendo excluída terá que potencialmente aprovar o evento de término agendado antes de o evento ser aprovado automaticamente (tempo limite).</span><span class="sxs-lookup"><span data-stu-id="35475-235">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35475-236">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="35475-236">-TerminateScheduledEvents</span></span>
<span data-ttu-id="35475-237">Especifica se o evento de término agendado está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="35475-237">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="35475-238">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="35475-238">-TimeZone</span></span>
<span data-ttu-id="35475-239">Especifica o fuso horário para o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="35475-239">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="35475-240">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="35475-240">-UltraSSDEnabled</span></span>
<span data-ttu-id="35475-241">O sinalizador que habilita ou desabilita uma funcionalidade para ter um ou mais discos de dados gerenciados com o tipo de conta de armazenamento UltraSSD_LRS no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35475-241">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="35475-242">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a um VMSS somente se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="35475-242">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="35475-243">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="35475-243">-UpgradePolicyMode</span></span>
<span data-ttu-id="35475-244">Especificou o modo de uma atualização para máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="35475-244">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="35475-245">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35475-245">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35475-246">Automático</span><span class="sxs-lookup"><span data-stu-id="35475-246">Automatic</span></span>
- <span data-ttu-id="35475-247">Manual</span><span class="sxs-lookup"><span data-stu-id="35475-247">Manual</span></span>
- <span data-ttu-id="35475-248">Implantação</span><span class="sxs-lookup"><span data-stu-id="35475-248">Rolling</span></span>

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

### <span data-ttu-id="35475-249">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="35475-249">-VhdContainer</span></span>
<span data-ttu-id="35475-250">Especifica as URLs de contêiner usadas para armazenar discos do sistema operacional para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="35475-250">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="35475-251">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="35475-251">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="35475-252">Especifica um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="35475-252">Specifies a local VMSS object.</span></span>
<span data-ttu-id="35475-253">Para obter um objeto VMSS, use o cmdlet Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="35475-253">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="35475-254">Esse objeto da máquina virtual contém o estado atualizado para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="35475-254">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="35475-255">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="35475-255">-VMScaleSetName</span></span>
<span data-ttu-id="35475-256">Especifica o nome do VMSS que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="35475-256">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="35475-257">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35475-257">-Confirm</span></span>
<span data-ttu-id="35475-258">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35475-258">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35475-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35475-259">-WhatIf</span></span>
<span data-ttu-id="35475-260">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35475-260">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35475-261">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35475-261">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35475-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35475-262">CommonParameters</span></span>
<span data-ttu-id="35475-263">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35475-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35475-264">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35475-264">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35475-265">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35475-265">INPUTS</span></span>

### <span data-ttu-id="35475-266">System. String</span><span class="sxs-lookup"><span data-stu-id="35475-266">System.String</span></span>

### <span data-ttu-id="35475-267">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="35475-267">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="35475-268">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35475-268">System.Boolean</span></span>

## <span data-ttu-id="35475-269">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35475-269">OUTPUTS</span></span>

### <span data-ttu-id="35475-270">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="35475-270">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="35475-271">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35475-271">NOTES</span></span>

## <span data-ttu-id="35475-272">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35475-272">RELATED LINKS</span></span>

[<span data-ttu-id="35475-273">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="35475-273">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="35475-274">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="35475-274">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="35475-275">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="35475-275">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="35475-276">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="35475-276">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="35475-277">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="35475-277">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="35475-278">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="35475-278">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="35475-279">Parar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="35475-279">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


