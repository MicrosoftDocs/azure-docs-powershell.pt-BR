---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258204"
---
# <span data-ttu-id="bcc2e-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bcc2e-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="bcc2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bcc2e-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc2e-103">Atualiza um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-103">Updates a route filter.</span></span>

## <span data-ttu-id="bcc2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcc2e-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcc2e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bcc2e-105">DESCRIPTION</span></span>
<span data-ttu-id="bcc2e-106">O cmdlet **set-AzApplicationGateway** atualiza um filtro de rota</span><span class="sxs-lookup"><span data-stu-id="bcc2e-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="bcc2e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcc2e-107">EXAMPLES</span></span>

### <span data-ttu-id="bcc2e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bcc2e-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="bcc2e-109">Esse comando atualiza o filtro de rota com as configurações na variável $rf.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="bcc2e-110">OS</span><span class="sxs-lookup"><span data-stu-id="bcc2e-110">PARAMETERS</span></span>

### <span data-ttu-id="bcc2e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcc2e-111">-AsJob</span></span>
<span data-ttu-id="bcc2e-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bcc2e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcc2e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc2e-113">-DefaultProfile</span></span>
<span data-ttu-id="bcc2e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcc2e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bcc2e-115">-Force</span></span>
<span data-ttu-id="bcc2e-116">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="bcc2e-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bcc2e-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bcc2e-117">-RouteFilter</span></span>
<span data-ttu-id="bcc2e-118">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bcc2e-118">The RouteFilter</span></span>

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

### <span data-ttu-id="bcc2e-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bcc2e-119">-Confirm</span></span>
<span data-ttu-id="bcc2e-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcc2e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcc2e-121">-WhatIf</span></span>
<span data-ttu-id="bcc2e-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcc2e-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcc2e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc2e-124">CommonParameters</span></span>
<span data-ttu-id="bcc2e-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcc2e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc2e-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcc2e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc2e-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bcc2e-127">INPUTS</span></span>

### <span data-ttu-id="bcc2e-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bcc2e-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="bcc2e-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bcc2e-129">OUTPUTS</span></span>

### <span data-ttu-id="bcc2e-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bcc2e-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="bcc2e-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bcc2e-131">NOTES</span></span>

## <span data-ttu-id="bcc2e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcc2e-132">RELATED LINKS</span></span>

[<span data-ttu-id="bcc2e-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bcc2e-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="bcc2e-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bcc2e-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="bcc2e-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bcc2e-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="bcc2e-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bcc2e-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bcc2e-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bcc2e-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bcc2e-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bcc2e-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bcc2e-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bcc2e-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bcc2e-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bcc2e-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
