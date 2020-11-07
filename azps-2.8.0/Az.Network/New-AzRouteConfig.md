---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 07b7d0decd196fba9cbf0a813af4d252d01dfc8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771596"
---
# <span data-ttu-id="9074e-101">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9074e-101">New-AzRouteConfig</span></span>

## <span data-ttu-id="9074e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9074e-102">SYNOPSIS</span></span>
<span data-ttu-id="9074e-103">Cria uma rota para uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="9074e-103">Creates a route for a route table.</span></span>

## <span data-ttu-id="9074e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9074e-104">SYNTAX</span></span>

```
New-AzRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9074e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9074e-105">DESCRIPTION</span></span>
<span data-ttu-id="9074e-106">O cmdlet **New-AzRouteConfig** cria uma rota para uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="9074e-106">The **New-AzRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="9074e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9074e-107">EXAMPLES</span></span>

### <span data-ttu-id="9074e-108">Exemplo 1: criar uma rota</span><span class="sxs-lookup"><span data-stu-id="9074e-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="9074e-109">O primeiro comando cria uma rota chamada Route07 e, em seguida, armazena-a na variável $Route.</span><span class="sxs-lookup"><span data-stu-id="9074e-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="9074e-110">Essa rota encaminha pacotes para a rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="9074e-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="9074e-111">O segundo comando exibe as propriedades da rota.</span><span class="sxs-lookup"><span data-stu-id="9074e-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="9074e-112">OS</span><span class="sxs-lookup"><span data-stu-id="9074e-112">PARAMETERS</span></span>

### <span data-ttu-id="9074e-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9074e-113">-AddressPrefix</span></span>
<span data-ttu-id="9074e-114">Especifica o destino, no formato CIDR (roteamento interdomínio sem classe), ao qual a rota se aplica.</span><span class="sxs-lookup"><span data-stu-id="9074e-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="9074e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9074e-115">-DefaultProfile</span></span>
<span data-ttu-id="9074e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9074e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9074e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9074e-117">-Name</span></span>
<span data-ttu-id="9074e-118">Especifica um nome para a rota.</span><span class="sxs-lookup"><span data-stu-id="9074e-118">Specifies a name for the route.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9074e-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="9074e-119">-NextHopIpAddress</span></span>
<span data-ttu-id="9074e-120">Especifica o endereço IP de um dispositivo virtual que você adiciona à sua rede do Azurevirtual.</span><span class="sxs-lookup"><span data-stu-id="9074e-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="9074e-121">Essa rota encaminha pacotes para esse endereço.</span><span class="sxs-lookup"><span data-stu-id="9074e-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="9074e-122">Especifique esse parâmetro somente se especificar um valor de VirtualAppliance para o parâmetro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="9074e-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="9074e-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="9074e-123">-NextHopType</span></span>
<span data-ttu-id="9074e-124">Especifica como essa rota encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="9074e-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="9074e-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9074e-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9074e-126">Rede.</span><span class="sxs-lookup"><span data-stu-id="9074e-126">Internet.</span></span>
<span data-ttu-id="9074e-127">O gateway padrão da Internet fornecido pelo Azure.</span><span class="sxs-lookup"><span data-stu-id="9074e-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="9074e-128">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="9074e-128">None.</span></span>
<span data-ttu-id="9074e-129">Se você especificar esse valor, a rota não encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="9074e-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="9074e-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="9074e-130">VirtualAppliance.</span></span>
<span data-ttu-id="9074e-131">Um dispositivo virtual que você adiciona à sua rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="9074e-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="9074e-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="9074e-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="9074e-133">Um gateway de rede virtual privada do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="9074e-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="9074e-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="9074e-134">VnetLocal.</span></span>
<span data-ttu-id="9074e-135">A rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="9074e-135">The local virtual network.</span></span>
<span data-ttu-id="9074e-136">Se você tiver duas sub-redes, 10.1.0.0/16 e 10.2.0.0/16 na mesma rede virtual, selecione um valor VnetLocal para cada sub-rede para encaminhar para a outra sub-rede.</span><span class="sxs-lookup"><span data-stu-id="9074e-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="9074e-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9074e-137">-Confirm</span></span>
<span data-ttu-id="9074e-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9074e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9074e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9074e-139">-WhatIf</span></span>
<span data-ttu-id="9074e-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9074e-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9074e-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9074e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9074e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9074e-142">CommonParameters</span></span>
<span data-ttu-id="9074e-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9074e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9074e-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9074e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9074e-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9074e-145">INPUTS</span></span>

### <span data-ttu-id="9074e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9074e-146">System.String</span></span>

## <span data-ttu-id="9074e-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9074e-147">OUTPUTS</span></span>

### <span data-ttu-id="9074e-148">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="9074e-148">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="9074e-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9074e-149">NOTES</span></span>

## <span data-ttu-id="9074e-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9074e-150">RELATED LINKS</span></span>

[<span data-ttu-id="9074e-151">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9074e-151">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="9074e-152">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9074e-152">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="9074e-153">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9074e-153">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="9074e-154">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9074e-154">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


