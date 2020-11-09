---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282183"
---
# <span data-ttu-id="e8190-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8190-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="e8190-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8190-102">SYNOPSIS</span></span>
<span data-ttu-id="e8190-103">Cria uma regra de filtro de rota para um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="e8190-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="e8190-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8190-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8190-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8190-105">DESCRIPTION</span></span>
<span data-ttu-id="e8190-106">O cmdlet New-AzRouteFilterRuleConfig cria uma regra de filtro de rota para um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="e8190-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="e8190-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8190-107">EXAMPLES</span></span>

### <span data-ttu-id="e8190-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8190-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="e8190-109">O comando cria uma nova regra de filtro de rota e a armazena em Variable $rule 1.</span><span class="sxs-lookup"><span data-stu-id="e8190-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="e8190-110">OS</span><span class="sxs-lookup"><span data-stu-id="e8190-110">PARAMETERS</span></span>

### <span data-ttu-id="e8190-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="e8190-111">-Access</span></span>
<span data-ttu-id="e8190-112">Acesso à regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="e8190-112">Access for route filter rule.</span></span>
<span data-ttu-id="e8190-113">Os valores válidos são Allow ou Deny.</span><span class="sxs-lookup"><span data-stu-id="e8190-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="e8190-114">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="e8190-114">-CommunityList</span></span>
<span data-ttu-id="e8190-115">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="e8190-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="e8190-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8190-116">-DefaultProfile</span></span>
<span data-ttu-id="e8190-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8190-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8190-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e8190-118">-Force</span></span>
<span data-ttu-id="e8190-119">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="e8190-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e8190-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8190-120">-Name</span></span>
<span data-ttu-id="e8190-121">Especifica um nome para a regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="e8190-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="e8190-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="e8190-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="e8190-123">Tipo de regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="e8190-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="e8190-124">Os valores válidos são: Comunidade</span><span class="sxs-lookup"><span data-stu-id="e8190-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="e8190-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e8190-125">-Confirm</span></span>
<span data-ttu-id="e8190-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8190-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8190-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8190-127">-WhatIf</span></span>
<span data-ttu-id="e8190-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8190-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8190-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8190-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8190-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8190-130">CommonParameters</span></span>
<span data-ttu-id="e8190-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8190-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8190-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8190-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8190-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8190-133">INPUTS</span></span>

### <span data-ttu-id="e8190-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e8190-134">None</span></span>

## <span data-ttu-id="e8190-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8190-135">OUTPUTS</span></span>

### <span data-ttu-id="e8190-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="e8190-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="e8190-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8190-137">NOTES</span></span>
<span data-ttu-id="e8190-138">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="e8190-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e8190-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8190-139">RELATED LINKS</span></span>

[<span data-ttu-id="e8190-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8190-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="e8190-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8190-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="e8190-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8190-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="e8190-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8190-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="e8190-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e8190-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="e8190-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e8190-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="e8190-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e8190-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="e8190-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e8190-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
