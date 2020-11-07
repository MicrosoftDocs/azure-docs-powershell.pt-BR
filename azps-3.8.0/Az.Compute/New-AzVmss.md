---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 914d942620eea7517b2bac635399fd7d1b3c1307
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943675"
---
# <span data-ttu-id="c8328-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8328-101">New-AzVmss</span></span>

## <span data-ttu-id="c8328-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8328-102">SYNOPSIS</span></span>
<span data-ttu-id="c8328-103">Cria um VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8328-103">Creates a VMSS.</span></span>

## <span data-ttu-id="c8328-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8328-104">SYNTAX</span></span>

### <span data-ttu-id="c8328-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="c8328-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8328-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8328-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-Priority <String>]
 [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8328-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8328-107">DESCRIPTION</span></span>
<span data-ttu-id="c8328-108">O cmdlet **New-AzVmss** cria um VMSS (conjunto de escala de máquina virtual) no Azure.</span><span class="sxs-lookup"><span data-stu-id="c8328-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="c8328-109">Use o conjunto de parâmetros simples ( `SimpleParameterSet` ) para criar rapidamente um VMSS predefinido e recursos associados.</span><span class="sxs-lookup"><span data-stu-id="c8328-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="c8328-110">Use o conjunto de parâmetros padrão ( `DefaultParameter` ) para cenários mais avançados quando precisar configurar precisamente cada componente do VMSS e cada recurso associado antes da criação.</span><span class="sxs-lookup"><span data-stu-id="c8328-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="c8328-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8328-111">EXAMPLES</span></span>

### <span data-ttu-id="c8328-112">Exemplo 1: criar um VMSS usando o **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="c8328-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="c8328-113">O comando acima cria o seguinte com o nome `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="c8328-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="c8328-114">Um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c8328-114">A Resource Group</span></span>
* <span data-ttu-id="c8328-115">Uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="c8328-115">A virtual network</span></span>
* <span data-ttu-id="c8328-116">Um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="c8328-116">A load balancer</span></span>
* <span data-ttu-id="c8328-117">Um IP público</span><span class="sxs-lookup"><span data-stu-id="c8328-117">A public IP</span></span>
* <span data-ttu-id="c8328-118">o VMSS com 2 instâncias</span><span class="sxs-lookup"><span data-stu-id="c8328-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="c8328-119">A imagem padrão selecionada para VMs no VMSS é `2016-Datacenter Windows Server` e a SKU é `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="c8328-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="c8328-120">Exemplo 2: criar um VMSS usando o **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="c8328-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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

<span data-ttu-id="c8328-121">O exemplo complexo acima cria um VMSS, seguindo uma explicação do que está acontecendo:</span><span class="sxs-lookup"><span data-stu-id="c8328-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="c8328-122">O primeiro comando cria um grupo de recursos com o nome e o local especificados.</span><span class="sxs-lookup"><span data-stu-id="c8328-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="c8328-123">O segundo comando usa o cmdlet **New-AzStorageAccount** para criar uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c8328-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="c8328-124">Em seguida, o terceiro comando usa o cmdlet **Get-AzStorageAccount** para obter a conta de armazenamento criada no segundo comando e armazena o resultado na variável $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="c8328-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="c8328-125">O quinto comando usa o cmdlet **New-AzVirtualNetworkSubnetConfig** para criar uma sub-rede e armazena o resultado na variável chamada $SubNet.</span><span class="sxs-lookup"><span data-stu-id="c8328-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="c8328-126">O sexto comando usa o cmdlet **New-AzVirtualNetwork** para criar uma rede virtual e armazena o resultado na variável chamada $VNet.</span><span class="sxs-lookup"><span data-stu-id="c8328-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="c8328-127">O sétimo comando usa o **Get-AzVirtualNetwork** para obter informações sobre a rede virtual criada no sexto comando e armazena as informações na variável chamada $VNet.</span><span class="sxs-lookup"><span data-stu-id="c8328-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="c8328-128">O oitavo e nono comando usam os **novos-AzPublicIpAddress** e **Get-AzureRmPublicIpAddress** para criar e obter informações desse endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="c8328-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="c8328-129">Os comandos armazenam as informações na variável chamada $PubIP.</span><span class="sxs-lookup"><span data-stu-id="c8328-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="c8328-130">O comando décimo usa o cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** para criar um balanceador de carga de front-end e armazena o resultado na variável chamada $frontend.</span><span class="sxs-lookup"><span data-stu-id="c8328-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="c8328-131">O décimo primeiro comando usa o **New-AzLoadBalancerBackendAddressPoolConfig** para criar uma configuração de pool de endereços back-end e armazena o resultado na variável chamada $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="c8328-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="c8328-132">O décimo segundo comando usa o **New-AzLoadBalancerProbeConfig** para criar um teste e armazena as informações da investigação na variável chamada $Probe.</span><span class="sxs-lookup"><span data-stu-id="c8328-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="c8328-133">O décimo terceiro comando usa o cmdlet **New-AzLoadBalancerInboundNatPoolConfig** para criar uma configuração de pool NAT (conversão de endereços de rede) de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="c8328-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="c8328-134">O comando fourteenth usa o **New-AzLoadBalancerRuleConfig** para criar uma configuração de regra de balanceador de carga e armazena o resultado na variável chamada $LBRule.</span><span class="sxs-lookup"><span data-stu-id="c8328-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="c8328-135">O comando Fifteenth usa o cmdlet **New-AzLoadBalancer** para criar um balanceador de carga e armazena o resultado na variável chamada $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="c8328-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="c8328-136">O comando dezesseis usa o **Get-AzLoadBalancer** para obter informações sobre o balanceador de carga que foi criado no comando Fifteenth e armazena as informações na variável chamada $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="c8328-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="c8328-137">O comando seventeenth usa o cmdlet **New-AzVmssIPConfig** para criar uma configuração de IP VMSS e armazena as informações na variável chamada $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="c8328-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="c8328-138">O comando décimo oitavo usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8328-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="c8328-139">O comando XIX usa o cmdlet **New-AzVmss** para criar o VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8328-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="c8328-140">OS</span><span class="sxs-lookup"><span data-stu-id="c8328-140">PARAMETERS</span></span>

### <span data-ttu-id="c8328-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="c8328-141">-AllocationMethod</span></span>
<span data-ttu-id="c8328-142">Método de alocação para o endereço IP público do conjunto de escala (estático ou dinâmico).</span><span class="sxs-lookup"><span data-stu-id="c8328-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="c8328-143">Se nenhum valor for fornecido, a alocação será estática.</span><span class="sxs-lookup"><span data-stu-id="c8328-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="c8328-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8328-144">-AsJob</span></span>
<span data-ttu-id="c8328-145">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="c8328-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c8328-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="c8328-146">-BackendPoolName</span></span>
<span data-ttu-id="c8328-147">O nome do pool de endereços de back-end a ser usado no balanceador de carga para este conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="c8328-148">Se nenhum valor for fornecido, um novo pool de backend será criado, com o mesmo nome do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="c8328-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c8328-149">-BackendPort</span></span>
<span data-ttu-id="c8328-150">Números de porta de back-end usados pelo balanceador de carga do conjunto de escala para se comunicar com VMs no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="c8328-151">Se nenhum valor for especificado, as portas 3389 e 5985 serão usadas para VMS do Windows, e a porta 22 será usada para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="c8328-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="c8328-152">-Credential</span><span class="sxs-lookup"><span data-stu-id="c8328-152">-Credential</span></span>
<span data-ttu-id="c8328-153">As credenciais de administrador (nome de usuário e senha) para VMs neste conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="c8328-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="c8328-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="c8328-155">Especifica o tamanho dos discos de dados em GB.</span><span class="sxs-lookup"><span data-stu-id="c8328-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="c8328-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8328-156">-DefaultProfile</span></span>
<span data-ttu-id="c8328-157">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8328-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8328-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="c8328-158">-DomainNameLabel</span></span>
<span data-ttu-id="c8328-159">O rótulo de nome de domínio para o nome de domínio do Fully-Qualified público (FQDN) desse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="c8328-160">Este é o primeiro componente do nome de domínio que é atribuído automaticamente ao conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="c8328-161">Os nomes de domínio atribuídos automaticamente usam o formulário ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="c8328-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="c8328-162">Se nenhum valor for fornecido, o rótulo de nome de domínio padrão será a concatenação de <ScaleSetName> e <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="c8328-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="c8328-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="c8328-163">-EnableUltraSSD</span></span>
<span data-ttu-id="c8328-164">Use discos UltraSSD para as VMs no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="c8328-165">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8328-165">-EvictionPolicy</span></span>
<span data-ttu-id="c8328-166">A política de remoção para o conjunto de escala da máquina virtual de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="c8328-166">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="c8328-167">Somente os valores com suporte são ' DEALLOCATE ' e ' Delete '.</span><span class="sxs-lookup"><span data-stu-id="c8328-167">Only supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="c8328-168">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="c8328-168">-FrontendPoolName</span></span>
<span data-ttu-id="c8328-169">O nome do pool de endereços de front-end a ser usado no balanceador de carga do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-169">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="c8328-170">Se nenhum valor for fornecido, um novo pool de endereços de front-end será criado com o mesmo nome do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-170">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="c8328-171">-ImageName</span><span class="sxs-lookup"><span data-stu-id="c8328-171">-ImageName</span></span>
<span data-ttu-id="c8328-172">O nome da imagem para VMs neste conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-172">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="c8328-173">Se nenhum valor for fornecido, a imagem "Windows Server 2016 datacenter" será usada.</span><span class="sxs-lookup"><span data-stu-id="c8328-173">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="c8328-174">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="c8328-174">-InstanceCount</span></span>
<span data-ttu-id="c8328-175">O número de imagens de VM no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-175">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="c8328-176">Se nenhum valor for fornecido, 2 instâncias serão criadas.</span><span class="sxs-lookup"><span data-stu-id="c8328-176">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="c8328-177">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="c8328-177">-LoadBalancerName</span></span>
<span data-ttu-id="c8328-178">O nome do balanceador de carga a ser usado com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-178">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="c8328-179">Um novo balanceador de carga usando o mesmo nome que o conjunto de escala será criado se nenhum valor for especificado.</span><span class="sxs-lookup"><span data-stu-id="c8328-179">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="c8328-180">-Local</span><span class="sxs-lookup"><span data-stu-id="c8328-180">-Location</span></span>
<span data-ttu-id="c8328-181">O local do Azure onde esse conjunto de escala será criado.</span><span class="sxs-lookup"><span data-stu-id="c8328-181">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="c8328-182">Se nenhum valor for especificado, o local será inferido da localização de outros recursos referenciados nos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c8328-182">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="c8328-183">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="c8328-183">-MaxPrice</span></span>
<span data-ttu-id="c8328-184">O preço máximo da cobrança de um conjunto de escala de máquina virtual de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="c8328-184">The max price of the billing of a low priority virtual machine scale set.</span></span>

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

### <span data-ttu-id="c8328-185">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="c8328-185">-NatBackendPort</span></span>
<span data-ttu-id="c8328-186">Porta back-end para conversão de endereços de rede de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8328-186">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="c8328-187">-Priority</span><span class="sxs-lookup"><span data-stu-id="c8328-187">-Priority</span></span>
<span data-ttu-id="c8328-188">A prioridade da máquina virtual no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-188">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="c8328-189">Somente os valores com suporte são ' regular ', ' spot ' e ' baixo '.</span><span class="sxs-lookup"><span data-stu-id="c8328-189">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="c8328-190">' Regular ' é para a máquina virtual normal.</span><span class="sxs-lookup"><span data-stu-id="c8328-190">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="c8328-191">' Spot ' é para máquina virtual Spot.</span><span class="sxs-lookup"><span data-stu-id="c8328-191">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="c8328-192">' Low ' também é para máquina virtual Spot, mas é substituído por ' spot '.</span><span class="sxs-lookup"><span data-stu-id="c8328-192">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="c8328-193">Use ' spot ' em vez de ' baixo '.</span><span class="sxs-lookup"><span data-stu-id="c8328-193">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="c8328-194">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="c8328-194">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="c8328-195">A ID do recurso do grupo de posicionamento de proximidade a ser usado com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-195">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="c8328-196">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="c8328-196">-PublicIpAddressName</span></span>
<span data-ttu-id="c8328-197">O nome do endereço IP público a ser usado com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-197">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="c8328-198">Um novo IPAddress público com o mesmo nome que o conjunto de escala será criado se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="c8328-198">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="c8328-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8328-199">-ResourceGroupName</span></span>
<span data-ttu-id="c8328-200">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="c8328-200">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="c8328-201">Se nenhum valor for especificado, um novo grupo de nova fonte será criado usando o mesmo nome que o conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-201">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="c8328-202">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="c8328-202">-ScaleInPolicy</span></span>
<span data-ttu-id="c8328-203">As regras a serem seguidas quando o dimensionamento for um conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c8328-203">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="c8328-204">Os valores possíveis são: "default", "OldestVM" e "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="c8328-204">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="c8328-205">"Padrão" quando um conjunto de escala da máquina virtual é dimensionado, o conjunto de escalas primeiro será balanceado entre zonas se for um conjunto de escala zonas.</span><span class="sxs-lookup"><span data-stu-id="c8328-205">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="c8328-206">Em seguida, ele será balanceado em domínios de falha o mais longe possível.</span><span class="sxs-lookup"><span data-stu-id="c8328-206">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="c8328-207">Em cada domínio de falha, as máquinas virtuais escolhidas para remoção serão as mais recentes que não estão protegidas do Scale-in.</span><span class="sxs-lookup"><span data-stu-id="c8328-207">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="c8328-208">"OldestVM" quando um conjunto de dimensionamento de máquina virtual está sendo ampliado, as máquinas virtuais mais antigas que não estão protegidas do Scale-in serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="c8328-208">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="c8328-209">Para conjuntos de escala da máquina virtual zonada, o conjunto de escala será balanceado primeiro entre zonas.</span><span class="sxs-lookup"><span data-stu-id="c8328-209">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="c8328-210">Em cada zona, as máquinas virtuais mais antigas que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="c8328-210">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="c8328-211">"NewestVM" quando um conjunto de dimensionamento de máquina virtual está sendo ampliado, as máquinas virtuais mais recentes que não estão protegidas do Scale-in serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="c8328-211">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="c8328-212">Para conjuntos de escala da máquina virtual zonada, o conjunto de escala será balanceado primeiro entre zonas.</span><span class="sxs-lookup"><span data-stu-id="c8328-212">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="c8328-213">Em cada zona, as máquinas virtuais mais recentes que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="c8328-213">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="c8328-214">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="c8328-214">-SecurityGroupName</span></span>
<span data-ttu-id="c8328-215">O nome do grupo de segurança de rede a ser aplicado a este conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-215">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="c8328-216">Se nenhum valor for fornecido, um grupo de segurança de rede padrão com o mesmo nome do conjunto de escala será criado e aplicado ao conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-216">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="c8328-217">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c8328-217">-SinglePlacementGroup</span></span>
<span data-ttu-id="c8328-218">Use isso para criar o conjunto de escala em um único grupo de posicionamento, o padrão é vários grupos</span><span class="sxs-lookup"><span data-stu-id="c8328-218">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="c8328-219">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="c8328-219">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="c8328-220">Especifica que as extensões não são executadas nas VMs extras superprovisionadas.</span><span class="sxs-lookup"><span data-stu-id="c8328-220">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="c8328-221">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c8328-221">-SubnetAddressPrefix</span></span>
<span data-ttu-id="c8328-222">O prefixo do endereço da sub-rede que será usada por ScaleMode.</span><span class="sxs-lookup"><span data-stu-id="c8328-222">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="c8328-223">As configurações de sub-rede padrão (192.168.1.0/24) serão aplicadas se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="c8328-223">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="c8328-224">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c8328-224">-SubnetName</span></span>
<span data-ttu-id="c8328-225">O nome da sub-rede a ser usada com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-225">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="c8328-226">Uma nova sub-rede será criada com o mesmo nome que o conjunto de escala, se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="c8328-226">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="c8328-227">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c8328-227">-SystemAssignedIdentity</span></span>
<span data-ttu-id="c8328-228">Se o parâmetro estiver presente, então a (s) VM (s) no conjunto de escala (is) é atribuída a uma identidade do sistema gerenciada que é gerada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c8328-228">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="c8328-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="c8328-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="c8328-230">O modo de política de atualização para instâncias de VM neste conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-230">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="c8328-231">A política de atualização pode especificar atualizações automáticas, manuais ou sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="c8328-231">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="c8328-232">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c8328-232">-UserAssignedIdentity</span></span>
<span data-ttu-id="c8328-233">O nome de uma identidade de serviço gerenciado que deve ser atribuída à (s) VM (s) no conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-233">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="c8328-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c8328-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c8328-235">Especifica o objeto **VirtualMachineScaleSet** que contém as propriedades do VMSS que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="c8328-235">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c8328-236">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c8328-236">-VirtualNetworkName</span></span>
<span data-ttu-id="c8328-237">O nome da rede virtual a ser usada com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-237">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="c8328-238">Se nenhum valor for fornecido, uma nova rede virtual com o mesmo nome que o conjunto de escala será criada.</span><span class="sxs-lookup"><span data-stu-id="c8328-238">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="c8328-239">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c8328-239">-VMScaleSetName</span></span>
<span data-ttu-id="c8328-240">Especifica o nome do VMSS que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="c8328-240">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c8328-241">-VmSize</span><span class="sxs-lookup"><span data-stu-id="c8328-241">-VmSize</span></span>
<span data-ttu-id="c8328-242">O tamanho das instâncias de VM nesse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-242">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="c8328-243">Um tamanho padrão (Standard_DS1_v2) será usado se nenhum tamanho for especificado.</span><span class="sxs-lookup"><span data-stu-id="c8328-243">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="c8328-244">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c8328-244">-VnetAddressPrefix</span></span>
<span data-ttu-id="c8328-245">O prefixo do endereço para a rede virtual usada com esse conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c8328-245">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="c8328-246">As configurações de prefixo de endereço de rede virtual padrão (192.168.0.0/16) serão usadas se nenhum valor for fornecido.</span><span class="sxs-lookup"><span data-stu-id="c8328-246">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="c8328-247">-Zone</span><span class="sxs-lookup"><span data-stu-id="c8328-247">-Zone</span></span>
<span data-ttu-id="c8328-248">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="c8328-248">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="c8328-249">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c8328-249">-Confirm</span></span>
<span data-ttu-id="c8328-250">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8328-250">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8328-251">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8328-251">-WhatIf</span></span>
<span data-ttu-id="c8328-252">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8328-252">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8328-253">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8328-253">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8328-254">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8328-254">CommonParameters</span></span>
<span data-ttu-id="c8328-255">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8328-255">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8328-256">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8328-256">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8328-257">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8328-257">INPUTS</span></span>

### <span data-ttu-id="c8328-258">System. String</span><span class="sxs-lookup"><span data-stu-id="c8328-258">System.String</span></span>

### <span data-ttu-id="c8328-259">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c8328-259">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="c8328-260">System. Collections. Generic. List ' 1 [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c8328-260">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c8328-261">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8328-261">OUTPUTS</span></span>

### <span data-ttu-id="c8328-262">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c8328-262">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c8328-263">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8328-263">NOTES</span></span>

## <span data-ttu-id="c8328-264">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8328-264">RELATED LINKS</span></span>

[<span data-ttu-id="c8328-265">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8328-265">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="c8328-266">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8328-266">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="c8328-267">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8328-267">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="c8328-268">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8328-268">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="c8328-269">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8328-269">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="c8328-270">Parar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8328-270">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="c8328-271">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8328-271">Update-AzVmss</span></span>](./Update-AzVmss.md)


