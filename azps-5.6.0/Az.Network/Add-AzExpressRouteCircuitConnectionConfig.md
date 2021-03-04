---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 19ceeb045c3a7cc86dd9152ee08d12078d858240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886018"
---
# <span data-ttu-id="60862-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60862-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="60862-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60862-102">SYNOPSIS</span></span>
<span data-ttu-id="60862-103">Adiciona uma configuração de conexão de circuito ao Private Peering de um Circuito de Rota Expressa.</span><span class="sxs-lookup"><span data-stu-id="60862-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="60862-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="60862-104">SYNTAX</span></span>

### <span data-ttu-id="60862-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="60862-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60862-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="60862-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60862-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="60862-107">DESCRIPTION</span></span>
<span data-ttu-id="60862-108">O cmdlet **Add-AzExpressRouteCircuitConnectionConfig** adiciona uma configuração de conexão de circuito ao peering privado para um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60862-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="60862-109">Isso permite a peering two Express Route Circuits across regions or subscriptions. Observe que, depois de executar **Add-AzExpressRouteCircuitConnectionConfig,** você deve chamar o cmdlet Set-AzExpressRouteCircuit para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="60862-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="60862-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60862-110">EXAMPLES</span></span>

### <span data-ttu-id="60862-111">Exemplo 1: Adicionar um recurso de conexão de circuito a um circuito ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="60862-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="60862-112">Exemplo 2: Adicionar uma configuração de conexão de circuito usando a canalização a um Circuito ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="60862-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="60862-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="60862-113">PARAMETERS</span></span>

### <span data-ttu-id="60862-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="60862-114">-AddressPrefix</span></span>
<span data-ttu-id="60862-115">Um espaço mínimo de endereço do cliente /29 para criar túneis VxLan entre Circuitos de Rota Expressa para tuneis IPv4.</span><span class="sxs-lookup"><span data-stu-id="60862-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="60862-116">ou um espaço mínimo de endereço do cliente /125 para criar túneis VxLan entre Circuitos de Rota Expressa para tuneis IPv6.</span><span class="sxs-lookup"><span data-stu-id="60862-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="60862-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="60862-117">-AddressPrefixType</span></span>
<span data-ttu-id="60862-118">Isso especifica a Família de Endereços à que o prefixo de endereço pertence.</span><span class="sxs-lookup"><span data-stu-id="60862-118">This specifies the Address Family that address prefix belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: IPv4
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60862-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="60862-119">-AuthorizationKey</span></span>
<span data-ttu-id="60862-120">Chave de Autorização para o Circuito de Rota Expressa par em outra assinatura.</span><span class="sxs-lookup"><span data-stu-id="60862-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="60862-121">A autorização no circuito de pares pode ser criada usando comandos existentes.</span><span class="sxs-lookup"><span data-stu-id="60862-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="60862-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60862-122">-DefaultProfile</span></span>
<span data-ttu-id="60862-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="60862-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60862-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60862-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="60862-125">O circuito ExpressRoute que está sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="60862-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="60862-126">Este é o objeto Azure retornado pelo cmdlet **Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="60862-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="60862-127">-Name</span><span class="sxs-lookup"><span data-stu-id="60862-127">-Name</span></span>
<span data-ttu-id="60862-128">O nome do recurso de conexão de circuito a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="60862-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="60862-129">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="60862-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="60862-130">ID de recurso para o Peering Privado do circuito remoto que será analisado com o circuito atual.</span><span class="sxs-lookup"><span data-stu-id="60862-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="60862-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60862-131">-Confirm</span></span>
<span data-ttu-id="60862-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60862-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60862-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60862-133">-WhatIf</span></span>
<span data-ttu-id="60862-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60862-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60862-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60862-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60862-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60862-136">CommonParameters</span></span>
<span data-ttu-id="60862-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60862-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60862-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60862-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60862-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60862-139">INPUTS</span></span>

### <span data-ttu-id="60862-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60862-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="60862-141">System.String</span><span class="sxs-lookup"><span data-stu-id="60862-141">System.String</span></span>

## <span data-ttu-id="60862-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="60862-142">OUTPUTS</span></span>

### <span data-ttu-id="60862-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60862-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="60862-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="60862-144">NOTES</span></span>

## <span data-ttu-id="60862-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60862-145">RELATED LINKS</span></span>

[<span data-ttu-id="60862-146">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60862-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="60862-147">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60862-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="60862-148">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60862-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="60862-149">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60862-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="60862-150">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60862-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)