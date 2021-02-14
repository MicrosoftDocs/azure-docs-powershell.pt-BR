---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111130"
---
# <span data-ttu-id="8d3d0-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d3d0-101">New-AzVmss</span></span>

## <span data-ttu-id="8d3d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="8d3d0-103">Cria um VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-103">Creates a VMSS.</span></span>

## <span data-ttu-id="8d3d0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d3d0-104">SYNTAX</span></span>

### <span data-ttu-id="8d3d0-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8d3d0-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d3d0-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d3d0-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d3d0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d3d0-107">DESCRIPTION</span></span>
<span data-ttu-id="8d3d0-108">O **cmdlet New-AzVmss** cria um VMSS (Virtual Machine Scale Set) no Azure.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="8d3d0-109">Use o conjunto de parâmetros simples ( ) para criar rapidamente um `SimpleParameterSet` VMSS pré-definido e recursos associados.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="8d3d0-110">Use o conjunto de parâmetros padrão ( ) para cenários mais avançados quando precisar configurar com precisão cada componente do VMSS e cada recurso associado antes da `DefaultParameter` criação.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="8d3d0-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8d3d0-111">EXAMPLES</span></span>

### <span data-ttu-id="8d3d0-112">Exemplo 1: Criar um VMSS usando o **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="8d3d0-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="8d3d0-113">O comando acima cria o seguinte com o `$vmssName` nome:</span><span class="sxs-lookup"><span data-stu-id="8d3d0-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="8d3d0-114">Um Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8d3d0-114">A Resource Group</span></span>
* <span data-ttu-id="8d3d0-115">Uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="8d3d0-115">A virtual network</span></span>
* <span data-ttu-id="8d3d0-116">Um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="8d3d0-116">A load balancer</span></span>
* <span data-ttu-id="8d3d0-117">Um IP público</span><span class="sxs-lookup"><span data-stu-id="8d3d0-117">A public IP</span></span>
* <span data-ttu-id="8d3d0-118">O VMSS com 2 instâncias</span><span class="sxs-lookup"><span data-stu-id="8d3d0-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="8d3d0-119">A imagem padrão escolhida para as VMs no VMSS é `2016-Datacenter Windows Server` e a SKU é `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="8d3d0-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="8d3d0-120">Exemplo 2: Criar um VMSS usando o **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="8d3d0-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
```powershell
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
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
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

<span data-ttu-id="8d3d0-121">O exemplo complexo acima cria um VMSS, a seguir está uma explicação do que está acontecendo:</span><span class="sxs-lookup"><span data-stu-id="8d3d0-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="8d3d0-122">O primeiro comando cria um grupo de recursos com o nome e o local especificados.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="8d3d0-123">O segundo comando usa o cmdlet **New-AzStorageAccount** para criar uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="8d3d0-124">O terceiro comando usa o cmdlet **Get-AzStorageAccount** para criar a conta de armazenamento no segundo comando e armazena o resultado na variável $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="8d3d0-125">O quinto comando usa o cmdlet **New-AzVirtualNetworkSubnetConfig** para criar uma sub-rede e armazena o resultado na variável chamada $SubNet.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="8d3d0-126">O sexto comando usa o cmdlet **New-AzVirtualNetwork** para criar uma rede virtual e armazena o resultado na variável chamada $VNet.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="8d3d0-127">O sétimo comando usa **a Get-AzVirtualNetwork** para obter informações sobre a rede virtual criada no sexto comando e armazena as informações na variável chamada $VNet.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="8d3d0-128">O oitavo e nono comando usa o **New-AzPublicIpAddress** e **Get- AzureRmPublicIpAddress** para criar e obter informações desse endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="8d3d0-129">Os comandos armazenam as informações na variável chamada $PubIP.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="8d3d0-130">O décimo comando usa o cmdlet **New- AzureRmLoadBalancerFrontendIpConfig** para criar um balanceador de carga frontend e armazena o resultado na variável chamada $Frontend.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="8d3d0-131">O décimo primeiro comando usa o **Novo-AzLoadBalancerBackendAddressPoolConfig** para criar uma configuração de pool de endereços back-end e armazena o resultado na variável chamada $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="8d3d0-132">O décimo segundo comando usa o **Novo-AzLoadBalancerProbeConfig** para criar um ataque e armazena as informações de ataque na variável chamada $Probe.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="8d3d0-133">O décimo terceiro comando usa o cmdlet **New-AzLoadBalancerInboundNatPoolConfig** para criar uma configuração de pool nat (conversão de endereço de rede de entrada) do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="8d3d0-134">O décimo quarto comando usa o **Novo-AzLoadBalancerRuleConfig** para criar uma configuração de regra de balanceador de carga e armazena o resultado na variável chamada $LBRule.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="8d3d0-135">O décimo quinto comando usa o cmdlet **New-AzLoadBalancer** para criar um balanceador de carga e armazena o resultado na variável chamada $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="8d3d0-136">O décimo sexto comando usa o **Get-AzLoadBalancer** para obter informações sobre o balanceador de carga que foi criado no décimo quinto comando e armazena as informações na variável chamada $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="8d3d0-137">O décimo sétimo comando usa o cmdlet **New-AzVmsSIPConfig** para criar uma configuração IP do VMSS e armazena as informações na variável chamada $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="8d3d0-138">O décimo oitavo comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="8d3d0-139">O comando de silêncio usa o cmdlet **New-AzVmss** para criar o VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="8d3d0-140">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d3d0-140">PARAMETERS</span></span>

### <span data-ttu-id="8d3d0-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="8d3d0-141">-AllocationMethod</span></span>
<span data-ttu-id="8d3d0-142">Método de alocação para o Endereço IP Público do Conjunto de Escalas (Estático ou Dinâmico).</span><span class="sxs-lookup"><span data-stu-id="8d3d0-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="8d3d0-143">Se nenhum valor for fornecido, a alocação será estática.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-143">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d3d0-144">-AsJob</span></span>
<span data-ttu-id="8d3d0-145">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8d3d0-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="8d3d0-146">-BackendPoolName</span></span>
<span data-ttu-id="8d3d0-147">O nome do pool de endereços de back-end a ser usado no balanceador de carga para este Conjunto de Escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="8d3d0-148">Se nenhum valor for fornecido, um novo pool de back-end será criado com o mesmo nome do Conjunto de Escala.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="8d3d0-149">-BackendPort</span></span>
<span data-ttu-id="8d3d0-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="8d3d0-151">Se nenhum valor for especificado, as portas 3389 e 5985 serão usadas para vMS do Windows e a porta 22 será usada para VMs do Linux.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-152">-Credencial</span><span class="sxs-lookup"><span data-stu-id="8d3d0-152">-Credential</span></span>
<span data-ttu-id="8d3d0-153">As credenciais de administrador (nome de usuário e senha) para VMs neste Conjunto de Escala.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="8d3d0-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="8d3d0-155">Especifica os tamanhos de discos de dados em GB.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-155">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d3d0-156">-DefaultProfile</span></span>
<span data-ttu-id="8d3d0-157">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d3d0-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="8d3d0-158">-DomainNameLabel</span></span>
<span data-ttu-id="8d3d0-159">O rótulo de nome de domínio para o Fully-Qualified de domínio público (FQDN) para este Conjunto de Escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="8d3d0-160">Este é o primeiro componente do nome de domínio atribuído automaticamente ao Conjunto de Escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="8d3d0-161">Os nomes de domínio atribuídos automaticamente usam o formulário ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="8d3d0-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="8d3d0-162">Se nenhum valor for fornecido, o rótulo de nome de domínio padrão será a concatenação <ScaleSetName> de e <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="8d3d0-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-163">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="8d3d0-163">-EnableUltraSSD</span></span>
<span data-ttu-id="8d3d0-164">Use discos UltraSSD para VMs no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="8d3d0-165">-EncryptionAtHost</span></span>
<span data-ttu-id="8d3d0-166">Esse parâmetro habilitará a criptografia para todos os discos, incluindo o disco Resource/Temp no próprio host.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="8d3d0-167">Padrão: a Criptografia no host será desabilitada, a menos que essa propriedade seja definida como verdadeira para o recurso.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-168">-EsporáciaPolicy</span><span class="sxs-lookup"><span data-stu-id="8d3d0-168">-EvictionPolicy</span></span>
<span data-ttu-id="8d3d0-169">A política de desapropriação para o conjunto de escala de máquina virtual de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="8d3d0-170">Somente valores com suporte são 'Deallocate' e 'Delete'.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="8d3d0-171">-FrontendPoolName</span></span>
<span data-ttu-id="8d3d0-172">O nome do pool de endereços frontend a ser usado no balanceador de carga de Conjunto de Escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="8d3d0-173">Se nenhum valor for fornecido, um novo Pool de Endereços Frontend será criado com o mesmo nome do conjunto de escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="8d3d0-174">-HostGroupId</span></span>
<span data-ttu-id="8d3d0-175">Especifica o grupo de host dedicado em que o conjunto de escala de máquina virtual irá residir.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-176">-NomedaImagem</span><span class="sxs-lookup"><span data-stu-id="8d3d0-176">-ImageName</span></span>
<span data-ttu-id="8d3d0-177">O nome da imagem para VMs neste Conjunto de Escala.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="8d3d0-178">Se nenhum valor for fornecido, a imagem "DataCenter do Windows Server 2016" será usada.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="8d3d0-179">-InstanceCount</span></span>
<span data-ttu-id="8d3d0-180">O número de imagens VM no Conjunto de Escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="8d3d0-181">Se nenhum valor for fornecido, duas instâncias serão criadas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-181">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="8d3d0-182">-LoadBalancerName</span></span>
<span data-ttu-id="8d3d0-183">O nome do balanceador de carga a ser usado com este Conjunto de Escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="8d3d0-184">Um novo balanceador de carga usando o mesmo nome do Conjunto de Escalas será criado se nenhum valor for especificado.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-185">-Local</span><span class="sxs-lookup"><span data-stu-id="8d3d0-185">-Location</span></span>
<span data-ttu-id="8d3d0-186">O local do Azure onde este Conjunto de Escalas será criado.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="8d3d0-187">Se nenhum valor for especificado, o local será inferido a partir da localização de outros recursos referenciados nos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="8d3d0-188">-MaxPrice</span></span>
<span data-ttu-id="8d3d0-189">O preço máximo da cobrança de um conjunto de escala de máquina virtual de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="8d3d0-190">-NatBackendPort</span></span>
<span data-ttu-id="8d3d0-191">Porta back-end para tradução de endereço de rede de entrada.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-191">Backend port for inbound network address translation.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="8d3d0-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="8d3d0-193">Contagem de domínios de falha para cada grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-193">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-194">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="8d3d0-194">-Priority</span></span>
<span data-ttu-id="8d3d0-195">A prioridade para a máquina virtual no conjunto de escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="8d3d0-196">Somente valores com suporte são 'Regular', 'Spot' e 'Baixo'.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="8d3d0-197">'Regular' é para máquina virtual normal.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="8d3d0-198">'Spot' é para uma máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="8d3d0-199">'Baixo' também é para uma máquina virtual local, mas é substituída por "Spot".</span><span class="sxs-lookup"><span data-stu-id="8d3d0-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="8d3d0-200">Use "Spot" em vez de "Baixo".</span><span class="sxs-lookup"><span data-stu-id="8d3d0-200">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="8d3d0-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="8d3d0-202">A ID do recurso do Grupo de Posicionamento de Proximidade a ser usado com esse conjunto de escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-203">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="8d3d0-203">-PublicIpAddressName</span></span>
<span data-ttu-id="8d3d0-204">O nome do Endereço IP público a ser usado com esse conjunto de escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="8d3d0-205">Um novo IPAddress Público com o mesmo nome do Conjunto de Escalas será criado se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d3d0-206">-ResourceGroupName</span></span>
<span data-ttu-id="8d3d0-207">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="8d3d0-208">Se nenhum valor for especificado, um novo Grupo de Recursos será criado usando o mesmo nome do Conjunto de Escala.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="8d3d0-209">-ScaleInPolicy</span></span>
<span data-ttu-id="8d3d0-210">As regras a serem seguidas ao dimensionar um conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="8d3d0-211">Os valores possíveis são: 'Padrão', 'OldestVM' e 'NewestVM'.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="8d3d0-212">"Padrão" quando um conjunto de escalas de máquina virtual é dimensionado, o conjunto de escalas primeiro será equilibrado entre zonas se for um conjunto de escalas zonais.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="8d3d0-213">Em seguida, ele será equilibrado em todos os Domínios de Falha o mais longe possível.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="8d3d0-214">Em cada Domínio de Falha, as máquinas virtuais escolhidas para remoção serão as mais novas que não estão protegidas da escala.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="8d3d0-215">'OldestVM' quando um conjunto de escalas de máquina virtual está sendo dimensionado, as máquinas virtuais mais antigas que não estão protegidas contra escalas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="8d3d0-216">Para conjuntos de escala de computador virtual zonal, o conjunto de escalas será primeiro equilibrado entre zonas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="8d3d0-217">Em cada zona, as máquinas virtuais mais antigas que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="8d3d0-218">'NewestVM' quando um conjunto de escalas de máquina virtual estiver sendo dimensionado, as máquinas virtuais mais novas que não estão protegidas contra escalas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="8d3d0-219">Para conjuntos de escala de computador virtual zonal, o conjunto de escalas será primeiro equilibrado entre zonas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="8d3d0-220">Em cada zona, as máquinas virtuais mais novas que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="8d3d0-221">-SecurityGroupName</span></span>
<span data-ttu-id="8d3d0-222">O nome do grupo de segurança de rede a ser aplicado a este Conjunto de Escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="8d3d0-223">Se nenhum valor for fornecido, um grupo de segurança de rede padrão com o mesmo nome do Conjunto de Escalas será criado e aplicado ao Conjunto de Escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8d3d0-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="8d3d0-225">Use isto para criar o conjunto de escalas em um único grupo de posicionamento, o padrão é vários grupos</span><span class="sxs-lookup"><span data-stu-id="8d3d0-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-226">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="8d3d0-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="8d3d0-227">Especifica que as extensões não são executados em VMs extra sobreprovisionadas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-228">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8d3d0-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="8d3d0-229">O prefixo de endereço da Sub-rede que este ScaleSet usará.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="8d3d0-230">As configurações padrão da Sub-rede (192.168.1.0/24) serão aplicadas se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-231">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="8d3d0-231">-SubnetName</span></span>
<span data-ttu-id="8d3d0-232">O nome da sub-rede a ser usada com este Conjunto de Escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="8d3d0-233">Uma nova Sub-rede será criada com o mesmo nome do Conjunto de Escala se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8d3d0-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="8d3d0-235">Se o parâmetro estiver presente, as VMs no conjunto de escalas serão atribuídas a uma identidade de sistema gerenciada gerada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="8d3d0-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="8d3d0-237">O modo de política de atualização para instâncias de VM neste Conjunto de Escala.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="8d3d0-238">A política de atualização pode especificar atualizações automáticas, manuais ou de rolagem.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-239">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8d3d0-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="8d3d0-240">O nome de uma identidade de serviço gerenciada que deve ser atribuída às VMs no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d3d0-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8d3d0-242">Especifica o **objeto VirtualMachineScaleSet** que contém as propriedades do VMSS que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8d3d0-243">-VirtualNetworkName</span></span>
<span data-ttu-id="8d3d0-244">O nome para a Rede Virtual a ser usada com esse conjunto de escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="8d3d0-245">Se nenhum valor for fornecido, uma nova rede virtual com o mesmo nome do Conjunto de Escalas será criada.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8d3d0-246">-VMScaleSetName</span></span>
<span data-ttu-id="8d3d0-247">Especifica o nome do VMSS que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="8d3d0-248">-VmSize</span></span>
<span data-ttu-id="8d3d0-249">O tamanho das instâncias de VM neste conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="8d3d0-250">Um tamanho padrão (Standard_DS1_v2) será usado se nenhum Tamanho for especificado.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8d3d0-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="8d3d0-252">O prefixo de endereço para a rede virtual usada com este Conjunto de Escalas.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="8d3d0-253">As configurações padrão de prefixo de endereço de rede virtual (192.168.0.0/16) serão usadas se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-254">-Zona</span><span class="sxs-lookup"><span data-stu-id="8d3d0-254">-Zone</span></span>
<span data-ttu-id="8d3d0-255">Uma lista de zonas de disponibilidade que denotam o IP alocado para o recurso precisa vir.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="8d3d0-256">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8d3d0-256">-Confirm</span></span>
<span data-ttu-id="8d3d0-257">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-257">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d3d0-258">-WhatIf</span></span>
<span data-ttu-id="8d3d0-259">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d3d0-260">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-260">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3d0-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d3d0-261">CommonParameters</span></span>
<span data-ttu-id="8d3d0-262">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d3d0-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d3d0-263">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d3d0-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d3d0-264">Entradas</span><span class="sxs-lookup"><span data-stu-id="8d3d0-264">INPUTS</span></span>

### <span data-ttu-id="8d3d0-265">System.String</span><span class="sxs-lookup"><span data-stu-id="8d3d0-265">System.String</span></span>

### <span data-ttu-id="8d3d0-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d3d0-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8d3d0-267">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8d3d0-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8d3d0-268">Saídas</span><span class="sxs-lookup"><span data-stu-id="8d3d0-268">OUTPUTS</span></span>

### <span data-ttu-id="8d3d0-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d3d0-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8d3d0-270">Notas</span><span class="sxs-lookup"><span data-stu-id="8d3d0-270">NOTES</span></span>

## <span data-ttu-id="8d3d0-271">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d3d0-271">RELATED LINKS</span></span>

[<span data-ttu-id="8d3d0-272">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d3d0-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="8d3d0-273">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d3d0-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="8d3d0-274">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d3d0-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="8d3d0-275">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d3d0-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="8d3d0-276">Iniciar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d3d0-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="8d3d0-277">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d3d0-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="8d3d0-278">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d3d0-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


