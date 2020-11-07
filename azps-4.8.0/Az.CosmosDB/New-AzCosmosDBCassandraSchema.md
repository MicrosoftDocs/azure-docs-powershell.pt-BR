---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955694"
---
# <span data-ttu-id="0a51a-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="0a51a-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="0a51a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a51a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a51a-103">Cria um novo esquema CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0a51a-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="0a51a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a51a-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a51a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a51a-105">DESCRIPTION</span></span>
<span data-ttu-id="0a51a-106">O **New-AzCosmosDBCassandraSchema** cria um novo esquema Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0a51a-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="0a51a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a51a-107">EXAMPLES</span></span>

### <span data-ttu-id="0a51a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0a51a-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="0a51a-109">OS</span><span class="sxs-lookup"><span data-stu-id="0a51a-109">PARAMETERS</span></span>

### <span data-ttu-id="0a51a-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="0a51a-110">-ClusterKey</span></span>
<span data-ttu-id="0a51a-111">Matriz de objetos PSClusterKey.</span><span class="sxs-lookup"><span data-stu-id="0a51a-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="0a51a-112">-Coluna</span><span class="sxs-lookup"><span data-stu-id="0a51a-112">-Column</span></span>
<span data-ttu-id="0a51a-113">Objeto PSColumn.</span><span class="sxs-lookup"><span data-stu-id="0a51a-113">PSColumn object.</span></span>

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

### <span data-ttu-id="0a51a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a51a-114">-DefaultProfile</span></span>
<span data-ttu-id="0a51a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a51a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a51a-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="0a51a-116">-PartitionKey</span></span>
<span data-ttu-id="0a51a-117">Matriz de cadeias de caracteres que contêm chaves de partição.</span><span class="sxs-lookup"><span data-stu-id="0a51a-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="0a51a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a51a-118">CommonParameters</span></span>
<span data-ttu-id="0a51a-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a51a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a51a-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a51a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a51a-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a51a-121">INPUTS</span></span>

### <span data-ttu-id="0a51a-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0a51a-122">None</span></span>

## <span data-ttu-id="0a51a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a51a-123">OUTPUTS</span></span>

### <span data-ttu-id="0a51a-124">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="0a51a-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="0a51a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a51a-125">NOTES</span></span>

## <span data-ttu-id="0a51a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a51a-126">RELATED LINKS</span></span>
