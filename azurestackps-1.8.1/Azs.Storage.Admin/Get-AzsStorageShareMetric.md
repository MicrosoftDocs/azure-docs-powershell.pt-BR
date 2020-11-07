---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 80c80cb38013701d3e58d6d6bf77f774e2d61548
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775158"
---
# <span data-ttu-id="567a0-101">Get-AzsStorageShareMetric</span><span class="sxs-lookup"><span data-stu-id="567a0-101">Get-AzsStorageShareMetric</span></span>

## <span data-ttu-id="567a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="567a0-102">SYNOPSIS</span></span>
<span data-ttu-id="567a0-103">Retorna uma lista de métricas para um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="567a0-103">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="567a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="567a0-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetric [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="567a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="567a0-105">DESCRIPTION</span></span>
<span data-ttu-id="567a0-106">Retorna uma lista de métricas para um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="567a0-106">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="567a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="567a0-107">EXAMPLES</span></span>

### <span data-ttu-id="567a0-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="567a0-108">EXAMPLE 1</span></span>
```
Get-AzsStorageShareMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="567a0-109">Obter a lista de métricas para um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="567a0-109">Get the list of metrics for a storage share.</span></span>

## <span data-ttu-id="567a0-110">OS</span><span class="sxs-lookup"><span data-stu-id="567a0-110">PARAMETERS</span></span>

### <span data-ttu-id="567a0-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="567a0-111">-FarmName</span></span>
<span data-ttu-id="567a0-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="567a0-112">Farm Id.</span></span>

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

### <span data-ttu-id="567a0-113">-ShareName</span><span class="sxs-lookup"><span data-stu-id="567a0-113">-ShareName</span></span>
<span data-ttu-id="567a0-114">Nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="567a0-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567a0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="567a0-115">-ResourceGroupName</span></span>
<span data-ttu-id="567a0-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="567a0-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567a0-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="567a0-117">-Skip</span></span>
<span data-ttu-id="567a0-118">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="567a0-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567a0-119">-Início</span><span class="sxs-lookup"><span data-stu-id="567a0-119">-Top</span></span>
<span data-ttu-id="567a0-120">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="567a0-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="567a0-121">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="567a0-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567a0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567a0-122">CommonParameters</span></span>
<span data-ttu-id="567a0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="567a0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567a0-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="567a0-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567a0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="567a0-125">INPUTS</span></span>

## <span data-ttu-id="567a0-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="567a0-126">OUTPUTS</span></span>

### <span data-ttu-id="567a0-127">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="567a0-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="567a0-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="567a0-128">NOTES</span></span>

## <span data-ttu-id="567a0-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="567a0-129">RELATED LINKS</span></span>