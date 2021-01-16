---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430060"
---
# <span data-ttu-id="1f6a0-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="1f6a0-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="1f6a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f6a0-102">SYNOPSIS</span></span>
<span data-ttu-id="1f6a0-103">Cria um novo esquema CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="1f6a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f6a0-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f6a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f6a0-105">DESCRIPTION</span></span>
<span data-ttu-id="1f6a0-106">O **New-AzCosmosDBCassandraSchema** cria um novo esquema Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="1f6a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f6a0-107">EXAMPLES</span></span>

### <span data-ttu-id="1f6a0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f6a0-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="1f6a0-109">OS</span><span class="sxs-lookup"><span data-stu-id="1f6a0-109">PARAMETERS</span></span>

### <span data-ttu-id="1f6a0-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="1f6a0-110">-ClusterKey</span></span>
<span data-ttu-id="1f6a0-111">Matriz de objetos PSClusterKey.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-111">Array of PSClusterKey objects.</span></span>

```yaml
Type: PSClusterKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f6a0-112">-Coluna</span><span class="sxs-lookup"><span data-stu-id="1f6a0-112">-Column</span></span>
<span data-ttu-id="1f6a0-113">Objeto PSColumn.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-113">PSColumn object.</span></span>

```yaml
Type: PSColumn[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f6a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6a0-114">-DefaultProfile</span></span>
<span data-ttu-id="1f6a0-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f6a0-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="1f6a0-116">-PartitionKey</span></span>
<span data-ttu-id="1f6a0-117">Matriz de cadeias de caracteres que contêm chaves de partição.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-117">Array of strings containing Partition Keys.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f6a0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6a0-118">CommonParameters</span></span>
<span data-ttu-id="1f6a0-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6a0-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f6a0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6a0-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f6a0-121">INPUTS</span></span>

### <span data-ttu-id="1f6a0-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1f6a0-122">None</span></span>

## <span data-ttu-id="1f6a0-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f6a0-123">OUTPUTS</span></span>

### <span data-ttu-id="1f6a0-124">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="1f6a0-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="1f6a0-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f6a0-125">NOTES</span></span>

## <span data-ttu-id="1f6a0-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f6a0-126">RELATED LINKS</span></span>
