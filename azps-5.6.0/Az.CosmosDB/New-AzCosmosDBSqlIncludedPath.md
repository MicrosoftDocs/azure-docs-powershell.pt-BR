---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: a9d77cc76521eca1e99dac630673ef3825d1155b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886690"
---
# <span data-ttu-id="a1b3b-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="a1b3b-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="a1b3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b3b-103">Cria um novo objeto do tipo PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="a1b3b-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="a1b3b-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="a1b3b-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="a1b3b-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a1b3b-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1b3b-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a1b3b-106">DESCRIPTION</span></span>
<span data-ttu-id="a1b3b-107">Objeto correspondente ao IncludedPath da API sql.</span><span class="sxs-lookup"><span data-stu-id="a1b3b-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="a1b3b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1b3b-108">EXAMPLES</span></span>

### <span data-ttu-id="a1b3b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1b3b-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="a1b3b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a1b3b-110">PARAMETERS</span></span>

### <span data-ttu-id="a1b3b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b3b-111">-DefaultProfile</span></span>
<span data-ttu-id="a1b3b-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b3b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b3b-113">-Index</span><span class="sxs-lookup"><span data-stu-id="a1b3b-113">-Index</span></span>
<span data-ttu-id="a1b3b-114">Lista de índices para esse caminho</span><span class="sxs-lookup"><span data-stu-id="a1b3b-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="a1b3b-115">-Path</span><span class="sxs-lookup"><span data-stu-id="a1b3b-115">-Path</span></span>
<span data-ttu-id="a1b3b-116">O caminho ao qual o comportamento de indexação se aplica.</span><span class="sxs-lookup"><span data-stu-id="a1b3b-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="a1b3b-117">Os caminhos de índice geralmente começam com raiz e terminam com caractere curinga (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="a1b3b-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="a1b3b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b3b-118">CommonParameters</span></span>
<span data-ttu-id="a1b3b-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b3b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b3b-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1b3b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b3b-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1b3b-121">INPUTS</span></span>

### <span data-ttu-id="a1b3b-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a1b3b-122">None</span></span>

## <span data-ttu-id="a1b3b-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a1b3b-123">OUTPUTS</span></span>

### <span data-ttu-id="a1b3b-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="a1b3b-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="a1b3b-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="a1b3b-125">NOTES</span></span>

## <span data-ttu-id="a1b3b-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1b3b-126">RELATED LINKS</span></span>
