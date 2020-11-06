---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: 98e3bf7f76475b451d3a8f6509e311d9d861f691
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610373"
---
# <span data-ttu-id="f1cb4-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f1cb4-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="f1cb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cb4-103">Cria uma rota para uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1cb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1cb4-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig [-AddressPrefix <String>] [-NextHopType <String>] [-NextHopIpAddress <String>]
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1cb4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1cb4-105">DESCRIPTION</span></span>
<span data-ttu-id="f1cb4-106">O cmdlet **New-AzureRmRouteConfig** cria uma rota para uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="f1cb4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1cb4-107">EXAMPLES</span></span>

### <span data-ttu-id="f1cb4-108">Exemplo 1: criar uma rota</span><span class="sxs-lookup"><span data-stu-id="f1cb4-108">Example 1: Create a route</span></span>
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

<span data-ttu-id="f1cb4-109">O primeiro comando cria uma rota chamada Route07 e, em seguida, armazena-a na variável $Route.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="f1cb4-110">Essa rota encaminha pacotes para a rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="f1cb4-111">O segundo comando exibe as propriedades da rota.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="f1cb4-112">OS</span><span class="sxs-lookup"><span data-stu-id="f1cb4-112">PARAMETERS</span></span>

### <span data-ttu-id="f1cb4-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f1cb4-113">-AddressPrefix</span></span>
<span data-ttu-id="f1cb4-114">Especifica o destino, no formato CIDR (roteamento interdomínio sem classe), ao qual a rota se aplica.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cb4-115">-DefaultProfile</span></span>
<span data-ttu-id="f1cb4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1cb4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1cb4-117">-Name</span></span>
<span data-ttu-id="f1cb4-118">Especifica um nome para a rota.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-118">Specifies a name for the route.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb4-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="f1cb4-119">-NextHopIpAddress</span></span>
<span data-ttu-id="f1cb4-120">Especifica o endereço IP de um dispositivo virtual que você adiciona à sua rede do Azurevirtual.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="f1cb4-121">Essa rota encaminha pacotes para esse endereço.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="f1cb4-122">Especifique esse parâmetro somente se especificar um valor de VirtualAppliance para o parâmetro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="f1cb4-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb4-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="f1cb4-123">-NextHopType</span></span>
<span data-ttu-id="f1cb4-124">Especifica como essa rota encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="f1cb4-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f1cb4-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1cb4-126">Rede.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-126">Internet.</span></span>
<span data-ttu-id="f1cb4-127">O gateway padrão da Internet fornecido pelo Azure.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="f1cb4-128">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-128">None.</span></span>
<span data-ttu-id="f1cb4-129">Se você especificar esse valor, a rota não encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="f1cb4-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-130">VirtualAppliance.</span></span>
<span data-ttu-id="f1cb4-131">Um dispositivo virtual que você adiciona à sua rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="f1cb4-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="f1cb4-133">Um gateway de rede virtual privada do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="f1cb4-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-134">VnetLocal.</span></span>
<span data-ttu-id="f1cb4-135">A rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-135">The local virtual network.</span></span>
<span data-ttu-id="f1cb4-136">Se você tiver duas sub-redes, 10.1.0.0/16 e 10.2.0.0/16 na mesma rede virtual, selecione um valor VnetLocal para cada sub-rede para encaminhar para a outra sub-rede.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb4-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1cb4-137">-Confirm</span></span>
<span data-ttu-id="f1cb4-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1cb4-139">-WhatIf</span></span>
<span data-ttu-id="f1cb4-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1cb4-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cb4-142">CommonParameters</span></span>
<span data-ttu-id="f1cb4-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cb4-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1cb4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cb4-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1cb4-145">INPUTS</span></span>

### <span data-ttu-id="f1cb4-146">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f1cb4-146">None</span></span>
<span data-ttu-id="f1cb4-147">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f1cb4-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1cb4-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1cb4-148">OUTPUTS</span></span>

### <span data-ttu-id="f1cb4-149">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="f1cb4-149">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="f1cb4-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1cb4-150">NOTES</span></span>

## <span data-ttu-id="f1cb4-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1cb4-151">RELATED LINKS</span></span>

[<span data-ttu-id="f1cb4-152">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f1cb4-152">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="f1cb4-153">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f1cb4-153">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="f1cb4-154">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f1cb4-154">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="f1cb4-155">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f1cb4-155">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


