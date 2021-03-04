---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: dbd1564ceb4a4315f62f11712c73c56b46dcff7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886161"
---
# <span data-ttu-id="bfb9f-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bfb9f-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="bfb9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfb9f-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb9f-103">Cria uma regra de filtro de rota para um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="bfb9f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bfb9f-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfb9f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bfb9f-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb9f-106">O New-AzRouteFilterRuleConfig cmdlet cria uma regra de filtro de rota para um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="bfb9f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfb9f-107">EXAMPLES</span></span>

### <span data-ttu-id="bfb9f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bfb9f-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="bfb9f-109">O comando cria uma nova regra de filtro de rota e a armazena em variável $rule 1.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="bfb9f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bfb9f-110">PARAMETERS</span></span>

### <span data-ttu-id="bfb9f-111">-Access</span><span class="sxs-lookup"><span data-stu-id="bfb9f-111">-Access</span></span>
<span data-ttu-id="bfb9f-112">Acesso para regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-112">Access for route filter rule.</span></span>
<span data-ttu-id="bfb9f-113">Os valores válidos são Allow ou Deny.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb9f-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="bfb9f-114">-CommunityList</span></span>
<span data-ttu-id="bfb9f-115">A lista de valor da comunidade em que o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="bfb9f-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb9f-116">-DefaultProfile</span></span>
<span data-ttu-id="bfb9f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfb9f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bfb9f-118">-Force</span></span>
<span data-ttu-id="bfb9f-119">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="bfb9f-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bfb9f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bfb9f-120">-Name</span></span>
<span data-ttu-id="bfb9f-121">Especifica um nome para a regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="bfb9f-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="bfb9f-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="bfb9f-123">Tipo de regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="bfb9f-124">Os valores válidos são: Comunidade</span><span class="sxs-lookup"><span data-stu-id="bfb9f-124">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb9f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfb9f-125">-Confirm</span></span>
<span data-ttu-id="bfb9f-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfb9f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfb9f-127">-WhatIf</span></span>
<span data-ttu-id="bfb9f-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfb9f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfb9f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb9f-130">CommonParameters</span></span>
<span data-ttu-id="bfb9f-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb9f-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb9f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb9f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfb9f-133">INPUTS</span></span>

### <span data-ttu-id="bfb9f-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bfb9f-134">None</span></span>

## <span data-ttu-id="bfb9f-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bfb9f-135">OUTPUTS</span></span>

### <span data-ttu-id="bfb9f-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="bfb9f-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="bfb9f-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="bfb9f-137">NOTES</span></span>
<span data-ttu-id="bfb9f-138">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="bfb9f-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bfb9f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfb9f-139">RELATED LINKS</span></span>

[<span data-ttu-id="bfb9f-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bfb9f-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bfb9f-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bfb9f-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bfb9f-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bfb9f-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bfb9f-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bfb9f-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bfb9f-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bfb9f-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="bfb9f-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bfb9f-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="bfb9f-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bfb9f-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="bfb9f-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bfb9f-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
