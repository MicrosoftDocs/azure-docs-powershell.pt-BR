---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: 7b28c50cfc53fee03d5715697a88e9356ea7664b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433079"
---
# <span data-ttu-id="a69b2-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a69b2-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="a69b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a69b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a69b2-103">Adiciona uma rota a uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="a69b2-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a69b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a69b2-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a69b2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a69b2-105">DESCRIPTION</span></span>
<span data-ttu-id="a69b2-106">O cmdlet **Add-AzureRmRouteConfig** adiciona uma rota a uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="a69b2-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="a69b2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a69b2-107">EXAMPLES</span></span>

### <span data-ttu-id="a69b2-108">Exemplo 1: adicionar uma rota a uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="a69b2-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="a69b2-109">O primeiro comando obtém uma tabela de rota chamada RouteTable01 usando o cmdlet Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="a69b2-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="a69b2-110">O comando armazena a tabela na variável $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="a69b2-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="a69b2-111">O segundo comando adiciona uma rota chamada Route13 à tabela de rota armazenada em $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="a69b2-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="a69b2-112">Essa rota encaminha pacotes para a rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="a69b2-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="a69b2-113">Exemplo 2: adicionar uma rota a uma tabela de rota usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="a69b2-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="a69b2-114">Esse comando obtém a tabela de rota chamada RouteTable01 usando **Get-AzureRmRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="a69b2-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="a69b2-115">O comando transmite essa tabela para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="a69b2-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a69b2-116">O cmdlet atual adiciona a rota chamada Route02 e, em seguida, passa o resultado para o cmdlet **set-AzureRmRouteTable** , que atualiza a tabela para refletir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="a69b2-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="a69b2-117">OS</span><span class="sxs-lookup"><span data-stu-id="a69b2-117">PARAMETERS</span></span>

### <span data-ttu-id="a69b2-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a69b2-118">-AddressPrefix</span></span>
<span data-ttu-id="a69b2-119">Especifica o destino, no formato CIDR (roteamento interdomínio sem classe), ao qual a rota se aplica.</span><span class="sxs-lookup"><span data-stu-id="a69b2-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="a69b2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a69b2-120">-Name</span></span>
<span data-ttu-id="a69b2-121">Especifica um nome da rota a ser adicionada à tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="a69b2-121">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="a69b2-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="a69b2-122">-NextHopIpAddress</span></span>
<span data-ttu-id="a69b2-123">Especifica o endereço IP de um dispositivo virtual que você adiciona à sua rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="a69b2-123">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="a69b2-124">Essa rota encaminha pacotes para esse endereço.</span><span class="sxs-lookup"><span data-stu-id="a69b2-124">This route forwards packets to that address.</span></span>
<span data-ttu-id="a69b2-125">Especifique esse parâmetro somente se especificar um valor de VirtualAppliance para o parâmetro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="a69b2-125">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="a69b2-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="a69b2-126">-NextHopType</span></span>
<span data-ttu-id="a69b2-127">Especifica como essa rota encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="a69b2-127">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="a69b2-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a69b2-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a69b2-129">Rede.</span><span class="sxs-lookup"><span data-stu-id="a69b2-129">Internet.</span></span>
<span data-ttu-id="a69b2-130">O gateway padrão da Internet fornecido pelo Azure.</span><span class="sxs-lookup"><span data-stu-id="a69b2-130">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="a69b2-131">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="a69b2-131">None.</span></span>
<span data-ttu-id="a69b2-132">Se você especificar esse valor, a rota não encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="a69b2-132">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="a69b2-133">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="a69b2-133">VirtualAppliance.</span></span>
<span data-ttu-id="a69b2-134">Um dispositivo virtual que você adiciona à sua rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="a69b2-134">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="a69b2-135">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="a69b2-135">VirtualNetworkGateway.</span></span>
<span data-ttu-id="a69b2-136">Um gateway de rede virtual privada do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="a69b2-136">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="a69b2-137">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="a69b2-137">VnetLocal.</span></span>
<span data-ttu-id="a69b2-138">A rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="a69b2-138">The local virtual network.</span></span>
<span data-ttu-id="a69b2-139">Se você tiver duas sub-redes, 10.1.0.0/16 e 10.2.0.0/16 na mesma rede virtual, selecione um valor VnetLocal para cada sub-rede para encaminhar para a outra sub-rede.</span><span class="sxs-lookup"><span data-stu-id="a69b2-139">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="a69b2-140">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a69b2-140">-RouteTable</span></span>
<span data-ttu-id="a69b2-141">Especifica a tabela de rota para a qual esse cmdlet adiciona uma rota.</span><span class="sxs-lookup"><span data-stu-id="a69b2-141">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a69b2-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69b2-142">-DefaultProfile</span></span>
<span data-ttu-id="a69b2-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a69b2-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a69b2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69b2-144">CommonParameters</span></span>
<span data-ttu-id="a69b2-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a69b2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69b2-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a69b2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69b2-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a69b2-147">INPUTS</span></span>

### <span data-ttu-id="a69b2-148">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="a69b2-148">PSRouteTable</span></span>
<span data-ttu-id="a69b2-149">O parâmetro ' RouteTable ' aceita o valor do tipo ' PSRouteTable ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="a69b2-149">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="a69b2-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a69b2-150">OUTPUTS</span></span>

### <span data-ttu-id="a69b2-151">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="a69b2-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="a69b2-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a69b2-152">NOTES</span></span>

## <span data-ttu-id="a69b2-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a69b2-153">RELATED LINKS</span></span>

[<span data-ttu-id="a69b2-154">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a69b2-154">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="a69b2-155">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="a69b2-155">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="a69b2-156">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a69b2-156">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="a69b2-157">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a69b2-157">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="a69b2-158">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a69b2-158">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="a69b2-159">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="a69b2-159">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


