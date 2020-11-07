---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: bcb0d59c564087e02cd152c1ae76f38c91f33e80
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776609"
---
# <span data-ttu-id="ed47f-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed47f-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="ed47f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed47f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed47f-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="ed47f-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="ed47f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed47f-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed47f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed47f-105">DESCRIPTION</span></span>
<span data-ttu-id="ed47f-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="ed47f-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ed47f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed47f-107">EXAMPLES</span></span>

### <span data-ttu-id="ed47f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed47f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ed47f-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="ed47f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ed47f-110">OS</span><span class="sxs-lookup"><span data-stu-id="ed47f-110">PARAMETERS</span></span>

### <span data-ttu-id="ed47f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed47f-111">-DefaultProfile</span></span>
<span data-ttu-id="ed47f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed47f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed47f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ed47f-113">-Force</span></span>
<span data-ttu-id="ed47f-114">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="ed47f-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="ed47f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed47f-115">-Name</span></span>
<span data-ttu-id="ed47f-116">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="ed47f-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="ed47f-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed47f-117">-RouteFilter</span></span>
<span data-ttu-id="ed47f-118">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed47f-118">The RouteFilter</span></span>

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

### <span data-ttu-id="ed47f-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ed47f-119">-Confirm</span></span>
<span data-ttu-id="ed47f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed47f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed47f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed47f-121">-WhatIf</span></span>
<span data-ttu-id="ed47f-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ed47f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed47f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed47f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed47f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed47f-124">CommonParameters</span></span>
<span data-ttu-id="ed47f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed47f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed47f-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed47f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed47f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed47f-127">INPUTS</span></span>

### <span data-ttu-id="ed47f-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed47f-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ed47f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed47f-129">OUTPUTS</span></span>

### <span data-ttu-id="ed47f-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="ed47f-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="ed47f-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed47f-131">NOTES</span></span>

## <span data-ttu-id="ed47f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed47f-132">RELATED LINKS</span></span>

