---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d81043e165600a549bace91458449577b23dbd8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947050"
---
# <span data-ttu-id="b2f1f-101">Get-AzsQueueServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b2f1f-101">Get-AzsQueueServiceMetricDefinition</span></span>

## <span data-ttu-id="b2f1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f1f-103">Retorna uma lista de definições de métricas do serviço de fila.</span><span class="sxs-lookup"><span data-stu-id="b2f1f-103">Returns a list of metric definitions for queue service.</span></span>

## <span data-ttu-id="b2f1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2f1f-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b2f1f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2f1f-105">DESCRIPTION</span></span>
<span data-ttu-id="b2f1f-106">Retorna uma lista de definições de métricas do serviço de fila.</span><span class="sxs-lookup"><span data-stu-id="b2f1f-106">Returns a list of metric definitions for queue service.</span></span>

## <span data-ttu-id="b2f1f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2f1f-107">EXAMPLES</span></span>

### <span data-ttu-id="b2f1f-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="b2f1f-108">EXAMPLE 1</span></span>
```
Get-AzsQueueServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="b2f1f-109">Obter a lista de definições de métricas do serviço de fila.</span><span class="sxs-lookup"><span data-stu-id="b2f1f-109">Get the list of metric definitions for queue service.</span></span>

## <span data-ttu-id="b2f1f-110">OS</span><span class="sxs-lookup"><span data-stu-id="b2f1f-110">PARAMETERS</span></span>

### <span data-ttu-id="b2f1f-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="b2f1f-111">-FarmName</span></span>
<span data-ttu-id="b2f1f-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="b2f1f-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f1f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2f1f-113">-ResourceGroupName</span></span>
<span data-ttu-id="b2f1f-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b2f1f-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f1f-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="b2f1f-115">-Skip</span></span>
<span data-ttu-id="b2f1f-116">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b2f1f-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f1f-117">-Início</span><span class="sxs-lookup"><span data-stu-id="b2f1f-117">-Top</span></span>
<span data-ttu-id="b2f1f-118">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b2f1f-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b2f1f-119">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="b2f1f-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f1f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f1f-120">CommonParameters</span></span>
<span data-ttu-id="b2f1f-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f1f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f1f-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f1f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f1f-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2f1f-123">INPUTS</span></span>

## <span data-ttu-id="b2f1f-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2f1f-124">OUTPUTS</span></span>

### <span data-ttu-id="b2f1f-125">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b2f1f-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="b2f1f-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2f1f-126">NOTES</span></span>

## <span data-ttu-id="b2f1f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2f1f-127">RELATED LINKS</span></span>
