---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 4b87c121368232769672c24bc5005f3a50bfd39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428975"
---
# <span data-ttu-id="70668-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="70668-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="70668-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70668-102">SYNOPSIS</span></span>
<span data-ttu-id="70668-103">Cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70668-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70668-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-PlanName <String>]
 [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RecoveryPolicyMode <RecoveryMode>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-IdentityType <ResourceIdentityType>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70668-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70668-105">DESCRIPTION</span></span>
<span data-ttu-id="70668-106">O cmdlet **New-AzureRmVmssConfig** cria um objeto configurável conjunto de escala do Gerenciador virtual (VMSS) local.</span><span class="sxs-lookup"><span data-stu-id="70668-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="70668-107">Outros cmdlets são necessários para configurar o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="70668-108">Estes cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="70668-108">These cmdlets are:</span></span>

- <span data-ttu-id="70668-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="70668-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="70668-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="70668-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="70668-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="70668-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="70668-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="70668-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="70668-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70668-113">EXAMPLES</span></span>

### <span data-ttu-id="70668-114">Exemplo 1: criar um objeto de configuração VMSS</span><span class="sxs-lookup"><span data-stu-id="70668-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="70668-115">Este exemplo cria um objeto de configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="70668-116">O primeiro comando usa o cmdlet **New-AzureRmVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="70668-117">O segundo comando usa o cmdlet **New-AzureRmVmss** para criar um VMSS que usa o objeto de configuração VMSS criado no primeiro comando.</span><span class="sxs-lookup"><span data-stu-id="70668-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="70668-118">OS</span><span class="sxs-lookup"><span data-stu-id="70668-118">PARAMETERS</span></span>

### <span data-ttu-id="70668-119">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="70668-119">-BootDiagnostic</span></span>
<span data-ttu-id="70668-120">Especifica o perfil de diagnóstico de inicialização do conjunto de dimensionamento da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="70668-120">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="70668-121">-Extensão</span><span class="sxs-lookup"><span data-stu-id="70668-121">-Extension</span></span>
<span data-ttu-id="70668-122">Especifica o objeto de informações de extensão para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-122">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="70668-123">Você pode usar o cmdlet **Add-AzureRmVmssExtension** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="70668-123">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="70668-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="70668-124">-IdentityType</span></span>
<span data-ttu-id="70668-125">Especifique a identidade do conjunto de escala da máquina virtual, se configurado.</span><span class="sxs-lookup"><span data-stu-id="70668-125">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70668-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="70668-126">-LicenseType</span></span>
<span data-ttu-id="70668-127">Especifique o tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="70668-127">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="70668-128">-Local</span><span class="sxs-lookup"><span data-stu-id="70668-128">-Location</span></span>
<span data-ttu-id="70668-129">Especifica o local do Azure em que o VMSS é criado.</span><span class="sxs-lookup"><span data-stu-id="70668-129">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="70668-130">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="70668-130">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="70668-131">Especifica o objeto de perfil de rede que contém as propriedades de rede da configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-131">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="70668-132">Você pode usar o cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** para adicionar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="70668-132">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="70668-133">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="70668-133">-OsProfile</span></span>
<span data-ttu-id="70668-134">Especifica o objeto de perfil do sistema operacional que contém as propriedades do sistema operacional para a configuração do VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-134">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="70668-135">Você pode usar o cmdlet **set-AzureRmVmssOsProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="70668-135">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="70668-136">-Superprovisionamento</span><span class="sxs-lookup"><span data-stu-id="70668-136">-Overprovision</span></span>
<span data-ttu-id="70668-137">Indica se o cmdlet está supervisionando o VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-137">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="70668-138">-PlanName</span><span class="sxs-lookup"><span data-stu-id="70668-138">-PlanName</span></span>
<span data-ttu-id="70668-139">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="70668-139">Specifies the plan name.</span></span>

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

### <span data-ttu-id="70668-140">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="70668-140">-PlanProduct</span></span>
<span data-ttu-id="70668-141">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="70668-141">Specifies the plan product.</span></span>

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

### <span data-ttu-id="70668-142">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="70668-142">-PlanPromotionCode</span></span>
<span data-ttu-id="70668-143">Especifica o código promocional do plano.</span><span class="sxs-lookup"><span data-stu-id="70668-143">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="70668-144">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="70668-144">-PlanPublisher</span></span>
<span data-ttu-id="70668-145">Especifica o fornecedor do plano.</span><span class="sxs-lookup"><span data-stu-id="70668-145">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="70668-146">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="70668-146">-RecoveryPolicyMode</span></span>
<span data-ttu-id="70668-147">Especifique a política de recuperação.</span><span class="sxs-lookup"><span data-stu-id="70668-147">Specify the recovery policy.</span></span>

```yaml
Type: RecoveryMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70668-148">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="70668-148">-SinglePlacementGroup</span></span>
<span data-ttu-id="70668-149">Especifica o grupo de posicionamento único.</span><span class="sxs-lookup"><span data-stu-id="70668-149">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="70668-150">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="70668-150">-SkuCapacity</span></span>
<span data-ttu-id="70668-151">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-151">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70668-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="70668-152">-SkuName</span></span>
<span data-ttu-id="70668-153">Especifica o tamanho de todas as instâncias de VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-153">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="70668-154">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="70668-154">-SkuTier</span></span>
<span data-ttu-id="70668-155">Especifica o nível de VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-155">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="70668-156">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="70668-156">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70668-157">Oficial</span><span class="sxs-lookup"><span data-stu-id="70668-157">Standard</span></span>
- <span data-ttu-id="70668-158">Basic</span><span class="sxs-lookup"><span data-stu-id="70668-158">Basic</span></span>

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

### <span data-ttu-id="70668-159">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="70668-159">-StorageProfile</span></span>
<span data-ttu-id="70668-160">Especifica o objeto de perfil de armazenamento que contém as propriedades de disco para a configuração VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-160">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="70668-161">Você pode usar o cmdlet **set-AzureRmVmssStorageProfile** para definir esse objeto.</span><span class="sxs-lookup"><span data-stu-id="70668-161">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="70668-162">-Marca</span><span class="sxs-lookup"><span data-stu-id="70668-162">-Tag</span></span>
<span data-ttu-id="70668-163">Especifica as marcas que serão atribuídas ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="70668-163">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="70668-164">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="70668-164">-UpgradePolicyMode</span></span>
<span data-ttu-id="70668-165">Especificou o modo de uma atualização para máquinas virtuais no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="70668-165">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="70668-166">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="70668-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70668-167">Automático</span><span class="sxs-lookup"><span data-stu-id="70668-167">Automatic</span></span>
- <span data-ttu-id="70668-168">Manual</span><span class="sxs-lookup"><span data-stu-id="70668-168">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70668-169">-Confirme</span><span class="sxs-lookup"><span data-stu-id="70668-169">-Confirm</span></span>
<span data-ttu-id="70668-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70668-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70668-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70668-171">-WhatIf</span></span>
<span data-ttu-id="70668-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70668-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70668-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70668-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70668-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70668-174">CommonParameters</span></span>
<span data-ttu-id="70668-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70668-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70668-176">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70668-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70668-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70668-177">INPUTS</span></span>

### <span data-ttu-id="70668-178">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="70668-178">None</span></span>
<span data-ttu-id="70668-179">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="70668-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70668-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70668-180">OUTPUTS</span></span>

### <span data-ttu-id="70668-181">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="70668-181">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="70668-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70668-182">NOTES</span></span>

## <span data-ttu-id="70668-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70668-183">RELATED LINKS</span></span>

[<span data-ttu-id="70668-184">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="70668-184">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="70668-185">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="70668-185">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="70668-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="70668-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="70668-187">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="70668-187">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="70668-188">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="70668-188">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


