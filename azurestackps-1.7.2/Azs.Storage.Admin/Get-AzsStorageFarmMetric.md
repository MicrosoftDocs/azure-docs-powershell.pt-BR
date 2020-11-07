---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95ea9afa5d3dce953f4e51e84d011886e4ba5688
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773911"
---
# <span data-ttu-id="737da-101">Get-AzsStorageFarmMetric</span><span class="sxs-lookup"><span data-stu-id="737da-101">Get-AzsStorageFarmMetric</span></span>

## <span data-ttu-id="737da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="737da-102">SYNOPSIS</span></span>
<span data-ttu-id="737da-103">Retorna uma lista de métricas de farm de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="737da-103">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="737da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="737da-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="737da-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="737da-105">DESCRIPTION</span></span>
<span data-ttu-id="737da-106">Retorna uma lista de métricas de farm de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="737da-106">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="737da-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="737da-107">EXAMPLES</span></span>

### <span data-ttu-id="737da-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="737da-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarmMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="737da-109">Obter a lista de métricas do farm de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="737da-109">Get the list of storage farm metrics.</span></span>

## <span data-ttu-id="737da-110">OS</span><span class="sxs-lookup"><span data-stu-id="737da-110">PARAMETERS</span></span>

### <span data-ttu-id="737da-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="737da-111">-FarmName</span></span>
<span data-ttu-id="737da-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="737da-112">Farm Id.</span></span>

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

### <span data-ttu-id="737da-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737da-113">-ResourceGroupName</span></span>
<span data-ttu-id="737da-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="737da-114">Resource group name.</span></span>

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

### <span data-ttu-id="737da-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="737da-115">-Skip</span></span>
<span data-ttu-id="737da-116">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="737da-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="737da-117">-Início</span><span class="sxs-lookup"><span data-stu-id="737da-117">-Top</span></span>
<span data-ttu-id="737da-118">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="737da-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="737da-119">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="737da-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="737da-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737da-120">CommonParameters</span></span>
<span data-ttu-id="737da-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737da-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737da-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="737da-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737da-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="737da-123">INPUTS</span></span>

## <span data-ttu-id="737da-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="737da-124">OUTPUTS</span></span>

### <span data-ttu-id="737da-125">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="737da-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="737da-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="737da-126">NOTES</span></span>

## <span data-ttu-id="737da-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="737da-127">RELATED LINKS</span></span>

