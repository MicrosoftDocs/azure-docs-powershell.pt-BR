---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e127b0cb9198471d237df62bfedf8d2d57ecdca2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947091"
---
# <span data-ttu-id="10ebe-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="10ebe-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="10ebe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="10ebe-103">Retorna uma lista de definições de métricas para um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10ebe-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="10ebe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10ebe-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="10ebe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10ebe-105">DESCRIPTION</span></span>
<span data-ttu-id="10ebe-106">Retorna uma lista de definições de métricas para um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10ebe-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="10ebe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10ebe-107">EXAMPLES</span></span>

### <span data-ttu-id="10ebe-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="10ebe-108">EXAMPLE 1</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="10ebe-109">Obter a lista de definições de métrica para um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10ebe-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="10ebe-110">OS</span><span class="sxs-lookup"><span data-stu-id="10ebe-110">PARAMETERS</span></span>

### <span data-ttu-id="10ebe-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="10ebe-111">-FarmName</span></span>
<span data-ttu-id="10ebe-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="10ebe-112">Farm Id.</span></span>

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

### <span data-ttu-id="10ebe-113">-ShareName</span><span class="sxs-lookup"><span data-stu-id="10ebe-113">-ShareName</span></span>
<span data-ttu-id="10ebe-114">Nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="10ebe-114">Share name.</span></span>

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

### <span data-ttu-id="10ebe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10ebe-115">-ResourceGroupName</span></span>
<span data-ttu-id="10ebe-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="10ebe-116">Resource group name.</span></span>

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

### <span data-ttu-id="10ebe-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="10ebe-117">-Skip</span></span>
<span data-ttu-id="10ebe-118">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="10ebe-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="10ebe-119">-Início</span><span class="sxs-lookup"><span data-stu-id="10ebe-119">-Top</span></span>
<span data-ttu-id="10ebe-120">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="10ebe-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="10ebe-121">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="10ebe-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="10ebe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ebe-122">CommonParameters</span></span>
<span data-ttu-id="10ebe-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10ebe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ebe-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10ebe-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ebe-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10ebe-125">INPUTS</span></span>

## <span data-ttu-id="10ebe-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10ebe-126">OUTPUTS</span></span>

### <span data-ttu-id="10ebe-127">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="10ebe-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="10ebe-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10ebe-128">NOTES</span></span>

## <span data-ttu-id="10ebe-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10ebe-129">RELATED LINKS</span></span>
