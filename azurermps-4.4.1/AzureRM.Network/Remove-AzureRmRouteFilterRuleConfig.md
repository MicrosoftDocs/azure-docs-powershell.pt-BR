---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: d73fbe14e4b1d4c4ea34c7405ad7da5b7954ffd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440200"
---
# <span data-ttu-id="74ffb-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74ffb-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="74ffb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="74ffb-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="74ffb-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74ffb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74ffb-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74ffb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74ffb-105">DESCRIPTION</span></span>
<span data-ttu-id="74ffb-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="74ffb-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="74ffb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74ffb-107">EXAMPLES</span></span>

### <span data-ttu-id="74ffb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="74ffb-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="74ffb-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="74ffb-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="74ffb-110">OS</span><span class="sxs-lookup"><span data-stu-id="74ffb-110">PARAMETERS</span></span>

### <span data-ttu-id="74ffb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="74ffb-111">-Force</span></span>
<span data-ttu-id="74ffb-112">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="74ffb-112">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="74ffb-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="74ffb-113">-Name</span></span>
<span data-ttu-id="74ffb-114">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="74ffb-114">The name of the route filter rule</span></span>

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

### <span data-ttu-id="74ffb-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="74ffb-115">-RouteFilter</span></span>
<span data-ttu-id="74ffb-116">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="74ffb-116">The RouteFilter</span></span>

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

### <span data-ttu-id="74ffb-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="74ffb-117">-Confirm</span></span>
<span data-ttu-id="74ffb-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74ffb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74ffb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74ffb-119">-WhatIf</span></span>
<span data-ttu-id="74ffb-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74ffb-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74ffb-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74ffb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74ffb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ffb-122">-DefaultProfile</span></span>
<span data-ttu-id="74ffb-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74ffb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74ffb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ffb-124">CommonParameters</span></span>
<span data-ttu-id="74ffb-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74ffb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ffb-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74ffb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ffb-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74ffb-127">INPUTS</span></span>

### <span data-ttu-id="74ffb-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="74ffb-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="74ffb-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74ffb-129">OUTPUTS</span></span>

### <span data-ttu-id="74ffb-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="74ffb-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="74ffb-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74ffb-131">NOTES</span></span>

## <span data-ttu-id="74ffb-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74ffb-132">RELATED LINKS</span></span>

