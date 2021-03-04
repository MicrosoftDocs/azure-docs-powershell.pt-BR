---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 5bf35b43db1f1d961f24c1aa2c75c9f17c333345
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886243"
---
# <span data-ttu-id="76a4f-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="76a4f-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="76a4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="76a4f-103">Obtém as configurações de transferência correspondentes a um Banco de Dados Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="76a4f-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="76a4f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="76a4f-104">SYNTAX</span></span>

### <span data-ttu-id="76a4f-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="76a4f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76a4f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76a4f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76a4f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="76a4f-107">DESCRIPTION</span></span>
<span data-ttu-id="76a4f-108">O cmdlet **Get-AzCosmosDBSqlDatabaseThroughput** obtém as configurações de transferência correspondentes a um Banco de Dados Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="76a4f-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="76a4f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76a4f-109">EXAMPLES</span></span>

### <span data-ttu-id="76a4f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76a4f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="76a4f-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="76a4f-111">PARAMETERS</span></span>

### <span data-ttu-id="76a4f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="76a4f-112">-AccountName</span></span>
<span data-ttu-id="76a4f-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="76a4f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="76a4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a4f-114">-DefaultProfile</span></span>
<span data-ttu-id="76a4f-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76a4f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a4f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76a4f-116">-InputObject</span></span>
<span data-ttu-id="76a4f-117">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="76a4f-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76a4f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="76a4f-118">-Name</span></span>
<span data-ttu-id="76a4f-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="76a4f-119">Database name.</span></span>

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

### <span data-ttu-id="76a4f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a4f-120">-ResourceGroupName</span></span>
<span data-ttu-id="76a4f-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="76a4f-121">Name of resource group.</span></span>

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

### <span data-ttu-id="76a4f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a4f-122">CommonParameters</span></span>
<span data-ttu-id="76a4f-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a4f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a4f-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76a4f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a4f-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76a4f-125">INPUTS</span></span>

### <span data-ttu-id="76a4f-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="76a4f-126">None</span></span>

## <span data-ttu-id="76a4f-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="76a4f-127">OUTPUTS</span></span>

### <span data-ttu-id="76a4f-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="76a4f-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="76a4f-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="76a4f-129">NOTES</span></span>

## <span data-ttu-id="76a4f-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76a4f-130">RELATED LINKS</span></span>
