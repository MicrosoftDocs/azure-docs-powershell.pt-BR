---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: 612f4623c7944c3c3d930ece44d4c2ae938e1a68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940912"
---
# <span data-ttu-id="c2ea9-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="c2ea9-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="c2ea9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ea9-103">Cria um novo objeto do tipo PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="c2ea9-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="c2ea9-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="c2ea9-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="c2ea9-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2ea9-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2ea9-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2ea9-106">DESCRIPTION</span></span>
<span data-ttu-id="c2ea9-107">Objeto correspondente ao CompositePath da API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="c2ea9-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="c2ea9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2ea9-108">EXAMPLES</span></span>

### <span data-ttu-id="c2ea9-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c2ea9-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="c2ea9-110">OS</span><span class="sxs-lookup"><span data-stu-id="c2ea9-110">PARAMETERS</span></span>

### <span data-ttu-id="c2ea9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ea9-111">-DefaultProfile</span></span>
<span data-ttu-id="c2ea9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ea9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ea9-113">-Pedido</span><span class="sxs-lookup"><span data-stu-id="c2ea9-113">-Order</span></span>
<span data-ttu-id="c2ea9-114">Obtém ou define a ordem de classificação para caminhos compostos.</span><span class="sxs-lookup"><span data-stu-id="c2ea9-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="c2ea9-115">Os valores possíveis incluem: ' crescente ', ' decrescente '</span><span class="sxs-lookup"><span data-stu-id="c2ea9-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="c2ea9-116">-Caminho</span><span class="sxs-lookup"><span data-stu-id="c2ea9-116">-Path</span></span>
<span data-ttu-id="c2ea9-117">O caminho ao qual o comportamento de indexação se aplica.</span><span class="sxs-lookup"><span data-stu-id="c2ea9-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="c2ea9-118">Os caminhos de índice geralmente começam com root e end com curinga (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="c2ea9-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="c2ea9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ea9-119">CommonParameters</span></span>
<span data-ttu-id="c2ea9-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ea9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ea9-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2ea9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ea9-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2ea9-122">INPUTS</span></span>

### <span data-ttu-id="c2ea9-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c2ea9-123">None</span></span>

## <span data-ttu-id="c2ea9-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2ea9-124">OUTPUTS</span></span>

### <span data-ttu-id="c2ea9-125">Microsoft. Azure. Commands. CosmosDB. Models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="c2ea9-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="c2ea9-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2ea9-126">NOTES</span></span>

## <span data-ttu-id="c2ea9-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2ea9-127">RELATED LINKS</span></span>
