---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: b01e0ecb48a5a4c27fc79448ca0e4d71e820d292
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944068"
---
# <span data-ttu-id="fe888-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="fe888-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="fe888-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe888-102">SYNOPSIS</span></span>
<span data-ttu-id="fe888-103">Remove uma configuração de conexão de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fe888-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="fe888-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe888-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe888-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe888-105">DESCRIPTION</span></span>
<span data-ttu-id="fe888-106">O cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** remove uma configuração de conexão de circuito do ExpressRoute associada a um determinado circuito de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="fe888-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="fe888-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe888-107">EXAMPLES</span></span>

### <span data-ttu-id="fe888-108">Exemplo 1: remover uma configuração de conexão de circuito de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="fe888-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="fe888-109">Exemplo 2: remover uma configuração de conexão de circuito usando o encanamento de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="fe888-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="fe888-110">OS</span><span class="sxs-lookup"><span data-stu-id="fe888-110">PARAMETERS</span></span>

### <span data-ttu-id="fe888-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe888-111">-DefaultProfile</span></span>
<span data-ttu-id="fe888-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe888-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe888-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe888-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="fe888-114">O circuito do ExpressRoute que contém a configuração de emparelhamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="fe888-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="fe888-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe888-115">-Name</span></span>
<span data-ttu-id="fe888-116">O nome da configuração de conexão de circuito a ser removida.</span><span class="sxs-lookup"><span data-stu-id="fe888-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="fe888-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fe888-117">-Confirm</span></span>
<span data-ttu-id="fe888-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe888-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe888-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe888-119">-WhatIf</span></span>
<span data-ttu-id="fe888-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe888-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe888-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe888-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe888-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe888-122">CommonParameters</span></span>
<span data-ttu-id="fe888-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe888-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe888-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe888-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe888-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe888-125">INPUTS</span></span>

### <span data-ttu-id="fe888-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe888-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="fe888-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe888-127">OUTPUTS</span></span>

### <span data-ttu-id="fe888-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe888-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="fe888-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe888-129">NOTES</span></span>

## <span data-ttu-id="fe888-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe888-130">RELATED LINKS</span></span>

[<span data-ttu-id="fe888-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe888-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="fe888-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="fe888-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="fe888-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="fe888-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="fe888-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="fe888-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="fe888-135">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="fe888-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="fe888-136">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe888-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="fe888-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe888-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)