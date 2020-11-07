---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: d11de748c8c86c974b45ac2f171b5eb54b97ee6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785884"
---
# <span data-ttu-id="ebcdb-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebcdb-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="ebcdb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ebcdb-102">SYNOPSIS</span></span>
<span data-ttu-id="ebcdb-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="ebcdb-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebcdb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ebcdb-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebcdb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ebcdb-105">DESCRIPTION</span></span>
<span data-ttu-id="ebcdb-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="ebcdb-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ebcdb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ebcdb-107">EXAMPLES</span></span>

### <span data-ttu-id="ebcdb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ebcdb-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ebcdb-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="ebcdb-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ebcdb-110">OS</span><span class="sxs-lookup"><span data-stu-id="ebcdb-110">PARAMETERS</span></span>

### <span data-ttu-id="ebcdb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebcdb-111">-DefaultProfile</span></span>
<span data-ttu-id="ebcdb-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ebcdb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebcdb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ebcdb-113">-Force</span></span>
<span data-ttu-id="ebcdb-114">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="ebcdb-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="ebcdb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ebcdb-115">-Name</span></span>
<span data-ttu-id="ebcdb-116">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="ebcdb-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="ebcdb-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebcdb-117">-RouteFilter</span></span>
<span data-ttu-id="ebcdb-118">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebcdb-118">The RouteFilter</span></span>

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

### <span data-ttu-id="ebcdb-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ebcdb-119">-Confirm</span></span>
<span data-ttu-id="ebcdb-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebcdb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebcdb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebcdb-121">-WhatIf</span></span>
<span data-ttu-id="ebcdb-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ebcdb-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebcdb-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ebcdb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebcdb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebcdb-124">CommonParameters</span></span>
<span data-ttu-id="ebcdb-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebcdb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebcdb-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebcdb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebcdb-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ebcdb-127">INPUTS</span></span>

### <span data-ttu-id="ebcdb-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebcdb-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ebcdb-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ebcdb-129">OUTPUTS</span></span>

### <span data-ttu-id="ebcdb-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="ebcdb-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="ebcdb-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ebcdb-131">NOTES</span></span>

## <span data-ttu-id="ebcdb-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ebcdb-132">RELATED LINKS</span></span>

