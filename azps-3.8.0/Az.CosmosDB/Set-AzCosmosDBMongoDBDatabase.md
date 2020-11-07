---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 2ee1f932e1829e6c1d9d35ccd2cf67473a851414
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944435"
---
# <span data-ttu-id="34232-101">Set-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="34232-101">Set-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="34232-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34232-102">SYNOPSIS</span></span>
<span data-ttu-id="34232-103">Define o banco de dados do CosmosDB MongoDB</span><span class="sxs-lookup"><span data-stu-id="34232-103">Sets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="34232-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34232-104">SYNTAX</span></span>

### <span data-ttu-id="34232-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="34232-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34232-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34232-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34232-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34232-107">DESCRIPTION</span></span>
<span data-ttu-id="34232-108">O cmdlet **set-AzCosmosDBMongoDBDatabase** Obtém o banco de dados do MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="34232-108">The **Set-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="34232-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34232-109">EXAMPLES</span></span>

### <span data-ttu-id="34232-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="34232-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="34232-111">Objeto de recurso contém propriedades _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="34232-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="34232-112">OS</span><span class="sxs-lookup"><span data-stu-id="34232-112">PARAMETERS</span></span>

### <span data-ttu-id="34232-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="34232-113">-AccountName</span></span>
<span data-ttu-id="34232-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="34232-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="34232-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="34232-115">-Confirm</span></span>
<span data-ttu-id="34232-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34232-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34232-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34232-117">-DefaultProfile</span></span>
<span data-ttu-id="34232-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34232-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34232-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34232-119">-InputObject</span></span>
<span data-ttu-id="34232-120">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="34232-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34232-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="34232-121">-Name</span></span>
<span data-ttu-id="34232-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="34232-122">Database name.</span></span>

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

### <span data-ttu-id="34232-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34232-123">-ResourceGroupName</span></span>
<span data-ttu-id="34232-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="34232-124">Name of resource group.</span></span>

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

### <span data-ttu-id="34232-125">-Throughput</span><span class="sxs-lookup"><span data-stu-id="34232-125">-Throughput</span></span>
<span data-ttu-id="34232-126">A produtividade do banco de dados do Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="34232-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="34232-127">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="34232-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34232-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34232-128">-WhatIf</span></span>
<span data-ttu-id="34232-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34232-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34232-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34232-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34232-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34232-131">CommonParameters</span></span>
<span data-ttu-id="34232-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34232-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34232-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34232-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34232-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34232-134">INPUTS</span></span>

### <span data-ttu-id="34232-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="34232-135">None</span></span>

## <span data-ttu-id="34232-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34232-136">OUTPUTS</span></span>

### <span data-ttu-id="34232-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="34232-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="34232-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34232-138">NOTES</span></span>

## <span data-ttu-id="34232-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34232-139">RELATED LINKS</span></span>
