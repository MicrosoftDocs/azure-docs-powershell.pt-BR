---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 3a19e0c60b5a32e1d1083b1afba55a8bf3045fe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889337"
---
# <span data-ttu-id="52482-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="52482-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="52482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52482-102">SYNOPSIS</span></span>
<span data-ttu-id="52482-103">Cria um novo Esquema de Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="52482-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="52482-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="52482-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52482-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52482-105">DESCRIPTION</span></span>
<span data-ttu-id="52482-106">O **New-AzCosmosDBCassandraSchema** cria um novo Esquema de Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="52482-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="52482-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52482-107">EXAMPLES</span></span>

### <span data-ttu-id="52482-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52482-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="52482-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="52482-109">PARAMETERS</span></span>

### <span data-ttu-id="52482-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="52482-110">-ClusterKey</span></span>
<span data-ttu-id="52482-111">Matriz de objetos PSClusterKey.</span><span class="sxs-lookup"><span data-stu-id="52482-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="52482-112">-Column</span><span class="sxs-lookup"><span data-stu-id="52482-112">-Column</span></span>
<span data-ttu-id="52482-113">Objeto PSColumn.</span><span class="sxs-lookup"><span data-stu-id="52482-113">PSColumn object.</span></span>

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

### <span data-ttu-id="52482-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52482-114">-DefaultProfile</span></span>
<span data-ttu-id="52482-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52482-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52482-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="52482-116">-PartitionKey</span></span>
<span data-ttu-id="52482-117">Matriz de cadeias de caracteres que contêm Chaves de Partição.</span><span class="sxs-lookup"><span data-stu-id="52482-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="52482-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52482-118">CommonParameters</span></span>
<span data-ttu-id="52482-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52482-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52482-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52482-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52482-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52482-121">INPUTS</span></span>

### <span data-ttu-id="52482-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="52482-122">None</span></span>

## <span data-ttu-id="52482-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="52482-123">OUTPUTS</span></span>

### <span data-ttu-id="52482-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="52482-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="52482-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="52482-125">NOTES</span></span>

## <span data-ttu-id="52482-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52482-126">RELATED LINKS</span></span>
