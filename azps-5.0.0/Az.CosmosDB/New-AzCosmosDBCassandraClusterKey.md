---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281344"
---
# <span data-ttu-id="e68d7-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="e68d7-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="e68d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e68d7-102">SYNOPSIS</span></span>
<span data-ttu-id="e68d7-103">Cria uma nova chave de cluster CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e68d7-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="e68d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e68d7-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e68d7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e68d7-105">DESCRIPTION</span></span>
<span data-ttu-id="e68d7-106">O **New-AzCosmosDBCassandraClusterKey** cria uma nova chave de cluster CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e68d7-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="e68d7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e68d7-107">EXAMPLES</span></span>

### <span data-ttu-id="e68d7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e68d7-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="e68d7-109">OS</span><span class="sxs-lookup"><span data-stu-id="e68d7-109">PARAMETERS</span></span>

### <span data-ttu-id="e68d7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e68d7-110">-DefaultProfile</span></span>
<span data-ttu-id="e68d7-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e68d7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e68d7-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="e68d7-112">-Name</span></span>
<span data-ttu-id="e68d7-113">Nome da chave de cluster Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e68d7-113">Name of Cassandra Cluster Key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68d7-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="e68d7-114">-OrderBy</span></span>
<span data-ttu-id="e68d7-115">Ordem da chave de cluster Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e68d7-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="e68d7-116">Os valores possíveis incluem: ' ASC ', ' DESC '</span><span class="sxs-lookup"><span data-stu-id="e68d7-116">Possible values include: 'Asc', 'Desc'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68d7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e68d7-117">CommonParameters</span></span>
<span data-ttu-id="e68d7-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e68d7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e68d7-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e68d7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e68d7-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e68d7-120">INPUTS</span></span>

### <span data-ttu-id="e68d7-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e68d7-121">None</span></span>

## <span data-ttu-id="e68d7-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e68d7-122">OUTPUTS</span></span>

### <span data-ttu-id="e68d7-123">Microsoft. Azure. Commands. CosmosDB. Models. PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="e68d7-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="e68d7-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e68d7-124">NOTES</span></span>

## <span data-ttu-id="e68d7-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e68d7-125">RELATED LINKS</span></span>
