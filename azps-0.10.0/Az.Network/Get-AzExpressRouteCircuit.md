---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: f72d398eaea1d127ba600130fae3bbc690052332
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775561"
---
# <span data-ttu-id="c7d06-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c7d06-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="c7d06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7d06-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d06-103">Obtém um circuito do Azure ExpressRoute do Azure.</span><span class="sxs-lookup"><span data-stu-id="c7d06-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="c7d06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7d06-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7d06-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7d06-105">DESCRIPTION</span></span>
<span data-ttu-id="c7d06-106">O cmdlet **Get-AzExpressRouteCircuit** é usado para recuperar um objeto de circuito do ExpressRoute da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="c7d06-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="c7d06-107">O objeto de circuito retornado pode ser usado como entrada para outros cmdlets que operam em circuitos do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c7d06-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="c7d06-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7d06-108">EXAMPLES</span></span>

### <span data-ttu-id="c7d06-109">Exemplo 1: baixar o circuito do ExpressRoute para ser excluído</span><span class="sxs-lookup"><span data-stu-id="c7d06-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="c7d06-110">OS</span><span class="sxs-lookup"><span data-stu-id="c7d06-110">PARAMETERS</span></span>

### <span data-ttu-id="c7d06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d06-111">-DefaultProfile</span></span>
<span data-ttu-id="c7d06-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7d06-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7d06-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7d06-113">-Name</span></span>
<span data-ttu-id="c7d06-114">O nome do circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c7d06-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d06-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7d06-115">-ResourceGroupName</span></span>
<span data-ttu-id="c7d06-116">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c7d06-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d06-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d06-117">CommonParameters</span></span>
<span data-ttu-id="c7d06-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7d06-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d06-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7d06-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d06-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7d06-120">INPUTS</span></span>

## <span data-ttu-id="c7d06-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7d06-121">OUTPUTS</span></span>

### <span data-ttu-id="c7d06-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c7d06-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c7d06-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7d06-123">NOTES</span></span>

## <span data-ttu-id="c7d06-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7d06-124">RELATED LINKS</span></span>

[<span data-ttu-id="c7d06-125">Mover-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c7d06-125">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="c7d06-126">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c7d06-126">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="c7d06-127">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c7d06-127">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="c7d06-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c7d06-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
