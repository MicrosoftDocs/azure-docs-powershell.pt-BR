---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: f73d39c9b09c0ef44edacfc42f439ee444eedc4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112064"
---
# <span data-ttu-id="0d0f5-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="0d0f5-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="0d0f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="0d0f5-103">Obtém as propriedades de produtividade do Banco de Dados MongoDB.</span><span class="sxs-lookup"><span data-stu-id="0d0f5-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="0d0f5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d0f5-104">SYNTAX</span></span>

### <span data-ttu-id="0d0f5-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0d0f5-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d0f5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d0f5-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d0f5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d0f5-107">DESCRIPTION</span></span>
<span data-ttu-id="0d0f5-108">O cmdlet **Get-AzCosmosDBMongoDBDatabaseThroughput** obtém as propriedades de produtividade do banco de dados MongoDB.</span><span class="sxs-lookup"><span data-stu-id="0d0f5-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="0d0f5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d0f5-109">EXAMPLES</span></span>

### <span data-ttu-id="0d0f5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d0f5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="0d0f5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d0f5-111">PARAMETERS</span></span>

### <span data-ttu-id="0d0f5-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="0d0f5-112">-AccountName</span></span>
<span data-ttu-id="0d0f5-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="0d0f5-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0d0f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d0f5-114">-DefaultProfile</span></span>
<span data-ttu-id="0d0f5-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d0f5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d0f5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d0f5-116">-InputObject</span></span>
<span data-ttu-id="0d0f5-117">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="0d0f5-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d0f5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d0f5-118">-Name</span></span>
<span data-ttu-id="0d0f5-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0d0f5-119">Database name.</span></span>

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

### <span data-ttu-id="0d0f5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d0f5-120">-ResourceGroupName</span></span>
<span data-ttu-id="0d0f5-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d0f5-121">Name of resource group.</span></span>

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

### <span data-ttu-id="0d0f5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d0f5-122">CommonParameters</span></span>
<span data-ttu-id="0d0f5-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d0f5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d0f5-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d0f5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d0f5-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="0d0f5-125">INPUTS</span></span>

### <span data-ttu-id="0d0f5-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0d0f5-126">None</span></span>

## <span data-ttu-id="0d0f5-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="0d0f5-127">OUTPUTS</span></span>

### <span data-ttu-id="0d0f5-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0d0f5-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0d0f5-129">Notas</span><span class="sxs-lookup"><span data-stu-id="0d0f5-129">NOTES</span></span>

## <span data-ttu-id="0d0f5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d0f5-130">RELATED LINKS</span></span>
