---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: f4aabb68fd1f508651406d7ccf7be91ff646d46c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114164"
---
# <span data-ttu-id="58353-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="58353-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="58353-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58353-102">SYNOPSIS</span></span>
<span data-ttu-id="58353-103">Obtém uma configuração de conexão de circuito do ExpressRoute associada ao Peering Particular do ExpressRoute Circuit.</span><span class="sxs-lookup"><span data-stu-id="58353-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="58353-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58353-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58353-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="58353-105">DESCRIPTION</span></span>
<span data-ttu-id="58353-106">O cmdlet **Get-AzExpressRoute CircuitConnectionConfig** recupera a configuração de uma conexão de circuito associada ao Peering Particular para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="58353-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="58353-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="58353-107">EXAMPLES</span></span>

### <span data-ttu-id="58353-108">Exemplo 1: Exibir a configuração de conexão de circuito para um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="58353-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="58353-109">Exemplo 2: Obter o recurso de conexão de circuito associado a um Circuito do ExpressRoute usando a canalização</span><span class="sxs-lookup"><span data-stu-id="58353-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="58353-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58353-110">PARAMETERS</span></span>

### <span data-ttu-id="58353-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58353-111">-DefaultProfile</span></span>
<span data-ttu-id="58353-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="58353-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58353-113">-ExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="58353-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="58353-114">O objeto de circuito do ExpressRoute que contém a configuração de conexão de circuito.</span><span class="sxs-lookup"><span data-stu-id="58353-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="58353-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="58353-115">-Name</span></span>
<span data-ttu-id="58353-116">O nome da configuração de conexão de circuito a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="58353-116">The name of the circuit connection configuration to be retrieved.</span></span>

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

### <span data-ttu-id="58353-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58353-117">CommonParameters</span></span>
<span data-ttu-id="58353-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58353-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58353-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58353-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58353-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="58353-120">INPUTS</span></span>

### <span data-ttu-id="58353-121">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="58353-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="58353-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="58353-122">OUTPUTS</span></span>

### <span data-ttu-id="58353-123">Microsoft.Azure.Commands.Network.Models.PSExpressRoute CircuitConnection</span><span class="sxs-lookup"><span data-stu-id="58353-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="58353-124">Notas</span><span class="sxs-lookup"><span data-stu-id="58353-124">NOTES</span></span>

## <span data-ttu-id="58353-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58353-125">RELATED LINKS</span></span>

[<span data-ttu-id="58353-126">Get-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="58353-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="58353-127">Add-AzExpressRoute CircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="58353-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="58353-128">Remove-AzExpressRoute CircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="58353-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="58353-129">Set-AzExpressRoute CircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="58353-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="58353-130">New-AzExpressRoute CircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="58353-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)