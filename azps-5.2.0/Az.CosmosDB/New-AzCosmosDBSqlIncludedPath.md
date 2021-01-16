---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: 0def7fc552563f9b859fd6af7d07be5cd14cd001
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262112"
---
# <span data-ttu-id="f0294-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="f0294-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="f0294-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0294-102">SYNOPSIS</span></span>
<span data-ttu-id="f0294-103">Cria um novo objeto do tipo PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="f0294-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="f0294-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="f0294-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="f0294-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0294-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0294-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0294-106">DESCRIPTION</span></span>
<span data-ttu-id="f0294-107">Objeto correspondente ao IncludedPath da API SQL.</span><span class="sxs-lookup"><span data-stu-id="f0294-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="f0294-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0294-108">EXAMPLES</span></span>

### <span data-ttu-id="f0294-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0294-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="f0294-110">OS</span><span class="sxs-lookup"><span data-stu-id="f0294-110">PARAMETERS</span></span>

### <span data-ttu-id="f0294-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0294-111">-DefaultProfile</span></span>
<span data-ttu-id="f0294-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0294-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0294-113">-Índice</span><span class="sxs-lookup"><span data-stu-id="f0294-113">-Index</span></span>
<span data-ttu-id="f0294-114">Lista de índices para esse caminho</span><span class="sxs-lookup"><span data-stu-id="f0294-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="f0294-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f0294-115">-Path</span></span>
<span data-ttu-id="f0294-116">O caminho ao qual o comportamento de indexação se aplica.</span><span class="sxs-lookup"><span data-stu-id="f0294-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="f0294-117">Os caminhos de índice geralmente começam com root e end com curinga (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="f0294-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="f0294-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0294-118">CommonParameters</span></span>
<span data-ttu-id="f0294-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0294-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0294-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0294-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0294-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0294-121">INPUTS</span></span>

### <span data-ttu-id="f0294-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f0294-122">None</span></span>

## <span data-ttu-id="f0294-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0294-123">OUTPUTS</span></span>

### <span data-ttu-id="f0294-124">Microsoft. Azure. Commands. CosmosDB. Models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="f0294-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="f0294-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0294-125">NOTES</span></span>

## <span data-ttu-id="f0294-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0294-126">RELATED LINKS</span></span>
