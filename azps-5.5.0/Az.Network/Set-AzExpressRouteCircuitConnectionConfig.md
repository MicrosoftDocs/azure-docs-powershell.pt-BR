---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115063"
---
# <span data-ttu-id="927dd-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="927dd-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="927dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="927dd-102">SYNOPSIS</span></span>
<span data-ttu-id="927dd-103">Atualiza uma configuração de conexão de circuito criada em Pares Particulares para um Circuito de Rota Expressa.</span><span class="sxs-lookup"><span data-stu-id="927dd-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="927dd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="927dd-104">SYNTAX</span></span>

### <span data-ttu-id="927dd-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="927dd-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="927dd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="927dd-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="927dd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="927dd-107">DESCRIPTION</span></span>
<span data-ttu-id="927dd-108">O cmdlet **Set-AzExpressRoute CircuitConnectionConfig** atualiza uma configuração de conexão de circuito criada em pares particulares para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="927dd-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="927dd-109">Isso permite o peering de dois Circuitos de Rota Expressa entre regiões ou assinaturas.</span><span class="sxs-lookup"><span data-stu-id="927dd-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="927dd-110">Observe que, antes de executar **o Set-AzExpressRoute CircuitConnectionConfig,** você deve adicionar a conexão de circuito usando **o Add-AzExpressRoute CircuitConnectionConfig.**</span><span class="sxs-lookup"><span data-stu-id="927dd-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="927dd-111">Além disso, depois de executar **Set-AzExpressRoute CircuitPeeringConfig,** você deve ligar para o cmdlet Set-AzExpressRouteCircuit para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="927dd-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="927dd-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="927dd-112">EXAMPLES</span></span>

### <span data-ttu-id="927dd-113">Exemplo 1: Atualizar um recurso de conexão de circuito para um circuito existente do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="927dd-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="927dd-114">Exemplo 2: Definir uma configuração de conexão de circuito usando a piping para um circuito do ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="927dd-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="927dd-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="927dd-115">PARAMETERS</span></span>

### <span data-ttu-id="927dd-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="927dd-116">-AddressPrefix</span></span>
<span data-ttu-id="927dd-117">Um espaço mínimo de endereço para o cliente /29 para criar túnel VxLan entre circuitos de rota expressa para túnel IPv4.</span><span class="sxs-lookup"><span data-stu-id="927dd-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="927dd-118">ou um mínimo de /125 espaço de endereço do cliente para criar túnel VxLan entre Circuitos de Rota Expressa para túnel IPv6.</span><span class="sxs-lookup"><span data-stu-id="927dd-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="927dd-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="927dd-119">-AddressPrefixType</span></span>
<span data-ttu-id="927dd-120">Especifica a família de endereços à que o prefixo do endereço pertence.</span><span class="sxs-lookup"><span data-stu-id="927dd-120">Specifies the address family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="927dd-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="927dd-121">-AuthorizationKey</span></span>
<span data-ttu-id="927dd-122">Chave de Autorização para peer Express Route Circuit em outra assinatura.</span><span class="sxs-lookup"><span data-stu-id="927dd-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="927dd-123">A autorização no circuito de pares pode ser criada usando comandos existentes.</span><span class="sxs-lookup"><span data-stu-id="927dd-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="927dd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="927dd-124">-DefaultProfile</span></span>
<span data-ttu-id="927dd-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="927dd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="927dd-126">-ExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="927dd-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="927dd-127">O circuito do ExpressRoute está sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="927dd-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="927dd-128">Este é o objeto do Azure retornado pelo cmdlet **Get-AzExpressRoute Circuit.**</span><span class="sxs-lookup"><span data-stu-id="927dd-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="927dd-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="927dd-129">-Name</span></span>
<span data-ttu-id="927dd-130">O nome do recurso de conexão de circuito a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="927dd-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="927dd-131">-PeerExpressRoute CircuitPeering</span><span class="sxs-lookup"><span data-stu-id="927dd-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="927dd-132">ID do Recurso para o Peering Particular de circuito remoto que será analisado com o circuito atual.</span><span class="sxs-lookup"><span data-stu-id="927dd-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="927dd-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="927dd-133">-Confirm</span></span>
<span data-ttu-id="927dd-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="927dd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="927dd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="927dd-135">-WhatIf</span></span>
<span data-ttu-id="927dd-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="927dd-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="927dd-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="927dd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="927dd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="927dd-138">CommonParameters</span></span>
<span data-ttu-id="927dd-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="927dd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="927dd-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="927dd-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="927dd-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="927dd-141">INPUTS</span></span>

### <span data-ttu-id="927dd-142">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="927dd-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="927dd-143">System.String</span><span class="sxs-lookup"><span data-stu-id="927dd-143">System.String</span></span>

## <span data-ttu-id="927dd-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="927dd-144">OUTPUTS</span></span>

### <span data-ttu-id="927dd-145">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="927dd-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="927dd-146">Notas</span><span class="sxs-lookup"><span data-stu-id="927dd-146">NOTES</span></span>

## <span data-ttu-id="927dd-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="927dd-147">RELATED LINKS</span></span>

[<span data-ttu-id="927dd-148">Get-AzExpressRoute CircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="927dd-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="927dd-149">Remove-AzExpressRoute CircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="927dd-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="927dd-150">Add-AzExpressRoute CircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="927dd-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="927dd-151">Set-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="927dd-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="927dd-152">Get-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="927dd-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
