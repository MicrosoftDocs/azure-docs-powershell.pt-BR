---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: 9afcffc281c48e0235c814b352e65ae47e5f4337
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892870"
---
# <span data-ttu-id="237e4-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="237e4-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="237e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="237e4-102">SYNOPSIS</span></span>
<span data-ttu-id="237e4-103">Cria uma nova Chave de Cluster de Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="237e4-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="237e4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="237e4-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="237e4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="237e4-105">DESCRIPTION</span></span>
<span data-ttu-id="237e4-106">O **New-AzCosmosDBCassandraClusterKey** cria uma nova Chave de Cluster de Cassandra de CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="237e4-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="237e4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="237e4-107">EXAMPLES</span></span>

### <span data-ttu-id="237e4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="237e4-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="237e4-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="237e4-109">PARAMETERS</span></span>

### <span data-ttu-id="237e4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237e4-110">-DefaultProfile</span></span>
<span data-ttu-id="237e4-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="237e4-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="237e4-112">-Name</span><span class="sxs-lookup"><span data-stu-id="237e4-112">-Name</span></span>
<span data-ttu-id="237e4-113">Nome da Chave de Cluster de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="237e4-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="237e4-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="237e4-114">-OrderBy</span></span>
<span data-ttu-id="237e4-115">Ordenação da chave do Cluster de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="237e4-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="237e4-116">Os valores possíveis incluem: 'Asc', 'Desc'</span><span class="sxs-lookup"><span data-stu-id="237e4-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="237e4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237e4-117">CommonParameters</span></span>
<span data-ttu-id="237e4-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="237e4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="237e4-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="237e4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237e4-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="237e4-120">INPUTS</span></span>

### <span data-ttu-id="237e4-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="237e4-121">None</span></span>

## <span data-ttu-id="237e4-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="237e4-122">OUTPUTS</span></span>

### <span data-ttu-id="237e4-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="237e4-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="237e4-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="237e4-124">NOTES</span></span>

## <span data-ttu-id="237e4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="237e4-125">RELATED LINKS</span></span>
