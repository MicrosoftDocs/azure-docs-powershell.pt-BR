---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: a37502abcee157e9666a49ea5db5d2afe206aa8c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786271"
---
# <span data-ttu-id="4aff4-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aff4-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="4aff4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4aff4-102">SYNOPSIS</span></span>
<span data-ttu-id="4aff4-103">Modifica um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4aff4-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aff4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aff4-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aff4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4aff4-105">DESCRIPTION</span></span>
<span data-ttu-id="4aff4-106">O cmdlet **set-AzureRmExpressRouteCircuit** salva o circuito do ExpressRoute modificado para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4aff4-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="4aff4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4aff4-107">EXAMPLES</span></span>

### <span data-ttu-id="4aff4-108">Exemplo 1: alterar o ServiceKey de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="4aff4-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="4aff4-109">OS</span><span class="sxs-lookup"><span data-stu-id="4aff4-109">PARAMETERS</span></span>

### <span data-ttu-id="4aff4-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4aff4-110">-AsJob</span></span>
<span data-ttu-id="4aff4-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4aff4-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aff4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aff4-112">-DefaultProfile</span></span>
<span data-ttu-id="4aff4-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4aff4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aff4-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aff4-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4aff4-115">Especifica o objeto **ExpressRouteCircuit** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="4aff4-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4aff4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aff4-116">CommonParameters</span></span>
<span data-ttu-id="4aff4-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aff4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aff4-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aff4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aff4-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4aff4-119">INPUTS</span></span>

### <span data-ttu-id="4aff4-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aff4-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="4aff4-121">O parâmetro ' ExpressRouteCircuit ' aceita o valor do tipo ' PSExpressRouteCircuit ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4aff4-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="4aff4-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4aff4-122">OUTPUTS</span></span>

### <span data-ttu-id="4aff4-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aff4-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4aff4-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4aff4-124">NOTES</span></span>

## <span data-ttu-id="4aff4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4aff4-125">RELATED LINKS</span></span>

[<span data-ttu-id="4aff4-126">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aff4-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4aff4-127">Mover-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aff4-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4aff4-128">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aff4-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4aff4-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aff4-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
