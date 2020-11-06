---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: ecd5df4728e963e8bcf4614a6acb554fdbf17788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432096"
---
# <span data-ttu-id="6578a-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6578a-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="6578a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6578a-102">SYNOPSIS</span></span>
<span data-ttu-id="6578a-103">Adiciona uma rota a uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="6578a-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6578a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6578a-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6578a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6578a-105">DESCRIPTION</span></span>
<span data-ttu-id="6578a-106">O cmdlet **Add-AzureRmRouteConfig** adiciona uma rota a uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="6578a-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="6578a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6578a-107">EXAMPLES</span></span>

### <span data-ttu-id="6578a-108">Exemplo 1: adicionar uma rota a uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="6578a-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="6578a-109">O primeiro comando obtém uma tabela de rota chamada RouteTable01 usando o cmdlet Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="6578a-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="6578a-110">O comando armazena a tabela na variável $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="6578a-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="6578a-111">O segundo comando adiciona uma rota chamada Route13 à tabela de rota armazenada em $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="6578a-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="6578a-112">Essa rota encaminha pacotes para a rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="6578a-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="6578a-113">Exemplo 2: adicionar uma rota a uma tabela de rota usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="6578a-113">Example 2: Add a route to a route table by using the pipeline</span></span>
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

<span data-ttu-id="6578a-114">Esse comando obtém a tabela de rota chamada RouteTable01 usando **Get-AzureRmRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="6578a-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="6578a-115">O comando transmite essa tabela para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="6578a-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6578a-116">O cmdlet atual adiciona a rota chamada Route02 e, em seguida, passa o resultado para o cmdlet **set-AzureRmRouteTable** , que atualiza a tabela para refletir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="6578a-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="6578a-117">OS</span><span class="sxs-lookup"><span data-stu-id="6578a-117">PARAMETERS</span></span>

### <span data-ttu-id="6578a-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6578a-118">-AddressPrefix</span></span>
<span data-ttu-id="6578a-119">Especifica o destino, no formato CIDR (roteamento interdomínio sem classe), ao qual a rota se aplica.</span><span class="sxs-lookup"><span data-stu-id="6578a-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="6578a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6578a-120">-DefaultProfile</span></span>
<span data-ttu-id="6578a-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6578a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6578a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6578a-122">-Name</span></span>
<span data-ttu-id="6578a-123">Especifica um nome da rota a ser adicionada à tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="6578a-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="6578a-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="6578a-124">-NextHopIpAddress</span></span>
<span data-ttu-id="6578a-125">Especifica o endereço IP de um dispositivo virtual que você adiciona à sua rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6578a-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="6578a-126">Essa rota encaminha pacotes para esse endereço.</span><span class="sxs-lookup"><span data-stu-id="6578a-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="6578a-127">Especifique esse parâmetro somente se especificar um valor de VirtualAppliance para o parâmetro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="6578a-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="6578a-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="6578a-128">-NextHopType</span></span>
<span data-ttu-id="6578a-129">Especifica como essa rota encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="6578a-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="6578a-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6578a-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6578a-131">Rede.</span><span class="sxs-lookup"><span data-stu-id="6578a-131">Internet.</span></span>
<span data-ttu-id="6578a-132">O gateway padrão da Internet fornecido pelo Azure.</span><span class="sxs-lookup"><span data-stu-id="6578a-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="6578a-133">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="6578a-133">None.</span></span>
<span data-ttu-id="6578a-134">Se você especificar esse valor, a rota não encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="6578a-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="6578a-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="6578a-135">VirtualAppliance.</span></span>
<span data-ttu-id="6578a-136">Um dispositivo virtual que você adiciona à sua rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6578a-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="6578a-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="6578a-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="6578a-138">Um gateway de rede virtual privada do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="6578a-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="6578a-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="6578a-139">VnetLocal.</span></span>
<span data-ttu-id="6578a-140">A rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="6578a-140">The local virtual network.</span></span>
<span data-ttu-id="6578a-141">Se você tiver duas sub-redes, 10.1.0.0/16 e 10.2.0.0/16 na mesma rede virtual, selecione um valor VnetLocal para cada sub-rede para encaminhar para a outra sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6578a-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="6578a-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="6578a-142">-RouteTable</span></span>
<span data-ttu-id="6578a-143">Especifica a tabela de rota para a qual esse cmdlet adiciona uma rota.</span><span class="sxs-lookup"><span data-stu-id="6578a-143">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6578a-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6578a-144">-Confirm</span></span>
<span data-ttu-id="6578a-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6578a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6578a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6578a-146">-WhatIf</span></span>
<span data-ttu-id="6578a-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6578a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6578a-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6578a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6578a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6578a-149">CommonParameters</span></span>
<span data-ttu-id="6578a-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6578a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6578a-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6578a-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6578a-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6578a-152">INPUTS</span></span>

### <span data-ttu-id="6578a-153">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="6578a-153">PSRouteTable</span></span>
<span data-ttu-id="6578a-154">O parâmetro ' RouteTable ' aceita o valor do tipo ' PSRouteTable ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="6578a-154">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="6578a-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6578a-155">OUTPUTS</span></span>

### <span data-ttu-id="6578a-156">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="6578a-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="6578a-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6578a-157">NOTES</span></span>

## <span data-ttu-id="6578a-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6578a-158">RELATED LINKS</span></span>

[<span data-ttu-id="6578a-159">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6578a-159">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="6578a-160">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="6578a-160">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="6578a-161">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6578a-161">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="6578a-162">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6578a-162">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="6578a-163">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6578a-163">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="6578a-164">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="6578a-164">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)

