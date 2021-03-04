---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: ba44e397aa09834b1371fa9188527a056153017c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890009"
---
# <span data-ttu-id="6bf67-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6bf67-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="6bf67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bf67-102">SYNOPSIS</span></span>
<span data-ttu-id="6bf67-103">Cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="6bf67-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6bf67-104">SYNTAX</span></span>

### <span data-ttu-id="6bf67-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6bf67-105">DefaultParameterSet (Default)</span></span>
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

### <span data-ttu-id="6bf67-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bf67-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="6bf67-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6bf67-107">DESCRIPTION</span></span>
<span data-ttu-id="6bf67-108">O cmdlet **New-AzVmssConfig** cria um objeto VMSS (Conjunto de Escala de Gerenciador Virtual) configurável.</span><span class="sxs-lookup"><span data-stu-id="6bf67-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="6bf67-109">Outros cmdlets são necessários para configurar o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="6bf67-110">Esses cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="6bf67-110">These cmdlets are:</span></span>
- <span data-ttu-id="6bf67-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="6bf67-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="6bf67-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6bf67-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="6bf67-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bf67-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="6bf67-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="6bf67-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="6bf67-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6bf67-115">EXAMPLES</span></span>

### <span data-ttu-id="6bf67-116">Exemplo 1: Criar um objeto de configuração VMSS</span><span class="sxs-lookup"><span data-stu-id="6bf67-116">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="6bf67-117">Este exemplo cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="6bf67-118">O primeiro comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="6bf67-119">O segundo comando usa o cmdlet **New-AzVmss** para criar um VMSS que usa o objeto de configuração VMSS criado no primeiro comando.</span><span class="sxs-lookup"><span data-stu-id="6bf67-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="6bf67-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6bf67-120">Example 2</span></span>

<span data-ttu-id="6bf67-121">Cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="6bf67-122">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="6bf67-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="6bf67-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6bf67-123">PARAMETERS</span></span>

### <span data-ttu-id="6bf67-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="6bf67-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="6bf67-125">O tempo para o qual os reparos automáticos são suspensos devido a uma alteração de estado na VM.</span><span class="sxs-lookup"><span data-stu-id="6bf67-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="6bf67-126">O tempo de carência começa após a conclusão da alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="6bf67-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="6bf67-127">Isso ajuda a evitar reparos prematuras ou acidentais.</span><span class="sxs-lookup"><span data-stu-id="6bf67-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="6bf67-128">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="6bf67-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="6bf67-129">O período mínimo de carência permitido é de 30 minutos (PT30M), que também é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="6bf67-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="6bf67-130">O período máximo permitido de carência é de 90 minutos (PT90M).</span><span class="sxs-lookup"><span data-stu-id="6bf67-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="6bf67-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6bf67-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="6bf67-132">Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias de conjunto de escalas de forma rolante quando uma versão mais recente da imagem se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="6bf67-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="6bf67-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6bf67-133">-BootDiagnostic</span></span>
<span data-ttu-id="6bf67-134">Especifica o perfil de diagnóstico de inicialização do conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6bf67-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="6bf67-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bf67-135">-DefaultProfile</span></span>
<span data-ttu-id="6bf67-136">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6bf67-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bf67-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="6bf67-137">-DisableAutoRollback</span></span>
<span data-ttu-id="6bf67-138">Desabilitar a Reação Automática para a Política de Atualização automática do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="6bf67-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="6bf67-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="6bf67-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="6bf67-140">Habilita reparos automáticos no conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6bf67-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="6bf67-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="6bf67-141">-EnableUltraSSD</span></span>
<span data-ttu-id="6bf67-142">Permite que um recurso tenha um ou mais discos de dados gerenciados com UltraSSD_LRS de conta de armazenamento no conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6bf67-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="6bf67-143">Discos gerenciados com tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a um VMSS somente se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="6bf67-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="6bf67-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="6bf67-144">-EncryptionAtHost</span></span>
<span data-ttu-id="6bf67-145">Esse parâmetro habilitará a criptografia para todos os discos, incluindo o disco Resource/Temp no próprio host.</span><span class="sxs-lookup"><span data-stu-id="6bf67-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="6bf67-146">Padrão: a Criptografia no host será desabilitada, a menos que essa propriedade seja definida como true para o recurso.</span><span class="sxs-lookup"><span data-stu-id="6bf67-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="6bf67-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="6bf67-147">-EvictionPolicy</span></span>
<span data-ttu-id="6bf67-148">Especifica a política de despejo das máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="6bf67-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="6bf67-149">-Extension</span><span class="sxs-lookup"><span data-stu-id="6bf67-149">-Extension</span></span>
<span data-ttu-id="6bf67-150">Especifica o objeto de informações de extensão do VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="6bf67-151">Você pode usar o cmdlet **Add-AzVmssExtension** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="6bf67-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="6bf67-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="6bf67-152">-HealthProbeId</span></span>
<span data-ttu-id="6bf67-153">Especifica a ID de uma sonda balanceador de carga usada para determinar a saúde de uma instância no conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6bf67-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="6bf67-154">HealthProbeId está na forma de '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span><span class="sxs-lookup"><span data-stu-id="6bf67-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="6bf67-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="6bf67-155">-IdentityId</span></span>
<span data-ttu-id="6bf67-156">Especifica a lista de identidades de usuário associadas ao conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6bf67-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="6bf67-157">As referências de identidade do usuário serão ARM ids de recurso no formato: '/subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identity/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="6bf67-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="6bf67-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6bf67-158">-IdentityType</span></span>
<span data-ttu-id="6bf67-159">Especifica o tipo de identidade usado para o conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6bf67-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="6bf67-160">O tipo "SystemAssignedUserAssigned" inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6bf67-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="6bf67-161">O tipo "Nenhum" removerá qualquer identidade do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6bf67-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="6bf67-162">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6bf67-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6bf67-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="6bf67-163">SystemAssigned</span></span>
- <span data-ttu-id="6bf67-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="6bf67-164">UserAssigned</span></span>
- <span data-ttu-id="6bf67-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="6bf67-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="6bf67-166">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6bf67-166">None</span></span>

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

### <span data-ttu-id="6bf67-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6bf67-167">-LicenseType</span></span>
<span data-ttu-id="6bf67-168">Especifique o tipo de licença, que é para trazer seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="6bf67-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="6bf67-169">-Location</span><span class="sxs-lookup"><span data-stu-id="6bf67-169">-Location</span></span>
<span data-ttu-id="6bf67-170">Especifica o local do Azure onde o VMSS é criado.</span><span class="sxs-lookup"><span data-stu-id="6bf67-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="6bf67-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="6bf67-171">-MaxPrice</span></span>
<span data-ttu-id="6bf67-172">Especifica o preço máximo que você está disposto a pagar por uma VM/VMSS Spot.</span><span class="sxs-lookup"><span data-stu-id="6bf67-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="6bf67-173">Esse preço está em dólares dos EUA.</span><span class="sxs-lookup"><span data-stu-id="6bf67-173">This price is in US Dollars.</span></span> <span data-ttu-id="6bf67-174">Esse preço será comparado com o preço spot atual para o tamanho da VM.</span><span class="sxs-lookup"><span data-stu-id="6bf67-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="6bf67-175">Além disso, os preços são comparados no momento da criação/atualização da VM/VMSS Spot e a operação só terá êxito se o maxPrice for maior do que o preço Spot atual.</span><span class="sxs-lookup"><span data-stu-id="6bf67-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="6bf67-176">O maxPrice também será usado para despejo de uma VM/VMSS Spot se o preço Spot atual for além do maxPrice após a criação da VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="6bf67-177">Os valores possíveis são: qualquer valor decimal maior que zero.</span><span class="sxs-lookup"><span data-stu-id="6bf67-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="6bf67-178">Exemplo: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="6bf67-178">Example: 0.01538.</span></span>  <span data-ttu-id="6bf67-179">-1 indica que a VM/VMSS Spot não deve ser despejada por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="6bf67-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="6bf67-180">Além disso, o preço máximo padrão será -1 se não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="6bf67-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="6bf67-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bf67-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="6bf67-182">Especifica o objeto de perfil de rede que contém as propriedades de rede para a configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="6bf67-183">Você pode usar o cmdlet **Add-AzVmssNetworkInterfaceConfiguration** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="6bf67-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="6bf67-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="6bf67-184">-OsProfile</span></span>
<span data-ttu-id="6bf67-185">Especifica o objeto de perfil do sistema operacional que contém as propriedades do sistema operacional para a configuração do VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="6bf67-186">Você pode usar o cmdlet **Set-AzVmssOsProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="6bf67-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="6bf67-187">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="6bf67-187">-Overprovision</span></span>
<span data-ttu-id="6bf67-188">Indica se o cmdlet sobreprovisiona o VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="6bf67-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="6bf67-189">-PlanName</span></span>
<span data-ttu-id="6bf67-190">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="6bf67-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="6bf67-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="6bf67-191">-PlanProduct</span></span>
<span data-ttu-id="6bf67-192">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="6bf67-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="6bf67-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="6bf67-193">-PlanPromotionCode</span></span>
<span data-ttu-id="6bf67-194">Especifica o código de promoção do plano.</span><span class="sxs-lookup"><span data-stu-id="6bf67-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="6bf67-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="6bf67-195">-PlanPublisher</span></span>
<span data-ttu-id="6bf67-196">Especifica o editor de planos.</span><span class="sxs-lookup"><span data-stu-id="6bf67-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="6bf67-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="6bf67-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="6bf67-198">Contagem de domínios de falha para cada grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="6bf67-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="6bf67-199">-Priority</span><span class="sxs-lookup"><span data-stu-id="6bf67-199">-Priority</span></span>
<span data-ttu-id="6bf67-200">A prioridade do machien virtual no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="6bf67-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="6bf67-201">Somente os valores com suporte são 'Regular', 'Spot' e 'Low'.</span><span class="sxs-lookup"><span data-stu-id="6bf67-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="6bf67-202">'Regular' é para máquina virtual regular.</span><span class="sxs-lookup"><span data-stu-id="6bf67-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="6bf67-203">'Spot' é para máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="6bf67-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="6bf67-204">'Baixo' também é para máquina virtual local, mas é substituído por 'Spot'.</span><span class="sxs-lookup"><span data-stu-id="6bf67-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="6bf67-205">Use 'Spot' em vez de 'Low'.</span><span class="sxs-lookup"><span data-stu-id="6bf67-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="6bf67-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="6bf67-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="6bf67-207">A id de recurso do Grupo de Posicionamento de Proximidade a ser usado com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="6bf67-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="6bf67-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="6bf67-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="6bf67-209">Especifica a política de atualização em circulação.</span><span class="sxs-lookup"><span data-stu-id="6bf67-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="6bf67-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="6bf67-210">-ScaleInPolicy</span></span>
<span data-ttu-id="6bf67-211">As regras a serem seguidas ao dimensionar um conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6bf67-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="6bf67-212">Os valores possíveis são: 'Default', 'OldestVM' e 'NewestVM'.</span><span class="sxs-lookup"><span data-stu-id="6bf67-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="6bf67-213">'Padrão' quando um conjunto de escala de máquina virtual é dimensionado, o conjunto de escala será balanceado primeiro entre zonas se for um conjunto de escala zonal.</span><span class="sxs-lookup"><span data-stu-id="6bf67-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="6bf67-214">Em seguida, ele será balanceado entre domínios de falha o mais longe possível.</span><span class="sxs-lookup"><span data-stu-id="6bf67-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="6bf67-215">Dentro de cada Domínio de Falha, as máquinas virtuais escolhidas para remoção serão as mais novas que não estão protegidas de dimensionar.</span><span class="sxs-lookup"><span data-stu-id="6bf67-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="6bf67-216">"OldestVM" quando um conjunto de escalas de máquina virtual está sendo dimensionado, as máquinas virtuais mais antigas que não estão protegidas contra a escala serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="6bf67-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="6bf67-217">Para conjuntos de escala de máquina virtual zonal, o conjunto de escalas primeiro será balanceado entre zonas.</span><span class="sxs-lookup"><span data-stu-id="6bf67-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="6bf67-218">Dentro de cada zona, as máquinas virtuais mais antigas que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="6bf67-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="6bf67-219">"NewestVM" quando um conjunto de escalas de máquina virtual está sendo dimensionado, as máquinas virtuais mais novas que não estão protegidas contra dimensionar serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="6bf67-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="6bf67-220">Para conjuntos de escala de máquina virtual zonal, o conjunto de escalas primeiro será balanceado entre zonas.</span><span class="sxs-lookup"><span data-stu-id="6bf67-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="6bf67-221">Dentro de cada zona, as máquinas virtuais mais novas que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="6bf67-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="6bf67-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6bf67-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="6bf67-223">Especifica o grupo de posicionamento único.</span><span class="sxs-lookup"><span data-stu-id="6bf67-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="6bf67-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="6bf67-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="6bf67-225">Especifica que as extensões não são executados nas VMs sobreprovisionadas extras.</span><span class="sxs-lookup"><span data-stu-id="6bf67-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="6bf67-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6bf67-226">-SkuCapacity</span></span>
<span data-ttu-id="6bf67-227">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="6bf67-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6bf67-228">-SkuName</span></span>
<span data-ttu-id="6bf67-229">Especifica o tamanho de todas as instâncias do VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="6bf67-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6bf67-230">-SkuTier</span></span>
<span data-ttu-id="6bf67-231">Especifica a camada de VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="6bf67-232">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6bf67-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6bf67-233">Standard</span><span class="sxs-lookup"><span data-stu-id="6bf67-233">Standard</span></span>
- <span data-ttu-id="6bf67-234">Básico</span><span class="sxs-lookup"><span data-stu-id="6bf67-234">Basic</span></span>

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

### <span data-ttu-id="6bf67-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="6bf67-235">-StorageProfile</span></span>
<span data-ttu-id="6bf67-236">Especifica o objeto de perfil de armazenamento que contém as propriedades de disco para a configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf67-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="6bf67-237">Você pode usar o cmdlet **Set-AzVmssStorageProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="6bf67-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="6bf67-238">-Tag</span><span class="sxs-lookup"><span data-stu-id="6bf67-238">-Tag</span></span>
<span data-ttu-id="6bf67-239">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6bf67-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6bf67-240">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="6bf67-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6bf67-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6bf67-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="6bf67-242">Tempo configurável (em minutos) uma Máquina Virtual que está sendo excluída terá que aprovar potencialmente o Evento Encerrado Agendado antes que o evento seja aprovado automaticamente (tempo final).</span><span class="sxs-lookup"><span data-stu-id="6bf67-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="6bf67-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="6bf67-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="6bf67-244">Habilitar os eventos encerrados agendados</span><span class="sxs-lookup"><span data-stu-id="6bf67-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="6bf67-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="6bf67-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="6bf67-246">Especificou o modo de atualização para máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="6bf67-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="6bf67-247">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6bf67-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6bf67-248">Automático</span><span class="sxs-lookup"><span data-stu-id="6bf67-248">Automatic</span></span>
- <span data-ttu-id="6bf67-249">Manual</span><span class="sxs-lookup"><span data-stu-id="6bf67-249">Manual</span></span>

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

### <span data-ttu-id="6bf67-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="6bf67-250">-Zone</span></span>
<span data-ttu-id="6bf67-251">Especifica a lista de zonas do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6bf67-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="6bf67-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="6bf67-252">-ZoneBalance</span></span>
<span data-ttu-id="6bf67-253">Se é necessário forçar estritamente até mesmo a distribuição da Máquina Virtual entre zonas x no caso de uma ina rebaixamento de zona.</span><span class="sxs-lookup"><span data-stu-id="6bf67-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="6bf67-254">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bf67-254">-Confirm</span></span>
<span data-ttu-id="6bf67-255">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bf67-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bf67-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bf67-256">-WhatIf</span></span>
<span data-ttu-id="6bf67-257">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6bf67-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bf67-258">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6bf67-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bf67-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bf67-259">CommonParameters</span></span>
<span data-ttu-id="6bf67-260">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bf67-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bf67-261">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bf67-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bf67-262">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bf67-262">INPUTS</span></span>

### <span data-ttu-id="6bf67-263">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6bf67-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6bf67-264">System.String</span><span class="sxs-lookup"><span data-stu-id="6bf67-264">System.String</span></span>

### <span data-ttu-id="6bf67-265">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6bf67-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6bf67-266">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6bf67-266">System.Int32</span></span>

### <span data-ttu-id="6bf67-267">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6bf67-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6bf67-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="6bf67-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="6bf67-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6bf67-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="6bf67-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="6bf67-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="6bf67-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span><span class="sxs-lookup"><span data-stu-id="6bf67-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="6bf67-272">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6bf67-272">System.String[]</span></span>

### <span data-ttu-id="6bf67-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="6bf67-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="6bf67-274">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6bf67-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6bf67-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6bf67-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="6bf67-276">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6bf67-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="6bf67-277">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6bf67-277">OUTPUTS</span></span>

### <span data-ttu-id="6bf67-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6bf67-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6bf67-279">NOTES</span><span class="sxs-lookup"><span data-stu-id="6bf67-279">NOTES</span></span>

## <span data-ttu-id="6bf67-280">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6bf67-280">RELATED LINKS</span></span>

[<span data-ttu-id="6bf67-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="6bf67-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="6bf67-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6bf67-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="6bf67-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bf67-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="6bf67-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="6bf67-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="6bf67-285">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6bf67-285">New-AzVmss</span></span>](./New-AzVmss.md)
