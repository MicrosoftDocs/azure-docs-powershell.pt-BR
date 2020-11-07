---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940558"
---
# <span data-ttu-id="15778-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="15778-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="15778-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15778-102">SYNOPSIS</span></span>
<span data-ttu-id="15778-103">Cria um novo esquema CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="15778-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="15778-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15778-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15778-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15778-105">DESCRIPTION</span></span>
<span data-ttu-id="15778-106">O **New-AzCosmosDBCassandraSchema** cria um novo esquema Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="15778-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="15778-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15778-107">EXAMPLES</span></span>

### <span data-ttu-id="15778-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="15778-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="15778-109">OS</span><span class="sxs-lookup"><span data-stu-id="15778-109">PARAMETERS</span></span>

### <span data-ttu-id="15778-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="15778-110">-ClusterKey</span></span>
<span data-ttu-id="15778-111">Matriz de objetos PSClusterKey.</span><span class="sxs-lookup"><span data-stu-id="15778-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="15778-112">-Coluna</span><span class="sxs-lookup"><span data-stu-id="15778-112">-Column</span></span>
<span data-ttu-id="15778-113">Objeto PSColumn.</span><span class="sxs-lookup"><span data-stu-id="15778-113">PSColumn object.</span></span>

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

### <span data-ttu-id="15778-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15778-114">-DefaultProfile</span></span>
<span data-ttu-id="15778-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15778-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15778-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="15778-116">-PartitionKey</span></span>
<span data-ttu-id="15778-117">Matriz de cadeias de caracteres que contêm chaves de partição.</span><span class="sxs-lookup"><span data-stu-id="15778-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="15778-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15778-118">CommonParameters</span></span>
<span data-ttu-id="15778-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15778-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15778-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15778-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15778-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15778-121">INPUTS</span></span>

### <span data-ttu-id="15778-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="15778-122">None</span></span>

## <span data-ttu-id="15778-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15778-123">OUTPUTS</span></span>

### <span data-ttu-id="15778-124">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="15778-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="15778-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15778-125">NOTES</span></span>

## <span data-ttu-id="15778-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15778-126">RELATED LINKS</span></span>
