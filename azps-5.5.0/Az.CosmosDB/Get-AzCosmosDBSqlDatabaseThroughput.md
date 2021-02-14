---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116467"
---
# <span data-ttu-id="989a7-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="989a7-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="989a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="989a7-102">SYNOPSIS</span></span>
<span data-ttu-id="989a7-103">Obtém as configurações de produtividade correspondentes a um Banco de Dados Sql do Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="989a7-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="989a7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="989a7-104">SYNTAX</span></span>

### <span data-ttu-id="989a7-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="989a7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="989a7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="989a7-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="989a7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="989a7-107">DESCRIPTION</span></span>
<span data-ttu-id="989a7-108">O cmdlet **Get-AzCosmosDBSqlDatabaseThroughput** obtém as configurações de produtividade correspondentes a um Banco de Dados Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="989a7-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="989a7-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="989a7-109">EXAMPLES</span></span>

### <span data-ttu-id="989a7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="989a7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="989a7-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="989a7-111">PARAMETERS</span></span>

### <span data-ttu-id="989a7-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="989a7-112">-AccountName</span></span>
<span data-ttu-id="989a7-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="989a7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="989a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989a7-114">-DefaultProfile</span></span>
<span data-ttu-id="989a7-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="989a7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="989a7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="989a7-116">-InputObject</span></span>
<span data-ttu-id="989a7-117">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="989a7-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="989a7-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="989a7-118">-Name</span></span>
<span data-ttu-id="989a7-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="989a7-119">Database name.</span></span>

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

### <span data-ttu-id="989a7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="989a7-120">-ResourceGroupName</span></span>
<span data-ttu-id="989a7-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="989a7-121">Name of resource group.</span></span>

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

### <span data-ttu-id="989a7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989a7-122">CommonParameters</span></span>
<span data-ttu-id="989a7-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="989a7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989a7-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="989a7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989a7-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="989a7-125">INPUTS</span></span>

### <span data-ttu-id="989a7-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="989a7-126">None</span></span>

## <span data-ttu-id="989a7-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="989a7-127">OUTPUTS</span></span>

### <span data-ttu-id="989a7-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="989a7-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="989a7-129">Notas</span><span class="sxs-lookup"><span data-stu-id="989a7-129">NOTES</span></span>

## <span data-ttu-id="989a7-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="989a7-130">RELATED LINKS</span></span>
