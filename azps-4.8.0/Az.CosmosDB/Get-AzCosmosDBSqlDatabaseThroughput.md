---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112874"
---
# <span data-ttu-id="a48fc-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="a48fc-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="a48fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a48fc-102">SYNOPSIS</span></span>
<span data-ttu-id="a48fc-103">Obtém as configurações de produtividade correspondentes a um banco de dados SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a48fc-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="a48fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a48fc-104">SYNTAX</span></span>

### <span data-ttu-id="a48fc-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a48fc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a48fc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a48fc-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a48fc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a48fc-107">DESCRIPTION</span></span>
<span data-ttu-id="a48fc-108">O cmdlet **Get-AzCosmosDBSqlDatabaseThroughput** Obtém as configurações de produtividade correspondentes a um banco de dados SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a48fc-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="a48fc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a48fc-109">EXAMPLES</span></span>

### <span data-ttu-id="a48fc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a48fc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="a48fc-111">OS</span><span class="sxs-lookup"><span data-stu-id="a48fc-111">PARAMETERS</span></span>

### <span data-ttu-id="a48fc-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a48fc-112">-AccountName</span></span>
<span data-ttu-id="a48fc-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="a48fc-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a48fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a48fc-114">-DefaultProfile</span></span>
<span data-ttu-id="a48fc-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a48fc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a48fc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a48fc-116">-InputObject</span></span>
<span data-ttu-id="a48fc-117">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a48fc-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a48fc-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a48fc-118">-Name</span></span>
<span data-ttu-id="a48fc-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a48fc-119">Database name.</span></span>

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

### <span data-ttu-id="a48fc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a48fc-120">-ResourceGroupName</span></span>
<span data-ttu-id="a48fc-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a48fc-121">Name of resource group.</span></span>

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

### <span data-ttu-id="a48fc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a48fc-122">CommonParameters</span></span>
<span data-ttu-id="a48fc-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a48fc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a48fc-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a48fc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a48fc-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a48fc-125">INPUTS</span></span>

### <span data-ttu-id="a48fc-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a48fc-126">None</span></span>

## <span data-ttu-id="a48fc-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a48fc-127">OUTPUTS</span></span>

### <span data-ttu-id="a48fc-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a48fc-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a48fc-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a48fc-129">NOTES</span></span>

## <span data-ttu-id="a48fc-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a48fc-130">RELATED LINKS</span></span>
