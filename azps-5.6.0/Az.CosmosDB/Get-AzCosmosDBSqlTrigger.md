---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 28b616315913ae70722b5a600d4b10879c7b8334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889795"
---
# <span data-ttu-id="24837-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="24837-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="24837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24837-102">SYNOPSIS</span></span>
<span data-ttu-id="24837-103">Obtém o Gatilho Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="24837-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="24837-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="24837-104">SYNTAX</span></span>

### <span data-ttu-id="24837-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="24837-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24837-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24837-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24837-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="24837-107">DESCRIPTION</span></span>
<span data-ttu-id="24837-108">O cmdlet **Get-AzCosmosDBSqlTrigger** obtém a lista de todos os Gatilhos Sql do CosmosDB existentes para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName e obtém um único Gatilho Sql do CosmosDB para um determinado ResourceGroupName, AccountName, DatabaseName, ContainerName e TriggerName.</span><span class="sxs-lookup"><span data-stu-id="24837-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="24837-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24837-109">EXAMPLES</span></span>

### <span data-ttu-id="24837-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="24837-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="24837-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="24837-111">PARAMETERS</span></span>

### <span data-ttu-id="24837-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24837-112">-AccountName</span></span>
<span data-ttu-id="24837-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="24837-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="24837-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="24837-114">-ContainerName</span></span>
<span data-ttu-id="24837-115">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="24837-115">Container name.</span></span>

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

### <span data-ttu-id="24837-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="24837-116">-DatabaseName</span></span>
<span data-ttu-id="24837-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="24837-117">Database name.</span></span>

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

### <span data-ttu-id="24837-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24837-118">-DefaultProfile</span></span>
<span data-ttu-id="24837-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24837-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24837-120">-Name</span><span class="sxs-lookup"><span data-stu-id="24837-120">-Name</span></span>
<span data-ttu-id="24837-121">Nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="24837-121">Trigger name.</span></span>

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

### <span data-ttu-id="24837-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="24837-122">-ParentObject</span></span>
<span data-ttu-id="24837-123">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="24837-123">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24837-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24837-124">-ResourceGroupName</span></span>
<span data-ttu-id="24837-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24837-125">Name of resource group.</span></span>

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

### <span data-ttu-id="24837-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24837-126">CommonParameters</span></span>
<span data-ttu-id="24837-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24837-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24837-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24837-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24837-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24837-129">INPUTS</span></span>

### <span data-ttu-id="24837-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="24837-130">None</span></span>

## <span data-ttu-id="24837-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="24837-131">OUTPUTS</span></span>

### <span data-ttu-id="24837-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="24837-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="24837-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="24837-133">NOTES</span></span>

## <span data-ttu-id="24837-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24837-134">RELATED LINKS</span></span>
