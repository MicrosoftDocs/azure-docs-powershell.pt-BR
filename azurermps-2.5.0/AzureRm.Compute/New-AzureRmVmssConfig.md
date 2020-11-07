---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
ms.openlocfilehash: 4bc4782aaf235f81853a7304861a33ca53a75b45
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786163"
---
# <span data-ttu-id="7b454-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7b454-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="7b454-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b454-102">SYNOPSIS</span></span>
<span data-ttu-id="7b454-103">Cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b454-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b454-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b454-104">SYNTAX</span></span>

### <span data-ttu-id="7b454-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7b454-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b454-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b454-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b454-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b454-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b454-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b454-108">DESCRIPTION</span></span>
<span data-ttu-id="7b454-109">O cmdlet **New-AzureRmVmssConfig** cria um objeto configurável conjunto de escala do Gerenciador virtual (VMSS) local.</span><span class="sxs-lookup"><span data-stu-id="7b454-109">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="7b454-110">Outros cmdlets são necessários para configurar o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b454-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="7b454-111">Estes cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="7b454-111">These cmdlets are:</span></span>

- <span data-ttu-id="7b454-112">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="7b454-112">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="7b454-113">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7b454-113">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="7b454-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b454-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="7b454-115">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7b454-115">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="7b454-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b454-116">EXAMPLES</span></span>

### <span data-ttu-id="7b454-117">Exemplo 1: criar um objeto de configuração VMSS</span><span class="sxs-lookup"><span data-stu-id="7b454-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="7b454-118">Este exemplo cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b454-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="7b454-119">O primeiro comando usa o cmdlet **New-AzureRmVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b454-119">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="7b454-120">O segundo comando usa o cmdlet **New-AzureRmVmss** para criar um VMSS que usa o objeto de configuração VMSS criado no primeiro comando.</span><span class="sxs-lookup"><span data-stu-id="7b454-120">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="7b454-121">OS</span><span class="sxs-lookup"><span data-stu-id="7b454-121">PARAMETERS</span></span>

### <span data-ttu-id="7b454-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7b454-122">-AssignIdentity</span></span>
<span data-ttu-id="7b454-123">Especifique a identidade atribuída ao sistema para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7b454-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="7b454-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="7b454-125">Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias do conjunto de escala de forma contínua quando uma versão mais recente da imagem se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="7b454-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="7b454-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7b454-126">-BootDiagnostic</span></span>
<span data-ttu-id="7b454-127">Especifica o perfil de diagnóstico de inicialização do conjunto de dimensionamento da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7b454-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b454-128">-DefaultProfile</span></span>
<span data-ttu-id="7b454-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b454-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b454-130">-Extensão</span><span class="sxs-lookup"><span data-stu-id="7b454-130">-Extension</span></span>
<span data-ttu-id="7b454-131">Especifica o objeto de informações de extensão para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b454-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="7b454-132">Você pode usar o cmdlet **Add-AzureRmVmssExtension** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="7b454-132">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-133">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="7b454-133">-HealthProbeId</span></span>
<span data-ttu-id="7b454-134">Especifica a ID de um teste de balanceador de carga usado para determinar a integridade de uma instância no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7b454-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="7b454-135">HealthProbeId está no formato de '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} '.</span><span class="sxs-lookup"><span data-stu-id="7b454-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-136">-Identityid</span><span class="sxs-lookup"><span data-stu-id="7b454-136">-IdentityId</span></span>
<span data-ttu-id="7b454-137">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7b454-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="7b454-138">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="7b454-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7b454-139">-IdentityType</span></span>
<span data-ttu-id="7b454-140">Especifica o tipo de identidade usado para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7b454-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="7b454-141">O tipo ' SystemAssignedUserAssigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="7b454-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="7b454-142">O tipo ' nenhum ' removerá todas as identidades do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7b454-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="7b454-143">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7b454-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b454-144">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="7b454-144">SystemAssigned</span></span>
- <span data-ttu-id="7b454-145">Userassigned</span><span class="sxs-lookup"><span data-stu-id="7b454-145">UserAssigned</span></span>
- <span data-ttu-id="7b454-146">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="7b454-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="7b454-147">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7b454-147">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7b454-148">-LicenseType</span></span>
<span data-ttu-id="7b454-149">Especifique o tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="7b454-149">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-150">-Local</span><span class="sxs-lookup"><span data-stu-id="7b454-150">-Location</span></span>
<span data-ttu-id="7b454-151">Especifica o local do Azure em que o VMSS é criado.</span><span class="sxs-lookup"><span data-stu-id="7b454-151">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-152">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b454-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="7b454-153">Especifica o objeto de perfil de rede que contém as propriedades de rede da configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b454-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="7b454-154">Você pode usar o cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="7b454-154">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="7b454-155">-OsProfile</span></span>
<span data-ttu-id="7b454-156">Especifica o objeto de perfil do sistema operacional que contém as propriedades do sistema operacional para a configuração do VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b454-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="7b454-157">Você pode usar o cmdlet **set-AzureRmVmssOsProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="7b454-157">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-158">-Superprovisionamento</span><span class="sxs-lookup"><span data-stu-id="7b454-158">-Overprovision</span></span>
<span data-ttu-id="7b454-159">Indica se o cmdlet está supervisionando o VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b454-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-160">-PlanName</span><span class="sxs-lookup"><span data-stu-id="7b454-160">-PlanName</span></span>
<span data-ttu-id="7b454-161">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="7b454-161">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-162">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="7b454-162">-PlanProduct</span></span>
<span data-ttu-id="7b454-163">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="7b454-163">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="7b454-164">-PlanPromotionCode</span></span>
<span data-ttu-id="7b454-165">Especifica o código promocional do plano.</span><span class="sxs-lookup"><span data-stu-id="7b454-165">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-166">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="7b454-166">-PlanPublisher</span></span>
<span data-ttu-id="7b454-167">Especifica o fornecedor do plano.</span><span class="sxs-lookup"><span data-stu-id="7b454-167">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-168">-Priority</span><span class="sxs-lookup"><span data-stu-id="7b454-168">-Priority</span></span>
<span data-ttu-id="7b454-169">Especifica a prioridade para as máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="7b454-169">Specifies the priority for the virtual machines in the scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="7b454-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="7b454-171">Especifica a política de atualização sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="7b454-171">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: RollingUpgradePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-172">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7b454-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="7b454-173">Especifica o grupo de posicionamento único.</span><span class="sxs-lookup"><span data-stu-id="7b454-173">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-174">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7b454-174">-SkuCapacity</span></span>
<span data-ttu-id="7b454-175">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b454-175">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-176">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7b454-176">-SkuName</span></span>
<span data-ttu-id="7b454-177">Especifica o tamanho de todas as instâncias de VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b454-177">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-178">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7b454-178">-SkuTier</span></span>
<span data-ttu-id="7b454-179">Especifica o nível de VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b454-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="7b454-180">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7b454-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b454-181">Oficial</span><span class="sxs-lookup"><span data-stu-id="7b454-181">Standard</span></span>
- <span data-ttu-id="7b454-182">Basic</span><span class="sxs-lookup"><span data-stu-id="7b454-182">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="7b454-183">-StorageProfile</span></span>
<span data-ttu-id="7b454-184">Especifica o objeto de perfil de armazenamento que contém as propriedades de disco para a configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b454-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="7b454-185">Você pode usar o cmdlet **set-AzureRmVmssStorageProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="7b454-185">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-186">-Marca</span><span class="sxs-lookup"><span data-stu-id="7b454-186">-Tag</span></span>
<span data-ttu-id="7b454-187">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7b454-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7b454-188">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="7b454-188">For example:</span></span>

<span data-ttu-id="7b454-189">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7b454-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="7b454-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="7b454-191">Especificou o modo de uma atualização para máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="7b454-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="7b454-192">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7b454-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b454-193">Automático</span><span class="sxs-lookup"><span data-stu-id="7b454-193">Automatic</span></span>
- <span data-ttu-id="7b454-194">Manual</span><span class="sxs-lookup"><span data-stu-id="7b454-194">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-195">-Zone</span><span class="sxs-lookup"><span data-stu-id="7b454-195">-Zone</span></span>
<span data-ttu-id="7b454-196">Especifica a lista de zonas para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7b454-196">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-197">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7b454-197">-Confirm</span></span>
<span data-ttu-id="7b454-198">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b454-198">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b454-199">-WhatIf</span></span>
<span data-ttu-id="7b454-200">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b454-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b454-201">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b454-201">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b454-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b454-202">CommonParameters</span></span>
<span data-ttu-id="7b454-203">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b454-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b454-204">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b454-204">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b454-205">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b454-205">INPUTS</span></span>

### <span data-ttu-id="7b454-206">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7b454-206">None</span></span>
<span data-ttu-id="7b454-207">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7b454-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b454-208">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b454-208">OUTPUTS</span></span>

### <span data-ttu-id="7b454-209">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7b454-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7b454-210">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b454-210">NOTES</span></span>

## <span data-ttu-id="7b454-211">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b454-211">RELATED LINKS</span></span>

[<span data-ttu-id="7b454-212">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="7b454-212">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="7b454-213">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7b454-213">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="7b454-214">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b454-214">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="7b454-215">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7b454-215">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="7b454-216">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7b454-216">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)
