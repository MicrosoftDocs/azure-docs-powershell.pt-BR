---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2e80ea57424b350a1255a2a19c7bea8c22c34c71
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775069"
---
# <span data-ttu-id="b3527-101">Get-AzsBlobServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b3527-101">Get-AzsBlobServiceMetricDefinition</span></span>

## <span data-ttu-id="b3527-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3527-102">SYNOPSIS</span></span>
<span data-ttu-id="b3527-103">Retorna a lista de definições de métricas do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="b3527-103">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="b3527-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3527-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b3527-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3527-105">DESCRIPTION</span></span>
<span data-ttu-id="b3527-106">Retorna a lista de definições de métricas do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="b3527-106">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="b3527-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3527-107">EXAMPLES</span></span>

### <span data-ttu-id="b3527-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="b3527-108">EXAMPLE 1</span></span>
```
Get-AzsBlobServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="b3527-109">Obtenha uma lista de definições de métricas para o serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="b3527-109">Get a list of metric definitions for the blob service.</span></span>

## <span data-ttu-id="b3527-110">OS</span><span class="sxs-lookup"><span data-stu-id="b3527-110">PARAMETERS</span></span>

### <span data-ttu-id="b3527-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="b3527-111">-FarmName</span></span>
<span data-ttu-id="b3527-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="b3527-112">Farm Id.</span></span>

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

### <span data-ttu-id="b3527-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3527-113">-ResourceGroupName</span></span>
<span data-ttu-id="b3527-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b3527-114">Resource group name.</span></span>

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

### <span data-ttu-id="b3527-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="b3527-115">-Skip</span></span>
<span data-ttu-id="b3527-116">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b3527-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b3527-117">-Início</span><span class="sxs-lookup"><span data-stu-id="b3527-117">-Top</span></span>
<span data-ttu-id="b3527-118">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b3527-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b3527-119">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="b3527-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b3527-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3527-120">CommonParameters</span></span>
<span data-ttu-id="b3527-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3527-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3527-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3527-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3527-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3527-123">INPUTS</span></span>

## <span data-ttu-id="b3527-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3527-124">OUTPUTS</span></span>

### <span data-ttu-id="b3527-125">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b3527-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="b3527-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3527-126">NOTES</span></span>

## <span data-ttu-id="b3527-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3527-127">RELATED LINKS</span></span>
