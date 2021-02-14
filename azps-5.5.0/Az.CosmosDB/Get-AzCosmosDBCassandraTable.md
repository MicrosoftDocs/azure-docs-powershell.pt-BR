---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116479"
---
# <span data-ttu-id="7c892-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="7c892-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="7c892-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c892-102">SYNOPSIS</span></span>
<span data-ttu-id="7c892-103">Obtém uma Tabela Desarmão Dalmdb.</span><span class="sxs-lookup"><span data-stu-id="7c892-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="7c892-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c892-104">SYNTAX</span></span>

### <span data-ttu-id="7c892-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7c892-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c892-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c892-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c892-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c892-107">DESCRIPTION</span></span>
<span data-ttu-id="7c892-108">O cmdlet **Get-AzCosmosDBCasstable** cria um novo ou atualiza um Espaço de Keyspace existente do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7c892-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="7c892-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7c892-109">EXAMPLES</span></span>

### <span data-ttu-id="7c892-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7c892-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="7c892-111">{{ Get-AzCosmosDBCassandraTable obtém as propriedades de umKeyspace existente.</span><span class="sxs-lookup"><span data-stu-id="7c892-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="7c892-112">Você pode expandir o Recurso para obter as propriedades DefaultTtl, Esquema, _etag, _ts, _rid.}}</span><span class="sxs-lookup"><span data-stu-id="7c892-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="7c892-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c892-113">PARAMETERS</span></span>

### <span data-ttu-id="7c892-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="7c892-114">-AccountName</span></span>
<span data-ttu-id="7c892-115">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="7c892-115">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c892-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c892-116">-DefaultProfile</span></span>
<span data-ttu-id="7c892-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c892-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c892-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="7c892-118">-KeyspaceName</span></span>
<span data-ttu-id="7c892-119">Nome do Espaço de Teclas Denúm.</span><span class="sxs-lookup"><span data-stu-id="7c892-119">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c892-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c892-120">-Name</span></span>
<span data-ttu-id="7c892-121">Nome da tabela Desarmá.</span><span class="sxs-lookup"><span data-stu-id="7c892-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="7c892-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7c892-122">-ParentObject</span></span>
<span data-ttu-id="7c892-123">Objeto Desarmado Keyspace.</span><span class="sxs-lookup"><span data-stu-id="7c892-123">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c892-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c892-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c892-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7c892-125">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c892-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c892-126">CommonParameters</span></span>
<span data-ttu-id="7c892-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c892-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c892-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c892-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c892-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="7c892-129">INPUTS</span></span>

### <span data-ttu-id="7c892-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="7c892-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="7c892-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="7c892-131">OUTPUTS</span></span>

### <span data-ttu-id="7c892-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCasstableGetResults</span><span class="sxs-lookup"><span data-stu-id="7c892-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="7c892-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7c892-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7c892-134">Notas</span><span class="sxs-lookup"><span data-stu-id="7c892-134">NOTES</span></span>

## <span data-ttu-id="7c892-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c892-135">RELATED LINKS</span></span>
