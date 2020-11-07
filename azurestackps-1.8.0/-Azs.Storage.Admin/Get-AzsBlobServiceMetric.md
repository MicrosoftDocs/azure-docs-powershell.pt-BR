---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37569cc786109a3a86b0406eb0aa24e7d106ed53
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774853"
---
# <span data-ttu-id="d7e97-101">Get-AzsBlobServiceMetric</span><span class="sxs-lookup"><span data-stu-id="d7e97-101">Get-AzsBlobServiceMetric</span></span>

## <span data-ttu-id="d7e97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7e97-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e97-103">Retorna uma lista de métricas do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="d7e97-103">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="d7e97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7e97-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7e97-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7e97-105">DESCRIPTION</span></span>
<span data-ttu-id="d7e97-106">Retorna uma lista de métricas do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="d7e97-106">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="d7e97-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7e97-107">EXAMPLES</span></span>

### <span data-ttu-id="d7e97-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d7e97-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBlobServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="d7e97-109">Obter uma lista de métricas do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="d7e97-109">Get a list of metrics for blob service.</span></span>

## <span data-ttu-id="d7e97-110">OS</span><span class="sxs-lookup"><span data-stu-id="d7e97-110">PARAMETERS</span></span>

### <span data-ttu-id="d7e97-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="d7e97-111">-FarmName</span></span>
<span data-ttu-id="d7e97-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="d7e97-112">Farm Id.</span></span>

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

### <span data-ttu-id="d7e97-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7e97-113">-ResourceGroupName</span></span>
<span data-ttu-id="d7e97-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7e97-114">Resource group name.</span></span>

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

### <span data-ttu-id="d7e97-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="d7e97-115">-Skip</span></span>
<span data-ttu-id="d7e97-116">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d7e97-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d7e97-117">-Início</span><span class="sxs-lookup"><span data-stu-id="d7e97-117">-Top</span></span>
<span data-ttu-id="d7e97-118">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d7e97-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d7e97-119">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="d7e97-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d7e97-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e97-120">CommonParameters</span></span>
<span data-ttu-id="d7e97-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7e97-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e97-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7e97-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e97-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7e97-123">INPUTS</span></span>

## <span data-ttu-id="d7e97-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7e97-124">OUTPUTS</span></span>

### <span data-ttu-id="d7e97-125">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="d7e97-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="d7e97-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7e97-126">NOTES</span></span>

## <span data-ttu-id="d7e97-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7e97-127">RELATED LINKS</span></span>

