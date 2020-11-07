---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777397"
---
# <span data-ttu-id="89bba-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="89bba-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="89bba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89bba-102">SYNOPSIS</span></span>
<span data-ttu-id="89bba-103">Cria um novo objeto do tipo PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="89bba-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="89bba-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="89bba-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="89bba-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89bba-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89bba-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89bba-106">DESCRIPTION</span></span>
<span data-ttu-id="89bba-107">Objeto correspondente ao IncludedPath da API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="89bba-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="89bba-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89bba-108">EXAMPLES</span></span>

### <span data-ttu-id="89bba-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89bba-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="89bba-110">OS</span><span class="sxs-lookup"><span data-stu-id="89bba-110">PARAMETERS</span></span>

### <span data-ttu-id="89bba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89bba-111">-DefaultProfile</span></span>
<span data-ttu-id="89bba-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89bba-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89bba-113">-Índice</span><span class="sxs-lookup"><span data-stu-id="89bba-113">-Index</span></span>
<span data-ttu-id="89bba-114">Lista de índices para esse caminho</span><span class="sxs-lookup"><span data-stu-id="89bba-114">List of indexes for this path</span></span>

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89bba-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="89bba-115">-Path</span></span>
<span data-ttu-id="89bba-116">O caminho ao qual o comportamento de indexação se aplica.</span><span class="sxs-lookup"><span data-stu-id="89bba-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="89bba-117">Os caminhos de índice geralmente começam com root e end com curinga (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="89bba-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="89bba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89bba-118">CommonParameters</span></span>
<span data-ttu-id="89bba-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89bba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89bba-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89bba-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89bba-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89bba-121">INPUTS</span></span>

### <span data-ttu-id="89bba-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="89bba-122">None</span></span>

## <span data-ttu-id="89bba-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89bba-123">OUTPUTS</span></span>

### <span data-ttu-id="89bba-124">Microsoft. Azure. Commands. CosmosDB. Models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="89bba-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="89bba-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89bba-125">NOTES</span></span>

## <span data-ttu-id="89bba-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89bba-126">RELATED LINKS</span></span>
