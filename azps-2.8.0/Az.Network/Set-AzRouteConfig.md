---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: ea0346ccae552a4167c545e36995ba4e8bca05fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772750"
---
# <span data-ttu-id="7ae2d-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7ae2d-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="7ae2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ae2d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae2d-103">Atualiza uma configuração de rota para uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="7ae2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ae2d-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ae2d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ae2d-105">DESCRIPTION</span></span>
<span data-ttu-id="7ae2d-106">O cmdlet **set-AzRouteConfig** atualiza uma configuração de rota para uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="7ae2d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ae2d-107">EXAMPLES</span></span>

### <span data-ttu-id="7ae2d-108">Exemplo 1: modificar uma rota</span><span class="sxs-lookup"><span data-stu-id="7ae2d-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : Routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"58c2922e-9efe-4554-a457-956ef44bc718"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/Routetable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.4.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="7ae2d-109">Esse comando obtém a tabela de rota chamada RouteTable01 usando o cmdlet Get-AzRouteTable.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="7ae2d-110">O comando transmite essa tabela para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7ae2d-111">O cmdlet atual modifica a rota chamada Route02 e, em seguida, passa o resultado para o cmdlet **set-AzRouteTable** , que atualiza a tabela para refletir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="7ae2d-112">OS</span><span class="sxs-lookup"><span data-stu-id="7ae2d-112">PARAMETERS</span></span>

### <span data-ttu-id="7ae2d-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7ae2d-113">-AddressPrefix</span></span>
<span data-ttu-id="7ae2d-114">Especifica o destino, no formato CIDR (roteamento interdomínio sem classe), ao qual a rota se aplica.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="7ae2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae2d-115">-DefaultProfile</span></span>
<span data-ttu-id="7ae2d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ae2d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ae2d-117">-Name</span></span>
<span data-ttu-id="7ae2d-118">Especifica o nome da rota modificada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7ae2d-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ae2d-119">-NextHopIpAddress</span></span>
<span data-ttu-id="7ae2d-120">Especifica o endereço IP de um dispositivo virtual que você adiciona à sua rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="7ae2d-121">Essa rota encaminha pacotes para esse endereço.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="7ae2d-122">Especifique esse parâmetro somente se especificar um valor de VirtualAppliance para o parâmetro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="7ae2d-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="7ae2d-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="7ae2d-123">-NextHopType</span></span>
<span data-ttu-id="7ae2d-124">Especifica como essa rota encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="7ae2d-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7ae2d-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ae2d-126">Rede.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-126">Internet.</span></span>
<span data-ttu-id="7ae2d-127">O gateway padrão da Internet fornecido pelo Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="7ae2d-128">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-128">None.</span></span>
<span data-ttu-id="7ae2d-129">Se você especificar esse valor, a rota não encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="7ae2d-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-130">VirtualAppliance.</span></span>
<span data-ttu-id="7ae2d-131">Um dispositivo virtual que você adiciona à sua rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="7ae2d-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="7ae2d-133">Um gateway de rede privada virtual do Azureserver-to-Server.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="7ae2d-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-134">VnetLocal.</span></span>
<span data-ttu-id="7ae2d-135">A rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-135">The local virtual network.</span></span>
<span data-ttu-id="7ae2d-136">Se você tiver duas sub-redes, 10.1.0.0/16 e 10.2.0.0/16 na mesma rede virtual, selecione um valor VnetLocal para cada sub-rede para encaminhar para a outra sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="7ae2d-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="7ae2d-137">-RouteTable</span></span>
<span data-ttu-id="7ae2d-138">Especifica a tabela de rota à qual essa rota está associada.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-138">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae2d-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ae2d-139">-Confirm</span></span>
<span data-ttu-id="7ae2d-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ae2d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ae2d-141">-WhatIf</span></span>
<span data-ttu-id="7ae2d-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ae2d-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ae2d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae2d-144">CommonParameters</span></span>
<span data-ttu-id="7ae2d-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae2d-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae2d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae2d-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ae2d-147">INPUTS</span></span>

### <span data-ttu-id="7ae2d-148">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ae2d-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="7ae2d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7ae2d-149">System.String</span></span>

## <span data-ttu-id="7ae2d-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ae2d-150">OUTPUTS</span></span>

### <span data-ttu-id="7ae2d-151">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ae2d-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="7ae2d-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ae2d-152">NOTES</span></span>

## <span data-ttu-id="7ae2d-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ae2d-153">RELATED LINKS</span></span>

[<span data-ttu-id="7ae2d-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7ae2d-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="7ae2d-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7ae2d-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="7ae2d-156">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7ae2d-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="7ae2d-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7ae2d-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


