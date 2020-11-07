---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 83f6f44af262719c9ed9fb5cae818bc6b70d5c2b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943251"
---
# <span data-ttu-id="fb977-101">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fb977-101">New-AzRouteConfig</span></span>

## <span data-ttu-id="fb977-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb977-102">SYNOPSIS</span></span>
<span data-ttu-id="fb977-103">Cria uma rota para uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="fb977-103">Creates a route for a route table.</span></span>

## <span data-ttu-id="fb977-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb977-104">SYNTAX</span></span>

```
New-AzRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb977-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb977-105">DESCRIPTION</span></span>
<span data-ttu-id="fb977-106">O cmdlet **New-AzRouteConfig** cria uma rota para uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb977-106">The **New-AzRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="fb977-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb977-107">EXAMPLES</span></span>

### <span data-ttu-id="fb977-108">Exemplo 1: criar uma rota</span><span class="sxs-lookup"><span data-stu-id="fb977-108">Example 1: Create a route</span></span>
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

<span data-ttu-id="fb977-109">O primeiro comando cria uma rota chamada Route07 e, em seguida, armazena-a na variável $Route.</span><span class="sxs-lookup"><span data-stu-id="fb977-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="fb977-110">Essa rota encaminha pacotes para a rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="fb977-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="fb977-111">O segundo comando exibe as propriedades da rota.</span><span class="sxs-lookup"><span data-stu-id="fb977-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="fb977-112">OS</span><span class="sxs-lookup"><span data-stu-id="fb977-112">PARAMETERS</span></span>

### <span data-ttu-id="fb977-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fb977-113">-AddressPrefix</span></span>
<span data-ttu-id="fb977-114">Especifica o destino, no formato CIDR (roteamento interdomínio sem classe), ao qual a rota se aplica.</span><span class="sxs-lookup"><span data-stu-id="fb977-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="fb977-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb977-115">-DefaultProfile</span></span>
<span data-ttu-id="fb977-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb977-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb977-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb977-117">-Name</span></span>
<span data-ttu-id="fb977-118">Especifica um nome para a rota.</span><span class="sxs-lookup"><span data-stu-id="fb977-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="fb977-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="fb977-119">-NextHopIpAddress</span></span>
<span data-ttu-id="fb977-120">Especifica o endereço IP de um dispositivo virtual que você adiciona à sua rede do Azurevirtual.</span><span class="sxs-lookup"><span data-stu-id="fb977-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="fb977-121">Essa rota encaminha pacotes para esse endereço.</span><span class="sxs-lookup"><span data-stu-id="fb977-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="fb977-122">Especifique esse parâmetro somente se especificar um valor de VirtualAppliance para o parâmetro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="fb977-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="fb977-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="fb977-123">-NextHopType</span></span>
<span data-ttu-id="fb977-124">Especifica como essa rota encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="fb977-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="fb977-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fb977-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb977-126">Rede.</span><span class="sxs-lookup"><span data-stu-id="fb977-126">Internet.</span></span>
<span data-ttu-id="fb977-127">O gateway padrão da Internet fornecido pelo Azure.</span><span class="sxs-lookup"><span data-stu-id="fb977-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="fb977-128">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="fb977-128">None.</span></span>
<span data-ttu-id="fb977-129">Se você especificar esse valor, a rota não encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="fb977-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="fb977-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="fb977-130">VirtualAppliance.</span></span>
<span data-ttu-id="fb977-131">Um dispositivo virtual que você adiciona à sua rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb977-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="fb977-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="fb977-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="fb977-133">Um gateway de rede virtual privada do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb977-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="fb977-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="fb977-134">VnetLocal.</span></span>
<span data-ttu-id="fb977-135">A rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="fb977-135">The local virtual network.</span></span>
<span data-ttu-id="fb977-136">Se você tiver duas sub-redes, 10.1.0.0/16 e 10.2.0.0/16 na mesma rede virtual, selecione um valor VnetLocal para cada sub-rede para encaminhar para a outra sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fb977-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="fb977-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb977-137">-Confirm</span></span>
<span data-ttu-id="fb977-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb977-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb977-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb977-139">-WhatIf</span></span>
<span data-ttu-id="fb977-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb977-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb977-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb977-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb977-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb977-142">CommonParameters</span></span>
<span data-ttu-id="fb977-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb977-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb977-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb977-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb977-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb977-145">INPUTS</span></span>

### <span data-ttu-id="fb977-146">System. String</span><span class="sxs-lookup"><span data-stu-id="fb977-146">System.String</span></span>

## <span data-ttu-id="fb977-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb977-147">OUTPUTS</span></span>

### <span data-ttu-id="fb977-148">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="fb977-148">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="fb977-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb977-149">NOTES</span></span>

## <span data-ttu-id="fb977-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb977-150">RELATED LINKS</span></span>

[<span data-ttu-id="fb977-151">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fb977-151">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="fb977-152">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fb977-152">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="fb977-153">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fb977-153">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="fb977-154">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fb977-154">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


