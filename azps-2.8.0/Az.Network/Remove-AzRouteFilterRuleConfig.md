---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: a7414690e1d0e1f5a6d8242af7b1d27490dcde93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772255"
---
# <span data-ttu-id="41379-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41379-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="41379-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41379-102">SYNOPSIS</span></span>
<span data-ttu-id="41379-103">Remove uma regra de filtro de rota de um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="41379-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="41379-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41379-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41379-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41379-105">DESCRIPTION</span></span>
<span data-ttu-id="41379-106">O cmdlet **Remove-AzRouteFilterRuleConfig** remove uma regra de filtro de rota de um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="41379-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="41379-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41379-107">EXAMPLES</span></span>

### <span data-ttu-id="41379-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="41379-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="41379-109">O primeiro comando obtém um filtro de rota chamado RouteFilter01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $rf.</span><span class="sxs-lookup"><span data-stu-id="41379-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="41379-110">O segundo comando Remove a regra de filtro de rota chamada Rule01 do filtro de rota armazenado em $rf.</span><span class="sxs-lookup"><span data-stu-id="41379-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="41379-111">OS</span><span class="sxs-lookup"><span data-stu-id="41379-111">PARAMETERS</span></span>

### <span data-ttu-id="41379-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41379-112">-DefaultProfile</span></span>
<span data-ttu-id="41379-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41379-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41379-114">-Force</span><span class="sxs-lookup"><span data-stu-id="41379-114">-Force</span></span>
<span data-ttu-id="41379-115">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="41379-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="41379-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="41379-116">-Name</span></span>
<span data-ttu-id="41379-117">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="41379-117">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41379-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="41379-118">-RouteFilter</span></span>
<span data-ttu-id="41379-119">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="41379-119">The RouteFilter</span></span>

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

### <span data-ttu-id="41379-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41379-120">-Confirm</span></span>
<span data-ttu-id="41379-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41379-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41379-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41379-122">-WhatIf</span></span>
<span data-ttu-id="41379-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41379-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41379-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41379-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41379-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41379-125">CommonParameters</span></span>
<span data-ttu-id="41379-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41379-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41379-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41379-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41379-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41379-128">INPUTS</span></span>

### <span data-ttu-id="41379-129">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="41379-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="41379-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41379-130">OUTPUTS</span></span>

### <span data-ttu-id="41379-131">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="41379-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="41379-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41379-132">NOTES</span></span>

## <span data-ttu-id="41379-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41379-133">RELATED LINKS</span></span>

[<span data-ttu-id="41379-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41379-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="41379-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41379-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="41379-136">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41379-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="41379-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41379-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="41379-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="41379-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="41379-139">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="41379-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="41379-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="41379-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="41379-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="41379-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)