---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885392"
---
# <span data-ttu-id="0d827-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0d827-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="0d827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d827-102">SYNOPSIS</span></span>
<span data-ttu-id="0d827-103">Atualiza uma configuração de conexão de circuito criada em Private Peerings para um Circuito de Rota Expressa.</span><span class="sxs-lookup"><span data-stu-id="0d827-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="0d827-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0d827-104">SYNTAX</span></span>

### <span data-ttu-id="0d827-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0d827-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d827-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0d827-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d827-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0d827-107">DESCRIPTION</span></span>
<span data-ttu-id="0d827-108">O cmdlet **Set-AzExpressRouteCircuitConnectionConfig** atualiza uma configuração de conexão de circuito criada em peering privado para um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0d827-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="0d827-109">Isso permite a peering two Express Route Circuits across regions or subscriptions.</span><span class="sxs-lookup"><span data-stu-id="0d827-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="0d827-110">Observe que, antes de executar **Set-AzExpressRouteCircuitConnectionConfig,** você deve adicionar a conexão de circuito usando **Add-AzExpressRouteCircuitConnectionConfig**.</span><span class="sxs-lookup"><span data-stu-id="0d827-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="0d827-111">Além disso, depois de executar **Set-AzExpressRouteCircuitPeeringConfig,** você deve chamar o cmdlet Set-AzExpressRouteCircuit para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="0d827-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="0d827-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d827-112">EXAMPLES</span></span>

### <span data-ttu-id="0d827-113">Exemplo 1: atualizar um recurso de conexão de circuito para um circuito ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="0d827-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="0d827-114">Exemplo 2: Definir uma configuração de conexão de circuito usando a canalização para um Circuito ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="0d827-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="0d827-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0d827-115">PARAMETERS</span></span>

### <span data-ttu-id="0d827-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0d827-116">-AddressPrefix</span></span>
<span data-ttu-id="0d827-117">Um espaço mínimo de endereço do cliente /29 para criar túneis VxLan entre Circuitos de Rota Expressa para tuneis IPv4.</span><span class="sxs-lookup"><span data-stu-id="0d827-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="0d827-118">ou um espaço mínimo de endereço do cliente /125 para criar túneis VxLan entre Circuitos de Rota Expressa para tuneis IPv6.</span><span class="sxs-lookup"><span data-stu-id="0d827-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="0d827-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="0d827-119">-AddressPrefixType</span></span>
<span data-ttu-id="0d827-120">Especifica a família de endereços à que o prefixo de endereço pertence.</span><span class="sxs-lookup"><span data-stu-id="0d827-120">Specifies the address family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="0d827-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="0d827-121">-AuthorizationKey</span></span>
<span data-ttu-id="0d827-122">Chave de Autorização para o Circuito de Rota Expressa par em outra assinatura.</span><span class="sxs-lookup"><span data-stu-id="0d827-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="0d827-123">A autorização no circuito de pares pode ser criada usando comandos existentes.</span><span class="sxs-lookup"><span data-stu-id="0d827-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="0d827-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d827-124">-DefaultProfile</span></span>
<span data-ttu-id="0d827-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0d827-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d827-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0d827-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0d827-127">O circuito ExpressRoute que está sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="0d827-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="0d827-128">Este é o objeto Azure retornado pelo cmdlet **Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="0d827-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="0d827-129">-Name</span><span class="sxs-lookup"><span data-stu-id="0d827-129">-Name</span></span>
<span data-ttu-id="0d827-130">O nome do recurso de conexão de circuito a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0d827-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="0d827-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="0d827-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="0d827-132">ID de recurso para o Peering Privado do circuito remoto que será analisado com o circuito atual.</span><span class="sxs-lookup"><span data-stu-id="0d827-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="0d827-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d827-133">-Confirm</span></span>
<span data-ttu-id="0d827-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d827-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d827-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d827-135">-WhatIf</span></span>
<span data-ttu-id="0d827-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0d827-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d827-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d827-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d827-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d827-138">CommonParameters</span></span>
<span data-ttu-id="0d827-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d827-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d827-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d827-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d827-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d827-141">INPUTS</span></span>

### <span data-ttu-id="0d827-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0d827-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="0d827-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0d827-143">System.String</span></span>

## <span data-ttu-id="0d827-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0d827-144">OUTPUTS</span></span>

### <span data-ttu-id="0d827-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0d827-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0d827-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="0d827-146">NOTES</span></span>

## <span data-ttu-id="0d827-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d827-147">RELATED LINKS</span></span>

[<span data-ttu-id="0d827-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0d827-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0d827-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0d827-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0d827-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0d827-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0d827-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0d827-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="0d827-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0d827-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
