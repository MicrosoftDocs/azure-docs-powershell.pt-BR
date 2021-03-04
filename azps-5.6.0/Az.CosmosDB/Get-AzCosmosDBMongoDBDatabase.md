---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 0dfcffe55eb3214f4be9d6ccfb34231d1c9ea50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890875"
---
# <span data-ttu-id="498dd-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="498dd-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="498dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="498dd-102">SYNOPSIS</span></span>
<span data-ttu-id="498dd-103">Obtém o banco de dados MongoDB do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="498dd-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="498dd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="498dd-104">SYNTAX</span></span>

### <span data-ttu-id="498dd-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="498dd-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="498dd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="498dd-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="498dd-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="498dd-107">DESCRIPTION</span></span>
<span data-ttu-id="498dd-108">O cmdlet **Get-AzCosmosDBMongoDBDatabase** obtém o Banco de Dados MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="498dd-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="498dd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="498dd-109">EXAMPLES</span></span>

### <span data-ttu-id="498dd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="498dd-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="498dd-111">Objeto Resource contém _rid, _ts, _etag propriedades.</span><span class="sxs-lookup"><span data-stu-id="498dd-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="498dd-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="498dd-112">PARAMETERS</span></span>

### <span data-ttu-id="498dd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="498dd-113">-AccountName</span></span>
<span data-ttu-id="498dd-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="498dd-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="498dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="498dd-115">-DefaultProfile</span></span>
<span data-ttu-id="498dd-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="498dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="498dd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="498dd-117">-Name</span></span>
<span data-ttu-id="498dd-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="498dd-118">Database name.</span></span>

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

### <span data-ttu-id="498dd-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="498dd-119">-ParentObject</span></span>
<span data-ttu-id="498dd-120">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="498dd-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="498dd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="498dd-121">-ResourceGroupName</span></span>
<span data-ttu-id="498dd-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="498dd-122">Name of resource group.</span></span>

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

### <span data-ttu-id="498dd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498dd-123">CommonParameters</span></span>
<span data-ttu-id="498dd-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="498dd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498dd-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="498dd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498dd-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="498dd-126">INPUTS</span></span>

### <span data-ttu-id="498dd-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="498dd-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="498dd-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="498dd-128">OUTPUTS</span></span>

### <span data-ttu-id="498dd-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="498dd-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="498dd-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="498dd-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="498dd-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="498dd-131">NOTES</span></span>

## <span data-ttu-id="498dd-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="498dd-132">RELATED LINKS</span></span>
