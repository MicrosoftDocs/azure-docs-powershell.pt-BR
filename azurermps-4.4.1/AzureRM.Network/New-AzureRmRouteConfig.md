---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: bb51d5bfb1ccc81aa10c7aecc4d7a255fc0f60d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429258"
---
# <span data-ttu-id="6aa9c-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6aa9c-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="6aa9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6aa9c-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa9c-103">Cria uma rota para uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6aa9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6aa9c-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig -Name <String> [-AddressPrefix <String>] -NextHopType <String>
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aa9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6aa9c-105">DESCRIPTION</span></span>
<span data-ttu-id="6aa9c-106">O cmdlet **New-AzureRmRouteConfig** cria uma rota para uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="6aa9c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6aa9c-107">EXAMPLES</span></span>

### <span data-ttu-id="6aa9c-108">Exemplo 1: criar uma rota</span><span class="sxs-lookup"><span data-stu-id="6aa9c-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="6aa9c-109">O primeiro comando cria uma rota chamada Route07 e, em seguida, armazena-a na variável $Route.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="6aa9c-110">Essa rota encaminha pacotes para a rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="6aa9c-111">O segundo comando exibe as propriedades da rota.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="6aa9c-112">OS</span><span class="sxs-lookup"><span data-stu-id="6aa9c-112">PARAMETERS</span></span>

### <span data-ttu-id="6aa9c-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6aa9c-113">-AddressPrefix</span></span>
<span data-ttu-id="6aa9c-114">Especifica o destino, no formato CIDR (roteamento interdomínio sem classe), ao qual a rota se aplica.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="6aa9c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6aa9c-115">-Name</span></span>
<span data-ttu-id="6aa9c-116">Especifica um nome para a rota.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-116">Specifies a name for the route.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aa9c-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="6aa9c-117">-NextHopIpAddress</span></span>
<span data-ttu-id="6aa9c-118">Especifica o endereço IP de um dispositivo virtual que você adiciona à sua rede do Azurevirtual.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-118">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="6aa9c-119">Essa rota encaminha pacotes para esse endereço.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="6aa9c-120">Especifique esse parâmetro somente se especificar um valor de VirtualAppliance para o parâmetro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="6aa9c-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="6aa9c-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="6aa9c-121">-NextHopType</span></span>
<span data-ttu-id="6aa9c-122">Especifica como essa rota encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="6aa9c-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6aa9c-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6aa9c-124">Rede.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-124">Internet.</span></span>
<span data-ttu-id="6aa9c-125">O gateway padrão da Internet fornecido pelo Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="6aa9c-126">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-126">None.</span></span>
<span data-ttu-id="6aa9c-127">Se você especificar esse valor, a rota não encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="6aa9c-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-128">VirtualAppliance.</span></span>
<span data-ttu-id="6aa9c-129">Um dispositivo virtual que você adiciona à sua rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="6aa9c-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="6aa9c-131">Um gateway de rede virtual privada do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-131">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="6aa9c-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-132">VnetLocal.</span></span>
<span data-ttu-id="6aa9c-133">A rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-133">The local virtual network.</span></span>
<span data-ttu-id="6aa9c-134">Se você tiver duas sub-redes, 10.1.0.0/16 e 10.2.0.0/16 na mesma rede virtual, selecione um valor VnetLocal para cada sub-rede para encaminhar para a outra sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Internet, None, VirtualAppliance, VirtualNetworkGateway, VnetLocal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aa9c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa9c-135">-DefaultProfile</span></span>
<span data-ttu-id="6aa9c-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aa9c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa9c-137">CommonParameters</span></span>
<span data-ttu-id="6aa9c-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa9c-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa9c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa9c-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6aa9c-140">INPUTS</span></span>

## <span data-ttu-id="6aa9c-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6aa9c-141">OUTPUTS</span></span>

### <span data-ttu-id="6aa9c-142">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="6aa9c-142">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="6aa9c-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6aa9c-143">NOTES</span></span>

## <span data-ttu-id="6aa9c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6aa9c-144">RELATED LINKS</span></span>

[<span data-ttu-id="6aa9c-145">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6aa9c-145">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="6aa9c-146">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6aa9c-146">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="6aa9c-147">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6aa9c-147">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="6aa9c-148">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6aa9c-148">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


