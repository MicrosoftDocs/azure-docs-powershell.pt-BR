---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37569cc786109a3a86b0406eb0aa24e7d106ed53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425965"
---
# <span data-ttu-id="f2713-101">Get-AzsBlobServiceMetric</span><span class="sxs-lookup"><span data-stu-id="f2713-101">Get-AzsBlobServiceMetric</span></span>

## <span data-ttu-id="f2713-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2713-102">SYNOPSIS</span></span>
<span data-ttu-id="f2713-103">Retorna uma lista de métricas do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="f2713-103">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="f2713-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2713-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2713-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2713-105">DESCRIPTION</span></span>
<span data-ttu-id="f2713-106">Retorna uma lista de métricas do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="f2713-106">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="f2713-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2713-107">EXAMPLES</span></span>

### <span data-ttu-id="f2713-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f2713-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBlobServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="f2713-109">Obter uma lista de métricas do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="f2713-109">Get a list of metrics for blob service.</span></span>

## <span data-ttu-id="f2713-110">OS</span><span class="sxs-lookup"><span data-stu-id="f2713-110">PARAMETERS</span></span>

### <span data-ttu-id="f2713-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="f2713-111">-FarmName</span></span>
<span data-ttu-id="f2713-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="f2713-112">Farm Id.</span></span>

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

### <span data-ttu-id="f2713-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2713-113">-ResourceGroupName</span></span>
<span data-ttu-id="f2713-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2713-114">Resource group name.</span></span>

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

### <span data-ttu-id="f2713-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="f2713-115">-Skip</span></span>
<span data-ttu-id="f2713-116">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f2713-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f2713-117">-Início</span><span class="sxs-lookup"><span data-stu-id="f2713-117">-Top</span></span>
<span data-ttu-id="f2713-118">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f2713-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f2713-119">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="f2713-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f2713-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2713-120">CommonParameters</span></span>
<span data-ttu-id="f2713-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2713-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2713-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2713-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2713-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2713-123">INPUTS</span></span>

## <span data-ttu-id="f2713-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2713-124">OUTPUTS</span></span>

### <span data-ttu-id="f2713-125">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="f2713-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="f2713-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2713-126">NOTES</span></span>

## <span data-ttu-id="f2713-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2713-127">RELATED LINKS</span></span>

