---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110426"
---
# <span data-ttu-id="57e06-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="57e06-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="57e06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57e06-102">SYNOPSIS</span></span>
<span data-ttu-id="57e06-103">Atualiza uma configuração de conexão de circuito criada em pares privados para um circuito de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="57e06-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="57e06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57e06-104">SYNTAX</span></span>

### <span data-ttu-id="57e06-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="57e06-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57e06-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="57e06-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57e06-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57e06-107">DESCRIPTION</span></span>
<span data-ttu-id="57e06-108">O cmdlet **set-AzExpressRouteCircuitConnectionConfig** atualiza uma configuração de conexão de circuito criada em emparelhamento privado para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="57e06-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="57e06-109">Isso permite o emparelhamento de dois circuitos de rota expressa entre regiões ou assinaturas.</span><span class="sxs-lookup"><span data-stu-id="57e06-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="57e06-110">Observe que, antes de executar **set-AzExpressRouteCircuitConnectionConfig** , você deve adicionar a conexão de circuito usando **Add-AzExpressRouteCircuitConnectionConfig**.</span><span class="sxs-lookup"><span data-stu-id="57e06-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="57e06-111">Além disso, após executar **set-AzExpressRouteCircuitPeeringConfig** , você deve chamar o cmdlet Set-AzExpressRouteCircuit para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="57e06-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="57e06-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57e06-112">EXAMPLES</span></span>

### <span data-ttu-id="57e06-113">Exemplo 1: atualizar um recurso de conexão de circuito para um circuito ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="57e06-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="57e06-114">Exemplo 2: definir uma configuração de conexão de circuito usando o encanamento para um circuito ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="57e06-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="57e06-115">OS</span><span class="sxs-lookup"><span data-stu-id="57e06-115">PARAMETERS</span></span>

### <span data-ttu-id="57e06-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="57e06-116">-AddressPrefix</span></span>
<span data-ttu-id="57e06-117">Um espaço de endereço de cliente mínimo/29 para criar túneis de VxLan entre os circuitos de rota expressa para túneis IPv4.</span><span class="sxs-lookup"><span data-stu-id="57e06-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="57e06-118">ou um espaço de endereço de cliente no mínimo/125 para criar túneis de VxLan entre circuitos de rota expressa para túneis IPv6.</span><span class="sxs-lookup"><span data-stu-id="57e06-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="57e06-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="57e06-119">-AddressPrefixType</span></span>
<span data-ttu-id="57e06-120">Especifica a família de endereços à qual pertence o prefixo de endereço.</span><span class="sxs-lookup"><span data-stu-id="57e06-120">Specifies the address family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="57e06-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="57e06-121">-AuthorizationKey</span></span>
<span data-ttu-id="57e06-122">Chave de autorização para circuito de rota de par expresso em outra assinatura.</span><span class="sxs-lookup"><span data-stu-id="57e06-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="57e06-123">A autorização no circuito de par pode ser criada usando comandos existentes.</span><span class="sxs-lookup"><span data-stu-id="57e06-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="57e06-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e06-124">-DefaultProfile</span></span>
<span data-ttu-id="57e06-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57e06-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57e06-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57e06-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="57e06-127">O circuito do ExpressRoute sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="57e06-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="57e06-128">Esse é o objeto do Azure retornado pelo cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="57e06-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="57e06-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="57e06-129">-Name</span></span>
<span data-ttu-id="57e06-130">O nome do recurso de conexão de circuito a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="57e06-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="57e06-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="57e06-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="57e06-132">ID do recurso para emparelhamento privado do circuito remoto que será emparelhado com o circuito atual.</span><span class="sxs-lookup"><span data-stu-id="57e06-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="57e06-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="57e06-133">-Confirm</span></span>
<span data-ttu-id="57e06-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57e06-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57e06-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57e06-135">-WhatIf</span></span>
<span data-ttu-id="57e06-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57e06-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57e06-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57e06-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57e06-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e06-138">CommonParameters</span></span>
<span data-ttu-id="57e06-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57e06-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e06-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57e06-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e06-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57e06-141">INPUTS</span></span>

### <span data-ttu-id="57e06-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57e06-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="57e06-143">System. String</span><span class="sxs-lookup"><span data-stu-id="57e06-143">System.String</span></span>

## <span data-ttu-id="57e06-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57e06-144">OUTPUTS</span></span>

### <span data-ttu-id="57e06-145">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57e06-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="57e06-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57e06-146">NOTES</span></span>

## <span data-ttu-id="57e06-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57e06-147">RELATED LINKS</span></span>

[<span data-ttu-id="57e06-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="57e06-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="57e06-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="57e06-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="57e06-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="57e06-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="57e06-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57e06-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="57e06-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57e06-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
