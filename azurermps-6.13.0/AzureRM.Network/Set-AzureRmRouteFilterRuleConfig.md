---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 88863b0db825eacfc844a8c24cc81f3ad866894d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431935"
---
# <span data-ttu-id="e8068-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8068-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="e8068-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8068-102">SYNOPSIS</span></span>
<span data-ttu-id="e8068-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="e8068-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8068-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8068-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8068-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8068-105">DESCRIPTION</span></span>
<span data-ttu-id="e8068-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="e8068-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="e8068-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8068-107">EXAMPLES</span></span>

### <span data-ttu-id="e8068-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8068-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e8068-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="e8068-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e8068-110">OS</span><span class="sxs-lookup"><span data-stu-id="e8068-110">PARAMETERS</span></span>

### <span data-ttu-id="e8068-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="e8068-111">-Access</span></span>
<span data-ttu-id="e8068-112">O tipo de acesso da regra.</span><span class="sxs-lookup"><span data-stu-id="e8068-112">The access type of the rule.</span></span>
<span data-ttu-id="e8068-113">Os valores possíveis são: ' Allow ', ' Deny '</span><span class="sxs-lookup"><span data-stu-id="e8068-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="e8068-114">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="e8068-114">-CommunityList</span></span>
<span data-ttu-id="e8068-115">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="e8068-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8068-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8068-116">-DefaultProfile</span></span>
<span data-ttu-id="e8068-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8068-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8068-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e8068-118">-Force</span></span>
<span data-ttu-id="e8068-119">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="e8068-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="e8068-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8068-120">-Name</span></span>
<span data-ttu-id="e8068-121">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="e8068-121">The name of the route filter rule</span></span>

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

### <span data-ttu-id="e8068-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="e8068-122">-RouteFilter</span></span>
<span data-ttu-id="e8068-123">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="e8068-123">The RouteFilter</span></span>

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

### <span data-ttu-id="e8068-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="e8068-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="e8068-125">O tipo de regra de filtro de rota da regra.</span><span class="sxs-lookup"><span data-stu-id="e8068-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="e8068-126">Os valores possíveis são: "Comunidade"</span><span class="sxs-lookup"><span data-stu-id="e8068-126">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="e8068-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e8068-127">-Confirm</span></span>
<span data-ttu-id="e8068-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8068-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8068-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8068-129">-WhatIf</span></span>
<span data-ttu-id="e8068-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8068-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8068-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8068-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8068-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8068-132">CommonParameters</span></span>
<span data-ttu-id="e8068-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8068-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8068-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8068-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8068-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8068-135">INPUTS</span></span>

### <span data-ttu-id="e8068-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e8068-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="e8068-137">Parâmetros: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8068-137">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="e8068-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8068-138">OUTPUTS</span></span>

### <span data-ttu-id="e8068-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e8068-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="e8068-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8068-140">NOTES</span></span>

## <span data-ttu-id="e8068-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8068-141">RELATED LINKS</span></span>
