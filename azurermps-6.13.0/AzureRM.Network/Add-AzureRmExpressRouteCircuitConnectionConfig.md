---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: aab4e78cd01e814ed8eb81b820e20bd3da4c03f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440368"
---
# <span data-ttu-id="371ad-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="371ad-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="371ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="371ad-102">SYNOPSIS</span></span>
<span data-ttu-id="371ad-103">Adiciona uma configuração de conexão de circuito ao emparelhamento privado de um circuito de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="371ad-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="371ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="371ad-104">SYNTAX</span></span>

### <span data-ttu-id="371ad-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="371ad-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="371ad-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="371ad-106">SetByResourceId</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="371ad-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="371ad-107">DESCRIPTION</span></span>
<span data-ttu-id="371ad-108">O cmdlet **Add-AzureRmExpressRouteCircuitConnectionConfig** adiciona uma configuração de conexão de circuito ao emparelhamento privado para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="371ad-108">The **Add-AzureRmExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="371ad-109">Isso permite o emparelhamento de dois circuitos de rota expressa entre regiões ou assinaturas. Observe que, depois de executar **Add-AzureRmExpressRouteCircuitPeeringConfig** , você deve chamar o cmdlet Set-AzureRmExpressRouteCircuit para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="371ad-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="371ad-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="371ad-110">EXAMPLES</span></span>

### <span data-ttu-id="371ad-111">Exemplo 1: adicionar um recurso de conexão de circuito a um circuito ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="371ad-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="371ad-112">Exemplo 2: adicionar uma configuração de conexão de circuito usando o encanamento para um circuito ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="371ad-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="371ad-113">OS</span><span class="sxs-lookup"><span data-stu-id="371ad-113">PARAMETERS</span></span>

### <span data-ttu-id="371ad-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="371ad-114">-AddressPrefix</span></span>
<span data-ttu-id="371ad-115">Um espaço de endereço de cliente no mínimo/29 para criar túneis de VxLan entre circuitos de rota expressa</span><span class="sxs-lookup"><span data-stu-id="371ad-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371ad-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="371ad-116">-AuthorizationKey</span></span>
<span data-ttu-id="371ad-117">Chave de autorização para circuito de rota de par expresso em outra assinatura.</span><span class="sxs-lookup"><span data-stu-id="371ad-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="371ad-118">A autorização no circuito de par pode ser criada usando comandos existentes.</span><span class="sxs-lookup"><span data-stu-id="371ad-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="371ad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="371ad-119">-DefaultProfile</span></span>
<span data-ttu-id="371ad-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="371ad-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="371ad-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="371ad-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="371ad-122">O circuito do ExpressRoute sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="371ad-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="371ad-123">Esse é o objeto do Azure retornado pelo cmdlet **Get-AzureRmExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="371ad-123">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="371ad-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="371ad-124">-Name</span></span>
<span data-ttu-id="371ad-125">O nome do recurso de conexão de circuito a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="371ad-125">The name of the circuit connection resource to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371ad-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="371ad-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="371ad-127">ID do recurso para emparelhamento privado do circuito remoto que será emparelhado com o circuito atual.</span><span class="sxs-lookup"><span data-stu-id="371ad-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="371ad-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="371ad-128">-Confirm</span></span>
<span data-ttu-id="371ad-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="371ad-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="371ad-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="371ad-130">-WhatIf</span></span>
<span data-ttu-id="371ad-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="371ad-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="371ad-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="371ad-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="371ad-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="371ad-133">CommonParameters</span></span>
<span data-ttu-id="371ad-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="371ad-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="371ad-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="371ad-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="371ad-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="371ad-136">INPUTS</span></span>

### <span data-ttu-id="371ad-137">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="371ad-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="371ad-138">Parâmetros: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="371ad-138">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="371ad-139">System. String</span><span class="sxs-lookup"><span data-stu-id="371ad-139">System.String</span></span>

## <span data-ttu-id="371ad-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="371ad-140">OUTPUTS</span></span>

### <span data-ttu-id="371ad-141">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="371ad-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="371ad-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="371ad-142">NOTES</span></span>

## <span data-ttu-id="371ad-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="371ad-143">RELATED LINKS</span></span>

[<span data-ttu-id="371ad-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="371ad-144">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="371ad-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="371ad-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="371ad-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="371ad-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="371ad-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="371ad-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="371ad-148">New-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="371ad-148">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="371ad-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="371ad-149">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="371ad-150">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="371ad-150">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
