---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: c8d35373c2891b9f0d3ac76ded8b4e9808f32f33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890782"
---
# <span data-ttu-id="9bbdc-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9bbdc-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="9bbdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bbdc-102">SYNOPSIS</span></span>
<span data-ttu-id="9bbdc-103">Obtém uma configuração de conexão de circuito ExpressRoute associada ao Peering Privado do ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="9bbdc-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="9bbdc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9bbdc-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bbdc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9bbdc-105">DESCRIPTION</span></span>
<span data-ttu-id="9bbdc-106">O cmdlet **Get-AzExpressRouteCircuitConnectionConfig** recupera a configuração de uma conexão de circuito associada ao Private Peering para um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9bbdc-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="9bbdc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bbdc-107">EXAMPLES</span></span>

### <span data-ttu-id="9bbdc-108">Exemplo 1: Exibir a configuração de conexão de circuito para um circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="9bbdc-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="9bbdc-109">Exemplo 2: Obter recurso de conexão de circuito associado a um Circuito ExpressRoute usando a canalização</span><span class="sxs-lookup"><span data-stu-id="9bbdc-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="9bbdc-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9bbdc-110">PARAMETERS</span></span>

### <span data-ttu-id="9bbdc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bbdc-111">-DefaultProfile</span></span>
<span data-ttu-id="9bbdc-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9bbdc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bbdc-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9bbdc-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="9bbdc-114">O objeto de circuito ExpressRoute que contém a configuração de conexão de circuito.</span><span class="sxs-lookup"><span data-stu-id="9bbdc-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="9bbdc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9bbdc-115">-Name</span></span>
<span data-ttu-id="9bbdc-116">O nome da configuração de conexão do circuito a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="9bbdc-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bbdc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bbdc-117">CommonParameters</span></span>
<span data-ttu-id="9bbdc-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bbdc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bbdc-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bbdc-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bbdc-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9bbdc-120">INPUTS</span></span>

### <span data-ttu-id="9bbdc-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9bbdc-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9bbdc-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9bbdc-122">OUTPUTS</span></span>

### <span data-ttu-id="9bbdc-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="9bbdc-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="9bbdc-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="9bbdc-124">NOTES</span></span>

## <span data-ttu-id="9bbdc-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bbdc-125">RELATED LINKS</span></span>

[<span data-ttu-id="9bbdc-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9bbdc-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="9bbdc-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9bbdc-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="9bbdc-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9bbdc-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="9bbdc-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9bbdc-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="9bbdc-130">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9bbdc-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)