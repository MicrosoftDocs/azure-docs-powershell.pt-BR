---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 8ef7121e057759a6fbdb341d9d6bc137692a36cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441227"
---
# <span data-ttu-id="6cb46-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6cb46-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="6cb46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cb46-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb46-103">Modifica um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6cb46-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cb46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cb46-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cb46-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cb46-105">DESCRIPTION</span></span>
<span data-ttu-id="6cb46-106">O cmdlet **set-AzureRmExpressRouteCircuit** salva o circuito do ExpressRoute modificado para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6cb46-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="6cb46-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cb46-107">EXAMPLES</span></span>

### <span data-ttu-id="6cb46-108">Exemplo 1: alterar o ServiceKey de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="6cb46-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="6cb46-109">OS</span><span class="sxs-lookup"><span data-stu-id="6cb46-109">PARAMETERS</span></span>

### <span data-ttu-id="6cb46-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cb46-110">-AsJob</span></span>
<span data-ttu-id="6cb46-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6cb46-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb46-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb46-112">-DefaultProfile</span></span>
<span data-ttu-id="6cb46-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6cb46-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cb46-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6cb46-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="6cb46-115">Especifica o objeto **ExpressRouteCircuit** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="6cb46-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb46-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb46-116">CommonParameters</span></span>
<span data-ttu-id="6cb46-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb46-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb46-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cb46-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb46-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cb46-119">INPUTS</span></span>

### <span data-ttu-id="6cb46-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6cb46-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="6cb46-121">Parâmetros: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6cb46-121">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="6cb46-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cb46-122">OUTPUTS</span></span>

### <span data-ttu-id="6cb46-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6cb46-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="6cb46-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cb46-124">NOTES</span></span>

## <span data-ttu-id="6cb46-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cb46-125">RELATED LINKS</span></span>

[<span data-ttu-id="6cb46-126">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6cb46-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6cb46-127">Mover-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6cb46-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6cb46-128">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6cb46-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6cb46-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6cb46-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
