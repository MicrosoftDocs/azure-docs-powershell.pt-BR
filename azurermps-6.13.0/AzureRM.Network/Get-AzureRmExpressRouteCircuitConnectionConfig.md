---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 4d9442ba87ba46704aaa93b31f41f111519c980b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440765"
---
# <span data-ttu-id="686ac-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="686ac-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="686ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="686ac-102">SYNOPSIS</span></span>
<span data-ttu-id="686ac-103">Obtém uma configuração de conexão de circuito do ExpressRoute associada ao emparelhamento privado do ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="686ac-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="686ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="686ac-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="686ac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="686ac-105">DESCRIPTION</span></span>
<span data-ttu-id="686ac-106">O cmdlet **Get-AzureRmExpressRouteCircuitConnectionConfig** recupera a configuração de uma conexão de circuito associada ao emparelhamento privado para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="686ac-106">The **Get-AzureRmExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="686ac-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="686ac-107">EXAMPLES</span></span>

### <span data-ttu-id="686ac-108">Exemplo 1: exibir a configuração de conexão de circuito para um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="686ac-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="686ac-109">Exemplo 2: obter recurso de conexão de circuito associado a um circuito do ExpressRoute usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="686ac-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="686ac-110">OS</span><span class="sxs-lookup"><span data-stu-id="686ac-110">PARAMETERS</span></span>

### <span data-ttu-id="686ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="686ac-111">-DefaultProfile</span></span>
<span data-ttu-id="686ac-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="686ac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="686ac-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="686ac-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="686ac-114">O objeto de circuito do ExpressRoute que contém a configuração de conexão de circuito.</span><span class="sxs-lookup"><span data-stu-id="686ac-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="686ac-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="686ac-115">-Name</span></span>
<span data-ttu-id="686ac-116">O nome da configuração de conexão de circuito a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="686ac-116">The name of the circuit connection configuration to be retrieved.</span></span>

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

### <span data-ttu-id="686ac-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="686ac-117">CommonParameters</span></span>
<span data-ttu-id="686ac-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="686ac-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="686ac-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="686ac-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="686ac-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="686ac-120">INPUTS</span></span>

### <span data-ttu-id="686ac-121">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="686ac-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="686ac-122">Parâmetros: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="686ac-122">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="686ac-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="686ac-123">OUTPUTS</span></span>

### <span data-ttu-id="686ac-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="686ac-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="686ac-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="686ac-125">NOTES</span></span>

## <span data-ttu-id="686ac-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="686ac-126">RELATED LINKS</span></span>

[<span data-ttu-id="686ac-127">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="686ac-127">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="686ac-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="686ac-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="686ac-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="686ac-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="686ac-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="686ac-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="686ac-131">New-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="686ac-131">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)
