---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: cf854be6ed6dd5a69ba730cf6da60884a493551e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412377"
---
# <span data-ttu-id="3b350-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3b350-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="3b350-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b350-102">SYNOPSIS</span></span>
<span data-ttu-id="3b350-103">Remove uma configuração de conexão de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3b350-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="3b350-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b350-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b350-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b350-105">DESCRIPTION</span></span>
<span data-ttu-id="3b350-106">O cmdlet **Remove-AzExpressRoute CircuitConnectionConfig** remove uma configuração de conexão de circuito do ExpressRoute associada a um determinado Circuito de Rota Expressa.</span><span class="sxs-lookup"><span data-stu-id="3b350-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="3b350-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b350-107">EXAMPLES</span></span>

### <span data-ttu-id="3b350-108">Exemplo 1: Remover uma configuração de conexão de circuito de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3b350-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="3b350-109">Exemplo 2: remover uma configuração de conexão de circuito usando a piping de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3b350-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="3b350-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b350-110">PARAMETERS</span></span>

### <span data-ttu-id="3b350-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b350-111">-DefaultProfile</span></span>
<span data-ttu-id="3b350-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3b350-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b350-113">-ExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="3b350-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3b350-114">O circuito do ExpressRoute que contém a configuração de peering a ser removido.</span><span class="sxs-lookup"><span data-stu-id="3b350-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="3b350-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b350-115">-Name</span></span>
<span data-ttu-id="3b350-116">O nome da configuração de conexão de circuito a ser removido.</span><span class="sxs-lookup"><span data-stu-id="3b350-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="3b350-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3b350-117">-Confirm</span></span>
<span data-ttu-id="3b350-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b350-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b350-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b350-119">-WhatIf</span></span>
<span data-ttu-id="3b350-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3b350-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b350-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b350-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b350-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b350-122">CommonParameters</span></span>
<span data-ttu-id="3b350-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b350-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b350-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b350-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b350-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="3b350-125">INPUTS</span></span>

### <span data-ttu-id="3b350-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="3b350-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3b350-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="3b350-127">OUTPUTS</span></span>

### <span data-ttu-id="3b350-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="3b350-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3b350-129">Notas</span><span class="sxs-lookup"><span data-stu-id="3b350-129">NOTES</span></span>

## <span data-ttu-id="3b350-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b350-130">RELATED LINKS</span></span>

[<span data-ttu-id="3b350-131">Get-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="3b350-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="3b350-132">Get-AzExpressRoute CircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3b350-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3b350-133">Add-AzExpressRoute CircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3b350-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3b350-134">Set-AzExpressRoute CircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3b350-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)



[<span data-ttu-id="3b350-135">Set-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="3b350-135">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="3b350-136">Get-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="3b350-136">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
