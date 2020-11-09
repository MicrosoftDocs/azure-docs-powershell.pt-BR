---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281808"
---
# <span data-ttu-id="bf23f-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bf23f-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="bf23f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf23f-102">SYNOPSIS</span></span>
<span data-ttu-id="bf23f-103">Cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="bf23f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf23f-104">SYNTAX</span></span>

### <span data-ttu-id="bf23f-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bf23f-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf23f-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf23f-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf23f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf23f-107">DESCRIPTION</span></span>
<span data-ttu-id="bf23f-108">O cmdlet **New-AzVmssConfig** cria um objeto configurável conjunto de escala do Gerenciador virtual (VMSS) local.</span><span class="sxs-lookup"><span data-stu-id="bf23f-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="bf23f-109">Outros cmdlets são necessários para configurar o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="bf23f-110">Estes cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="bf23f-110">These cmdlets are:</span></span>
- <span data-ttu-id="bf23f-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="bf23f-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="bf23f-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="bf23f-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="bf23f-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf23f-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="bf23f-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="bf23f-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="bf23f-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf23f-115">EXAMPLES</span></span>

### <span data-ttu-id="bf23f-116">Exemplo 1: criar um objeto de configuração VMSS</span><span class="sxs-lookup"><span data-stu-id="bf23f-116">Example 1: Create a VMSS configuration object</span></span>
```powershell
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

<span data-ttu-id="bf23f-117">Este exemplo cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="bf23f-118">O primeiro comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="bf23f-119">O segundo comando usa o cmdlet **New-AzVmss** para criar um VMSS que usa o objeto de configuração VMSS criado no primeiro comando.</span><span class="sxs-lookup"><span data-stu-id="bf23f-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="bf23f-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bf23f-120">Example 2</span></span>

<span data-ttu-id="bf23f-121">Cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="bf23f-122">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="bf23f-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="bf23f-123">OS</span><span class="sxs-lookup"><span data-stu-id="bf23f-123">PARAMETERS</span></span>

### <span data-ttu-id="bf23f-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="bf23f-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="bf23f-125">A quantidade de tempo em que os reparos automáticos são suspensos devido a uma alteração de estado na VM.</span><span class="sxs-lookup"><span data-stu-id="bf23f-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="bf23f-126">O tempo de carência começará após a conclusão da alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="bf23f-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="bf23f-127">Isso ajuda a evitar reparos prematuros ou acidentais.</span><span class="sxs-lookup"><span data-stu-id="bf23f-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="bf23f-128">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="bf23f-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="bf23f-129">O período de cortesia mínimo permitido é de 30 minutos (PT30M), que também é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="bf23f-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="bf23f-130">O período de cortesia máximo permitido é de 90 minutos (PT90M).</span><span class="sxs-lookup"><span data-stu-id="bf23f-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="bf23f-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="bf23f-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="bf23f-132">Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias do conjunto de escala de forma contínua quando uma versão mais recente da imagem se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="bf23f-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="bf23f-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bf23f-133">-BootDiagnostic</span></span>
<span data-ttu-id="bf23f-134">Especifica o perfil de diagnóstico de inicialização do conjunto de dimensionamento da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf23f-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="bf23f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf23f-135">-DefaultProfile</span></span>
<span data-ttu-id="bf23f-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf23f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf23f-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="bf23f-137">-DisableAutoRollback</span></span>
<span data-ttu-id="bf23f-138">Desabilitar a reversão automática para a política de atualização automática de so</span><span class="sxs-lookup"><span data-stu-id="bf23f-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="bf23f-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="bf23f-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="bf23f-140">Habilita reparos automáticos no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf23f-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="bf23f-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="bf23f-141">-EnableUltraSSD</span></span>
<span data-ttu-id="bf23f-142">Habilita um recurso para ter um ou mais discos de dados gerenciados com o tipo de conta de armazenamento UltraSSD_LRS no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf23f-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="bf23f-143">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a um VMSS somente se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="bf23f-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="bf23f-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="bf23f-144">-EncryptionAtHost</span></span>
<span data-ttu-id="bf23f-145">Esse parâmetro habilitará a criptografia para todos os discos, incluindo o disco de recursos/temp no próprio host.</span><span class="sxs-lookup"><span data-stu-id="bf23f-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="bf23f-146">Padrão: a criptografia no host será desabilitada, a menos que essa propriedade seja definida como true para o recurso.</span><span class="sxs-lookup"><span data-stu-id="bf23f-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="bf23f-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf23f-147">-EvictionPolicy</span></span>
<span data-ttu-id="bf23f-148">Especifica a política de remoção para as máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="bf23f-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="bf23f-149">-Extensão</span><span class="sxs-lookup"><span data-stu-id="bf23f-149">-Extension</span></span>
<span data-ttu-id="bf23f-150">Especifica o objeto de informações de extensão para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="bf23f-151">Você pode usar o cmdlet **Add-AzVmssExtension** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="bf23f-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="bf23f-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="bf23f-152">-HealthProbeId</span></span>
<span data-ttu-id="bf23f-153">Especifica a ID de um teste de balanceador de carga usado para determinar a integridade de uma instância no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf23f-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="bf23f-154">HealthProbeId está no formato de '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} '.</span><span class="sxs-lookup"><span data-stu-id="bf23f-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="bf23f-155">-Identityid</span><span class="sxs-lookup"><span data-stu-id="bf23f-155">-IdentityId</span></span>
<span data-ttu-id="bf23f-156">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf23f-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="bf23f-157">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="bf23f-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="bf23f-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="bf23f-158">-IdentityType</span></span>
<span data-ttu-id="bf23f-159">Especifica o tipo de identidade usado para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf23f-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="bf23f-160">O tipo ' SystemAssignedUserAssigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="bf23f-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="bf23f-161">O tipo ' nenhum ' removerá todas as identidades do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf23f-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="bf23f-162">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bf23f-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bf23f-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="bf23f-163">SystemAssigned</span></span>
- <span data-ttu-id="bf23f-164">Userassigned</span><span class="sxs-lookup"><span data-stu-id="bf23f-164">UserAssigned</span></span>
- <span data-ttu-id="bf23f-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="bf23f-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="bf23f-166">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bf23f-166">None</span></span>

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

### <span data-ttu-id="bf23f-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="bf23f-167">-LicenseType</span></span>
<span data-ttu-id="bf23f-168">Especifique o tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="bf23f-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="bf23f-169">-Local</span><span class="sxs-lookup"><span data-stu-id="bf23f-169">-Location</span></span>
<span data-ttu-id="bf23f-170">Especifica o local do Azure em que o VMSS é criado.</span><span class="sxs-lookup"><span data-stu-id="bf23f-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="bf23f-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="bf23f-171">-MaxPrice</span></span>
<span data-ttu-id="bf23f-172">Especifica o preço máximo que você quer pagar por uma VM de spot/VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="bf23f-173">Este preço está em dólares americanos.</span><span class="sxs-lookup"><span data-stu-id="bf23f-173">This price is in US Dollars.</span></span> <span data-ttu-id="bf23f-174">Esse preço será comparado com o preço spot atual do tamanho da VM.</span><span class="sxs-lookup"><span data-stu-id="bf23f-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="bf23f-175">Além disso, os preços são comparados no momento da criação/atualização de VM/VMSS Spot e a operação será bem-sucedida apenas se o maxPrice for maior que o preço spot atual.</span><span class="sxs-lookup"><span data-stu-id="bf23f-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="bf23f-176">O maxPrice também será usado para remover uma VM de spot/VMSS se o preço spot atual vai além do maxPrice após a criação de VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="bf23f-177">Os valores possíveis são: qualquer valor decimal maior do que zero.</span><span class="sxs-lookup"><span data-stu-id="bf23f-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="bf23f-178">Exemplo: 0, 1538.</span><span class="sxs-lookup"><span data-stu-id="bf23f-178">Example: 0.01538.</span></span>  <span data-ttu-id="bf23f-179">-1 indica que a VM de spot/VMSS não deve ser removida por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="bf23f-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="bf23f-180">Além disso, o preço máximo padrão é-1 se não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="bf23f-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="bf23f-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf23f-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="bf23f-182">Especifica o objeto de perfil de rede que contém as propriedades de rede da configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="bf23f-183">Você pode usar o cmdlet **Add-AzVmssNetworkInterfaceConfiguration** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="bf23f-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="bf23f-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="bf23f-184">-OsProfile</span></span>
<span data-ttu-id="bf23f-185">Especifica o objeto de perfil do sistema operacional que contém as propriedades do sistema operacional para a configuração do VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="bf23f-186">Você pode usar o cmdlet **set-AzVmssOsProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="bf23f-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="bf23f-187">-Superprovisionamento</span><span class="sxs-lookup"><span data-stu-id="bf23f-187">-Overprovision</span></span>
<span data-ttu-id="bf23f-188">Indica se o cmdlet está supervisionando o VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="bf23f-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="bf23f-189">-PlanName</span></span>
<span data-ttu-id="bf23f-190">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="bf23f-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="bf23f-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="bf23f-191">-PlanProduct</span></span>
<span data-ttu-id="bf23f-192">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="bf23f-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="bf23f-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="bf23f-193">-PlanPromotionCode</span></span>
<span data-ttu-id="bf23f-194">Especifica o código promocional do plano.</span><span class="sxs-lookup"><span data-stu-id="bf23f-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="bf23f-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="bf23f-195">-PlanPublisher</span></span>
<span data-ttu-id="bf23f-196">Especifica o fornecedor do plano.</span><span class="sxs-lookup"><span data-stu-id="bf23f-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="bf23f-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="bf23f-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="bf23f-198">Contagem de domínios de falha para cada grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="bf23f-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="bf23f-199">-Priority</span><span class="sxs-lookup"><span data-stu-id="bf23f-199">-Priority</span></span>
<span data-ttu-id="bf23f-200">A prioridade para o machien virtual no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="bf23f-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="bf23f-201">Somente os valores com suporte são ' regular ', ' spot ' e ' baixo '.</span><span class="sxs-lookup"><span data-stu-id="bf23f-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="bf23f-202">' Regular ' é para a máquina virtual normal.</span><span class="sxs-lookup"><span data-stu-id="bf23f-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="bf23f-203">' Spot ' é para máquina virtual Spot.</span><span class="sxs-lookup"><span data-stu-id="bf23f-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="bf23f-204">' Low ' também é para máquina virtual Spot, mas é substituído por ' spot '.</span><span class="sxs-lookup"><span data-stu-id="bf23f-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="bf23f-205">Use ' spot ' em vez de ' baixo '.</span><span class="sxs-lookup"><span data-stu-id="bf23f-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="bf23f-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="bf23f-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="bf23f-207">A ID do recurso do grupo de posicionamento de proximidade a ser usado com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="bf23f-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="bf23f-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="bf23f-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="bf23f-209">Especifica a política de atualização sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="bf23f-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="bf23f-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="bf23f-210">-ScaleInPolicy</span></span>
<span data-ttu-id="bf23f-211">As regras a serem seguidas quando o dimensionamento for um conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf23f-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="bf23f-212">Os valores possíveis são: "default", "OldestVM" e "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="bf23f-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="bf23f-213">"Padrão" quando um conjunto de escala da máquina virtual é dimensionado, o conjunto de escalas primeiro será balanceado entre zonas se for um conjunto de escala zonas.</span><span class="sxs-lookup"><span data-stu-id="bf23f-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="bf23f-214">Em seguida, ele será balanceado em domínios de falha o mais longe possível.</span><span class="sxs-lookup"><span data-stu-id="bf23f-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="bf23f-215">Em cada domínio de falha, as máquinas virtuais escolhidas para remoção serão as mais recentes que não estão protegidas do Scale-in.</span><span class="sxs-lookup"><span data-stu-id="bf23f-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="bf23f-216">"OldestVM" quando um conjunto de dimensionamento de máquina virtual está sendo ampliado, as máquinas virtuais mais antigas que não estão protegidas do Scale-in serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="bf23f-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="bf23f-217">Para conjuntos de escala da máquina virtual zonada, o conjunto de escala será balanceado primeiro entre zonas.</span><span class="sxs-lookup"><span data-stu-id="bf23f-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="bf23f-218">Em cada zona, as máquinas virtuais mais antigas que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="bf23f-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="bf23f-219">"NewestVM" quando um conjunto de dimensionamento de máquina virtual está sendo ampliado, as máquinas virtuais mais recentes que não estão protegidas do Scale-in serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="bf23f-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="bf23f-220">Para conjuntos de escala da máquina virtual zonada, o conjunto de escala será balanceado primeiro entre zonas.</span><span class="sxs-lookup"><span data-stu-id="bf23f-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="bf23f-221">Em cada zona, as máquinas virtuais mais recentes que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="bf23f-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="bf23f-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="bf23f-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="bf23f-223">Especifica o grupo de posicionamento único.</span><span class="sxs-lookup"><span data-stu-id="bf23f-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="bf23f-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="bf23f-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="bf23f-225">Especifica que as extensões não são executadas nas VMs extras superprovisionadas.</span><span class="sxs-lookup"><span data-stu-id="bf23f-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="bf23f-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="bf23f-226">-SkuCapacity</span></span>
<span data-ttu-id="bf23f-227">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="bf23f-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bf23f-228">-SkuName</span></span>
<span data-ttu-id="bf23f-229">Especifica o tamanho de todas as instâncias de VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="bf23f-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="bf23f-230">-SkuTier</span></span>
<span data-ttu-id="bf23f-231">Especifica o nível de VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="bf23f-232">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bf23f-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bf23f-233">Oficial</span><span class="sxs-lookup"><span data-stu-id="bf23f-233">Standard</span></span>
- <span data-ttu-id="bf23f-234">Basic</span><span class="sxs-lookup"><span data-stu-id="bf23f-234">Basic</span></span>

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

### <span data-ttu-id="bf23f-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="bf23f-235">-StorageProfile</span></span>
<span data-ttu-id="bf23f-236">Especifica o objeto de perfil de armazenamento que contém as propriedades de disco para a configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf23f-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="bf23f-237">Você pode usar o cmdlet **set-AzVmssStorageProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="bf23f-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="bf23f-238">-Marca</span><span class="sxs-lookup"><span data-stu-id="bf23f-238">-Tag</span></span>
<span data-ttu-id="bf23f-239">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bf23f-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bf23f-240">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="bf23f-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bf23f-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="bf23f-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="bf23f-242">Período de tempo configurável (em minutos) em que uma máquina virtual que está sendo excluída terá que potencialmente aprovar o evento de término agendado antes de o evento ser aprovado automaticamente (tempo limite).</span><span class="sxs-lookup"><span data-stu-id="bf23f-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="bf23f-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="bf23f-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="bf23f-244">Habilitar os eventos de término agendado</span><span class="sxs-lookup"><span data-stu-id="bf23f-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="bf23f-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="bf23f-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="bf23f-246">Especificou o modo de uma atualização para máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="bf23f-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="bf23f-247">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bf23f-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bf23f-248">Automático</span><span class="sxs-lookup"><span data-stu-id="bf23f-248">Automatic</span></span>
- <span data-ttu-id="bf23f-249">Manual</span><span class="sxs-lookup"><span data-stu-id="bf23f-249">Manual</span></span>

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

### <span data-ttu-id="bf23f-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="bf23f-250">-Zone</span></span>
<span data-ttu-id="bf23f-251">Especifica a lista de zonas para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf23f-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="bf23f-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="bf23f-252">-ZoneBalance</span></span>
<span data-ttu-id="bf23f-253">Se devem ser forçadas rigorosamente entre x-Zones de distribuição de máquinas virtuais, caso haja falha na zona.</span><span class="sxs-lookup"><span data-stu-id="bf23f-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="bf23f-254">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bf23f-254">-Confirm</span></span>
<span data-ttu-id="bf23f-255">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf23f-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf23f-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf23f-256">-WhatIf</span></span>
<span data-ttu-id="bf23f-257">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf23f-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf23f-258">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf23f-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf23f-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf23f-259">CommonParameters</span></span>
<span data-ttu-id="bf23f-260">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf23f-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf23f-261">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf23f-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf23f-262">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf23f-262">INPUTS</span></span>

### <span data-ttu-id="bf23f-263">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bf23f-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bf23f-264">System. String</span><span class="sxs-lookup"><span data-stu-id="bf23f-264">System.String</span></span>

### <span data-ttu-id="bf23f-265">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bf23f-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bf23f-266">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bf23f-266">System.Int32</span></span>

### <span data-ttu-id="bf23f-267">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. Upgrademode, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bf23f-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="bf23f-268">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="bf23f-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="bf23f-269">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="bf23f-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="bf23f-270">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="bf23f-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="bf23f-271">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="bf23f-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="bf23f-272">System. String []</span><span class="sxs-lookup"><span data-stu-id="bf23f-272">System.String[]</span></span>

### <span data-ttu-id="bf23f-273">Microsoft. Azure. Management. COMPUTE. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="bf23f-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="bf23f-274">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bf23f-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bf23f-275">Microsoft. Azure. Management. COMPUTE. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bf23f-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="bf23f-276">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. ResourceIdentityType, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bf23f-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="bf23f-277">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf23f-277">OUTPUTS</span></span>

### <span data-ttu-id="bf23f-278">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bf23f-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bf23f-279">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf23f-279">NOTES</span></span>

## <span data-ttu-id="bf23f-280">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf23f-280">RELATED LINKS</span></span>

[<span data-ttu-id="bf23f-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="bf23f-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="bf23f-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="bf23f-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="bf23f-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf23f-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="bf23f-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="bf23f-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="bf23f-285">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="bf23f-285">New-AzVmss</span></span>](./New-AzVmss.md)
