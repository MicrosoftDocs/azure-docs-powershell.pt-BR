---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 90814e90b4d4951a9e899fd8cf50f365b646f497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429266"
---
# <span data-ttu-id="fd0b6-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fd0b6-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="fd0b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd0b6-102">SYNOPSIS</span></span>
<span data-ttu-id="fd0b6-103">Obtém um circuito do Azure ExpressRoute do Azure.</span><span class="sxs-lookup"><span data-stu-id="fd0b6-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd0b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd0b6-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd0b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd0b6-105">DESCRIPTION</span></span>
<span data-ttu-id="fd0b6-106">O cmdlet **Get-AzureRmExpressRouteCircuit** é usado para recuperar um objeto de circuito do ExpressRoute da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="fd0b6-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="fd0b6-107">O objeto de circuito retornado pode ser usado como entrada para outros cmdlets que operam em circuitos do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fd0b6-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="fd0b6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd0b6-108">EXAMPLES</span></span>

### <span data-ttu-id="fd0b6-109">Exemplo 1: baixar o circuito do ExpressRoute para ser excluído</span><span class="sxs-lookup"><span data-stu-id="fd0b6-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="fd0b6-110">OS</span><span class="sxs-lookup"><span data-stu-id="fd0b6-110">PARAMETERS</span></span>

### <span data-ttu-id="fd0b6-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd0b6-111">-Name</span></span>
<span data-ttu-id="fd0b6-112">O nome do circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fd0b6-112">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd0b6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd0b6-113">-ResourceGroupName</span></span>
<span data-ttu-id="fd0b6-114">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fd0b6-114">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd0b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd0b6-115">-DefaultProfile</span></span>
<span data-ttu-id="fd0b6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd0b6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd0b6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd0b6-117">CommonParameters</span></span>
<span data-ttu-id="fd0b6-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd0b6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd0b6-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd0b6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd0b6-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd0b6-120">INPUTS</span></span>

## <span data-ttu-id="fd0b6-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd0b6-121">OUTPUTS</span></span>

### <span data-ttu-id="fd0b6-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fd0b6-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="fd0b6-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd0b6-123">NOTES</span></span>

## <span data-ttu-id="fd0b6-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd0b6-124">RELATED LINKS</span></span>

[<span data-ttu-id="fd0b6-125">Mover-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fd0b6-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="fd0b6-126">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fd0b6-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="fd0b6-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fd0b6-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="fd0b6-128">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fd0b6-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
