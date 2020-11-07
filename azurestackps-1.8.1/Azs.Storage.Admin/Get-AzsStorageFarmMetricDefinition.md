---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc0e931c97a60d35db48dbceb1446ff944ee689
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775028"
---
# <span data-ttu-id="62579-101">Get-AzsStorageFarmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="62579-101">Get-AzsStorageFarmMetricDefinition</span></span>

## <span data-ttu-id="62579-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62579-102">SYNOPSIS</span></span>
<span data-ttu-id="62579-103">Retorna uma lista de definições de métricas de um farm de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="62579-103">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="62579-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62579-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="62579-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62579-105">DESCRIPTION</span></span>
<span data-ttu-id="62579-106">Retorna uma lista de definições de métricas de um farm de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="62579-106">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="62579-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62579-107">EXAMPLES</span></span>

### <span data-ttu-id="62579-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="62579-108">EXAMPLE 1</span></span>
```
Get-AzsStorageFarmMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="62579-109">Obter a lista de definições de métrica para um farm de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="62579-109">Get the list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="62579-110">OS</span><span class="sxs-lookup"><span data-stu-id="62579-110">PARAMETERS</span></span>

### <span data-ttu-id="62579-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="62579-111">-FarmName</span></span>
<span data-ttu-id="62579-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="62579-112">Farm Id.</span></span>

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

### <span data-ttu-id="62579-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62579-113">-ResourceGroupName</span></span>
<span data-ttu-id="62579-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="62579-114">Resource group name.</span></span>

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

### <span data-ttu-id="62579-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="62579-115">-Skip</span></span>
<span data-ttu-id="62579-116">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="62579-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="62579-117">-Início</span><span class="sxs-lookup"><span data-stu-id="62579-117">-Top</span></span>
<span data-ttu-id="62579-118">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="62579-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="62579-119">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="62579-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="62579-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62579-120">CommonParameters</span></span>
<span data-ttu-id="62579-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62579-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62579-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62579-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62579-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62579-123">INPUTS</span></span>

## <span data-ttu-id="62579-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62579-124">OUTPUTS</span></span>

### <span data-ttu-id="62579-125">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="62579-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="62579-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62579-126">NOTES</span></span>

## <span data-ttu-id="62579-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62579-127">RELATED LINKS</span></span>
