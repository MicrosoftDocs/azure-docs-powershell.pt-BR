---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281804"
---
# <span data-ttu-id="5748d-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="5748d-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="5748d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5748d-102">SYNOPSIS</span></span>
<span data-ttu-id="5748d-103">Cria uma configuração de IP para uma interface de rede de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="5748d-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="5748d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5748d-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5748d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5748d-105">DESCRIPTION</span></span>
<span data-ttu-id="5748d-106">O cmdlet **New-AzVmssIpConfig** cria um objeto de configuração de IP para uma interface de rede de um conjunto de escala de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5748d-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="5748d-107">Especifique a configuração deste cmdlet como o parâmetro *IPConfiguration* do cmdlet Add-AzVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5748d-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="5748d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5748d-108">EXAMPLES</span></span>

### <span data-ttu-id="5748d-109">Exemplo 1: criar um objeto de configuração de IP para uma interface VMSS</span><span class="sxs-lookup"><span data-stu-id="5748d-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="5748d-110">Esse comando cria um objeto de configuração de IP chamado ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="5748d-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="5748d-111">O comando usa uma ID de sub-rede previamente definida armazenada em $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="5748d-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="5748d-112">O comando armazena as definições de configuração na variável $IPConfiguration para uso posterior com **Add-AzVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5748d-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="5748d-113">Exemplo 2: criar um objeto de configuração de IP que inclua as configurações de pool NAT</span><span class="sxs-lookup"><span data-stu-id="5748d-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="5748d-114">Esse comando cria um objeto de configuração de IP chamado ContosoVmssInterface03 e, em seguida, armazena-o na variável $IPConfiguration para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="5748d-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="5748d-115">O comando usa uma ID de sub-rede previamente definida armazenada em $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="5748d-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="5748d-116">O comando armazena as definições de configuração na variável $IPConfiguration para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="5748d-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="5748d-117">O comando especifica valores para os parâmetros *LoadBalancerInboundNatPoolsId* e *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="5748d-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="5748d-118">OS</span><span class="sxs-lookup"><span data-stu-id="5748d-118">PARAMETERS</span></span>

### <span data-ttu-id="5748d-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="5748d-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="5748d-120">Especifica uma matriz de referências a pools de endereços de back-end de balanceadores de carga.</span><span class="sxs-lookup"><span data-stu-id="5748d-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="5748d-121">Um conjunto de escala pode fazer referência A pools de endereços de back-end de um balanceador de carga público e um interno.</span><span class="sxs-lookup"><span data-stu-id="5748d-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="5748d-122">Vários conjuntos de escala não podem usar o mesmo balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="5748d-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5748d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5748d-123">-DefaultProfile</span></span>
<span data-ttu-id="5748d-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5748d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5748d-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="5748d-125">-DnsSetting</span></span>
<span data-ttu-id="5748d-126">As configurações de DNS a serem aplicadas nos endereços publicIP.</span><span class="sxs-lookup"><span data-stu-id="5748d-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="5748d-127">O rótulo do nome do domínio das configurações de DNS a ser aplicado aos endereços publicIP.</span><span class="sxs-lookup"><span data-stu-id="5748d-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="5748d-128">A concatenação do rótulo de nome de domínio e do índice de VM será os rótulos de nome de domínio dos recursos de endereço IP público que serão criados.</span><span class="sxs-lookup"><span data-stu-id="5748d-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5748d-129">-ID</span><span class="sxs-lookup"><span data-stu-id="5748d-129">-Id</span></span>
<span data-ttu-id="5748d-130">Especifica uma ID.</span><span class="sxs-lookup"><span data-stu-id="5748d-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="5748d-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="5748d-131">-IpTag</span></span>
<span data-ttu-id="5748d-132">Especifica uma matriz de objetos de marca IP.</span><span class="sxs-lookup"><span data-stu-id="5748d-132">Specifies an array of Ip Tag objects.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5748d-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="5748d-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="5748d-134">Especifica uma matriz de referências a pools de conversão de endereços de rede (NAT) de entrada dos balanceadores de carga.</span><span class="sxs-lookup"><span data-stu-id="5748d-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="5748d-135">Um conjunto de escala pode fazer referência A pools de NAT de entrada de um balanceador de carga público e um interno.</span><span class="sxs-lookup"><span data-stu-id="5748d-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="5748d-136">Vários conjuntos de escala não podem usar o mesmo balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="5748d-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5748d-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="5748d-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="5748d-138">Especifica uma matriz de referências a pools de NAT de entrada dos balanceadores de carga.</span><span class="sxs-lookup"><span data-stu-id="5748d-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="5748d-139">Um conjunto de escala pode fazer referência A pools de NAT de entrada de um balanceador de carga público e um interno.</span><span class="sxs-lookup"><span data-stu-id="5748d-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="5748d-140">Vários conjuntos de escala não podem usar o mesmo balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="5748d-140">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5748d-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="5748d-141">-Name</span></span>
<span data-ttu-id="5748d-142">Especifica o nome da configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="5748d-142">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5748d-143">-Principal</span><span class="sxs-lookup"><span data-stu-id="5748d-143">-Primary</span></span>
<span data-ttu-id="5748d-144">Especifica a configuração de IP primário em caso de a interface de rede ter mais de uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="5748d-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="5748d-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="5748d-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="5748d-146">Especifique a configuração de IP para o endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="5748d-146">Specify the IP configuration for private IP address.</span></span>  <span data-ttu-id="5748d-147">O padrão é considerado IPv4.</span><span class="sxs-lookup"><span data-stu-id="5748d-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="5748d-148">Os valores possíveis são: ' IPv4 ' e ' IPv6 '.</span><span class="sxs-lookup"><span data-stu-id="5748d-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="5748d-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5748d-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="5748d-150">O tempo limite de ociosidade do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="5748d-150">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5748d-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5748d-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="5748d-152">O nome de configuração do endereço publicIP.</span><span class="sxs-lookup"><span data-stu-id="5748d-152">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5748d-153">-PublicIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="5748d-153">-PublicIPAddressVersion</span></span>
<span data-ttu-id="5748d-154">Especifique a configuração de IP para o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="5748d-154">Specify the IP configuration for public IP address.</span></span>  <span data-ttu-id="5748d-155">O padrão é considerado IPv4.</span><span class="sxs-lookup"><span data-stu-id="5748d-155">Default is taken as IPv4.</span></span>  <span data-ttu-id="5748d-156">Os valores possíveis são: ' IPv4 ' e ' IPv6 '.</span><span class="sxs-lookup"><span data-stu-id="5748d-156">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="5748d-157">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="5748d-157">-PublicIPPrefix</span></span>
<span data-ttu-id="5748d-158">A ID do prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="5748d-158">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="5748d-159">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="5748d-159">-SubnetId</span></span>
<span data-ttu-id="5748d-160">Especifica a ID de sub-rede na qual a configuração cria a interface de rede VMSS.</span><span class="sxs-lookup"><span data-stu-id="5748d-160">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5748d-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5748d-161">-Confirm</span></span>
<span data-ttu-id="5748d-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5748d-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5748d-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5748d-163">-WhatIf</span></span>
<span data-ttu-id="5748d-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5748d-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5748d-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5748d-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5748d-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5748d-166">CommonParameters</span></span>
<span data-ttu-id="5748d-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5748d-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5748d-168">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5748d-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5748d-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5748d-169">INPUTS</span></span>

### <span data-ttu-id="5748d-170">System. String</span><span class="sxs-lookup"><span data-stu-id="5748d-170">System.String</span></span>

### <span data-ttu-id="5748d-171">System. String []</span><span class="sxs-lookup"><span data-stu-id="5748d-171">System.String[]</span></span>

### <span data-ttu-id="5748d-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5748d-172">System.Int32</span></span>

### <span data-ttu-id="5748d-173">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIpTag []</span><span class="sxs-lookup"><span data-stu-id="5748d-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="5748d-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5748d-174">OUTPUTS</span></span>

### <span data-ttu-id="5748d-175">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5748d-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="5748d-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5748d-176">NOTES</span></span>

## <span data-ttu-id="5748d-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5748d-177">RELATED LINKS</span></span>

[<span data-ttu-id="5748d-178">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5748d-178">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


