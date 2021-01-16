---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264042"
---
# <span data-ttu-id="8711e-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8711e-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="8711e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8711e-102">SYNOPSIS</span></span>
<span data-ttu-id="8711e-103">Obtém uma regra de filtro de rota em um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="8711e-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="8711e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8711e-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8711e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8711e-105">DESCRIPTION</span></span>
<span data-ttu-id="8711e-106">O cmdlet **Get-AzRouteFilterRuleConfig** Obtém uma regra de filtro de rota ou uma lista de regras de filtro de rota em um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="8711e-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="8711e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8711e-107">EXAMPLES</span></span>

### <span data-ttu-id="8711e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8711e-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="8711e-109">O primeiro comando obtém o filtro de rota chamado MyRouteFilter e, em seguida, armazena-o na variável $rf.</span><span class="sxs-lookup"><span data-stu-id="8711e-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="8711e-110">O segundo comando obtém a regra de filtro de rota chamada Rule01 associada a esse filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="8711e-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="8711e-111">O terceiro comando obtém uma lista de regras de filtro de rota associadas a esse filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="8711e-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="8711e-112">OS</span><span class="sxs-lookup"><span data-stu-id="8711e-112">PARAMETERS</span></span>

### <span data-ttu-id="8711e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8711e-113">-DefaultProfile</span></span>
<span data-ttu-id="8711e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8711e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8711e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8711e-115">-Name</span></span>
<span data-ttu-id="8711e-116">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="8711e-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="8711e-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8711e-117">-RouteFilter</span></span>
<span data-ttu-id="8711e-118">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8711e-118">The RouteFilter</span></span>

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

### <span data-ttu-id="8711e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8711e-119">CommonParameters</span></span>
<span data-ttu-id="8711e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8711e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8711e-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8711e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8711e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8711e-122">INPUTS</span></span>

### <span data-ttu-id="8711e-123">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8711e-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8711e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8711e-124">OUTPUTS</span></span>

### <span data-ttu-id="8711e-125">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="8711e-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="8711e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8711e-126">NOTES</span></span>

## <span data-ttu-id="8711e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8711e-127">RELATED LINKS</span></span>

[<span data-ttu-id="8711e-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8711e-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8711e-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8711e-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8711e-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8711e-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8711e-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8711e-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8711e-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8711e-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="8711e-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8711e-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="8711e-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8711e-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="8711e-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8711e-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
