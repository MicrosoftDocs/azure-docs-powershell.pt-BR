---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 262dd4333b2490c5035a00de179b9b2092ccb71e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776548"
---
# <span data-ttu-id="04fc8-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="04fc8-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="04fc8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="04fc8-103">Modifica um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="04fc8-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="04fc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04fc8-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04fc8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04fc8-105">DESCRIPTION</span></span>
<span data-ttu-id="04fc8-106">O cmdlet **set-AzExpressRouteCircuit** salva o circuito do ExpressRoute modificado para o Azure.</span><span class="sxs-lookup"><span data-stu-id="04fc8-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="04fc8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04fc8-107">EXAMPLES</span></span>

### <span data-ttu-id="04fc8-108">Exemplo 1: alterar o ServiceKey de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="04fc8-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="04fc8-109">OS</span><span class="sxs-lookup"><span data-stu-id="04fc8-109">PARAMETERS</span></span>

### <span data-ttu-id="04fc8-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04fc8-110">-AsJob</span></span>
<span data-ttu-id="04fc8-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="04fc8-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04fc8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04fc8-112">-DefaultProfile</span></span>
<span data-ttu-id="04fc8-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04fc8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04fc8-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="04fc8-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="04fc8-115">Especifica o objeto **ExpressRouteCircuit** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="04fc8-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="04fc8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04fc8-116">CommonParameters</span></span>
<span data-ttu-id="04fc8-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04fc8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04fc8-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04fc8-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04fc8-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04fc8-119">INPUTS</span></span>

### <span data-ttu-id="04fc8-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="04fc8-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="04fc8-121">O parâmetro ' ExpressRouteCircuit ' aceita o valor do tipo ' PSExpressRouteCircuit ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="04fc8-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="04fc8-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04fc8-122">OUTPUTS</span></span>

### <span data-ttu-id="04fc8-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="04fc8-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="04fc8-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04fc8-124">NOTES</span></span>

## <span data-ttu-id="04fc8-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04fc8-125">RELATED LINKS</span></span>

[<span data-ttu-id="04fc8-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="04fc8-126">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="04fc8-127">Mover-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="04fc8-127">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="04fc8-128">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="04fc8-128">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="04fc8-129">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="04fc8-129">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
