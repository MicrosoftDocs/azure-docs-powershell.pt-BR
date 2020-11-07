---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 3c22f34b1dc4e01cf4e3ea2f2b3f9c6045197734
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940294"
---
# <span data-ttu-id="b2c03-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b2c03-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="b2c03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2c03-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c03-103">Cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="b2c03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2c03-104">SYNTAX</span></span>

### <span data-ttu-id="b2c03-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b2c03-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2c03-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2c03-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2c03-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2c03-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2c03-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2c03-108">DESCRIPTION</span></span>
<span data-ttu-id="b2c03-109">O cmdlet **New-AzVmssConfig** cria um objeto configurável conjunto de escala do Gerenciador virtual (VMSS) local.</span><span class="sxs-lookup"><span data-stu-id="b2c03-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="b2c03-110">Outros cmdlets são necessários para configurar o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="b2c03-111">Estes cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="b2c03-111">These cmdlets are:</span></span>
- <span data-ttu-id="b2c03-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="b2c03-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="b2c03-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="b2c03-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="b2c03-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2c03-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="b2c03-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b2c03-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="b2c03-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2c03-116">EXAMPLES</span></span>

### <span data-ttu-id="b2c03-117">Exemplo 1: criar um objeto de configuração VMSS</span><span class="sxs-lookup"><span data-stu-id="b2c03-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="b2c03-118">Este exemplo cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="b2c03-119">O primeiro comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="b2c03-120">O segundo comando usa o cmdlet **New-AzVmss** para criar um VMSS que usa o objeto de configuração VMSS criado no primeiro comando.</span><span class="sxs-lookup"><span data-stu-id="b2c03-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="b2c03-121">OS</span><span class="sxs-lookup"><span data-stu-id="b2c03-121">PARAMETERS</span></span>

### <span data-ttu-id="b2c03-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b2c03-122">-AssignIdentity</span></span>
<span data-ttu-id="b2c03-123">Especifique a identidade atribuída ao sistema para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b2c03-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="b2c03-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="b2c03-125">A quantidade de tempo em que os reparos automáticos são suspensos devido a uma alteração de estado na VM.</span><span class="sxs-lookup"><span data-stu-id="b2c03-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="b2c03-126">O tempo de carência começará após a conclusão da alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="b2c03-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="b2c03-127">Isso ajuda a evitar reparos prematuros ou acidentais.</span><span class="sxs-lookup"><span data-stu-id="b2c03-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="b2c03-128">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="b2c03-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="b2c03-129">O valor padrão é 5 minutos (PT5M).</span><span class="sxs-lookup"><span data-stu-id="b2c03-129">The default value is 5 minutes (PT5M).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-130">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="b2c03-130">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="b2c03-131">A porcentagem (capacidade de ScaleMode) de máquinas virtuais que serão reparadas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="b2c03-131">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="b2c03-132">O valor padrão é 20%.</span><span class="sxs-lookup"><span data-stu-id="b2c03-132">The default value is 20%.</span></span>

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

### <span data-ttu-id="b2c03-133">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="b2c03-133">-AutoOSUpgrade</span></span>
<span data-ttu-id="b2c03-134">Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias do conjunto de escala de forma contínua quando uma versão mais recente da imagem se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="b2c03-134">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="b2c03-135">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b2c03-135">-BootDiagnostic</span></span>
<span data-ttu-id="b2c03-136">Especifica o perfil de diagnóstico de inicialização do conjunto de dimensionamento da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b2c03-136">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c03-137">-DefaultProfile</span></span>
<span data-ttu-id="b2c03-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c03-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2c03-139">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="b2c03-139">-DisableAutoRollback</span></span>
<span data-ttu-id="b2c03-140">Desabilitar a reversão automática para a política de atualização automática de so</span><span class="sxs-lookup"><span data-stu-id="b2c03-140">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="b2c03-141">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="b2c03-141">-EnableAutomaticRepair</span></span>
<span data-ttu-id="b2c03-142">Habilita reparos automáticos no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b2c03-142">Enables automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-143">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="b2c03-143">-EnableUltraSSD</span></span>
<span data-ttu-id="b2c03-144">Habilita um recurso para ter um ou mais discos de dados gerenciados com o tipo de conta de armazenamento UltraSSD_LRS no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b2c03-144">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="b2c03-145">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a um VMSS somente se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="b2c03-145">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-146">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2c03-146">-EvictionPolicy</span></span>
<span data-ttu-id="b2c03-147">Especifica a política de remoção para as máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="b2c03-147">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-148">-Extensão</span><span class="sxs-lookup"><span data-stu-id="b2c03-148">-Extension</span></span>
<span data-ttu-id="b2c03-149">Especifica o objeto de informações de extensão para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-149">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="b2c03-150">Você pode usar o cmdlet **Add-AzVmssExtension** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="b2c03-150">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-151">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="b2c03-151">-HealthProbeId</span></span>
<span data-ttu-id="b2c03-152">Especifica a ID de um teste de balanceador de carga usado para determinar a integridade de uma instância no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b2c03-152">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="b2c03-153">HealthProbeId está no formato de '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} '.</span><span class="sxs-lookup"><span data-stu-id="b2c03-153">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-154">-Identityid</span><span class="sxs-lookup"><span data-stu-id="b2c03-154">-IdentityId</span></span>
<span data-ttu-id="b2c03-155">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b2c03-155">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="b2c03-156">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="b2c03-156">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-157">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b2c03-157">-IdentityType</span></span>
<span data-ttu-id="b2c03-158">Especifica o tipo de identidade usado para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b2c03-158">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="b2c03-159">O tipo ' SystemAssignedUserAssigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="b2c03-159">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="b2c03-160">O tipo ' nenhum ' removerá todas as identidades do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b2c03-160">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="b2c03-161">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b2c03-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2c03-162">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="b2c03-162">SystemAssigned</span></span>
- <span data-ttu-id="b2c03-163">Userassigned</span><span class="sxs-lookup"><span data-stu-id="b2c03-163">UserAssigned</span></span>
- <span data-ttu-id="b2c03-164">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="b2c03-164">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="b2c03-165">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b2c03-165">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-166">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b2c03-166">-LicenseType</span></span>
<span data-ttu-id="b2c03-167">Especifique o tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="b2c03-167">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-168">-Local</span><span class="sxs-lookup"><span data-stu-id="b2c03-168">-Location</span></span>
<span data-ttu-id="b2c03-169">Especifica o local do Azure em que o VMSS é criado.</span><span class="sxs-lookup"><span data-stu-id="b2c03-169">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="b2c03-170">-MaxPrice</span></span>
<span data-ttu-id="b2c03-171">Especifica o preço máximo que você está disposto a pagar por uma VM/VMSS de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="b2c03-171">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="b2c03-172">Este preço está em dólares americanos.</span><span class="sxs-lookup"><span data-stu-id="b2c03-172">This price is in US Dollars.</span></span> <span data-ttu-id="b2c03-173">Esse preço será comparado com o preço de baixa prioridade atual para o tamanho da VM.</span><span class="sxs-lookup"><span data-stu-id="b2c03-173">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="b2c03-174">Além disso, os preços são comparados no momento da criação/atualização de VMs/VMSS de baixa prioridade e a operação será bem-sucedida apenas se o maxPrice for maior do que o preço de baixa prioridade atual.</span><span class="sxs-lookup"><span data-stu-id="b2c03-174">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="b2c03-175">O maxPrice também será usado para remover uma VM/VMSS de baixa prioridade se o preço atual de baixa prioridade vai além do maxPrice após a criação de VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-175">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="b2c03-176">Os valores possíveis são: qualquer valor decimal maior do que zero.</span><span class="sxs-lookup"><span data-stu-id="b2c03-176">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="b2c03-177">Exemplo: 0, 1538.</span><span class="sxs-lookup"><span data-stu-id="b2c03-177">Example: 0.01538.</span></span>  <span data-ttu-id="b2c03-178">-1 indica que a VM de baixa prioridade/VMSS não deve ser removida por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="b2c03-178">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="b2c03-179">Além disso, o preço máximo padrão é-1 se não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="b2c03-179">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-180">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2c03-180">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="b2c03-181">Especifica o objeto de perfil de rede que contém as propriedades de rede da configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-181">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="b2c03-182">Você pode usar o cmdlet **Add-AzVmssNetworkInterfaceConfiguration** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="b2c03-182">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-183">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="b2c03-183">-OsProfile</span></span>
<span data-ttu-id="b2c03-184">Especifica o objeto de perfil do sistema operacional que contém as propriedades do sistema operacional para a configuração do VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-184">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="b2c03-185">Você pode usar o cmdlet **set-AzVmssOsProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="b2c03-185">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-186">-Superprovisionamento</span><span class="sxs-lookup"><span data-stu-id="b2c03-186">-Overprovision</span></span>
<span data-ttu-id="b2c03-187">Indica se o cmdlet está supervisionando o VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-187">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-188">-PlanName</span><span class="sxs-lookup"><span data-stu-id="b2c03-188">-PlanName</span></span>
<span data-ttu-id="b2c03-189">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="b2c03-189">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-190">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="b2c03-190">-PlanProduct</span></span>
<span data-ttu-id="b2c03-191">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="b2c03-191">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-192">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="b2c03-192">-PlanPromotionCode</span></span>
<span data-ttu-id="b2c03-193">Especifica o código promocional do plano.</span><span class="sxs-lookup"><span data-stu-id="b2c03-193">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-194">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="b2c03-194">-PlanPublisher</span></span>
<span data-ttu-id="b2c03-195">Especifica o fornecedor do plano.</span><span class="sxs-lookup"><span data-stu-id="b2c03-195">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-196">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="b2c03-196">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="b2c03-197">Contagem de domínios de falha para cada grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="b2c03-197">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="b2c03-198">-Priority</span><span class="sxs-lookup"><span data-stu-id="b2c03-198">-Priority</span></span>
<span data-ttu-id="b2c03-199">A prioridade para o machien virtual no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="b2c03-199">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="b2c03-200">Somente os valores com suporte são ' regular ', ' spot ' e ' baixo '.</span><span class="sxs-lookup"><span data-stu-id="b2c03-200">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="b2c03-201">' Regular ' é para a máquina virtual normal.</span><span class="sxs-lookup"><span data-stu-id="b2c03-201">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="b2c03-202">' Spot ' é para máquina virtual Spot.</span><span class="sxs-lookup"><span data-stu-id="b2c03-202">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="b2c03-203">' Low ' também é para máquina virtual Spot, mas é substituído por ' spot '.</span><span class="sxs-lookup"><span data-stu-id="b2c03-203">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="b2c03-204">Use ' spot ' em vez de ' baixo '.</span><span class="sxs-lookup"><span data-stu-id="b2c03-204">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-205">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="b2c03-205">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="b2c03-206">A ID do recurso do grupo de posicionamento de proximidade a ser usado com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="b2c03-206">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-207">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="b2c03-207">-RollingUpgradePolicy</span></span>
<span data-ttu-id="b2c03-208">Especifica a política de atualização sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="b2c03-208">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="b2c03-209">-ScaleInPolicy</span></span>
<span data-ttu-id="b2c03-210">As regras a serem seguidas quando o dimensionamento for um conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b2c03-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="b2c03-211">Os valores possíveis são: "default", "OldestVM" e "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="b2c03-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="b2c03-212">"Padrão" quando um conjunto de escala da máquina virtual é dimensionado, o conjunto de escalas primeiro será balanceado entre zonas se for um conjunto de escala zonas.</span><span class="sxs-lookup"><span data-stu-id="b2c03-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="b2c03-213">Em seguida, ele será balanceado em domínios de falha o mais longe possível.</span><span class="sxs-lookup"><span data-stu-id="b2c03-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="b2c03-214">Em cada domínio de falha, as máquinas virtuais escolhidas para remoção serão as mais recentes que não estão protegidas do Scale-in.</span><span class="sxs-lookup"><span data-stu-id="b2c03-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="b2c03-215">"OldestVM" quando um conjunto de dimensionamento de máquina virtual está sendo ampliado, as máquinas virtuais mais antigas que não estão protegidas do Scale-in serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="b2c03-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="b2c03-216">Para conjuntos de escala da máquina virtual zonada, o conjunto de escala será balanceado primeiro entre zonas.</span><span class="sxs-lookup"><span data-stu-id="b2c03-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="b2c03-217">Em cada zona, as máquinas virtuais mais antigas que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="b2c03-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="b2c03-218">"NewestVM" quando um conjunto de dimensionamento de máquina virtual está sendo ampliado, as máquinas virtuais mais recentes que não estão protegidas do Scale-in serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="b2c03-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="b2c03-219">Para conjuntos de escala da máquina virtual zonada, o conjunto de escala será balanceado primeiro entre zonas.</span><span class="sxs-lookup"><span data-stu-id="b2c03-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="b2c03-220">Em cada zona, as máquinas virtuais mais recentes que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="b2c03-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-221">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b2c03-221">-SinglePlacementGroup</span></span>
<span data-ttu-id="b2c03-222">Especifica o grupo de posicionamento único.</span><span class="sxs-lookup"><span data-stu-id="b2c03-222">Specifies the single placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-223">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="b2c03-223">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="b2c03-224">Especifica que as extensões não são executadas nas VMs extras superprovisionadas.</span><span class="sxs-lookup"><span data-stu-id="b2c03-224">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="b2c03-225">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b2c03-225">-SkuCapacity</span></span>
<span data-ttu-id="b2c03-226">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-226">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-227">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b2c03-227">-SkuName</span></span>
<span data-ttu-id="b2c03-228">Especifica o tamanho de todas as instâncias de VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-228">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-229">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b2c03-229">-SkuTier</span></span>
<span data-ttu-id="b2c03-230">Especifica o nível de VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-230">Specifies the tier of VMSS.</span></span> <span data-ttu-id="b2c03-231">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b2c03-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2c03-232">Oficial</span><span class="sxs-lookup"><span data-stu-id="b2c03-232">Standard</span></span>
- <span data-ttu-id="b2c03-233">Basic</span><span class="sxs-lookup"><span data-stu-id="b2c03-233">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-234">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="b2c03-234">-StorageProfile</span></span>
<span data-ttu-id="b2c03-235">Especifica o objeto de perfil de armazenamento que contém as propriedades de disco para a configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2c03-235">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="b2c03-236">Você pode usar o cmdlet **set-AzVmssStorageProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="b2c03-236">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-237">-Marca</span><span class="sxs-lookup"><span data-stu-id="b2c03-237">-Tag</span></span>
<span data-ttu-id="b2c03-238">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b2c03-238">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b2c03-239">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b2c03-239">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b2c03-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="b2c03-241">Período de tempo configurável (em minutos) em que uma máquina virtual que está sendo excluída terá que potencialmente aprovar o evento de término agendado antes de o evento ser aprovado automaticamente (tempo limite).</span><span class="sxs-lookup"><span data-stu-id="b2c03-241">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="b2c03-242">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="b2c03-242">-TerminateScheduledEvents</span></span>
<span data-ttu-id="b2c03-243">Habilitar os eventos de término agendado</span><span class="sxs-lookup"><span data-stu-id="b2c03-243">Enable the Terminate Scheduled events</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-244">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="b2c03-244">-UpgradePolicyMode</span></span>
<span data-ttu-id="b2c03-245">Especificou o modo de uma atualização para máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="b2c03-245">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="b2c03-246">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b2c03-246">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2c03-247">Automático</span><span class="sxs-lookup"><span data-stu-id="b2c03-247">Automatic</span></span>
- <span data-ttu-id="b2c03-248">Manual</span><span class="sxs-lookup"><span data-stu-id="b2c03-248">Manual</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-249">-Zone</span><span class="sxs-lookup"><span data-stu-id="b2c03-249">-Zone</span></span>
<span data-ttu-id="b2c03-250">Especifica a lista de zonas para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b2c03-250">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c03-251">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="b2c03-251">-ZoneBalance</span></span>
<span data-ttu-id="b2c03-252">Se devem ser forçadas rigorosamente entre x-Zones de distribuição de máquinas virtuais, caso haja falha na zona.</span><span class="sxs-lookup"><span data-stu-id="b2c03-252">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="b2c03-253">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2c03-253">-Confirm</span></span>
<span data-ttu-id="b2c03-254">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2c03-254">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c03-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c03-255">-WhatIf</span></span>
<span data-ttu-id="b2c03-256">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2c03-256">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2c03-257">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2c03-257">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c03-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c03-258">CommonParameters</span></span>
<span data-ttu-id="b2c03-259">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c03-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c03-260">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2c03-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c03-261">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2c03-261">INPUTS</span></span>

### <span data-ttu-id="b2c03-262">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b2c03-262">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b2c03-263">System. String</span><span class="sxs-lookup"><span data-stu-id="b2c03-263">System.String</span></span>

### <span data-ttu-id="b2c03-264">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b2c03-264">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b2c03-265">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b2c03-265">System.Int32</span></span>

### <span data-ttu-id="b2c03-266">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. Upgrademode, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b2c03-266">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b2c03-267">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="b2c03-267">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="b2c03-268">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="b2c03-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="b2c03-269">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="b2c03-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="b2c03-270">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="b2c03-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="b2c03-271">System. String []</span><span class="sxs-lookup"><span data-stu-id="b2c03-271">System.String[]</span></span>

### <span data-ttu-id="b2c03-272">Microsoft. Azure. Management. COMPUTE. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="b2c03-272">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="b2c03-273">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b2c03-273">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b2c03-274">Microsoft. Azure. Management. COMPUTE. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b2c03-274">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="b2c03-275">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. ResourceIdentityType, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b2c03-275">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b2c03-276">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2c03-276">OUTPUTS</span></span>

### <span data-ttu-id="b2c03-277">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b2c03-277">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b2c03-278">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2c03-278">NOTES</span></span>

## <span data-ttu-id="b2c03-279">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2c03-279">RELATED LINKS</span></span>

[<span data-ttu-id="b2c03-280">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="b2c03-280">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="b2c03-281">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="b2c03-281">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="b2c03-282">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2c03-282">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="b2c03-283">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b2c03-283">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="b2c03-284">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b2c03-284">New-AzVmss</span></span>](./New-AzVmss.md)
