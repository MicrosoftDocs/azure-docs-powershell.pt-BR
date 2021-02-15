---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: ca7335abfd8fe2dc9591dcb7d96fb6ca71dda4fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114626"
---
# <span data-ttu-id="06a87-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="06a87-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="06a87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06a87-102">SYNOPSIS</span></span>
<span data-ttu-id="06a87-103">Atualiza uma configuração de rota para uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="06a87-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="06a87-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06a87-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06a87-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="06a87-105">DESCRIPTION</span></span>
<span data-ttu-id="06a87-106">O **cmdlet Set-AzRouteConfig** atualiza uma configuração de rota para uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="06a87-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="06a87-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="06a87-107">EXAMPLES</span></span>

### <span data-ttu-id="06a87-108">Exemplo 1: Modificar uma rota</span><span class="sxs-lookup"><span data-stu-id="06a87-108">Example 1: Modify a route</span></span>
```powershell
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

<span data-ttu-id="06a87-109">Esse comando obtém a tabela de rota chamada Roteável01 usando o cmdlet Get-AzRouteTable rota.</span><span class="sxs-lookup"><span data-stu-id="06a87-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="06a87-110">O comando passa essa tabela para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="06a87-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="06a87-111">O cmdlet atual modifica a rota chamada Rota02 e passa o resultado para o cmdlet **Set-AzRouteTable,** que atualiza a tabela para refletir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="06a87-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="06a87-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06a87-112">PARAMETERS</span></span>

### <span data-ttu-id="06a87-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="06a87-113">-AddressPrefix</span></span>
<span data-ttu-id="06a87-114">Especifica o destino, no formato CIDR (Roteamento Interdomínio sem Classe), ao qual a rota se aplica.</span><span class="sxs-lookup"><span data-stu-id="06a87-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="06a87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a87-115">-DefaultProfile</span></span>
<span data-ttu-id="06a87-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="06a87-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06a87-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="06a87-117">-Name</span></span>
<span data-ttu-id="06a87-118">Especifica o nome da rota que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="06a87-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="06a87-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="06a87-119">-NextHopIpAddress</span></span>
<span data-ttu-id="06a87-120">Especifica o endereço IP de um dispositivo virtual que você adiciona à sua rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="06a87-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="06a87-121">Essa rota encaminha pacotes para esse endereço.</span><span class="sxs-lookup"><span data-stu-id="06a87-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="06a87-122">Especifique esse parâmetro somente se você especificar um valor de VirtualAppliance para o *parâmetro NextType.*</span><span class="sxs-lookup"><span data-stu-id="06a87-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="06a87-123">-NextType</span><span class="sxs-lookup"><span data-stu-id="06a87-123">-NextHopType</span></span>
<span data-ttu-id="06a87-124">Especifica como essa rota encaminha pacotes.</span><span class="sxs-lookup"><span data-stu-id="06a87-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="06a87-125">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="06a87-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06a87-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="06a87-126">Internet.</span></span>
<span data-ttu-id="06a87-127">O gateway de Internet padrão fornecido pelo Azure.</span><span class="sxs-lookup"><span data-stu-id="06a87-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="06a87-128">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="06a87-128">None.</span></span>
<span data-ttu-id="06a87-129">Se você especificar esse valor, a rota não encaminhará pacotes.</span><span class="sxs-lookup"><span data-stu-id="06a87-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="06a87-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="06a87-130">VirtualAppliance.</span></span>
<span data-ttu-id="06a87-131">Um dispositivo virtual que você adiciona à sua rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="06a87-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="06a87-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="06a87-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="06a87-133">Um gateway de rede virtual privada do Azureserver-to-server.</span><span class="sxs-lookup"><span data-stu-id="06a87-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="06a87-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="06a87-134">VnetLocal.</span></span>
<span data-ttu-id="06a87-135">A rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="06a87-135">The local virtual network.</span></span>
<span data-ttu-id="06a87-136">Se você tiver duas sub-redes, 10.1.0.0/16 e 10.2.0.0/16 na mesma rede virtual, selecione um valor de VnetLocal para cada sub-rede para encaminhar para a outra sub-rede.</span><span class="sxs-lookup"><span data-stu-id="06a87-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="06a87-137">-Tabela de Rota</span><span class="sxs-lookup"><span data-stu-id="06a87-137">-RouteTable</span></span>
<span data-ttu-id="06a87-138">Especifica a tabela de rota à qual essa rota está associada.</span><span class="sxs-lookup"><span data-stu-id="06a87-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="06a87-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="06a87-139">-Confirm</span></span>
<span data-ttu-id="06a87-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06a87-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06a87-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06a87-141">-WhatIf</span></span>
<span data-ttu-id="06a87-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="06a87-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06a87-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="06a87-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06a87-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a87-144">CommonParameters</span></span>
<span data-ttu-id="06a87-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06a87-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a87-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06a87-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a87-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="06a87-147">INPUTS</span></span>

### <span data-ttu-id="06a87-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="06a87-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="06a87-149">System.String</span><span class="sxs-lookup"><span data-stu-id="06a87-149">System.String</span></span>

## <span data-ttu-id="06a87-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="06a87-150">OUTPUTS</span></span>

### <span data-ttu-id="06a87-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="06a87-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="06a87-152">Notas</span><span class="sxs-lookup"><span data-stu-id="06a87-152">NOTES</span></span>

## <span data-ttu-id="06a87-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06a87-153">RELATED LINKS</span></span>

[<span data-ttu-id="06a87-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="06a87-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="06a87-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="06a87-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="06a87-156">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="06a87-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="06a87-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="06a87-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


