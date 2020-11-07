---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
ms.openlocfilehash: f93e05448278e2aaa70ff226a5d3618fdad0e6b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786164"
---
# <span data-ttu-id="52ca7-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52ca7-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="52ca7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="52ca7-103">Cria um VMSS.</span><span class="sxs-lookup"><span data-stu-id="52ca7-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52ca7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52ca7-104">SYNTAX</span></span>

### <span data-ttu-id="52ca7-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="52ca7-105">DefaultParameter (Default)</span></span>
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52ca7-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="52ca7-106">SimpleParameterSet</span></span>
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52ca7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52ca7-107">DESCRIPTION</span></span>
<span data-ttu-id="52ca7-108">O cmdlet **New-AzureRmVmss** cria um VMSS (conjunto de escala de máquina virtual) no Azure.</span><span class="sxs-lookup"><span data-stu-id="52ca7-108">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="52ca7-109">Esse cmdlet leva um objeto **VirtualMachineScaleSet** como entrada.</span><span class="sxs-lookup"><span data-stu-id="52ca7-109">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="52ca7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52ca7-110">EXAMPLES</span></span>

### <span data-ttu-id="52ca7-111">Exemplo 1: criar um VMSS</span><span class="sxs-lookup"><span data-stu-id="52ca7-111">Example 1: Create a VMSS</span></span>
```
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="52ca7-112">O exemplo complexo a seguir cria um VMSS.</span><span class="sxs-lookup"><span data-stu-id="52ca7-112">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="52ca7-113">O primeiro comando cria um grupo de recursos com o nome e o local especificados.</span><span class="sxs-lookup"><span data-stu-id="52ca7-113">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="52ca7-114">O segundo comando usa o cmdlet **New-AzureRmStorageAccount** para criar uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="52ca7-114">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="52ca7-115">Em seguida, o terceiro comando usa o cmdlet **Get-AzureRmStorageAccount** para obter a conta de armazenamento criada no segundo comando e armazena o resultado na variável $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="52ca7-115">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="52ca7-116">O quinto comando usa o cmdlet **New-AzureRmVirtualNetworkSubnetConfig** para criar uma sub-rede e armazena o resultado na variável chamada $SubNet.</span><span class="sxs-lookup"><span data-stu-id="52ca7-116">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="52ca7-117">O sexto comando usa o cmdlet **New-AzureRmVirtualNetwork** para criar uma rede virtual e armazena o resultado na variável chamada $VNet.</span><span class="sxs-lookup"><span data-stu-id="52ca7-117">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="52ca7-118">O sétimo comando usa o **Get-AzureRmVirtualNetwork** para obter informações sobre a rede virtual criada no sexto comando e armazena as informações na variável chamada $VNet.</span><span class="sxs-lookup"><span data-stu-id="52ca7-118">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="52ca7-119">O oitavo e nono comando usam os **novos-AzureRmPublicIpAddress** e **Get-AzureRmPublicIpAddress** para criar e obter informações desse endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="52ca7-119">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="52ca7-120">Os comandos armazenam as informações na variável chamada $PubIP.</span><span class="sxs-lookup"><span data-stu-id="52ca7-120">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="52ca7-121">O comando décimo usa o cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** para criar um balanceador de carga de front-end e armazena o resultado na variável chamada $frontend.</span><span class="sxs-lookup"><span data-stu-id="52ca7-121">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="52ca7-122">O décimo primeiro comando usa o **New-AzureRmLoadBalancerBackendAddressPoolConfig** para criar uma configuração de pool de endereços back-end e armazena o resultado na variável chamada $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="52ca7-122">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="52ca7-123">O décimo segundo comando usa o **New-AzureRmLoadBalancerProbeConfig** para criar um teste e armazena as informações da investigação na variável chamada $Probe.</span><span class="sxs-lookup"><span data-stu-id="52ca7-123">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="52ca7-124">O décimo terceiro comando usa o cmdlet **New-AzureRmLoadBalancerInboundNatPoolConfig** para criar uma configuração de pool NAT (conversão de endereços de rede) de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="52ca7-124">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="52ca7-125">O comando fourteenth usa o **New-AzureRmLoadBalancerRuleConfig** para criar uma configuração de regra de balanceador de carga e armazena o resultado na variável chamada $LBRule.</span><span class="sxs-lookup"><span data-stu-id="52ca7-125">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="52ca7-126">O comando Fifteenth usa o cmdlet **New-AzureRmLoadBalancer** para criar um balanceador de carga e armazena o resultado na variável chamada $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="52ca7-126">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="52ca7-127">O comando dezesseis usa o **Get-AzureRmLoadBalancer** para obter informações sobre o balanceador de carga que foi criado no comando Fifteenth e armazena as informações na variável chamada $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="52ca7-127">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="52ca7-128">O comando seventeenth usa o cmdlet **New-AzureRmVmssIPConfig** para criar uma configuração de IP VMSS e armazena as informações na variável chamada $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="52ca7-128">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="52ca7-129">O comando décimo oitavo usa o cmdlet **New-AzureRmVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="52ca7-129">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="52ca7-130">O comando XIX usa o cmdlet **New-AzureRmVmss** para criar o VMSS.</span><span class="sxs-lookup"><span data-stu-id="52ca7-130">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="52ca7-131">OS</span><span class="sxs-lookup"><span data-stu-id="52ca7-131">PARAMETERS</span></span>

### <span data-ttu-id="52ca7-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="52ca7-132">-AllocationMethod</span></span>
<span data-ttu-id="52ca7-133">Método de alocação para o endereço IP público do conjunto de escala (estático ou dinâmico).</span><span class="sxs-lookup"><span data-stu-id="52ca7-133">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="52ca7-134">Se nenhum valor for fornecido, a alocação será estática.</span><span class="sxs-lookup"><span data-stu-id="52ca7-134">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="52ca7-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52ca7-135">-AsJob</span></span>
<span data-ttu-id="52ca7-136">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="52ca7-136">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="52ca7-137">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="52ca7-137">-BackendPoolName</span></span>
<span data-ttu-id="52ca7-138">O nome do pool de endereços de back-end a ser usado no balanceador de carga para este conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-138">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="52ca7-139">Se nenhum valor for fornecido, um novo pool de backend será criado, com o mesmo nome do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-139">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="52ca7-140">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="52ca7-140">-BackendPort</span></span>
<span data-ttu-id="52ca7-141">Números de porta de back-end usados pelo balanceador de carga do conjunto de escala para se comunicar com VMs no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-141">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="52ca7-142">Se nenhum valor for especificado, as portas 3389 e 5985 serão usadas para VMS do Windows, e a porta 22 será usada para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="52ca7-142">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="52ca7-143">-Credential</span><span class="sxs-lookup"><span data-stu-id="52ca7-143">-Credential</span></span>
<span data-ttu-id="52ca7-144">As credenciais de administrador (nome de usuário e senha) para VMs neste conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-144">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="52ca7-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ca7-145">-DefaultProfile</span></span>
<span data-ttu-id="52ca7-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52ca7-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52ca7-147">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="52ca7-147">-DomainNameLabel</span></span>
<span data-ttu-id="52ca7-148">O rótulo de nome de domínio para o nome de domínio do Fully-Qualified público (FQDN) desse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-148">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="52ca7-149">Este é o primeiro componente do nome de domínio que é atribuído automaticamente ao conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-149">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="52ca7-150">Os nomes de domínio atribuídos automaticamente usam o formulário ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="52ca7-150">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="52ca7-151">Se nenhum valor for fornecido, o rótulo de nome de domínio padrão será a concatenação de <ScaleSetName> e <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="52ca7-151">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="52ca7-152">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="52ca7-152">-FrontendPoolName</span></span>
<span data-ttu-id="52ca7-153">O nome do pool de endereços de front-end a ser usado no balanceador de carga do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-153">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="52ca7-154">Se nenhum valor for fornecido, um novo pool de endereços de front-end será criado com o mesmo nome do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-154">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="52ca7-155">-ImageName</span><span class="sxs-lookup"><span data-stu-id="52ca7-155">-ImageName</span></span>
<span data-ttu-id="52ca7-156">O nome da imagem para VMs neste conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-156">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="52ca7-157">Se nenhum valor for fornecido, a imagem "Windows Server 2016 datacenter" será usada.</span><span class="sxs-lookup"><span data-stu-id="52ca7-157">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="52ca7-158">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="52ca7-158">-InstanceCount</span></span>
<span data-ttu-id="52ca7-159">O número de imagens de VM no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-159">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="52ca7-160">Se nenhum valor for fornecido, 2 instâncias serão criadas.</span><span class="sxs-lookup"><span data-stu-id="52ca7-160">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="52ca7-161">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="52ca7-161">-LoadBalancerName</span></span>
<span data-ttu-id="52ca7-162">O nome do balanceador de carga a ser usado com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-162">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="52ca7-163">Um novo balanceador de carga usando o mesmo nome que o conjunto de escala será criado se nenhum valor for especificado.</span><span class="sxs-lookup"><span data-stu-id="52ca7-163">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="52ca7-164">-Local</span><span class="sxs-lookup"><span data-stu-id="52ca7-164">-Location</span></span>
<span data-ttu-id="52ca7-165">O local do Azure onde esse conjunto de escala será criado.</span><span class="sxs-lookup"><span data-stu-id="52ca7-165">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="52ca7-166">Se nenhum valor for especificado, o local será inferido da localização de outros recursos referenciados nos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="52ca7-166">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="52ca7-167">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="52ca7-167">-NatBackendPort</span></span>
<span data-ttu-id="52ca7-168">Porta back-end para conversão de endereços de rede de entrada.</span><span class="sxs-lookup"><span data-stu-id="52ca7-168">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="52ca7-169">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="52ca7-169">-PublicIpAddressName</span></span>
<span data-ttu-id="52ca7-170">O nome do endereço IP público a ser usado com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-170">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="52ca7-171">Um novo IPAddress público com o mesmo nome que o conjunto de escala será criado se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="52ca7-171">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="52ca7-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52ca7-172">-ResourceGroupName</span></span>
<span data-ttu-id="52ca7-173">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="52ca7-173">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="52ca7-174">Se nenhum valor for especificado, um novo grupo de nova fonte será criado usando o mesmo nome que o conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-174">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="52ca7-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="52ca7-175">-SecurityGroupName</span></span>
<span data-ttu-id="52ca7-176">O nome do grupo de segurança de rede a ser aplicado a este conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-176">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="52ca7-177">Se nenhum valor for fornecido, um grupo de segurança de rede padrão com o mesmo nome do conjunto de escala será criado e aplicado ao conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-177">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="52ca7-178">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="52ca7-178">-SubnetAddressPrefix</span></span>
<span data-ttu-id="52ca7-179">O prefixo do endereço da sub-rede que será usada por ScaleMode.</span><span class="sxs-lookup"><span data-stu-id="52ca7-179">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="52ca7-180">As configurações de sub-rede padrão (192.168.1.0/24) serão aplicadas se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="52ca7-180">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="52ca7-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="52ca7-181">-SubnetName</span></span>
<span data-ttu-id="52ca7-182">O nome da sub-rede a ser usada com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-182">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="52ca7-183">Uma nova sub-rede será criada com o mesmo nome que o conjunto de escala, se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="52ca7-183">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="52ca7-184">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="52ca7-184">-UpgradePolicyMode</span></span>
<span data-ttu-id="52ca7-185">O modo de política de atualização para instâncias de VM neste conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-185">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="52ca7-186">A política de atualização pode especificar atualizações automáticas, manuais ou sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="52ca7-186">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="52ca7-187">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="52ca7-187">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="52ca7-188">Especifica o objeto **VirtualMachineScaleSet** que contém as propriedades do VMSS que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="52ca7-188">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="52ca7-189">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="52ca7-189">-VirtualNetworkName</span></span>
<span data-ttu-id="52ca7-190">O nome da rede virtual a ser usada com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-190">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="52ca7-191">Se nenhum valor for fornecido, uma nova rede virtual com o mesmo nome que o conjunto de escala será criada.</span><span class="sxs-lookup"><span data-stu-id="52ca7-191">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="52ca7-192">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="52ca7-192">-VMScaleSetName</span></span>
<span data-ttu-id="52ca7-193">Especifica o nome do VMSS que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="52ca7-193">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="52ca7-194">-VmSize</span><span class="sxs-lookup"><span data-stu-id="52ca7-194">-VmSize</span></span>
<span data-ttu-id="52ca7-195">O tamanho das instâncias de VM nesse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-195">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="52ca7-196">Um tamanho padrão (Standard_DS1_v2) será usado se nenhum tamanho for especificado.</span><span class="sxs-lookup"><span data-stu-id="52ca7-196">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="52ca7-197">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="52ca7-197">-VnetAddressPrefix</span></span>
<span data-ttu-id="52ca7-198">O prefixo do endereço para a rede virtual usada com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="52ca7-198">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="52ca7-199">As configurações de prefixo de endereço de rede virtual padrão (192.168.0.0/16) serão usadas se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="52ca7-199">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="52ca7-200">-Zone</span><span class="sxs-lookup"><span data-stu-id="52ca7-200">-Zone</span></span>
<span data-ttu-id="52ca7-201">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="52ca7-201">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="52ca7-202">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52ca7-202">-Confirm</span></span>
<span data-ttu-id="52ca7-203">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52ca7-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52ca7-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52ca7-204">-WhatIf</span></span>
<span data-ttu-id="52ca7-205">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52ca7-205">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="52ca7-206">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52ca7-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52ca7-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ca7-207">CommonParameters</span></span>
<span data-ttu-id="52ca7-208">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52ca7-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ca7-209">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ca7-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ca7-210">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52ca7-210">INPUTS</span></span>

### <span data-ttu-id="52ca7-211">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="52ca7-211">VirtualMachineScaleSet</span></span>
<span data-ttu-id="52ca7-212">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="52ca7-212">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="52ca7-213">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52ca7-213">OUTPUTS</span></span>

### <span data-ttu-id="52ca7-214">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="52ca7-214">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="52ca7-215">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52ca7-215">NOTES</span></span>

## <span data-ttu-id="52ca7-216">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52ca7-216">RELATED LINKS</span></span>

[<span data-ttu-id="52ca7-217">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52ca7-217">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="52ca7-218">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52ca7-218">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="52ca7-219">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52ca7-219">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="52ca7-220">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52ca7-220">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="52ca7-221">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52ca7-221">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="52ca7-222">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52ca7-222">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="52ca7-223">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52ca7-223">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


