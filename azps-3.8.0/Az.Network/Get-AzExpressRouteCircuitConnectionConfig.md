---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: f4aabb68fd1f508651406d7ccf7be91ff646d46c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943384"
---
# <span data-ttu-id="59071-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="59071-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="59071-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59071-102">SYNOPSIS</span></span>
<span data-ttu-id="59071-103">Obtém uma configuração de conexão de circuito do ExpressRoute associada ao emparelhamento privado do ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="59071-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="59071-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59071-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59071-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59071-105">DESCRIPTION</span></span>
<span data-ttu-id="59071-106">O cmdlet **Get-AzExpressRouteCircuitConnectionConfig** recupera a configuração de uma conexão de circuito associada ao emparelhamento privado para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="59071-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="59071-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59071-107">EXAMPLES</span></span>

### <span data-ttu-id="59071-108">Exemplo 1: exibir a configuração de conexão de circuito para um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="59071-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="59071-109">Exemplo 2: obter recurso de conexão de circuito associado a um circuito do ExpressRoute usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="59071-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="59071-110">OS</span><span class="sxs-lookup"><span data-stu-id="59071-110">PARAMETERS</span></span>

### <span data-ttu-id="59071-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59071-111">-DefaultProfile</span></span>
<span data-ttu-id="59071-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59071-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59071-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="59071-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="59071-114">O objeto de circuito do ExpressRoute que contém a configuração de conexão de circuito.</span><span class="sxs-lookup"><span data-stu-id="59071-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="59071-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="59071-115">-Name</span></span>
<span data-ttu-id="59071-116">O nome da configuração de conexão de circuito a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="59071-116">The name of the circuit connection configuration to be retrieved.</span></span>

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

### <span data-ttu-id="59071-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59071-117">CommonParameters</span></span>
<span data-ttu-id="59071-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59071-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59071-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59071-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59071-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59071-120">INPUTS</span></span>

### <span data-ttu-id="59071-121">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="59071-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="59071-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59071-122">OUTPUTS</span></span>

### <span data-ttu-id="59071-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="59071-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="59071-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59071-124">NOTES</span></span>

## <span data-ttu-id="59071-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59071-125">RELATED LINKS</span></span>

[<span data-ttu-id="59071-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="59071-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="59071-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="59071-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="59071-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="59071-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="59071-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="59071-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="59071-130">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="59071-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)