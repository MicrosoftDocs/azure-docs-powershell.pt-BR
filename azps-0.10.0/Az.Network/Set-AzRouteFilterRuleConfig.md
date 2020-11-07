---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 8ab95789b73623716edc818c8092c8c0cd58c534
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776510"
---
# <span data-ttu-id="b220f-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b220f-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="b220f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b220f-102">SYNOPSIS</span></span>
<span data-ttu-id="b220f-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="b220f-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="b220f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b220f-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b220f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b220f-105">DESCRIPTION</span></span>
<span data-ttu-id="b220f-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="b220f-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="b220f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b220f-107">EXAMPLES</span></span>

### <span data-ttu-id="b220f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b220f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b220f-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="b220f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b220f-110">OS</span><span class="sxs-lookup"><span data-stu-id="b220f-110">PARAMETERS</span></span>

### <span data-ttu-id="b220f-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="b220f-111">-Access</span></span>
<span data-ttu-id="b220f-112">O tipo de acesso da regra.</span><span class="sxs-lookup"><span data-stu-id="b220f-112">The access type of the rule.</span></span>
<span data-ttu-id="b220f-113">Os valores possíveis são: ' Allow ', ' Deny '</span><span class="sxs-lookup"><span data-stu-id="b220f-113">Possible values are: 'Allow', 'Deny'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b220f-114">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="b220f-114">-CommunityList</span></span>
<span data-ttu-id="b220f-115">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="b220f-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="b220f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b220f-116">-DefaultProfile</span></span>
<span data-ttu-id="b220f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b220f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b220f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b220f-118">-Force</span></span>
<span data-ttu-id="b220f-119">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="b220f-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b220f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b220f-120">-Name</span></span>
<span data-ttu-id="b220f-121">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="b220f-121">The name of the route filter rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b220f-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b220f-122">-RouteFilter</span></span>
<span data-ttu-id="b220f-123">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b220f-123">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b220f-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="b220f-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="b220f-125">O tipo de regra de filtro de rota da regra.</span><span class="sxs-lookup"><span data-stu-id="b220f-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="b220f-126">Os valores possíveis são: "Comunidade"</span><span class="sxs-lookup"><span data-stu-id="b220f-126">Possible values are: 'Community'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b220f-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b220f-127">-Confirm</span></span>
<span data-ttu-id="b220f-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b220f-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b220f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b220f-129">-WhatIf</span></span>
<span data-ttu-id="b220f-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b220f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b220f-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b220f-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b220f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b220f-132">CommonParameters</span></span>
<span data-ttu-id="b220f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b220f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b220f-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b220f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b220f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b220f-135">INPUTS</span></span>

### <span data-ttu-id="b220f-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b220f-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b220f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b220f-137">OUTPUTS</span></span>

### <span data-ttu-id="b220f-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b220f-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b220f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b220f-139">NOTES</span></span>

## <span data-ttu-id="b220f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b220f-140">RELATED LINKS</span></span>

