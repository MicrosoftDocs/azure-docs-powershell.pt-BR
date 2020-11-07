---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: fc788d40cbcd807ef05be4ab43fcda4371aaa084
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776951"
---
# <span data-ttu-id="f4ed4-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f4ed4-101">New-AzVmss</span></span>

## <span data-ttu-id="f4ed4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ed4-103">Cria um VMSS.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-103">Creates a VMSS.</span></span>

## <span data-ttu-id="f4ed4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4ed4-104">SYNTAX</span></span>

### <span data-ttu-id="f4ed4-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="f4ed4-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ed4-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4ed4-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ed4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4ed4-107">DESCRIPTION</span></span>
<span data-ttu-id="f4ed4-108">O cmdlet **New-AzVmss** cria um VMSS (conjunto de escala de máquina virtual) no Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="f4ed4-109">Esse cmdlet leva um objeto **VirtualMachineScaleSet** como entrada.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-109">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="f4ed4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4ed4-110">EXAMPLES</span></span>

### <span data-ttu-id="f4ed4-111">Exemplo 1: criar um VMSS</span><span class="sxs-lookup"><span data-stu-id="f4ed4-111">Example 1: Create a VMSS</span></span>
```
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="f4ed4-112">O exemplo complexo a seguir cria um VMSS.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-112">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="f4ed4-113">O primeiro comando cria um grupo de recursos com o nome e o local especificados.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-113">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="f4ed4-114">O segundo comando usa o cmdlet **New-AzStorageAccount** para criar uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-114">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="f4ed4-115">Em seguida, o terceiro comando usa o cmdlet **Get-AzStorageAccount** para obter a conta de armazenamento criada no segundo comando e armazena o resultado na variável $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-115">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="f4ed4-116">O quinto comando usa o cmdlet **New-AzVirtualNetworkSubnetConfig** para criar uma sub-rede e armazena o resultado na variável chamada $SubNet.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-116">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="f4ed4-117">O sexto comando usa o cmdlet **New-AzVirtualNetwork** para criar uma rede virtual e armazena o resultado na variável chamada $VNet.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-117">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="f4ed4-118">O sétimo comando usa o **Get-AzVirtualNetwork** para obter informações sobre a rede virtual criada no sexto comando e armazena as informações na variável chamada $VNet.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-118">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="f4ed4-119">O oitavo e nono comando usam os **novos-AzPublicIpAddress** e **Get-AzureRmPublicIpAddress** para criar e obter informações desse endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-119">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="f4ed4-120">Os comandos armazenam as informações na variável chamada $PubIP.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-120">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="f4ed4-121">O comando décimo usa o cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** para criar um balanceador de carga de front-end e armazena o resultado na variável chamada $frontend.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-121">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="f4ed4-122">O décimo primeiro comando usa o **New-AzLoadBalancerBackendAddressPoolConfig** para criar uma configuração de pool de endereços back-end e armazena o resultado na variável chamada $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-122">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="f4ed4-123">O décimo segundo comando usa o **New-AzLoadBalancerProbeConfig** para criar um teste e armazena as informações da investigação na variável chamada $Probe.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-123">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="f4ed4-124">O décimo terceiro comando usa o cmdlet **New-AzLoadBalancerInboundNatPoolConfig** para criar uma configuração de pool NAT (conversão de endereços de rede) de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-124">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="f4ed4-125">O comando fourteenth usa o **New-AzLoadBalancerRuleConfig** para criar uma configuração de regra de balanceador de carga e armazena o resultado na variável chamada $LBRule.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-125">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="f4ed4-126">O comando Fifteenth usa o cmdlet **New-AzLoadBalancer** para criar um balanceador de carga e armazena o resultado na variável chamada $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-126">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="f4ed4-127">O comando dezesseis usa o **Get-AzLoadBalancer** para obter informações sobre o balanceador de carga que foi criado no comando Fifteenth e armazena as informações na variável chamada $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-127">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="f4ed4-128">O comando seventeenth usa o cmdlet **New-AzVmssIPConfig** para criar uma configuração de IP VMSS e armazena as informações na variável chamada $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-128">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="f4ed4-129">O comando décimo oitavo usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-129">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="f4ed4-130">O comando XIX usa o cmdlet **New-AzVmss** para criar o VMSS.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-130">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="f4ed4-131">OS</span><span class="sxs-lookup"><span data-stu-id="f4ed4-131">PARAMETERS</span></span>

### <span data-ttu-id="f4ed4-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="f4ed4-132">-AllocationMethod</span></span>
<span data-ttu-id="f4ed4-133">Método de alocação para o endereço IP público do conjunto de escala (estático ou dinâmico).</span><span class="sxs-lookup"><span data-stu-id="f4ed4-133">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="f4ed4-134">Se nenhum valor for fornecido, a alocação será estática.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-134">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4ed4-135">-AsJob</span></span>
<span data-ttu-id="f4ed4-136">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-136">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f4ed4-137">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="f4ed4-137">-BackendPoolName</span></span>
<span data-ttu-id="f4ed4-138">O nome do pool de endereços de back-end a ser usado no balanceador de carga para este conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-138">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="f4ed4-139">Se nenhum valor for fornecido, um novo pool de backend será criado, com o mesmo nome do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-139">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-140">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="f4ed4-140">-BackendPort</span></span>
<span data-ttu-id="f4ed4-141">Números de porta de back-end usados pelo balanceador de carga do conjunto de escala para se comunicar com VMs no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-141">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="f4ed4-142">Se nenhum valor for especificado, as portas 3389 e 5985 serão usadas para VMS do Windows, e a porta 22 será usada para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-142">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-143">-Credential</span><span class="sxs-lookup"><span data-stu-id="f4ed4-143">-Credential</span></span>
<span data-ttu-id="f4ed4-144">As credenciais de administrador (nome de usuário e senha) para VMs neste conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-144">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ed4-145">-DefaultProfile</span></span>
<span data-ttu-id="f4ed4-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4ed4-147">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="f4ed4-147">-DomainNameLabel</span></span>
<span data-ttu-id="f4ed4-148">O rótulo de nome de domínio para o nome de domínio do Fully-Qualified público (FQDN) desse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-148">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="f4ed4-149">Este é o primeiro componente do nome de domínio que é automaticamente assiged para o conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-149">This is the first component of the domain name that is automatically assiged to the Scale Set.</span></span> <span data-ttu-id="f4ed4-150">Os nomes de domínio atribuídos automaticamente usam o formulário ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f4ed4-150">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="f4ed4-151">Se nenhum valor for fornecido, o rótulo de nome de domínio padrão será a concatenação de <ScaleSetName> e <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="f4ed4-151">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-152">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="f4ed4-152">-FrontendPoolName</span></span>
<span data-ttu-id="f4ed4-153">O nome do pool de endereços de front-end para usein o balanceador colocalizado do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-153">The name of the frontend address pool to usein the Scale Set locad balancer.</span></span>  <span data-ttu-id="f4ed4-154">Se nenhum valor for fornecido, um novo pool de endereços de front-end será criado com o mesmo nome do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-154">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-155">-ImageName</span><span class="sxs-lookup"><span data-stu-id="f4ed4-155">-ImageName</span></span>
<span data-ttu-id="f4ed4-156">O nome da imagem para VMs neste conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-156">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="f4ed4-157">Se nenhum valor for fornecido, a imagem "Windows Server 2016 datacenter" será usada.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-157">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-158">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="f4ed4-158">-InstanceCount</span></span>
<span data-ttu-id="f4ed4-159">O número de imagens de VM no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-159">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="f4ed4-160">Se nenhum valor for fornecido, 2 instâncias serão criadas.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-160">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: Int32
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-161">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="f4ed4-161">-LoadBalancerName</span></span>
<span data-ttu-id="f4ed4-162">O nome do balanceador de carga a ser usado com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-162">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="f4ed4-163">Um novo balanceador de carga usando o mesmo nome que o conjunto de escala será criado se nenhum valor for especificado.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-163">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-164">-Local</span><span class="sxs-lookup"><span data-stu-id="f4ed4-164">-Location</span></span>
<span data-ttu-id="f4ed4-165">O local do Azure onde esse conjunto de escala será criado.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-165">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="f4ed4-166">Se nenhum valor for especificado, o local será inferido da localização de outros recursos referenciados nos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-166">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-167">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="f4ed4-167">-NatBackendPort</span></span>
<span data-ttu-id="f4ed4-168">Porta back-end para conversão de endereços de rede de entrada.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-168">Backend port for inbound network address translation.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-169">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="f4ed4-169">-PublicIpAddressName</span></span>
<span data-ttu-id="f4ed4-170">O nome do endereço IP público a ser usado com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-170">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="f4ed4-171">Um novo IPAddress público com o mesmo nome que o conjunto de escala será criado se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-171">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ed4-172">-ResourceGroupName</span></span>
<span data-ttu-id="f4ed4-173">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-173">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="f4ed4-174">Se nenhum valor for especificado, um novo grupo de nova fonte será criado usando o mesmo nome que o conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-174">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ed4-175">-SecurityGroupName</span></span>
<span data-ttu-id="f4ed4-176">O nome do grupo de segurança de rede a ser aplicado a este conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-176">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="f4ed4-177">Se nenhum valor for fornecido, um grupo de segurança de rede padrão com o mesmo nome do conjunto de escala será criado e aplicado ao conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-177">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-178">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f4ed4-178">-SubnetAddressPrefix</span></span>
<span data-ttu-id="f4ed4-179">O prefixo do endereço da sub-rede que será usada por ScaleMode.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-179">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="f4ed4-180">As configurações de sub-rede padrão (192.168.1.0/24) serão aplicadas se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-180">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f4ed4-181">-SubnetName</span></span>
<span data-ttu-id="f4ed4-182">O nome da sub-rede a ser usada com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-182">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="f4ed4-183">Uma nova sub-rede será criada com o mesmo nome que o conjunto de escala, se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-183">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-184">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="f4ed4-184">-UpgradePolicyMode</span></span>
<span data-ttu-id="f4ed4-185">O modo de política de atualização para instâncias de VM neste conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-185">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="f4ed4-186">A política de atualização pode especificar atualizações automáticas, manuais ou sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-186">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-187">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f4ed4-187">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f4ed4-188">Especifica o objeto **VirtualMachineScaleSet** que contém as propriedades do VMSS que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-188">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-189">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f4ed4-189">-VirtualNetworkName</span></span>
<span data-ttu-id="f4ed4-190">O nome da rede virtual a ser usada com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-190">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="f4ed4-191">Se nenhum valor for fornecido, uma nova rede virtual com o mesmo nome que o conjunto de escala será criada.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-191">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-192">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f4ed4-192">-VMScaleSetName</span></span>
<span data-ttu-id="f4ed4-193">Especifica o nome do VMSS que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-193">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-194">-VmSize</span><span class="sxs-lookup"><span data-stu-id="f4ed4-194">-VmSize</span></span>
<span data-ttu-id="f4ed4-195">O tamanho das instâncias de VM nesse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-195">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="f4ed4-196">Um tamanho padrão (Standard_DS1_v2) será usado se nenhum tamanho for especificado.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-196">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-197">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f4ed4-197">-VnetAddressPrefix</span></span>
<span data-ttu-id="f4ed4-198">O prefixo do endereço para a rede virtual usada com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-198">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="f4ed4-199">As configurações de prefixo de endereço de rede virtual padrão (192.168.0.0/16) serão usadas se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-199">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-200">-Zone</span><span class="sxs-lookup"><span data-stu-id="f4ed4-200">-Zone</span></span>
<span data-ttu-id="f4ed4-201">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-201">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-202">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f4ed4-202">-Confirm</span></span>
<span data-ttu-id="f4ed4-203">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-203">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ed4-204">-WhatIf</span></span>
<span data-ttu-id="f4ed4-205">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-205">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f4ed4-206">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-206">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed4-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ed4-207">CommonParameters</span></span>
<span data-ttu-id="f4ed4-208">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ed4-209">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ed4-209">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ed4-210">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4ed4-210">INPUTS</span></span>

### <span data-ttu-id="f4ed4-211">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f4ed4-211">VirtualMachineScaleSet</span></span>
<span data-ttu-id="f4ed4-212">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f4ed4-212">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="f4ed4-213">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4ed4-213">OUTPUTS</span></span>

### <span data-ttu-id="f4ed4-214">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f4ed4-214">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f4ed4-215">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4ed4-215">NOTES</span></span>

## <span data-ttu-id="f4ed4-216">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4ed4-216">RELATED LINKS</span></span>

[<span data-ttu-id="f4ed4-217">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f4ed4-217">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="f4ed4-218">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f4ed4-218">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="f4ed4-219">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f4ed4-219">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="f4ed4-220">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f4ed4-220">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="f4ed4-221">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f4ed4-221">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="f4ed4-222">Parar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f4ed4-222">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="f4ed4-223">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f4ed4-223">Update-AzVmss</span></span>](./Update-AzVmss.md)


