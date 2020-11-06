---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: ee18925960b7f2afd9e35250a3cc33a5bd16e073
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428546"
---
# <span data-ttu-id="2e3fb-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2e3fb-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="2e3fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e3fb-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3fb-103">Cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e3fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e3fb-104">SYNTAX</span></span>

### <span data-ttu-id="2e3fb-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e3fb-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e3fb-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e3fb-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e3fb-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e3fb-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e3fb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e3fb-108">DESCRIPTION</span></span>
<span data-ttu-id="2e3fb-109">O cmdlet **New-AzureRmVmssConfig** cria um objeto configurável conjunto de escala do Gerenciador virtual (VMSS) local.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-109">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="2e3fb-110">Outros cmdlets são necessários para configurar o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="2e3fb-111">Estes cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="2e3fb-111">These cmdlets are:</span></span>
- <span data-ttu-id="2e3fb-112">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="2e3fb-112">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="2e3fb-113">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="2e3fb-113">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="2e3fb-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e3fb-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="2e3fb-115">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="2e3fb-115">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="2e3fb-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e3fb-116">EXAMPLES</span></span>

### <span data-ttu-id="2e3fb-117">Exemplo 1: criar um objeto de configuração VMSS</span><span class="sxs-lookup"><span data-stu-id="2e3fb-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="2e3fb-118">Este exemplo cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="2e3fb-119">O primeiro comando usa o cmdlet **New-AzureRmVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-119">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="2e3fb-120">O segundo comando usa o cmdlet **New-AzureRmVmss** para criar um VMSS que usa o objeto de configuração VMSS criado no primeiro comando.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-120">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="2e3fb-121">OS</span><span class="sxs-lookup"><span data-stu-id="2e3fb-121">PARAMETERS</span></span>

### <span data-ttu-id="2e3fb-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2e3fb-122">-AssignIdentity</span></span>
<span data-ttu-id="2e3fb-123">Especifique a identidade atribuída ao sistema para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="2e3fb-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="2e3fb-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="2e3fb-125">Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias do conjunto de escala de forma contínua quando uma versão mais recente da imagem se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="2e3fb-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2e3fb-126">-BootDiagnostic</span></span>
<span data-ttu-id="2e3fb-127">Especifica o perfil de diagnóstico de inicialização do conjunto de dimensionamento da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="2e3fb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3fb-128">-DefaultProfile</span></span>
<span data-ttu-id="2e3fb-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e3fb-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="2e3fb-130">-DisableAutoRollback</span></span>
<span data-ttu-id="2e3fb-131">Desabilitar a reversão automática para a política de atualização automática de so</span><span class="sxs-lookup"><span data-stu-id="2e3fb-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="2e3fb-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="2e3fb-132">-EnableUltraSSD</span></span>
<span data-ttu-id="2e3fb-133">Habilita um recurso para ter um ou mais discos de dados gerenciados com o tipo de conta de armazenamento UltraSSD_LRS no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="2e3fb-134">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a um VMSS somente se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="2e3fb-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="2e3fb-135">-EvictionPolicy</span></span>
<span data-ttu-id="2e3fb-136">Especifica a política de remoção para as máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="2e3fb-137">-Extensão</span><span class="sxs-lookup"><span data-stu-id="2e3fb-137">-Extension</span></span>
<span data-ttu-id="2e3fb-138">Especifica o objeto de informações de extensão para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="2e3fb-139">Você pode usar o cmdlet **Add-AzureRmVmssExtension** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-139">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3fb-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="2e3fb-140">-HealthProbeId</span></span>
<span data-ttu-id="2e3fb-141">Especifica a ID de um teste de balanceador de carga usado para determinar a integridade de uma instância no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="2e3fb-142">HealthProbeId está no formato de '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} '.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="2e3fb-143">-Identityid</span><span class="sxs-lookup"><span data-stu-id="2e3fb-143">-IdentityId</span></span>
<span data-ttu-id="2e3fb-144">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="2e3fb-145">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="2e3fb-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="2e3fb-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2e3fb-146">-IdentityType</span></span>
<span data-ttu-id="2e3fb-147">Especifica o tipo de identidade usado para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="2e3fb-148">O tipo ' SystemAssignedUserAssigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="2e3fb-149">O tipo ' nenhum ' removerá todas as identidades do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="2e3fb-150">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2e3fb-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2e3fb-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="2e3fb-151">SystemAssigned</span></span>
- <span data-ttu-id="2e3fb-152">Userassigned</span><span class="sxs-lookup"><span data-stu-id="2e3fb-152">UserAssigned</span></span>
- <span data-ttu-id="2e3fb-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="2e3fb-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="2e3fb-154">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2e3fb-154">None</span></span>

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

### <span data-ttu-id="2e3fb-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2e3fb-155">-LicenseType</span></span>
<span data-ttu-id="2e3fb-156">Especifique o tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="2e3fb-157">-Local</span><span class="sxs-lookup"><span data-stu-id="2e3fb-157">-Location</span></span>
<span data-ttu-id="2e3fb-158">Especifica o local do Azure em que o VMSS é criado.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="2e3fb-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e3fb-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="2e3fb-160">Especifica o objeto de perfil de rede que contém as propriedades de rede da configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="2e3fb-161">Você pode usar o cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-161">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="2e3fb-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="2e3fb-162">-OsProfile</span></span>
<span data-ttu-id="2e3fb-163">Especifica o objeto de perfil do sistema operacional que contém as propriedades do sistema operacional para a configuração do VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="2e3fb-164">Você pode usar o cmdlet **set-AzureRmVmssOsProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-164">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="2e3fb-165">-Superprovisionamento</span><span class="sxs-lookup"><span data-stu-id="2e3fb-165">-Overprovision</span></span>
<span data-ttu-id="2e3fb-166">Indica se o cmdlet está supervisionando o VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="2e3fb-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="2e3fb-167">-PlanName</span></span>
<span data-ttu-id="2e3fb-168">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="2e3fb-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="2e3fb-169">-PlanProduct</span></span>
<span data-ttu-id="2e3fb-170">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="2e3fb-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="2e3fb-171">-PlanPromotionCode</span></span>
<span data-ttu-id="2e3fb-172">Especifica o código promocional do plano.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="2e3fb-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="2e3fb-173">-PlanPublisher</span></span>
<span data-ttu-id="2e3fb-174">Especifica o fornecedor do plano.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="2e3fb-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="2e3fb-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="2e3fb-176">Contagem de domínios de falha para cada grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="2e3fb-177">-Priority</span><span class="sxs-lookup"><span data-stu-id="2e3fb-177">-Priority</span></span>
<span data-ttu-id="2e3fb-178">Especifica a prioridade para as máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="2e3fb-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="2e3fb-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="2e3fb-180">Especifica a política de atualização sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="2e3fb-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2e3fb-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="2e3fb-182">Especifica o grupo de posicionamento único.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="2e3fb-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2e3fb-183">-SkuCapacity</span></span>
<span data-ttu-id="2e3fb-184">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="2e3fb-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2e3fb-185">-SkuName</span></span>
<span data-ttu-id="2e3fb-186">Especifica o tamanho de todas as instâncias de VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="2e3fb-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2e3fb-187">-SkuTier</span></span>
<span data-ttu-id="2e3fb-188">Especifica o nível de VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="2e3fb-189">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2e3fb-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2e3fb-190">Oficial</span><span class="sxs-lookup"><span data-stu-id="2e3fb-190">Standard</span></span>
- <span data-ttu-id="2e3fb-191">Basic</span><span class="sxs-lookup"><span data-stu-id="2e3fb-191">Basic</span></span>

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

### <span data-ttu-id="2e3fb-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="2e3fb-192">-StorageProfile</span></span>
<span data-ttu-id="2e3fb-193">Especifica o objeto de perfil de armazenamento que contém as propriedades de disco para a configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="2e3fb-194">Você pode usar o cmdlet **set-AzureRmVmssStorageProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-194">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="2e3fb-195">-Marca</span><span class="sxs-lookup"><span data-stu-id="2e3fb-195">-Tag</span></span>
<span data-ttu-id="2e3fb-196">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2e3fb-197">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2e3fb-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2e3fb-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="2e3fb-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="2e3fb-199">Especificou o modo de uma atualização para máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="2e3fb-200">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2e3fb-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2e3fb-201">Automático</span><span class="sxs-lookup"><span data-stu-id="2e3fb-201">Automatic</span></span>
- <span data-ttu-id="2e3fb-202">Manual</span><span class="sxs-lookup"><span data-stu-id="2e3fb-202">Manual</span></span>

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

### <span data-ttu-id="2e3fb-203">-Zone</span><span class="sxs-lookup"><span data-stu-id="2e3fb-203">-Zone</span></span>
<span data-ttu-id="2e3fb-204">Especifica a lista de zonas para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="2e3fb-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="2e3fb-205">-ZoneBalance</span></span>
<span data-ttu-id="2e3fb-206">Se devem ser forçadas rigorosamente entre x-Zones de distribuição de máquinas virtuais, caso haja falha na zona.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="2e3fb-207">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e3fb-207">-Confirm</span></span>
<span data-ttu-id="2e3fb-208">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e3fb-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e3fb-209">-WhatIf</span></span>
<span data-ttu-id="2e3fb-210">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e3fb-211">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e3fb-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e3fb-212">CommonParameters</span></span>
<span data-ttu-id="2e3fb-213">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e3fb-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e3fb-214">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e3fb-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e3fb-215">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e3fb-215">INPUTS</span></span>

### <span data-ttu-id="2e3fb-216">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2e3fb-216">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2e3fb-217">System. String</span><span class="sxs-lookup"><span data-stu-id="2e3fb-217">System.String</span></span>

### <span data-ttu-id="2e3fb-218">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e3fb-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2e3fb-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2e3fb-219">System.Int32</span></span>

### <span data-ttu-id="2e3fb-220">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. Upgrademode, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2e3fb-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2e3fb-221">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="2e3fb-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="2e3fb-222">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="2e3fb-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="2e3fb-223">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="2e3fb-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="2e3fb-224">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="2e3fb-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="2e3fb-225">System. String []</span><span class="sxs-lookup"><span data-stu-id="2e3fb-225">System.String[]</span></span>

### <span data-ttu-id="2e3fb-226">Microsoft. Azure. Management. COMPUTE. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="2e3fb-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="2e3fb-227">Microsoft. Azure. Management. COMPUTE. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="2e3fb-227">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="2e3fb-228">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. ResourceIdentityType, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2e3fb-228">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="2e3fb-229">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e3fb-229">OUTPUTS</span></span>

### <span data-ttu-id="2e3fb-230">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2e3fb-230">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2e3fb-231">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e3fb-231">NOTES</span></span>

## <span data-ttu-id="2e3fb-232">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e3fb-232">RELATED LINKS</span></span>

[<span data-ttu-id="2e3fb-233">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="2e3fb-233">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="2e3fb-234">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="2e3fb-234">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="2e3fb-235">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e3fb-235">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="2e3fb-236">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="2e3fb-236">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="2e3fb-237">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2e3fb-237">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)
