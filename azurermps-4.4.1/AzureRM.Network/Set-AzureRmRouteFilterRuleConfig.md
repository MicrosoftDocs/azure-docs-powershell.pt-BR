---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: f5b2a3f66a1972edbf6d3e475f5f30fc9530929f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429215"
---
# <span data-ttu-id="b21d0-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b21d0-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="b21d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b21d0-102">SYNOPSIS</span></span>
<span data-ttu-id="b21d0-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="b21d0-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b21d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b21d0-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b21d0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b21d0-105">DESCRIPTION</span></span>
<span data-ttu-id="b21d0-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="b21d0-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="b21d0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b21d0-107">EXAMPLES</span></span>

### <span data-ttu-id="b21d0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b21d0-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b21d0-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="b21d0-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b21d0-110">OS</span><span class="sxs-lookup"><span data-stu-id="b21d0-110">PARAMETERS</span></span>

### <span data-ttu-id="b21d0-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="b21d0-111">-Access</span></span>
<span data-ttu-id="b21d0-112">O tipo de acesso da regra.</span><span class="sxs-lookup"><span data-stu-id="b21d0-112">The access type of the rule.</span></span>
<span data-ttu-id="b21d0-113">Os valores possíveis são: ' Allow ', ' Deny '</span><span class="sxs-lookup"><span data-stu-id="b21d0-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="b21d0-114">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="b21d0-114">-CommunityList</span></span>
<span data-ttu-id="b21d0-115">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="b21d0-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="b21d0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b21d0-116">-Force</span></span>
<span data-ttu-id="b21d0-117">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="b21d0-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="b21d0-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b21d0-118">-Name</span></span>
<span data-ttu-id="b21d0-119">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="b21d0-119">The name of the route filter rule</span></span>

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

### <span data-ttu-id="b21d0-120">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b21d0-120">-RouteFilter</span></span>
<span data-ttu-id="b21d0-121">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b21d0-121">The RouteFilter</span></span>

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

### <span data-ttu-id="b21d0-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="b21d0-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="b21d0-123">O tipo de regra de filtro de rota da regra.</span><span class="sxs-lookup"><span data-stu-id="b21d0-123">The route filter rule type of the rule.</span></span>
<span data-ttu-id="b21d0-124">Os valores possíveis são: "Comunidade"</span><span class="sxs-lookup"><span data-stu-id="b21d0-124">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="b21d0-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b21d0-125">-Confirm</span></span>
<span data-ttu-id="b21d0-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b21d0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b21d0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b21d0-127">-WhatIf</span></span>
<span data-ttu-id="b21d0-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b21d0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b21d0-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b21d0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b21d0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b21d0-130">-DefaultProfile</span></span>
<span data-ttu-id="b21d0-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b21d0-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b21d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b21d0-132">CommonParameters</span></span>
<span data-ttu-id="b21d0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b21d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b21d0-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b21d0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b21d0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b21d0-135">INPUTS</span></span>

### <span data-ttu-id="b21d0-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b21d0-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b21d0-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b21d0-137">OUTPUTS</span></span>

### <span data-ttu-id="b21d0-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b21d0-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b21d0-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b21d0-139">NOTES</span></span>

## <span data-ttu-id="b21d0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b21d0-140">RELATED LINKS</span></span>

