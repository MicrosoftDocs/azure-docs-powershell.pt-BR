---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bc08305d7aa604dd9c7540573ffb5a199e85b287
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402126"
---
# <span data-ttu-id="4e62b-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4e62b-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="4e62b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e62b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e62b-103">Adiciona uma configuração de conexão de circuito ao Peering Particular de um Circuito de Rota Expressa.</span><span class="sxs-lookup"><span data-stu-id="4e62b-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="4e62b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e62b-104">SYNTAX</span></span>

### <span data-ttu-id="4e62b-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4e62b-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e62b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e62b-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e62b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e62b-107">DESCRIPTION</span></span>
<span data-ttu-id="4e62b-108">O cmdlet **Add-AzExpressRoute CircuitConnectionConfig** adiciona uma configuração de conexão de circuito ao peering privado para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4e62b-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="4e62b-109">Isso permite o peering de dois Circuitos de Rota Expressa entre regiões ou assinaturas. Observe que, depois de executar **o Add-AzExpressRoute CircuitPeeringConfig,** você deve ligar para o cmdlet Set-AzExpressRouteCircuit para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="4e62b-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="4e62b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4e62b-110">EXAMPLES</span></span>

### <span data-ttu-id="4e62b-111">Exemplo 1: Adicionar um recurso de conexão de circuito a um circuito existente do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="4e62b-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="4e62b-112">Exemplo 2: Adicionar uma configuração de conexão de circuito usando o Piping a um circuito do ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="4e62b-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="4e62b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e62b-113">PARAMETERS</span></span>

### <span data-ttu-id="4e62b-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4e62b-114">-AddressPrefix</span></span>
<span data-ttu-id="4e62b-115">Um espaço mínimo de endereço do cliente /29 para criar túnel VxLan entre Circuitos de Rota Expressa</span><span class="sxs-lookup"><span data-stu-id="4e62b-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="4e62b-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="4e62b-116">-AuthorizationKey</span></span>
<span data-ttu-id="4e62b-117">Chave de Autorização para peer Express Route Circuit em outra assinatura.</span><span class="sxs-lookup"><span data-stu-id="4e62b-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="4e62b-118">A autorização no circuito de pares pode ser criada usando comandos existentes.</span><span class="sxs-lookup"><span data-stu-id="4e62b-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="4e62b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e62b-119">-DefaultProfile</span></span>
<span data-ttu-id="4e62b-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4e62b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e62b-121">-ExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="4e62b-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4e62b-122">O circuito do ExpressRoute está sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="4e62b-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="4e62b-123">Este é o objeto do Azure retornado pelo cmdlet **Get-AzExpressRoute Circuit.**</span><span class="sxs-lookup"><span data-stu-id="4e62b-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="4e62b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e62b-124">-Name</span></span>
<span data-ttu-id="4e62b-125">O nome do recurso de conexão de circuito a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="4e62b-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="4e62b-126">-PeerExpressRoute CircuitPeering</span><span class="sxs-lookup"><span data-stu-id="4e62b-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="4e62b-127">ID do Recurso para o Peering Particular de circuito remoto que será analisado com o circuito atual.</span><span class="sxs-lookup"><span data-stu-id="4e62b-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="4e62b-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4e62b-128">-Confirm</span></span>
<span data-ttu-id="4e62b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e62b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e62b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e62b-130">-WhatIf</span></span>
<span data-ttu-id="4e62b-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4e62b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e62b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4e62b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e62b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e62b-133">CommonParameters</span></span>
<span data-ttu-id="4e62b-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e62b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e62b-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e62b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e62b-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="4e62b-136">INPUTS</span></span>

### <span data-ttu-id="4e62b-137">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="4e62b-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="4e62b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4e62b-138">System.String</span></span>

## <span data-ttu-id="4e62b-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="4e62b-139">OUTPUTS</span></span>

### <span data-ttu-id="4e62b-140">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="4e62b-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4e62b-141">Notas</span><span class="sxs-lookup"><span data-stu-id="4e62b-141">NOTES</span></span>

## <span data-ttu-id="4e62b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e62b-142">RELATED LINKS</span></span>

[<span data-ttu-id="4e62b-143">Get-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="4e62b-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4e62b-144">Get-AzExpressRoute CircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4e62b-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="4e62b-145">Remove-AzExpressRoute CircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4e62b-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)





[<span data-ttu-id="4e62b-146">Set-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="4e62b-146">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="4e62b-147">Get-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="4e62b-147">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
