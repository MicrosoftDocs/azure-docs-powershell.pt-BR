---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111129"
---
# <span data-ttu-id="ddd8a-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ddd8a-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="ddd8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ddd8a-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd8a-103">Cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="ddd8a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ddd8a-104">SYNTAX</span></span>

### <span data-ttu-id="ddd8a-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ddd8a-105">DefaultParameterSet (Default)</span></span>
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

### <span data-ttu-id="ddd8a-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd8a-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="ddd8a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ddd8a-107">DESCRIPTION</span></span>
<span data-ttu-id="ddd8a-108">O cmdlet **New-AzVmssConfig** cria um objeto local configurável do VMSS (Virtual Manager Scale Set).</span><span class="sxs-lookup"><span data-stu-id="ddd8a-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="ddd8a-109">Outros cmdlets são necessários para configurar o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="ddd8a-110">Estes cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="ddd8a-110">These cmdlets are:</span></span>
- <span data-ttu-id="ddd8a-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ddd8a-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="ddd8a-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ddd8a-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="ddd8a-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddd8a-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="ddd8a-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ddd8a-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="ddd8a-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ddd8a-115">EXAMPLES</span></span>

### <span data-ttu-id="ddd8a-116">Exemplo 1: Criar um objeto de configuração VMSS</span><span class="sxs-lookup"><span data-stu-id="ddd8a-116">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="ddd8a-117">Este exemplo cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="ddd8a-118">O primeiro comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="ddd8a-119">O segundo comando usa o cmdlet **New-AzVmss** para criar um VMSS que usa o objeto de configuração VMSS criado no primeiro comando.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="ddd8a-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ddd8a-120">Example 2</span></span>

<span data-ttu-id="ddd8a-121">Cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="ddd8a-122">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="ddd8a-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="ddd8a-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ddd8a-123">PARAMETERS</span></span>

### <span data-ttu-id="ddd8a-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="ddd8a-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="ddd8a-125">O tempo para o qual os reparos automáticos são suspensos devido a uma alteração de estado no VM.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="ddd8a-126">O período de carência começa após a conclusão da alteração do estado.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="ddd8a-127">Isso ajuda a evitar reparos acidental ou acidental.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="ddd8a-128">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="ddd8a-129">O período mínimo permitido de carência é de 30 minutos (PT30M), que também é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="ddd8a-130">O período máximo permitido de carência é de 90 minutos (PT90M).</span><span class="sxs-lookup"><span data-stu-id="ddd8a-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="ddd8a-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ddd8a-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="ddd8a-132">Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias de conjunto de escalas de forma rolando quando uma versão mais recente da imagem estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="ddd8a-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ddd8a-133">-BootDiagnostic</span></span>
<span data-ttu-id="ddd8a-134">Especifica o perfil de diagnóstico de inicialização de conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="ddd8a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd8a-135">-DefaultProfile</span></span>
<span data-ttu-id="ddd8a-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddd8a-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="ddd8a-137">-DisableAutoRollback</span></span>
<span data-ttu-id="ddd8a-138">Desabilitar a Reação Automática para a Política de Atualização do Sistema Operacional Automático</span><span class="sxs-lookup"><span data-stu-id="ddd8a-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="ddd8a-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="ddd8a-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="ddd8a-140">Habilita reparos automáticos no conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ddd8a-141">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="ddd8a-141">-EnableUltraSSD</span></span>
<span data-ttu-id="ddd8a-142">Permite que um ou mais discos de dados gerenciados tenham um UltraSSD_LRS de armazenamento no conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="ddd8a-143">Discos gerenciados com tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a um VMSS somente se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="ddd8a-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="ddd8a-144">-EncryptionAtHost</span></span>
<span data-ttu-id="ddd8a-145">Esse parâmetro habilitará a criptografia para todos os discos, incluindo o disco Resource/Temp no próprio host.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="ddd8a-146">Padrão: a Criptografia no host será desabilitada, a menos que essa propriedade seja definida como verdadeira para o recurso.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="ddd8a-147">-EsporáciaPolicy</span><span class="sxs-lookup"><span data-stu-id="ddd8a-147">-EvictionPolicy</span></span>
<span data-ttu-id="ddd8a-148">Especifica a política de desapropriação para as máquinas virtuais no conjunto de escalas.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="ddd8a-149">-Extensão</span><span class="sxs-lookup"><span data-stu-id="ddd8a-149">-Extension</span></span>
<span data-ttu-id="ddd8a-150">Especifica o objeto de informações de extensão do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="ddd8a-151">Você pode usar **o cmdlet Add-AzVmssExtension** para adicionar este objeto.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="ddd8a-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="ddd8a-152">-HealthProbeId</span></span>
<span data-ttu-id="ddd8a-153">Especifica a ID de um equilíbrio de carga usado para determinar a saúde de uma instância no conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="ddd8a-154">HealthProbeId está na forma de '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/constraints/{name}'.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="ddd8a-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="ddd8a-155">-IdentityId</span></span>
<span data-ttu-id="ddd8a-156">Especifica a lista de identidades de usuário associadas ao conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="ddd8a-157">As referências de identidade do usuário serão IDs de recurso ARM no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="ddd8a-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="ddd8a-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ddd8a-158">-IdentityType</span></span>
<span data-ttu-id="ddd8a-159">Especifica o tipo de identidade usado para o conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="ddd8a-160">O tipo "SystemAssignedUserAssigned" inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="ddd8a-161">O tipo "Nenhum" removerá as identidades do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="ddd8a-162">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ddd8a-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd8a-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ddd8a-163">SystemAssigned</span></span>
- <span data-ttu-id="ddd8a-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="ddd8a-164">UserAssigned</span></span>
- <span data-ttu-id="ddd8a-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="ddd8a-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="ddd8a-166">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ddd8a-166">None</span></span>

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

### <span data-ttu-id="ddd8a-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ddd8a-167">-LicenseType</span></span>
<span data-ttu-id="ddd8a-168">Especifique o tipo de licença, que é para trazer seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ddd8a-169">-Local</span><span class="sxs-lookup"><span data-stu-id="ddd8a-169">-Location</span></span>
<span data-ttu-id="ddd8a-170">Especifica o local do Azure onde o VMSS é criado.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="ddd8a-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="ddd8a-171">-MaxPrice</span></span>
<span data-ttu-id="ddd8a-172">Especifica o preço máximo que você está disposto a pagar por um VM/VMSS Spot.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="ddd8a-173">Este preço está em dólares americanos.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-173">This price is in US Dollars.</span></span> <span data-ttu-id="ddd8a-174">Esse preço será comparado com o preço spot atual para o tamanho de VM.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="ddd8a-175">Além disso, os preços são comparados no momento da criação/atualização do VM/VMSS Spot, e a operação só será bem-sucedida se o preço máximo for maior do que o preço Spot atual.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="ddd8a-176">O maxPrice também será usado para desapropriar um VM/VMSS Spot se o preço spot atual ultrapassar o máximoPrice após a criação do VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="ddd8a-177">Os valores possíveis são: qualquer valor decimal maior que zero.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="ddd8a-178">Exemplo: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-178">Example: 0.01538.</span></span>  <span data-ttu-id="ddd8a-179">-1 indica que o VM/VMSS Spot não deve ser despejado por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="ddd8a-180">Além disso, o preço máximo padrão será -1 se ele não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="ddd8a-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddd8a-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="ddd8a-182">Especifica o objeto de perfil de rede que contém as propriedades de rede para a configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="ddd8a-183">Você pode usar **o cmdlet Add-AzVmssNetworkInterfaceConfiguration** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="ddd8a-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="ddd8a-184">-OsProfile</span></span>
<span data-ttu-id="ddd8a-185">Especifica o objeto de perfil do sistema operacional que contém as propriedades do sistema operacional para a configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="ddd8a-186">Você pode usar **o cmdlet Set-AzVmssOsProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="ddd8a-187">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="ddd8a-187">-Overprovision</span></span>
<span data-ttu-id="ddd8a-188">Indica se o cmdlet sobreprovisiona o VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="ddd8a-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ddd8a-189">-PlanName</span></span>
<span data-ttu-id="ddd8a-190">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="ddd8a-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="ddd8a-191">-PlanProduct</span></span>
<span data-ttu-id="ddd8a-192">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="ddd8a-193">-PlanProcode</span><span class="sxs-lookup"><span data-stu-id="ddd8a-193">-PlanPromotionCode</span></span>
<span data-ttu-id="ddd8a-194">Especifica o código de promoção do plano.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="ddd8a-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ddd8a-195">-PlanPublisher</span></span>
<span data-ttu-id="ddd8a-196">Especifica o editor do plano.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="ddd8a-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="ddd8a-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="ddd8a-198">Contagem de domínios de falha para cada grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="ddd8a-199">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="ddd8a-199">-Priority</span></span>
<span data-ttu-id="ddd8a-200">A prioridade para o virtual que está no conjunto de escalas.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="ddd8a-201">Somente valores com suporte são 'Regular', 'Spot' e 'Low'.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="ddd8a-202">'Regular' é para máquina virtual normal.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="ddd8a-203">'Spot' é para uma máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="ddd8a-204">'Baixo' também é para uma máquina virtual local, mas é substituída por "Spot".</span><span class="sxs-lookup"><span data-stu-id="ddd8a-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="ddd8a-205">Use "Spot" em vez de "Baixo".</span><span class="sxs-lookup"><span data-stu-id="ddd8a-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="ddd8a-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="ddd8a-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="ddd8a-207">A ID do recurso do Grupo de Posicionamento de Proximidade a ser usado com esse conjunto de escalas.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="ddd8a-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="ddd8a-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="ddd8a-209">Especifica a política de atualização em implantação.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="ddd8a-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="ddd8a-210">-ScaleInPolicy</span></span>
<span data-ttu-id="ddd8a-211">As regras a serem seguidas ao dimensionar um conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="ddd8a-212">Os valores possíveis são: 'Padrão', 'OldestVM' e 'NewestVM'.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="ddd8a-213">"Padrão" quando um conjunto de escalas de máquina virtual é dimensionado, o conjunto de escalas primeiro será equilibrado entre zonas se for um conjunto de escalas zonais.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="ddd8a-214">Em seguida, ele será equilibrado em todos os Domínios de Falha o mais longe possível.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="ddd8a-215">Em cada Domínio de Falha, as máquinas virtuais escolhidas para remoção serão as mais novas que não estão protegidas da escala.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="ddd8a-216">'OldestVM' quando um conjunto de escalas de máquina virtual está sendo dimensionado, as máquinas virtuais mais antigas que não estão protegidas contra escalas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="ddd8a-217">Para conjuntos de escala de computador virtual zonal, o conjunto de escalas será primeiro equilibrado entre zonas.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="ddd8a-218">Em cada zona, as máquinas virtuais mais antigas que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="ddd8a-219">'NewestVM' quando um conjunto de escalas de máquina virtual estiver sendo dimensionado, as máquinas virtuais mais novas que não estão protegidas contra escalas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="ddd8a-220">Para conjuntos de escala de computador virtual zonal, o conjunto de escalas será primeiro equilibrado entre zonas.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="ddd8a-221">Em cada zona, as máquinas virtuais mais novas que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="ddd8a-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ddd8a-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="ddd8a-223">Especifica o único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="ddd8a-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="ddd8a-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="ddd8a-225">Especifica que as extensões não são executados em VMs extra sobreprovisionadas.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="ddd8a-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ddd8a-226">-SkuCapacity</span></span>
<span data-ttu-id="ddd8a-227">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="ddd8a-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ddd8a-228">-SkuName</span></span>
<span data-ttu-id="ddd8a-229">Especifica o tamanho de todas as instâncias do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="ddd8a-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ddd8a-230">-SkuTier</span></span>
<span data-ttu-id="ddd8a-231">Especifica o nível de VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="ddd8a-232">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ddd8a-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd8a-233">Padrão</span><span class="sxs-lookup"><span data-stu-id="ddd8a-233">Standard</span></span>
- <span data-ttu-id="ddd8a-234">Basic</span><span class="sxs-lookup"><span data-stu-id="ddd8a-234">Basic</span></span>

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

### <span data-ttu-id="ddd8a-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="ddd8a-235">-StorageProfile</span></span>
<span data-ttu-id="ddd8a-236">Especifica o objeto de perfil de armazenamento que contém as propriedades de disco para a configuração do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="ddd8a-237">Você pode usar **o cmdlet Set-AzVmssStorageProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="ddd8a-238">-Tag</span><span class="sxs-lookup"><span data-stu-id="ddd8a-238">-Tag</span></span>
<span data-ttu-id="ddd8a-239">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ddd8a-240">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ddd8a-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ddd8a-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ddd8a-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="ddd8a-242">Duração configurável (em minutos) que uma Máquina Virtual seja excluída terá que aprovar potencialmente o Evento Agendado para que o evento seja aprovado automaticamente (com tempo de tempo).</span><span class="sxs-lookup"><span data-stu-id="ddd8a-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="ddd8a-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="ddd8a-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="ddd8a-244">Habilitar os eventos Encerrar Agendado</span><span class="sxs-lookup"><span data-stu-id="ddd8a-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="ddd8a-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="ddd8a-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="ddd8a-246">Especificou o modo de uma atualização para máquinas virtuais no conjunto de escalas.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="ddd8a-247">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ddd8a-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd8a-248">Automático</span><span class="sxs-lookup"><span data-stu-id="ddd8a-248">Automatic</span></span>
- <span data-ttu-id="ddd8a-249">Manual</span><span class="sxs-lookup"><span data-stu-id="ddd8a-249">Manual</span></span>

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

### <span data-ttu-id="ddd8a-250">-Zona</span><span class="sxs-lookup"><span data-stu-id="ddd8a-250">-Zone</span></span>
<span data-ttu-id="ddd8a-251">Especifica a lista de zonas para o conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ddd8a-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="ddd8a-252">-ZoneBalance</span></span>
<span data-ttu-id="ddd8a-253">Se você quer forçar estritamente até mesmo a distribuição de Máquina Virtual entre zonas x, caso haja uma inotização de zona.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="ddd8a-254">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ddd8a-254">-Confirm</span></span>
<span data-ttu-id="ddd8a-255">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd8a-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd8a-256">-WhatIf</span></span>
<span data-ttu-id="ddd8a-257">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddd8a-258">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd8a-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd8a-259">CommonParameters</span></span>
<span data-ttu-id="ddd8a-260">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd8a-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd8a-261">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddd8a-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd8a-262">Entradas</span><span class="sxs-lookup"><span data-stu-id="ddd8a-262">INPUTS</span></span>

### <span data-ttu-id="ddd8a-263">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ddd8a-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ddd8a-264">System.String</span><span class="sxs-lookup"><span data-stu-id="ddd8a-264">System.String</span></span>

### <span data-ttu-id="ddd8a-265">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ddd8a-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ddd8a-266">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ddd8a-266">System.Int32</span></span>

### <span data-ttu-id="ddd8a-267">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ddd8a-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ddd8a-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="ddd8a-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="ddd8a-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ddd8a-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="ddd8a-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="ddd8a-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="ddd8a-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span><span class="sxs-lookup"><span data-stu-id="ddd8a-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="ddd8a-272">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ddd8a-272">System.String[]</span></span>

### <span data-ttu-id="ddd8a-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="ddd8a-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="ddd8a-274">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ddd8a-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ddd8a-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ddd8a-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="ddd8a-276">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ddd8a-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ddd8a-277">Saídas</span><span class="sxs-lookup"><span data-stu-id="ddd8a-277">OUTPUTS</span></span>

### <span data-ttu-id="ddd8a-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddd8a-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ddd8a-279">Notas</span><span class="sxs-lookup"><span data-stu-id="ddd8a-279">NOTES</span></span>

## <span data-ttu-id="ddd8a-280">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddd8a-280">RELATED LINKS</span></span>

[<span data-ttu-id="ddd8a-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ddd8a-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="ddd8a-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ddd8a-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="ddd8a-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddd8a-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="ddd8a-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ddd8a-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="ddd8a-285">Novos AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd8a-285">New-AzVmss</span></span>](./New-AzVmss.md)
