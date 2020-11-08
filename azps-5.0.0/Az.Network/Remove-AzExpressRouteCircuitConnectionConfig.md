---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125584"
---
# <span data-ttu-id="5e9e4-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5e9e4-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="5e9e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e9e4-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9e4-103">Remove uma configuração de conexão de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5e9e4-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="5e9e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e9e4-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e9e4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e9e4-105">DESCRIPTION</span></span>
<span data-ttu-id="5e9e4-106">O cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** remove uma configuração de conexão de circuito do ExpressRoute associada a um determinado circuito de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="5e9e4-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="5e9e4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e9e4-107">EXAMPLES</span></span>

### <span data-ttu-id="5e9e4-108">Exemplo 1: remover uma configuração de conexão de circuito de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="5e9e4-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="5e9e4-109">Exemplo 2: remover uma configuração de conexão de circuito usando o encanamento de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="5e9e4-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="5e9e4-110">Exemplo 3: remover uma configuração de conexão de circuito de um circuito do ExpressRoute para uma família de endereços específica</span><span class="sxs-lookup"><span data-stu-id="5e9e4-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="5e9e4-111">Exemplo 4: remover uma configuração de conexão de circuito usando o encanamento de um circuito do ExpressRoute para uma família de endereços específica</span><span class="sxs-lookup"><span data-stu-id="5e9e4-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="5e9e4-112">OS</span><span class="sxs-lookup"><span data-stu-id="5e9e4-112">PARAMETERS</span></span>

### <span data-ttu-id="5e9e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9e4-113">-DefaultProfile</span></span>
<span data-ttu-id="5e9e4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e9e4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e9e4-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e9e4-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5e9e4-116">O circuito do ExpressRoute que contém a configuração de emparelhamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="5e9e4-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="5e9e4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e9e4-117">-Name</span></span>
<span data-ttu-id="5e9e4-118">O nome da configuração de conexão de circuito a ser removida.</span><span class="sxs-lookup"><span data-stu-id="5e9e4-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="5e9e4-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="5e9e4-119">-AddressPrefixType</span></span>
<span data-ttu-id="5e9e4-120">Especifica a família de endereços que precisa ser removida do arquivo config</span><span class="sxs-lookup"><span data-stu-id="5e9e4-120">Specifies the address family that needs to be removed from the config</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: IPv4 
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9e4-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e9e4-121">-Confirm</span></span>
<span data-ttu-id="5e9e4-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e9e4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e9e4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e9e4-123">-WhatIf</span></span>
<span data-ttu-id="5e9e4-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e9e4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e9e4-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e9e4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e9e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9e4-126">CommonParameters</span></span>
<span data-ttu-id="5e9e4-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e9e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9e4-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e9e4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9e4-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e9e4-129">INPUTS</span></span>

### <span data-ttu-id="5e9e4-130">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e9e4-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5e9e4-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e9e4-131">OUTPUTS</span></span>

### <span data-ttu-id="5e9e4-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e9e4-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5e9e4-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e9e4-133">NOTES</span></span>

## <span data-ttu-id="5e9e4-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e9e4-134">RELATED LINKS</span></span>

[<span data-ttu-id="5e9e4-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e9e4-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="5e9e4-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5e9e4-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5e9e4-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5e9e4-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5e9e4-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5e9e4-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5e9e4-139">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5e9e4-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5e9e4-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e9e4-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="5e9e4-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e9e4-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)