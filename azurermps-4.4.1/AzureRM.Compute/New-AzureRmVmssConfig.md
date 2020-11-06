---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 3229f1e09cca1b32b62e5b7233806b20ed8ed78e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610514"
---
# <span data-ttu-id="5a8ab-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5a8ab-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="5a8ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="5a8ab-103">Cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a8ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a8ab-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-AssignIdentity]
 [-IdentityType <ResourceIdentityType>] [-RecoveryPolicyMode <RecoveryMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a8ab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a8ab-105">DESCRIPTION</span></span>
<span data-ttu-id="5a8ab-106">O cmdlet **New-AzureRmVmssConfig** cria um objeto configurável conjunto de escala do Gerenciador virtual (VMSS) local.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="5a8ab-107">Outros cmdlets são necessários para configurar o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="5a8ab-108">Estes cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="5a8ab-108">These cmdlets are:</span></span>

- <span data-ttu-id="5a8ab-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="5a8ab-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="5a8ab-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5a8ab-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="5a8ab-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a8ab-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="5a8ab-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5a8ab-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="5a8ab-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a8ab-113">EXAMPLES</span></span>

### <span data-ttu-id="5a8ab-114">Exemplo 1: criar um objeto de configuração VMSS</span><span class="sxs-lookup"><span data-stu-id="5a8ab-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="5a8ab-115">Este exemplo cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="5a8ab-116">O primeiro comando usa o cmdlet **New-AzureRmVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="5a8ab-117">O segundo comando usa o cmdlet **New-AzureRmVmss** para criar um VMSS que usa o objeto de configuração VMSS criado no primeiro comando.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="5a8ab-118">OS</span><span class="sxs-lookup"><span data-stu-id="5a8ab-118">PARAMETERS</span></span>

### <span data-ttu-id="5a8ab-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5a8ab-119">-AssignIdentity</span></span>
<span data-ttu-id="5a8ab-120">Especifique a identidade atribuída ao sistema para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-120">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8ab-121">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="5a8ab-121">-AutoOSUpgrade</span></span>
<span data-ttu-id="5a8ab-122">Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias do conjunto de escala de forma contínua quando uma versão mais recente da imagem se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-122">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a8ab-123">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5a8ab-123">-BootDiagnostic</span></span>
<span data-ttu-id="5a8ab-124">Especifica o perfil de diagnóstico de inicialização do conjunto de dimensionamento da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-124">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="5a8ab-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a8ab-125">-DefaultProfile</span></span>
<span data-ttu-id="5a8ab-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a8ab-127">-Extensão</span><span class="sxs-lookup"><span data-stu-id="5a8ab-127">-Extension</span></span>
<span data-ttu-id="5a8ab-128">Especifica o objeto de informações de extensão para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-128">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="5a8ab-129">Você pode usar o cmdlet **Add-AzureRmVmssExtension** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-129">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="5a8ab-130">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="5a8ab-130">-HealthProbeId</span></span>
<span data-ttu-id="5a8ab-131">Especifique a ID de um teste de balanceador de carga usado para determinar a integridade de uma instância no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-131">Specify the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span> <span data-ttu-id="5a8ab-132">HealthProbeId está no formato de '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} '.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-132">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="5a8ab-133">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5a8ab-133">-IdentityType</span></span>
<span data-ttu-id="5a8ab-134">Especifique a identidade do conjunto de escala da máquina virtual, se configurado.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-134">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a8ab-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5a8ab-135">-LicenseType</span></span>
<span data-ttu-id="5a8ab-136">Especifique o tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-136">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="5a8ab-137">-Local</span><span class="sxs-lookup"><span data-stu-id="5a8ab-137">-Location</span></span>
<span data-ttu-id="5a8ab-138">Especifica o local do Azure em que o VMSS é criado.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-138">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="5a8ab-139">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a8ab-139">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="5a8ab-140">Especifica o objeto de perfil de rede que contém as propriedades de rede da configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-140">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="5a8ab-141">Você pode usar o cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-141">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="5a8ab-142">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="5a8ab-142">-OsProfile</span></span>
<span data-ttu-id="5a8ab-143">Especifica o objeto de perfil do sistema operacional que contém as propriedades do sistema operacional para a configuração do VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-143">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="5a8ab-144">Você pode usar o cmdlet **set-AzureRmVmssOsProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-144">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="5a8ab-145">-Superprovisionamento</span><span class="sxs-lookup"><span data-stu-id="5a8ab-145">-Overprovision</span></span>
<span data-ttu-id="5a8ab-146">Indica se o cmdlet está supervisionando o VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-146">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="5a8ab-147">-PlanName</span><span class="sxs-lookup"><span data-stu-id="5a8ab-147">-PlanName</span></span>
<span data-ttu-id="5a8ab-148">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-148">Specifies the plan name.</span></span>

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

### <span data-ttu-id="5a8ab-149">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="5a8ab-149">-PlanProduct</span></span>
<span data-ttu-id="5a8ab-150">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-150">Specifies the plan product.</span></span>

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

### <span data-ttu-id="5a8ab-151">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="5a8ab-151">-PlanPromotionCode</span></span>
<span data-ttu-id="5a8ab-152">Especifica o código promocional do plano.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-152">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="5a8ab-153">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="5a8ab-153">-PlanPublisher</span></span>
<span data-ttu-id="5a8ab-154">Especifica o fornecedor do plano.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-154">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="5a8ab-155">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="5a8ab-155">-RecoveryPolicyMode</span></span>
<span data-ttu-id="5a8ab-156">Especifique a política de recuperação.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-156">Specify the recovery policy.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Compute.Automation.RecoveryMode]
Parameter Sets: (All)
Aliases: 
Accepted values: None, OverProvision, Reprovision

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a8ab-157">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="5a8ab-157">-RollingUpgradePolicy</span></span>
<span data-ttu-id="5a8ab-158">Especifica a política de atualização sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-158">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="5a8ab-159">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5a8ab-159">-SinglePlacementGroup</span></span>
<span data-ttu-id="5a8ab-160">Especifica o grupo de posicionamento único.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-160">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="5a8ab-161">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5a8ab-161">-SkuCapacity</span></span>
<span data-ttu-id="5a8ab-162">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-162">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a8ab-163">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5a8ab-163">-SkuName</span></span>
<span data-ttu-id="5a8ab-164">Especifica o tamanho de todas as instâncias de VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-164">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="5a8ab-165">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5a8ab-165">-SkuTier</span></span>
<span data-ttu-id="5a8ab-166">Especifica o nível de VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-166">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="5a8ab-167">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5a8ab-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a8ab-168">Oficial</span><span class="sxs-lookup"><span data-stu-id="5a8ab-168">Standard</span></span>
- <span data-ttu-id="5a8ab-169">Basic</span><span class="sxs-lookup"><span data-stu-id="5a8ab-169">Basic</span></span>

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

### <span data-ttu-id="5a8ab-170">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="5a8ab-170">-StorageProfile</span></span>
<span data-ttu-id="5a8ab-171">Especifica o objeto de perfil de armazenamento que contém as propriedades de disco para a configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-171">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="5a8ab-172">Você pode usar o cmdlet **set-AzureRmVmssStorageProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-172">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="5a8ab-173">-Marca</span><span class="sxs-lookup"><span data-stu-id="5a8ab-173">-Tag</span></span>
<span data-ttu-id="5a8ab-174">Especifica as marcas que serão atribuídas ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-174">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="5a8ab-175">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="5a8ab-175">-UpgradePolicyMode</span></span>
<span data-ttu-id="5a8ab-176">Especificou o modo de uma atualização para máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-176">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="5a8ab-177">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5a8ab-177">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a8ab-178">Automático</span><span class="sxs-lookup"><span data-stu-id="5a8ab-178">Automatic</span></span>
- <span data-ttu-id="5a8ab-179">Manual</span><span class="sxs-lookup"><span data-stu-id="5a8ab-179">Manual</span></span>

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

### <span data-ttu-id="5a8ab-180">-Zone</span><span class="sxs-lookup"><span data-stu-id="5a8ab-180">-Zone</span></span>
<span data-ttu-id="5a8ab-181">Especifica a lista de zonas para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-181">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="5a8ab-182">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5a8ab-182">-Confirm</span></span>
<span data-ttu-id="5a8ab-183">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a8ab-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a8ab-184">-WhatIf</span></span>
<span data-ttu-id="5a8ab-185">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-185">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a8ab-186">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a8ab-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a8ab-187">CommonParameters</span></span>
<span data-ttu-id="5a8ab-188">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a8ab-189">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a8ab-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a8ab-190">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a8ab-190">INPUTS</span></span>

## <span data-ttu-id="5a8ab-191">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a8ab-191">OUTPUTS</span></span>

### <span data-ttu-id="5a8ab-192">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="5a8ab-192">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5a8ab-193">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a8ab-193">NOTES</span></span>

## <span data-ttu-id="5a8ab-194">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a8ab-194">RELATED LINKS</span></span>

[<span data-ttu-id="5a8ab-195">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="5a8ab-195">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="5a8ab-196">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5a8ab-196">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="5a8ab-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a8ab-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="5a8ab-198">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5a8ab-198">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="5a8ab-199">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a8ab-199">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


