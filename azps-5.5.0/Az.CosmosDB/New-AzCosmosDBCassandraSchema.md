---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111041"
---
# <span data-ttu-id="f7e37-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="f7e37-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="f7e37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7e37-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e37-103">Cria um novo Esquema Defamado DalMdb.</span><span class="sxs-lookup"><span data-stu-id="f7e37-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="f7e37-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7e37-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7e37-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7e37-105">DESCRIPTION</span></span>
<span data-ttu-id="f7e37-106">O **New-AzCosmosDBCasschema** cria um novo Esquema de Schema do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f7e37-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="f7e37-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f7e37-107">EXAMPLES</span></span>

### <span data-ttu-id="f7e37-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f7e37-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="f7e37-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7e37-109">PARAMETERS</span></span>

### <span data-ttu-id="f7e37-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="f7e37-110">-ClusterKey</span></span>
<span data-ttu-id="f7e37-111">Matriz de objetos PSClusterKey.</span><span class="sxs-lookup"><span data-stu-id="f7e37-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="f7e37-112">-Coluna</span><span class="sxs-lookup"><span data-stu-id="f7e37-112">-Column</span></span>
<span data-ttu-id="f7e37-113">Objeto PSColumn.</span><span class="sxs-lookup"><span data-stu-id="f7e37-113">PSColumn object.</span></span>

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

### <span data-ttu-id="f7e37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e37-114">-DefaultProfile</span></span>
<span data-ttu-id="f7e37-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7e37-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7e37-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="f7e37-116">-PartitionKey</span></span>
<span data-ttu-id="f7e37-117">Matriz de cadeias de caracteres que contêm as Teclas de Partição.</span><span class="sxs-lookup"><span data-stu-id="f7e37-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="f7e37-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e37-118">CommonParameters</span></span>
<span data-ttu-id="f7e37-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7e37-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e37-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7e37-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e37-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="f7e37-121">INPUTS</span></span>

### <span data-ttu-id="f7e37-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f7e37-122">None</span></span>

## <span data-ttu-id="f7e37-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="f7e37-123">OUTPUTS</span></span>

### <span data-ttu-id="f7e37-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCasschema</span><span class="sxs-lookup"><span data-stu-id="f7e37-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="f7e37-125">Notas</span><span class="sxs-lookup"><span data-stu-id="f7e37-125">NOTES</span></span>

## <span data-ttu-id="f7e37-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7e37-126">RELATED LINKS</span></span>
