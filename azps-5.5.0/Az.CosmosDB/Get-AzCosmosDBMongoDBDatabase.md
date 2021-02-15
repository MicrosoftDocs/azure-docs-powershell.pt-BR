---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112065"
---
# <span data-ttu-id="43894-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="43894-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="43894-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43894-102">SYNOPSIS</span></span>
<span data-ttu-id="43894-103">Obtém o Banco de Dados MongoDB do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="43894-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="43894-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43894-104">SYNTAX</span></span>

### <span data-ttu-id="43894-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="43894-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43894-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43894-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43894-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="43894-107">DESCRIPTION</span></span>
<span data-ttu-id="43894-108">O cmdlet **Get-AzCosmosDBMongoDBDatabase** obtém o Banco de Dados MongoDB DoDb.</span><span class="sxs-lookup"><span data-stu-id="43894-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="43894-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="43894-109">EXAMPLES</span></span>

### <span data-ttu-id="43894-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43894-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="43894-111">O Objeto de Recurso contém _rid, _ts, _etag propriedades.</span><span class="sxs-lookup"><span data-stu-id="43894-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="43894-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43894-112">PARAMETERS</span></span>

### <span data-ttu-id="43894-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="43894-113">-AccountName</span></span>
<span data-ttu-id="43894-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="43894-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="43894-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43894-115">-DefaultProfile</span></span>
<span data-ttu-id="43894-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43894-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43894-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="43894-117">-Name</span></span>
<span data-ttu-id="43894-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="43894-118">Database name.</span></span>

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

### <span data-ttu-id="43894-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="43894-119">-ParentObject</span></span>
<span data-ttu-id="43894-120">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="43894-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="43894-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43894-121">-ResourceGroupName</span></span>
<span data-ttu-id="43894-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="43894-122">Name of resource group.</span></span>

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

### <span data-ttu-id="43894-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43894-123">CommonParameters</span></span>
<span data-ttu-id="43894-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43894-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43894-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43894-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43894-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="43894-126">INPUTS</span></span>

### <span data-ttu-id="43894-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="43894-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="43894-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="43894-128">OUTPUTS</span></span>

### <span data-ttu-id="43894-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="43894-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="43894-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="43894-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="43894-131">Notas</span><span class="sxs-lookup"><span data-stu-id="43894-131">NOTES</span></span>

## <span data-ttu-id="43894-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43894-132">RELATED LINKS</span></span>
