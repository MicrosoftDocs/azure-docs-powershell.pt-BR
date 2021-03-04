---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 0ed7233cda87c376707e0a5b5682a61a179550d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885646"
---
# <span data-ttu-id="2925c-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2925c-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="2925c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2925c-102">SYNOPSIS</span></span>
<span data-ttu-id="2925c-103">Obtém uma regra de filtro de rota em um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="2925c-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="2925c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2925c-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2925c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2925c-105">DESCRIPTION</span></span>
<span data-ttu-id="2925c-106">O cmdlet **Get-AzRouteFilterRuleConfig** obtém uma regra de filtro de rota ou uma lista de regras de filtro de rota em um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="2925c-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="2925c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2925c-107">EXAMPLES</span></span>

### <span data-ttu-id="2925c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2925c-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="2925c-109">O primeiro comando obtém o filtro de rota chamado MyRouteFilter e o armazena na variável $rf.</span><span class="sxs-lookup"><span data-stu-id="2925c-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="2925c-110">O segundo comando obtém a regra de filtro de rota chamada Rule01 associada a esse filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="2925c-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="2925c-111">O terceiro comando obtém uma lista de regras de filtro de rota associadas a esse filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="2925c-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="2925c-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2925c-112">PARAMETERS</span></span>

### <span data-ttu-id="2925c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2925c-113">-DefaultProfile</span></span>
<span data-ttu-id="2925c-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2925c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2925c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2925c-115">-Name</span></span>
<span data-ttu-id="2925c-116">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="2925c-116">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2925c-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2925c-117">-RouteFilter</span></span>
<span data-ttu-id="2925c-118">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2925c-118">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2925c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2925c-119">CommonParameters</span></span>
<span data-ttu-id="2925c-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2925c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2925c-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2925c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2925c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2925c-122">INPUTS</span></span>

### <span data-ttu-id="2925c-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2925c-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2925c-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2925c-124">OUTPUTS</span></span>

### <span data-ttu-id="2925c-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="2925c-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="2925c-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="2925c-126">NOTES</span></span>

## <span data-ttu-id="2925c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2925c-127">RELATED LINKS</span></span>

[<span data-ttu-id="2925c-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2925c-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2925c-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2925c-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2925c-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2925c-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2925c-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2925c-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2925c-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2925c-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="2925c-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2925c-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="2925c-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2925c-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="2925c-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2925c-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
