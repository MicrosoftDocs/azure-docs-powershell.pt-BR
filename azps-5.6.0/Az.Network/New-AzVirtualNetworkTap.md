---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 93bc2a622d2bba077b5176c67df4d7894a95d4ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888668"
---
# <span data-ttu-id="04f76-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="04f76-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="04f76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04f76-102">SYNOPSIS</span></span>
<span data-ttu-id="04f76-103">Cria um recurso VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="04f76-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="04f76-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="04f76-104">SYNTAX</span></span>

### <span data-ttu-id="04f76-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="04f76-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04f76-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="04f76-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04f76-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="04f76-107">DESCRIPTION</span></span>
<span data-ttu-id="04f76-108">O cmdlet **New-AzVirtualNetworkTap** cria um recurso de toque de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="04f76-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="04f76-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04f76-109">EXAMPLES</span></span>

### <span data-ttu-id="04f76-110">Exemplo 1: Criar um toque de rede virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="04f76-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="04f76-111">Este comando cria um toque de rede virtual chamado "VirtualNetworkTap1" que tem detalhes de configuração de VM de destino (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="04f76-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="04f76-112">Todo o toque de origem configurou o tráfego da VM será roteado para este IP + Porta de Destino.</span><span class="sxs-lookup"><span data-stu-id="04f76-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="04f76-113">Exemplo 2: Criar um toque de rede virtual do Azure usando o IP LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="04f76-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="04f76-114">Este comando cria um toque de rede virtual chamado "VirtualNetworkTap1" que tem detalhes de configuração de VM de destino (FrontEndIpConfiguration).</span><span class="sxs-lookup"><span data-stu-id="04f76-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="04f76-115">Todo o tráfego da VM configurado do toque de origem será roteado para este IpConfiguration LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="04f76-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="04f76-116">A porta de destino padrão é 4789.</span><span class="sxs-lookup"><span data-stu-id="04f76-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="04f76-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="04f76-117">PARAMETERS</span></span>

### <span data-ttu-id="04f76-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04f76-118">-AsJob</span></span>
<span data-ttu-id="04f76-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="04f76-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04f76-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f76-120">-DefaultProfile</span></span>
<span data-ttu-id="04f76-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04f76-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04f76-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="04f76-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="04f76-123">A referência do recurso de configuração ip front-end do balanceador de carga de destino.</span><span class="sxs-lookup"><span data-stu-id="04f76-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="04f76-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="04f76-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="04f76-125">A referência do recurso de configuração ip front-end do balanceador de carga de destino.</span><span class="sxs-lookup"><span data-stu-id="04f76-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="04f76-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="04f76-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="04f76-127">A referência do recurso de configuração IP da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="04f76-127">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="04f76-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="04f76-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="04f76-129">A referência do recurso de configuração IP da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="04f76-129">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="04f76-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="04f76-130">-DestinationPort</span></span>
<span data-ttu-id="04f76-131">A Porta de Destino do coletor de pacotes</span><span class="sxs-lookup"><span data-stu-id="04f76-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="04f76-132">-Force</span><span class="sxs-lookup"><span data-stu-id="04f76-132">-Force</span></span>
<span data-ttu-id="04f76-133">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="04f76-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="04f76-134">-Location</span><span class="sxs-lookup"><span data-stu-id="04f76-134">-Location</span></span>
<span data-ttu-id="04f76-135">O local.</span><span class="sxs-lookup"><span data-stu-id="04f76-135">The location.</span></span>

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

### <span data-ttu-id="04f76-136">-Name</span><span class="sxs-lookup"><span data-stu-id="04f76-136">-Name</span></span>
<span data-ttu-id="04f76-137">O nome do toque.</span><span class="sxs-lookup"><span data-stu-id="04f76-137">The name of the tap.</span></span>

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

### <span data-ttu-id="04f76-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04f76-138">-ResourceGroupName</span></span>
<span data-ttu-id="04f76-139">O nome do grupo de recursos do toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="04f76-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="04f76-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="04f76-140">-Tag</span></span>
<span data-ttu-id="04f76-141">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="04f76-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="04f76-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04f76-142">-Confirm</span></span>
<span data-ttu-id="04f76-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04f76-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04f76-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04f76-144">-WhatIf</span></span>
<span data-ttu-id="04f76-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04f76-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04f76-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04f76-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04f76-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f76-147">CommonParameters</span></span>
<span data-ttu-id="04f76-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04f76-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f76-149">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04f76-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f76-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04f76-150">INPUTS</span></span>

### <span data-ttu-id="04f76-151">System.String</span><span class="sxs-lookup"><span data-stu-id="04f76-151">System.String</span></span>

### <span data-ttu-id="04f76-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="04f76-152">System.Int32</span></span>

### <span data-ttu-id="04f76-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="04f76-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="04f76-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="04f76-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="04f76-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="04f76-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="04f76-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="04f76-156">OUTPUTS</span></span>

### <span data-ttu-id="04f76-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="04f76-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="04f76-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="04f76-158">NOTES</span></span>

## <span data-ttu-id="04f76-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04f76-159">RELATED LINKS</span></span>

[<span data-ttu-id="04f76-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="04f76-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="04f76-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="04f76-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="04f76-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="04f76-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
