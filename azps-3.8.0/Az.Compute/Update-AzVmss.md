---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: bf8fa8c4b7d1d08cdb6d0c2c348f5c97a2788a4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944587"
---
# <span data-ttu-id="79068-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="79068-101">Update-AzVmss</span></span>

## <span data-ttu-id="79068-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79068-102">SYNOPSIS</span></span>
<span data-ttu-id="79068-103">Atualiza o estado de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="79068-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="79068-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79068-104">SYNTAX</span></span>

### <span data-ttu-id="79068-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="79068-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79068-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="79068-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79068-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79068-107">DESCRIPTION</span></span>
<span data-ttu-id="79068-108">O cmdlet **Update-AzVmss** atualiza o estado de um VMSS (conjunto de dimensionamento de máquina virtual) para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="79068-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="79068-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79068-109">EXAMPLES</span></span>

### <span data-ttu-id="79068-110">Exemplo 1: Atualize o estado de um VMSS para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="79068-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="79068-111">Esse comando atualiza o estado do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001 para o estado de um objeto VMSS local, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="79068-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="79068-112">OS</span><span class="sxs-lookup"><span data-stu-id="79068-112">PARAMETERS</span></span>

### <span data-ttu-id="79068-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79068-113">-AsJob</span></span>
<span data-ttu-id="79068-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="79068-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="79068-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="79068-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="79068-116">Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias do conjunto de escala de forma contínua quando uma versão mais recente da imagem se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="79068-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="79068-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="79068-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="79068-118">A quantidade de tempo em que os reparos automáticos são suspensos devido a uma alteração de estado na VM.</span><span class="sxs-lookup"><span data-stu-id="79068-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="79068-119">O tempo de carência começará após a conclusão da alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="79068-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="79068-120">Isso ajuda a evitar reparos prematuros ou acidentais.</span><span class="sxs-lookup"><span data-stu-id="79068-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="79068-121">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="79068-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="79068-122">O valor padrão é 5 minutos (PT5M).</span><span class="sxs-lookup"><span data-stu-id="79068-122">The default value is 5 minutes (PT5M).</span></span>

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

### <span data-ttu-id="79068-123">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="79068-123">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="79068-124">A porcentagem (capacidade de ScaleMode) de máquinas virtuais que serão reparadas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="79068-124">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="79068-125">O valor padrão é 20%.</span><span class="sxs-lookup"><span data-stu-id="79068-125">The default value is 20%.</span></span>

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

### <span data-ttu-id="79068-126">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="79068-126">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="79068-127">Se o diagnóstico de inicialização deve ser habilitado no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79068-127">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="79068-128">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="79068-128">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="79068-129">URL da conta de armazenamento a ser usada para colocar a captura de tela e a saída do console.</span><span class="sxs-lookup"><span data-stu-id="79068-129">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="79068-130">-CustomData</span><span class="sxs-lookup"><span data-stu-id="79068-130">-CustomData</span></span>
<span data-ttu-id="79068-131">Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.</span><span class="sxs-lookup"><span data-stu-id="79068-131">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="79068-132">Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79068-132">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="79068-133">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="79068-133">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="79068-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79068-134">-DefaultProfile</span></span>
<span data-ttu-id="79068-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79068-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79068-136">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="79068-136">-DisableAutoRollback</span></span>
<span data-ttu-id="79068-137">Desabilitar a reversão automática para a política de atualização automática de so</span><span class="sxs-lookup"><span data-stu-id="79068-137">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="79068-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="79068-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="79068-139">Indica que esse cmdlet desabilita a autenticação de senha para o SO Linux.</span><span class="sxs-lookup"><span data-stu-id="79068-139">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="79068-140">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="79068-140">-EnableAutomaticRepair</span></span>
<span data-ttu-id="79068-141">Habilite ou desabilite reparos automáticos no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79068-141">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="79068-142">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="79068-142">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="79068-143">Indica se as máquinas virtuais do Windows no VMSS estão habilitadas para atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="79068-143">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="79068-144">-Identityid</span><span class="sxs-lookup"><span data-stu-id="79068-144">-IdentityId</span></span>
<span data-ttu-id="79068-145">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79068-145">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="79068-146">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="79068-146">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="79068-147">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="79068-147">-IdentityType</span></span>
<span data-ttu-id="79068-148">Especifica o tipo de identidade usado para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79068-148">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="79068-149">O tipo ' SystemAssignedUserAssigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="79068-149">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="79068-150">O tipo ' nenhum ' removerá todas as identidades do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79068-150">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="79068-151">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="79068-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79068-152">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="79068-152">SystemAssigned</span></span>
- <span data-ttu-id="79068-153">Userassigned</span><span class="sxs-lookup"><span data-stu-id="79068-153">UserAssigned</span></span>
- <span data-ttu-id="79068-154">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="79068-154">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="79068-155">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="79068-155">None</span></span>

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

### <span data-ttu-id="79068-156">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="79068-156">-ImageReferenceId</span></span>
<span data-ttu-id="79068-157">Especifica a ID de referência da imagem.</span><span class="sxs-lookup"><span data-stu-id="79068-157">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="79068-158">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="79068-158">-ImageReferenceOffer</span></span>
<span data-ttu-id="79068-159">Especifica o tipo de oferta da máquina virtual da máquina (VMImage).</span><span class="sxs-lookup"><span data-stu-id="79068-159">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="79068-160">Para obter uma oferta de imagem, use o cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="79068-160">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="79068-161">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="79068-161">-ImageReferencePublisher</span></span>
<span data-ttu-id="79068-162">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="79068-162">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="79068-163">Para obter um fornecedor, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="79068-163">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="79068-164">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="79068-164">-ImageReferenceSku</span></span>
<span data-ttu-id="79068-165">Especifica o SKU da VMImage.</span><span class="sxs-lookup"><span data-stu-id="79068-165">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="79068-166">Para obter os SKUs, use o cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="79068-166">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="79068-167">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="79068-167">-ImageReferenceVersion</span></span>
<span data-ttu-id="79068-168">Especifica a versão da VMImage.</span><span class="sxs-lookup"><span data-stu-id="79068-168">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="79068-169">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="79068-169">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="79068-170">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="79068-170">-ImageUri</span></span>
<span data-ttu-id="79068-171">Especifica o URI do blob para a imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="79068-171">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="79068-172">O VMSS cria um disco do sistema operacional no mesmo contêiner da imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="79068-172">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="79068-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="79068-173">-LicenseType</span></span>
<span data-ttu-id="79068-174">Especifique o tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="79068-174">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="79068-175">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="79068-175">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="79068-176">Especifica o tipo de conta de armazenamento para o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="79068-176">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="79068-177">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="79068-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79068-178">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="79068-178">StandardLRS</span></span>
- <span data-ttu-id="79068-179">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="79068-179">PremiumLRS</span></span>

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

### <span data-ttu-id="79068-180">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="79068-180">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="79068-181">A porcentagem máxima do total de instâncias da máquina virtual que serão atualizadas simultaneamente pela atualização sem interrupção em um lote.</span><span class="sxs-lookup"><span data-stu-id="79068-181">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="79068-182">Como se trata de um valor máximo, instâncias não íntegras em lotes anteriores ou futuros podem fazer com que a porcentagem de instâncias em um lote seja reduzida para garantir maior confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="79068-182">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="79068-183">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="79068-183">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="79068-184">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="79068-184">-MaxPrice</span></span>
<span data-ttu-id="79068-185">Especifica o preço máximo que você está disposto a pagar por uma VM/VMSS de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="79068-185">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="79068-186">Este preço está em dólares americanos.</span><span class="sxs-lookup"><span data-stu-id="79068-186">This price is in US Dollars.</span></span> <span data-ttu-id="79068-187">Esse preço será comparado com o preço de baixa prioridade atual para o tamanho da VM.</span><span class="sxs-lookup"><span data-stu-id="79068-187">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="79068-188">Além disso, os preços são comparados no momento da criação/atualização de VMs/VMSS de baixa prioridade e a operação será bem-sucedida apenas se o maxPrice for maior do que o preço de baixa prioridade atual.</span><span class="sxs-lookup"><span data-stu-id="79068-188">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="79068-189">O maxPrice também será usado para remover uma VM/VMSS de baixa prioridade se o preço atual de baixa prioridade vai além do maxPrice após a criação de VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="79068-189">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="79068-190">Os valores possíveis são: qualquer valor decimal maior do que zero.</span><span class="sxs-lookup"><span data-stu-id="79068-190">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="79068-191">Exemplo: 0, 1538.</span><span class="sxs-lookup"><span data-stu-id="79068-191">Example: 0.01538.</span></span>  <span data-ttu-id="79068-192">-1 indica que a VM de baixa prioridade/VMSS não deve ser removida por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="79068-192">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="79068-193">Além disso, o preço máximo padrão é-1 se não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="79068-193">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="79068-194">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="79068-194">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="79068-195">A porcentagem máxima do total de instâncias da máquina virtual no conjunto de escala que podem ser simultaneamente não íntegras, como resultado da atualização ou por estar em um estado não íntegro pelas verificações de integridade da máquina virtual antes de anular a atualização sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="79068-195">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="79068-196">Esta restrição será verificada antes de iniciar qualquer lote.</span><span class="sxs-lookup"><span data-stu-id="79068-196">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="79068-197">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="79068-197">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="79068-198">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="79068-198">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="79068-199">A porcentagem máxima de instâncias da máquina virtual atualizadas que podem ser encontradas em um estado não íntegro.</span><span class="sxs-lookup"><span data-stu-id="79068-199">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="79068-200">Essa verificação ocorrerá após a atualização de cada lote.</span><span class="sxs-lookup"><span data-stu-id="79068-200">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="79068-201">Se essa porcentagem já tiver sido excedida, a atualização sem interrupção será anulada.</span><span class="sxs-lookup"><span data-stu-id="79068-201">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="79068-202">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="79068-202">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="79068-203">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="79068-203">-OsDiskCaching</span></span>
<span data-ttu-id="79068-204">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79068-204">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="79068-205">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="79068-205">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79068-206">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="79068-206">None</span></span>
- <span data-ttu-id="79068-207">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="79068-207">ReadOnly</span></span>
- <span data-ttu-id="79068-208">ReadWrite o valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="79068-208">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="79068-209">Se você alterar o valor de cache, o cmdlet reiniciará a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79068-209">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="79068-210">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="79068-210">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="79068-211">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="79068-211">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="79068-212">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79068-212">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="79068-213">-Superprovisionamento</span><span class="sxs-lookup"><span data-stu-id="79068-213">-Overprovision</span></span>
<span data-ttu-id="79068-214">Indica se o cmdlet está supervisionando o VMSS.</span><span class="sxs-lookup"><span data-stu-id="79068-214">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="79068-215">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="79068-215">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="79068-216">O tempo de espera entre concluir a atualização de todas as máquinas virtuais em um lote e iniciar o próximo lote.</span><span class="sxs-lookup"><span data-stu-id="79068-216">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="79068-217">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="79068-217">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="79068-218">O valor padrão é 0 segundos (PT0S).</span><span class="sxs-lookup"><span data-stu-id="79068-218">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="79068-219">-PlanName</span><span class="sxs-lookup"><span data-stu-id="79068-219">-PlanName</span></span>
<span data-ttu-id="79068-220">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="79068-220">Specifies the plan name.</span></span>

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

### <span data-ttu-id="79068-221">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="79068-221">-PlanProduct</span></span>
<span data-ttu-id="79068-222">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="79068-222">Specifies the plan product.</span></span>

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

### <span data-ttu-id="79068-223">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="79068-223">-PlanPromotionCode</span></span>
<span data-ttu-id="79068-224">Especifica o código promocional do plano.</span><span class="sxs-lookup"><span data-stu-id="79068-224">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="79068-225">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="79068-225">-PlanPublisher</span></span>
<span data-ttu-id="79068-226">Especifica o fornecedor do plano.</span><span class="sxs-lookup"><span data-stu-id="79068-226">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="79068-227">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="79068-227">-ProvisionVMAgent</span></span>
<span data-ttu-id="79068-228">Indica se o agente da máquina virtual deve ser provisionado nas máquinas virtuais do Windows no VMSS.</span><span class="sxs-lookup"><span data-stu-id="79068-228">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="79068-229">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="79068-229">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="79068-230">A ID do recurso do grupo de posicionamento de proximidade a ser usado com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="79068-230">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="79068-231">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79068-231">-ResourceGroupName</span></span>
<span data-ttu-id="79068-232">Especifica o nome do grupo de recursos ao qual o VMSS pertence.</span><span class="sxs-lookup"><span data-stu-id="79068-232">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="79068-233">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="79068-233">-ScaleInPolicy</span></span>
<span data-ttu-id="79068-234">As regras a serem seguidas quando o dimensionamento for um conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79068-234">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="79068-235">Os valores possíveis são: "default", "OldestVM" e "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="79068-235">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="79068-236">"Padrão" quando um conjunto de escala da máquina virtual é dimensionado, o conjunto de escalas primeiro será balanceado entre zonas se for um conjunto de escala zonas.</span><span class="sxs-lookup"><span data-stu-id="79068-236">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="79068-237">Em seguida, ele será balanceado em domínios de falha o mais longe possível.</span><span class="sxs-lookup"><span data-stu-id="79068-237">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="79068-238">Em cada domínio de falha, as máquinas virtuais escolhidas para remoção serão as mais recentes que não estão protegidas do Scale-in.</span><span class="sxs-lookup"><span data-stu-id="79068-238">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="79068-239">"OldestVM" quando um conjunto de dimensionamento de máquina virtual está sendo ampliado, as máquinas virtuais mais antigas que não estão protegidas do Scale-in serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="79068-239">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="79068-240">Para conjuntos de escala da máquina virtual zonada, o conjunto de escala será balanceado primeiro entre zonas.</span><span class="sxs-lookup"><span data-stu-id="79068-240">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="79068-241">Em cada zona, as máquinas virtuais mais antigas que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="79068-241">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="79068-242">"NewestVM" quando um conjunto de dimensionamento de máquina virtual está sendo ampliado, as máquinas virtuais mais recentes que não estão protegidas do Scale-in serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="79068-242">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="79068-243">Para conjuntos de escala da máquina virtual zonada, o conjunto de escala será balanceado primeiro entre zonas.</span><span class="sxs-lookup"><span data-stu-id="79068-243">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="79068-244">Em cada zona, as máquinas virtuais mais recentes que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="79068-244">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="79068-245">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="79068-245">-SinglePlacementGroup</span></span>
<span data-ttu-id="79068-246">Especifica o grupo de posicionamento único.</span><span class="sxs-lookup"><span data-stu-id="79068-246">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="79068-247">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="79068-247">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="79068-248">Especifica que as extensões não são executadas nas VMs extras superprovisionadas.</span><span class="sxs-lookup"><span data-stu-id="79068-248">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="79068-249">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="79068-249">-SkuCapacity</span></span>
<span data-ttu-id="79068-250">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="79068-250">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="79068-251">-SkuName</span><span class="sxs-lookup"><span data-stu-id="79068-251">-SkuName</span></span>
<span data-ttu-id="79068-252">Especifica o tamanho de todas as instâncias de VMSS.</span><span class="sxs-lookup"><span data-stu-id="79068-252">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="79068-253">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="79068-253">-SkuTier</span></span>
<span data-ttu-id="79068-254">Especifica o nível de VMSS.</span><span class="sxs-lookup"><span data-stu-id="79068-254">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="79068-255">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="79068-255">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79068-256">Oficial</span><span class="sxs-lookup"><span data-stu-id="79068-256">Standard</span></span>
- <span data-ttu-id="79068-257">Basic</span><span class="sxs-lookup"><span data-stu-id="79068-257">Basic</span></span>

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

### <span data-ttu-id="79068-258">-Marca</span><span class="sxs-lookup"><span data-stu-id="79068-258">-Tag</span></span>
<span data-ttu-id="79068-259">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="79068-259">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="79068-260">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="79068-260">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="79068-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="79068-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="79068-262">Período de tempo configurável (em minutos) em que uma máquina virtual que está sendo excluída terá que potencialmente aprovar o evento de término agendado antes de o evento ser aprovado automaticamente (tempo limite).</span><span class="sxs-lookup"><span data-stu-id="79068-262">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="79068-263">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="79068-263">-TerminateScheduledEvents</span></span>
<span data-ttu-id="79068-264">Especifica se o evento de término agendado está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="79068-264">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="79068-265">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="79068-265">-TimeZone</span></span>
<span data-ttu-id="79068-266">Especifica o fuso horário para o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="79068-266">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="79068-267">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="79068-267">-UltraSSDEnabled</span></span>
<span data-ttu-id="79068-268">O sinalizador que habilita ou desabilita uma funcionalidade para ter um ou mais discos de dados gerenciados com o tipo de conta de armazenamento UltraSSD_LRS no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79068-268">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="79068-269">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a um VMSS somente se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="79068-269">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="79068-270">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="79068-270">-UpgradePolicyMode</span></span>
<span data-ttu-id="79068-271">Especificou o modo de uma atualização para máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="79068-271">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="79068-272">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="79068-272">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79068-273">Automático</span><span class="sxs-lookup"><span data-stu-id="79068-273">Automatic</span></span>
- <span data-ttu-id="79068-274">Manual</span><span class="sxs-lookup"><span data-stu-id="79068-274">Manual</span></span>
- <span data-ttu-id="79068-275">Implantação</span><span class="sxs-lookup"><span data-stu-id="79068-275">Rolling</span></span>

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

### <span data-ttu-id="79068-276">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="79068-276">-VhdContainer</span></span>
<span data-ttu-id="79068-277">Especifica as URLs de contêiner usadas para armazenar discos do sistema operacional para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="79068-277">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="79068-278">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="79068-278">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="79068-279">Especifica um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="79068-279">Specifies a local VMSS object.</span></span>
<span data-ttu-id="79068-280">Para obter um objeto VMSS, use o cmdlet Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="79068-280">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="79068-281">Esse objeto da máquina virtual contém o estado atualizado para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="79068-281">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="79068-282">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="79068-282">-VMScaleSetName</span></span>
<span data-ttu-id="79068-283">Especifica o nome do VMSS que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="79068-283">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="79068-284">-Confirme</span><span class="sxs-lookup"><span data-stu-id="79068-284">-Confirm</span></span>
<span data-ttu-id="79068-285">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79068-285">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79068-286">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79068-286">-WhatIf</span></span>
<span data-ttu-id="79068-287">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="79068-287">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79068-288">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79068-288">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79068-289">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79068-289">CommonParameters</span></span>
<span data-ttu-id="79068-290">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79068-290">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79068-291">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79068-291">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79068-292">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79068-292">INPUTS</span></span>

### <span data-ttu-id="79068-293">System. String</span><span class="sxs-lookup"><span data-stu-id="79068-293">System.String</span></span>

### <span data-ttu-id="79068-294">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="79068-294">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="79068-295">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79068-295">System.Boolean</span></span>

## <span data-ttu-id="79068-296">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79068-296">OUTPUTS</span></span>

### <span data-ttu-id="79068-297">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="79068-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="79068-298">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79068-298">NOTES</span></span>

## <span data-ttu-id="79068-299">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79068-299">RELATED LINKS</span></span>

[<span data-ttu-id="79068-300">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="79068-300">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="79068-301">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="79068-301">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="79068-302">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="79068-302">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="79068-303">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="79068-303">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="79068-304">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="79068-304">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="79068-305">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="79068-305">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="79068-306">Parar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="79068-306">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


