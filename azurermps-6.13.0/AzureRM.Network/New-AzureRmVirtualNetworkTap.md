---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: d40d9c378afdbbc9380114a7b5998b173cb4652f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610554"
---
# <span data-ttu-id="015da-101">New-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="015da-101">New-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="015da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="015da-102">SYNOPSIS</span></span>
<span data-ttu-id="015da-103">Cria um recurso VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="015da-103">Creates a VirtualNetworkTap resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="015da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="015da-104">SYNTAX</span></span>

### <span data-ttu-id="015da-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="015da-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="015da-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="015da-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="015da-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="015da-107">DESCRIPTION</span></span>
<span data-ttu-id="015da-108">O cmdlet **New-AzureRmVirtualNetworkTap** cria um recurso de toque virtual da rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="015da-108">The **New-AzureRmVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="015da-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="015da-109">EXAMPLES</span></span>

### <span data-ttu-id="015da-110">Exemplo 1: criar um toque de rede virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="015da-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzureRmVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="015da-111">Esse comando cria um toque de rede virtual chamado "VirtualNetworkTap1" que tem detalhes de configuração de VM de destino (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="015da-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="015da-112">Todos os toques de origem configurados o tráfego da VM serão roteados para esta porta IP + destino.</span><span class="sxs-lookup"><span data-stu-id="015da-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="015da-113">Exemplo 2: criar uma rede virtual do Azure toque usando o IP do loadbalancer</span><span class="sxs-lookup"><span data-stu-id="015da-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzureRmVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="015da-114">Esse comando cria um toque de rede virtual chamado "VirtualNetworkTap1" que tem dados de configuração da VM de destino (FrontEndIpConfiguration).</span><span class="sxs-lookup"><span data-stu-id="015da-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="015da-115">Todos os toques de origem configurados o tráfego da VM serão roteados para esta IpConfiguration de loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="015da-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="015da-116">A porta de destino padrão é 4789.</span><span class="sxs-lookup"><span data-stu-id="015da-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="015da-117">OS</span><span class="sxs-lookup"><span data-stu-id="015da-117">PARAMETERS</span></span>

### <span data-ttu-id="015da-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="015da-118">-AsJob</span></span>
<span data-ttu-id="015da-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="015da-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="015da-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="015da-120">-DefaultProfile</span></span>
<span data-ttu-id="015da-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="015da-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="015da-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="015da-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="015da-123">A referência do recurso de configuração de IP de front-end do balanceador de carga de destino.</span><span class="sxs-lookup"><span data-stu-id="015da-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="015da-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="015da-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="015da-125">A referência do recurso de configuração de IP de front-end do balanceador de carga de destino.</span><span class="sxs-lookup"><span data-stu-id="015da-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="015da-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="015da-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="015da-127">A referência do recurso de configuração de IP da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="015da-127">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="015da-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="015da-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="015da-129">A referência do recurso de configuração de IP da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="015da-129">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="015da-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="015da-130">-DestinationPort</span></span>
<span data-ttu-id="015da-131">A porta de destino do coletor de pacotes</span><span class="sxs-lookup"><span data-stu-id="015da-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="015da-132">-Force</span><span class="sxs-lookup"><span data-stu-id="015da-132">-Force</span></span>
<span data-ttu-id="015da-133">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="015da-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="015da-134">-Local</span><span class="sxs-lookup"><span data-stu-id="015da-134">-Location</span></span>
<span data-ttu-id="015da-135">O local.</span><span class="sxs-lookup"><span data-stu-id="015da-135">The location.</span></span>

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

### <span data-ttu-id="015da-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="015da-136">-Name</span></span>
<span data-ttu-id="015da-137">O nome do toque.</span><span class="sxs-lookup"><span data-stu-id="015da-137">The name of the tap.</span></span>

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

### <span data-ttu-id="015da-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="015da-138">-ResourceGroupName</span></span>
<span data-ttu-id="015da-139">O nome do grupo de recursos da rede virtual toque.</span><span class="sxs-lookup"><span data-stu-id="015da-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="015da-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="015da-140">-Tag</span></span>
<span data-ttu-id="015da-141">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="015da-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="015da-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="015da-142">-Confirm</span></span>
<span data-ttu-id="015da-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="015da-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="015da-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="015da-144">-WhatIf</span></span>
<span data-ttu-id="015da-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="015da-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="015da-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="015da-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="015da-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="015da-147">CommonParameters</span></span>
<span data-ttu-id="015da-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="015da-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="015da-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="015da-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="015da-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="015da-150">INPUTS</span></span>

### <span data-ttu-id="015da-151">System. String</span><span class="sxs-lookup"><span data-stu-id="015da-151">System.String</span></span>

### <span data-ttu-id="015da-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="015da-152">System.Int32</span></span>

### <span data-ttu-id="015da-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="015da-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="015da-154">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="015da-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="015da-155">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="015da-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="015da-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="015da-156">OUTPUTS</span></span>

### <span data-ttu-id="015da-157">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="015da-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="015da-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="015da-158">NOTES</span></span>

## <span data-ttu-id="015da-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="015da-159">RELATED LINKS</span></span>
