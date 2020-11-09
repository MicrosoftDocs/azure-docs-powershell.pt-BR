---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: 0def7fc552563f9b859fd6af7d07be5cd14cd001
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281300"
---
# <span data-ttu-id="e99f0-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="e99f0-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="e99f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e99f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e99f0-103">Cria um novo objeto do tipo PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="e99f0-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="e99f0-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="e99f0-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="e99f0-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e99f0-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e99f0-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e99f0-106">DESCRIPTION</span></span>
<span data-ttu-id="e99f0-107">Objeto correspondente ao IncludedPath da API SQL.</span><span class="sxs-lookup"><span data-stu-id="e99f0-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="e99f0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e99f0-108">EXAMPLES</span></span>

### <span data-ttu-id="e99f0-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e99f0-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="e99f0-110">OS</span><span class="sxs-lookup"><span data-stu-id="e99f0-110">PARAMETERS</span></span>

### <span data-ttu-id="e99f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e99f0-111">-DefaultProfile</span></span>
<span data-ttu-id="e99f0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e99f0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e99f0-113">-Índice</span><span class="sxs-lookup"><span data-stu-id="e99f0-113">-Index</span></span>
<span data-ttu-id="e99f0-114">Lista de índices para esse caminho</span><span class="sxs-lookup"><span data-stu-id="e99f0-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="e99f0-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="e99f0-115">-Path</span></span>
<span data-ttu-id="e99f0-116">O caminho ao qual o comportamento de indexação se aplica.</span><span class="sxs-lookup"><span data-stu-id="e99f0-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="e99f0-117">Os caminhos de índice geralmente começam com root e end com curinga (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="e99f0-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="e99f0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e99f0-118">CommonParameters</span></span>
<span data-ttu-id="e99f0-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e99f0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e99f0-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e99f0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e99f0-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e99f0-121">INPUTS</span></span>

### <span data-ttu-id="e99f0-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e99f0-122">None</span></span>

## <span data-ttu-id="e99f0-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e99f0-123">OUTPUTS</span></span>

### <span data-ttu-id="e99f0-124">Microsoft. Azure. Commands. CosmosDB. Models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="e99f0-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="e99f0-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e99f0-125">NOTES</span></span>

## <span data-ttu-id="e99f0-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e99f0-126">RELATED LINKS</span></span>
