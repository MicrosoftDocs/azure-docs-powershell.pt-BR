---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 1091a8433cd226982d3f2addf7e02b2414020fe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440101"
---
# <span data-ttu-id="b8448-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b8448-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="b8448-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8448-102">SYNOPSIS</span></span>
<span data-ttu-id="b8448-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="b8448-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8448-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8448-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8448-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8448-105">DESCRIPTION</span></span>
<span data-ttu-id="b8448-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="b8448-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="b8448-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8448-107">EXAMPLES</span></span>

### <span data-ttu-id="b8448-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8448-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b8448-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="b8448-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b8448-110">OS</span><span class="sxs-lookup"><span data-stu-id="b8448-110">PARAMETERS</span></span>

### <span data-ttu-id="b8448-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8448-111">-AsJob</span></span>
<span data-ttu-id="b8448-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b8448-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8448-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8448-113">-DefaultProfile</span></span>
<span data-ttu-id="b8448-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8448-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8448-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b8448-115">-Force</span></span>
<span data-ttu-id="b8448-116">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="b8448-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="b8448-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b8448-117">-RouteFilter</span></span>
<span data-ttu-id="b8448-118">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b8448-118">The RouteFilter</span></span>

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

### <span data-ttu-id="b8448-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8448-119">-Confirm</span></span>
<span data-ttu-id="b8448-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8448-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8448-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8448-121">-WhatIf</span></span>
<span data-ttu-id="b8448-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8448-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8448-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8448-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8448-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8448-124">CommonParameters</span></span>
<span data-ttu-id="b8448-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8448-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8448-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8448-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8448-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8448-127">INPUTS</span></span>

### <span data-ttu-id="b8448-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b8448-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b8448-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8448-129">OUTPUTS</span></span>

### <span data-ttu-id="b8448-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b8448-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b8448-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8448-131">NOTES</span></span>

## <span data-ttu-id="b8448-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8448-132">RELATED LINKS</span></span>

