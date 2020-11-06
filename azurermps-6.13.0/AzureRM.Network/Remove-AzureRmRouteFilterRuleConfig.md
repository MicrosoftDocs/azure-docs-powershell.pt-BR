---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: b865f7e2351a3432d05887a5f554d26226831b58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430138"
---
# <span data-ttu-id="b85f9-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b85f9-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="b85f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b85f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b85f9-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="b85f9-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b85f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b85f9-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b85f9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b85f9-105">DESCRIPTION</span></span>
<span data-ttu-id="b85f9-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="b85f9-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="b85f9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b85f9-107">EXAMPLES</span></span>

### <span data-ttu-id="b85f9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b85f9-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b85f9-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="b85f9-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b85f9-110">OS</span><span class="sxs-lookup"><span data-stu-id="b85f9-110">PARAMETERS</span></span>

### <span data-ttu-id="b85f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85f9-111">-DefaultProfile</span></span>
<span data-ttu-id="b85f9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b85f9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b85f9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b85f9-113">-Force</span></span>
<span data-ttu-id="b85f9-114">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="b85f9-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="b85f9-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b85f9-115">-Name</span></span>
<span data-ttu-id="b85f9-116">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="b85f9-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="b85f9-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b85f9-117">-RouteFilter</span></span>
<span data-ttu-id="b85f9-118">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b85f9-118">The RouteFilter</span></span>

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

### <span data-ttu-id="b85f9-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b85f9-119">-Confirm</span></span>
<span data-ttu-id="b85f9-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b85f9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b85f9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b85f9-121">-WhatIf</span></span>
<span data-ttu-id="b85f9-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b85f9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b85f9-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b85f9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b85f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85f9-124">CommonParameters</span></span>
<span data-ttu-id="b85f9-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b85f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85f9-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b85f9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85f9-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b85f9-127">INPUTS</span></span>

### <span data-ttu-id="b85f9-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b85f9-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="b85f9-129">Parâmetros: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b85f9-129">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="b85f9-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b85f9-130">OUTPUTS</span></span>

### <span data-ttu-id="b85f9-131">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="b85f9-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="b85f9-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b85f9-132">NOTES</span></span>

## <span data-ttu-id="b85f9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b85f9-133">RELATED LINKS</span></span>
