---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 11939edc15d49614d2a1fd1692825cd07cd82b2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771577"
---
# <span data-ttu-id="689e1-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="689e1-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="689e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="689e1-102">SYNOPSIS</span></span>
<span data-ttu-id="689e1-103">Cria um recurso VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="689e1-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="689e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="689e1-104">SYNTAX</span></span>

### <span data-ttu-id="689e1-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="689e1-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="689e1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="689e1-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="689e1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="689e1-107">DESCRIPTION</span></span>
<span data-ttu-id="689e1-108">O cmdlet **New-AzVirtualNetworkTap** cria um recurso de toque virtual da rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="689e1-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="689e1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="689e1-109">EXAMPLES</span></span>

### <span data-ttu-id="689e1-110">Exemplo 1: criar um toque de rede virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="689e1-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="689e1-111">Esse comando cria um toque de rede virtual chamado "VirtualNetworkTap1" que tem detalhes de configuração de VM de destino (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="689e1-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="689e1-112">Todos os toques de origem configurados o tráfego da VM serão roteados para esta porta IP + destino.</span><span class="sxs-lookup"><span data-stu-id="689e1-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="689e1-113">Exemplo 2: criar uma rede virtual do Azure toque usando o IP do loadbalancer</span><span class="sxs-lookup"><span data-stu-id="689e1-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="689e1-114">Esse comando cria um toque de rede virtual chamado "VirtualNetworkTap1" que tem dados de configuração da VM de destino (FrontEndIpConfiguration).</span><span class="sxs-lookup"><span data-stu-id="689e1-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="689e1-115">Todos os toques de origem configurados o tráfego da VM serão roteados para esta IpConfiguration de loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="689e1-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="689e1-116">A porta de destino padrão é 4789.</span><span class="sxs-lookup"><span data-stu-id="689e1-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="689e1-117">OS</span><span class="sxs-lookup"><span data-stu-id="689e1-117">PARAMETERS</span></span>

### <span data-ttu-id="689e1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="689e1-118">-AsJob</span></span>
<span data-ttu-id="689e1-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="689e1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="689e1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689e1-120">-DefaultProfile</span></span>
<span data-ttu-id="689e1-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="689e1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="689e1-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="689e1-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="689e1-123">A referência do recurso de configuração de IP de front-end do balanceador de carga de destino.</span><span class="sxs-lookup"><span data-stu-id="689e1-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689e1-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="689e1-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="689e1-125">A referência do recurso de configuração de IP de front-end do balanceador de carga de destino.</span><span class="sxs-lookup"><span data-stu-id="689e1-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689e1-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="689e1-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="689e1-127">A referência do recurso de configuração de IP da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="689e1-127">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689e1-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="689e1-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="689e1-129">A referência do recurso de configuração de IP da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="689e1-129">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689e1-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="689e1-130">-DestinationPort</span></span>
<span data-ttu-id="689e1-131">A porta de destino do coletor de pacotes</span><span class="sxs-lookup"><span data-stu-id="689e1-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="689e1-132">-Force</span><span class="sxs-lookup"><span data-stu-id="689e1-132">-Force</span></span>
<span data-ttu-id="689e1-133">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="689e1-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="689e1-134">-Local</span><span class="sxs-lookup"><span data-stu-id="689e1-134">-Location</span></span>
<span data-ttu-id="689e1-135">O local.</span><span class="sxs-lookup"><span data-stu-id="689e1-135">The location.</span></span>

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

### <span data-ttu-id="689e1-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="689e1-136">-Name</span></span>
<span data-ttu-id="689e1-137">O nome do toque.</span><span class="sxs-lookup"><span data-stu-id="689e1-137">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689e1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="689e1-138">-ResourceGroupName</span></span>
<span data-ttu-id="689e1-139">O nome do grupo de recursos da rede virtual toque.</span><span class="sxs-lookup"><span data-stu-id="689e1-139">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689e1-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="689e1-140">-Tag</span></span>
<span data-ttu-id="689e1-141">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="689e1-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689e1-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="689e1-142">-Confirm</span></span>
<span data-ttu-id="689e1-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="689e1-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="689e1-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="689e1-144">-WhatIf</span></span>
<span data-ttu-id="689e1-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="689e1-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="689e1-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="689e1-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="689e1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689e1-147">CommonParameters</span></span>
<span data-ttu-id="689e1-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="689e1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689e1-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="689e1-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689e1-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="689e1-150">INPUTS</span></span>

### <span data-ttu-id="689e1-151">System. String</span><span class="sxs-lookup"><span data-stu-id="689e1-151">System.String</span></span>

### <span data-ttu-id="689e1-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="689e1-152">System.Int32</span></span>

### <span data-ttu-id="689e1-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="689e1-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="689e1-154">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="689e1-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="689e1-155">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="689e1-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="689e1-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="689e1-156">OUTPUTS</span></span>

### <span data-ttu-id="689e1-157">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="689e1-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="689e1-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="689e1-158">NOTES</span></span>

## <span data-ttu-id="689e1-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="689e1-159">RELATED LINKS</span></span>

[<span data-ttu-id="689e1-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="689e1-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="689e1-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="689e1-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="689e1-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="689e1-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
