---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112886"
---
# <span data-ttu-id="0ff88-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff88-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="0ff88-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ff88-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff88-103">Obtém uma regra de filtro de rota em um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="0ff88-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="0ff88-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ff88-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ff88-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ff88-105">DESCRIPTION</span></span>
<span data-ttu-id="0ff88-106">O cmdlet **Get-AzRouteFilterRuleConfig obtém** uma regra de filtro de rota ou uma lista de regras de filtro de rota em um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="0ff88-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="0ff88-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0ff88-107">EXAMPLES</span></span>

### <span data-ttu-id="0ff88-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0ff88-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="0ff88-109">O primeiro comando obtém o filtro de rota chamado MyRouteFilter e o armazena na variável $rf.</span><span class="sxs-lookup"><span data-stu-id="0ff88-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="0ff88-110">O segundo comando obtém a regra de filtro de rota chamada Rule01 associada a esse filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="0ff88-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="0ff88-111">O terceiro comando obtém uma lista de regras de filtro de rota associadas a esse filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="0ff88-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="0ff88-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ff88-112">PARAMETERS</span></span>

### <span data-ttu-id="0ff88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff88-113">-DefaultProfile</span></span>
<span data-ttu-id="0ff88-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0ff88-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ff88-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ff88-115">-Name</span></span>
<span data-ttu-id="0ff88-116">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="0ff88-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="0ff88-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ff88-117">-RouteFilter</span></span>
<span data-ttu-id="0ff88-118">O Filtro de Rota</span><span class="sxs-lookup"><span data-stu-id="0ff88-118">The RouteFilter</span></span>

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

### <span data-ttu-id="0ff88-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff88-119">CommonParameters</span></span>
<span data-ttu-id="0ff88-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ff88-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff88-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ff88-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff88-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="0ff88-122">INPUTS</span></span>

### <span data-ttu-id="0ff88-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ff88-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="0ff88-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="0ff88-124">OUTPUTS</span></span>

### <span data-ttu-id="0ff88-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="0ff88-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="0ff88-126">Notas</span><span class="sxs-lookup"><span data-stu-id="0ff88-126">NOTES</span></span>

## <span data-ttu-id="0ff88-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ff88-127">RELATED LINKS</span></span>

[<span data-ttu-id="0ff88-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff88-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0ff88-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff88-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0ff88-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff88-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0ff88-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff88-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0ff88-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ff88-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="0ff88-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ff88-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="0ff88-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ff88-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="0ff88-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ff88-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
