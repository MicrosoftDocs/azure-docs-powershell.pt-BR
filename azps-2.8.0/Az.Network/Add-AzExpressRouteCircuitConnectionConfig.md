---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: a3b5b20eac34076dd6a5490a5d9cf1a5e2c49684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772107"
---
# <span data-ttu-id="7b4da-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7b4da-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="7b4da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b4da-102">SYNOPSIS</span></span>
<span data-ttu-id="7b4da-103">Adiciona uma configuração de conexão de circuito ao emparelhamento privado de um circuito de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="7b4da-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="7b4da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b4da-104">SYNTAX</span></span>

### <span data-ttu-id="7b4da-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="7b4da-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b4da-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b4da-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b4da-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b4da-107">DESCRIPTION</span></span>
<span data-ttu-id="7b4da-108">O cmdlet **Add-AzExpressRouteCircuitConnectionConfig** adiciona uma configuração de conexão de circuito ao emparelhamento privado para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7b4da-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="7b4da-109">Isso permite o emparelhamento de dois circuitos de rota expressa entre regiões ou assinaturas. Observe que, depois de executar **Add-AzExpressRouteCircuitPeeringConfig** , você deve chamar o cmdlet Set-AzExpressRouteCircuit para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="7b4da-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="7b4da-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b4da-110">EXAMPLES</span></span>

### <span data-ttu-id="7b4da-111">Exemplo 1: adicionar um recurso de conexão de circuito a um circuito ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="7b4da-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="7b4da-112">Exemplo 2: adicionar uma configuração de conexão de circuito usando o encanamento para um circuito ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="7b4da-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="7b4da-113">OS</span><span class="sxs-lookup"><span data-stu-id="7b4da-113">PARAMETERS</span></span>

### <span data-ttu-id="7b4da-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7b4da-114">-AddressPrefix</span></span>
<span data-ttu-id="7b4da-115">Um espaço de endereço de cliente no mínimo/29 para criar túneis de VxLan entre circuitos de rota expressa</span><span class="sxs-lookup"><span data-stu-id="7b4da-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="7b4da-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="7b4da-116">-AuthorizationKey</span></span>
<span data-ttu-id="7b4da-117">Chave de autorização para circuito de rota de par expresso em outra assinatura.</span><span class="sxs-lookup"><span data-stu-id="7b4da-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="7b4da-118">A autorização no circuito de par pode ser criada usando comandos existentes.</span><span class="sxs-lookup"><span data-stu-id="7b4da-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="7b4da-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b4da-119">-DefaultProfile</span></span>
<span data-ttu-id="7b4da-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b4da-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b4da-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b4da-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7b4da-122">O circuito do ExpressRoute sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="7b4da-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="7b4da-123">Esse é o objeto do Azure retornado pelo cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="7b4da-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="7b4da-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b4da-124">-Name</span></span>
<span data-ttu-id="7b4da-125">O nome do recurso de conexão de circuito a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="7b4da-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="7b4da-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="7b4da-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="7b4da-127">ID do recurso para emparelhamento privado do circuito remoto que será emparelhado com o circuito atual.</span><span class="sxs-lookup"><span data-stu-id="7b4da-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="7b4da-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7b4da-128">-Confirm</span></span>
<span data-ttu-id="7b4da-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b4da-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b4da-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b4da-130">-WhatIf</span></span>
<span data-ttu-id="7b4da-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b4da-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b4da-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b4da-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b4da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b4da-133">CommonParameters</span></span>
<span data-ttu-id="7b4da-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b4da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b4da-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b4da-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b4da-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b4da-136">INPUTS</span></span>

### <span data-ttu-id="7b4da-137">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b4da-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="7b4da-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7b4da-138">System.String</span></span>

## <span data-ttu-id="7b4da-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b4da-139">OUTPUTS</span></span>

### <span data-ttu-id="7b4da-140">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b4da-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7b4da-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b4da-141">NOTES</span></span>

## <span data-ttu-id="7b4da-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b4da-142">RELATED LINKS</span></span>

[<span data-ttu-id="7b4da-143">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b4da-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="7b4da-144">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7b4da-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7b4da-145">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7b4da-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7b4da-146">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7b4da-146">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7b4da-147">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7b4da-147">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7b4da-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b4da-148">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="7b4da-149">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b4da-149">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)