---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281380"
---
# <span data-ttu-id="06169-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="06169-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="06169-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06169-102">SYNOPSIS</span></span>
<span data-ttu-id="06169-103">Obtém as configurações de produtividade correspondentes a um banco de dados SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="06169-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="06169-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06169-104">SYNTAX</span></span>

### <span data-ttu-id="06169-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="06169-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06169-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06169-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06169-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06169-107">DESCRIPTION</span></span>
<span data-ttu-id="06169-108">O cmdlet **Get-AzCosmosDBSqlDatabaseThroughput** Obtém as configurações de produtividade correspondentes a um banco de dados SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="06169-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="06169-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06169-109">EXAMPLES</span></span>

### <span data-ttu-id="06169-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06169-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="06169-111">OS</span><span class="sxs-lookup"><span data-stu-id="06169-111">PARAMETERS</span></span>

### <span data-ttu-id="06169-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="06169-112">-AccountName</span></span>
<span data-ttu-id="06169-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="06169-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="06169-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06169-114">-DefaultProfile</span></span>
<span data-ttu-id="06169-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06169-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06169-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06169-116">-InputObject</span></span>
<span data-ttu-id="06169-117">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="06169-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="06169-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="06169-118">-Name</span></span>
<span data-ttu-id="06169-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="06169-119">Database name.</span></span>

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

### <span data-ttu-id="06169-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06169-120">-ResourceGroupName</span></span>
<span data-ttu-id="06169-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06169-121">Name of resource group.</span></span>

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

### <span data-ttu-id="06169-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06169-122">CommonParameters</span></span>
<span data-ttu-id="06169-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06169-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06169-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06169-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06169-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06169-125">INPUTS</span></span>

### <span data-ttu-id="06169-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="06169-126">None</span></span>

## <span data-ttu-id="06169-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06169-127">OUTPUTS</span></span>

### <span data-ttu-id="06169-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="06169-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="06169-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06169-129">NOTES</span></span>

## <span data-ttu-id="06169-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06169-130">RELATED LINKS</span></span>
