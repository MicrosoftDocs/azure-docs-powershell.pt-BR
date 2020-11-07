---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bf69b628224baa74014d75b4c687a15d830d13c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771538"
---
# <span data-ttu-id="ab8e1-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ab8e1-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="ab8e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8e1-103">Remove uma configuração de conexão de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="ab8e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab8e1-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab8e1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab8e1-105">DESCRIPTION</span></span>
<span data-ttu-id="ab8e1-106">O cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** remove uma configuração de conexão de circuito do ExpressRoute associada a um determinado circuito de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="ab8e1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab8e1-107">EXAMPLES</span></span>

### <span data-ttu-id="ab8e1-108">Exemplo 1: remover uma configuração de conexão de circuito de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ab8e1-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="ab8e1-109">Exemplo 2: remover uma configuração de conexão de circuito usando o encanamento de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ab8e1-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="ab8e1-110">OS</span><span class="sxs-lookup"><span data-stu-id="ab8e1-110">PARAMETERS</span></span>

### <span data-ttu-id="ab8e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8e1-111">-DefaultProfile</span></span>
<span data-ttu-id="ab8e1-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab8e1-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ab8e1-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ab8e1-114">O circuito do ExpressRoute que contém a configuração de emparelhamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ab8e1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab8e1-115">-Name</span></span>
<span data-ttu-id="ab8e1-116">O nome da configuração de conexão de circuito a ser removida.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="ab8e1-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ab8e1-117">-Confirm</span></span>
<span data-ttu-id="ab8e1-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab8e1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab8e1-119">-WhatIf</span></span>
<span data-ttu-id="ab8e1-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab8e1-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab8e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8e1-122">CommonParameters</span></span>
<span data-ttu-id="ab8e1-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab8e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8e1-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab8e1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8e1-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab8e1-125">INPUTS</span></span>

### <span data-ttu-id="ab8e1-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ab8e1-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ab8e1-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab8e1-127">OUTPUTS</span></span>

### <span data-ttu-id="ab8e1-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ab8e1-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ab8e1-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab8e1-129">NOTES</span></span>

## <span data-ttu-id="ab8e1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab8e1-130">RELATED LINKS</span></span>

[<span data-ttu-id="ab8e1-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ab8e1-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ab8e1-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ab8e1-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ab8e1-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ab8e1-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ab8e1-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ab8e1-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ab8e1-135">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ab8e1-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ab8e1-136">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ab8e1-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="ab8e1-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ab8e1-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)