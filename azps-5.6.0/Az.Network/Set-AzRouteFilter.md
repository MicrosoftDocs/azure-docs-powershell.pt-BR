---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 0c6fa8b973af2f2ab4a9c8547dddffda18eb15c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890365"
---
# <span data-ttu-id="f7317-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f7317-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="f7317-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7317-102">SYNOPSIS</span></span>
<span data-ttu-id="f7317-103">Atualiza um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="f7317-103">Updates a route filter.</span></span>

## <span data-ttu-id="f7317-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7317-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7317-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7317-105">DESCRIPTION</span></span>
<span data-ttu-id="f7317-106">O cmdlet **Set-AzApplicationGateway** atualiza um filtro de rota</span><span class="sxs-lookup"><span data-stu-id="f7317-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="f7317-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7317-107">EXAMPLES</span></span>

### <span data-ttu-id="f7317-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f7317-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="f7317-109">Este comando atualiza o filtro de rota com configurações na variável $rf de rota.</span><span class="sxs-lookup"><span data-stu-id="f7317-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="f7317-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7317-110">PARAMETERS</span></span>

### <span data-ttu-id="f7317-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7317-111">-AsJob</span></span>
<span data-ttu-id="f7317-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f7317-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7317-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7317-113">-DefaultProfile</span></span>
<span data-ttu-id="f7317-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f7317-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7317-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f7317-115">-Force</span></span>
<span data-ttu-id="f7317-116">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="f7317-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f7317-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f7317-117">-RouteFilter</span></span>
<span data-ttu-id="f7317-118">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f7317-118">The RouteFilter</span></span>

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

### <span data-ttu-id="f7317-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7317-119">-Confirm</span></span>
<span data-ttu-id="f7317-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7317-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7317-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7317-121">-WhatIf</span></span>
<span data-ttu-id="f7317-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f7317-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7317-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7317-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7317-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7317-124">CommonParameters</span></span>
<span data-ttu-id="f7317-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7317-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7317-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7317-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7317-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7317-127">INPUTS</span></span>

### <span data-ttu-id="f7317-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f7317-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f7317-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7317-129">OUTPUTS</span></span>

### <span data-ttu-id="f7317-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f7317-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f7317-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7317-131">NOTES</span></span>

## <span data-ttu-id="f7317-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7317-132">RELATED LINKS</span></span>

[<span data-ttu-id="f7317-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f7317-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="f7317-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f7317-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="f7317-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f7317-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="f7317-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7317-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f7317-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7317-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f7317-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7317-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f7317-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7317-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f7317-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7317-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
