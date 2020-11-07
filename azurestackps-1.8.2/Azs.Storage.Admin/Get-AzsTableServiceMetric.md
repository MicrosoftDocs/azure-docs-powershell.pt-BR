---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1affc11e3e5ff360cf08468c4935b6d48d68321
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947052"
---
# <span data-ttu-id="48581-101">Get-AzsTableServiceMetric</span><span class="sxs-lookup"><span data-stu-id="48581-101">Get-AzsTableServiceMetric</span></span>

## <span data-ttu-id="48581-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48581-102">SYNOPSIS</span></span>
<span data-ttu-id="48581-103">Retorna uma lista de métricas do serviço de tabela.</span><span class="sxs-lookup"><span data-stu-id="48581-103">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="48581-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48581-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="48581-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48581-105">DESCRIPTION</span></span>
<span data-ttu-id="48581-106">Retorna uma lista de métricas do serviço de tabela.</span><span class="sxs-lookup"><span data-stu-id="48581-106">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="48581-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48581-107">EXAMPLES</span></span>

### <span data-ttu-id="48581-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="48581-108">EXAMPLE 1</span></span>
```
Get-AzsTableServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="48581-109">Obter a lista de métricas do serviço de tabela.</span><span class="sxs-lookup"><span data-stu-id="48581-109">Get the list of metrics for table service.</span></span>

## <span data-ttu-id="48581-110">OS</span><span class="sxs-lookup"><span data-stu-id="48581-110">PARAMETERS</span></span>

### <span data-ttu-id="48581-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="48581-111">-FarmName</span></span>
<span data-ttu-id="48581-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="48581-112">Farm Id.</span></span>

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

### <span data-ttu-id="48581-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48581-113">-ResourceGroupName</span></span>
<span data-ttu-id="48581-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="48581-114">Resource group name.</span></span>

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

### <span data-ttu-id="48581-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="48581-115">-Skip</span></span>
<span data-ttu-id="48581-116">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="48581-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="48581-117">-Início</span><span class="sxs-lookup"><span data-stu-id="48581-117">-Top</span></span>
<span data-ttu-id="48581-118">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="48581-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="48581-119">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="48581-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="48581-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48581-120">CommonParameters</span></span>
<span data-ttu-id="48581-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48581-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48581-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48581-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48581-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48581-123">INPUTS</span></span>

## <span data-ttu-id="48581-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48581-124">OUTPUTS</span></span>

### <span data-ttu-id="48581-125">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="48581-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="48581-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48581-126">NOTES</span></span>

## <span data-ttu-id="48581-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48581-127">RELATED LINKS</span></span>
