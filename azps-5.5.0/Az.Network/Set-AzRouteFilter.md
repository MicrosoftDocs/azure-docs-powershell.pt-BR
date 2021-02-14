---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117320"
---
# <span data-ttu-id="8242f-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8242f-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="8242f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8242f-102">SYNOPSIS</span></span>
<span data-ttu-id="8242f-103">Atualiza um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="8242f-103">Updates a route filter.</span></span>

## <span data-ttu-id="8242f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8242f-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8242f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8242f-105">DESCRIPTION</span></span>
<span data-ttu-id="8242f-106">O **cmdlet Set-AzApplicationGateway** atualiza um filtro de rota</span><span class="sxs-lookup"><span data-stu-id="8242f-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="8242f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8242f-107">EXAMPLES</span></span>

### <span data-ttu-id="8242f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8242f-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="8242f-109">Esse comando atualiza o filtro de rota com configurações na variável $rf dados.</span><span class="sxs-lookup"><span data-stu-id="8242f-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="8242f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8242f-110">PARAMETERS</span></span>

### <span data-ttu-id="8242f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8242f-111">-AsJob</span></span>
<span data-ttu-id="8242f-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8242f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8242f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8242f-113">-DefaultProfile</span></span>
<span data-ttu-id="8242f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8242f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8242f-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="8242f-115">-Force</span></span>
<span data-ttu-id="8242f-116">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="8242f-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8242f-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8242f-117">-RouteFilter</span></span>
<span data-ttu-id="8242f-118">O Filtro de Rota</span><span class="sxs-lookup"><span data-stu-id="8242f-118">The RouteFilter</span></span>

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

### <span data-ttu-id="8242f-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8242f-119">-Confirm</span></span>
<span data-ttu-id="8242f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8242f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8242f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8242f-121">-WhatIf</span></span>
<span data-ttu-id="8242f-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8242f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8242f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8242f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8242f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8242f-124">CommonParameters</span></span>
<span data-ttu-id="8242f-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8242f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8242f-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8242f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8242f-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="8242f-127">INPUTS</span></span>

### <span data-ttu-id="8242f-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8242f-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8242f-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="8242f-129">OUTPUTS</span></span>

### <span data-ttu-id="8242f-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8242f-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8242f-131">Notas</span><span class="sxs-lookup"><span data-stu-id="8242f-131">NOTES</span></span>

## <span data-ttu-id="8242f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8242f-132">RELATED LINKS</span></span>

[<span data-ttu-id="8242f-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8242f-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="8242f-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8242f-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="8242f-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8242f-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="8242f-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8242f-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8242f-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8242f-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8242f-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8242f-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8242f-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8242f-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8242f-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8242f-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
