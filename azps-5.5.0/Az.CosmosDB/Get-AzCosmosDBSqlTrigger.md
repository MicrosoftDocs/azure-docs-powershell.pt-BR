---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112062"
---
# <span data-ttu-id="dac34-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="dac34-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="dac34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dac34-102">SYNOPSIS</span></span>
<span data-ttu-id="dac34-103">Obtém o Gatilho Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="dac34-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="dac34-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dac34-104">SYNTAX</span></span>

### <span data-ttu-id="dac34-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dac34-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dac34-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dac34-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dac34-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="dac34-107">DESCRIPTION</span></span>
<span data-ttu-id="dac34-108">O cmdlet **Get-AzCosmosDBSqlTrigroup** obtém a lista de todos os Gatilhos Sql Do Sql Existentes para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName e obtém um único Gatilho Sql Do Sql Sql Para um determinado ResourceGroupName, AccountName, DatabaseName, ContainerName e TriggerName.</span><span class="sxs-lookup"><span data-stu-id="dac34-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="dac34-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dac34-109">EXAMPLES</span></span>

### <span data-ttu-id="dac34-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dac34-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="dac34-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dac34-111">PARAMETERS</span></span>

### <span data-ttu-id="dac34-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="dac34-112">-AccountName</span></span>
<span data-ttu-id="dac34-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="dac34-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dac34-114">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="dac34-114">-ContainerName</span></span>
<span data-ttu-id="dac34-115">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="dac34-115">Container name.</span></span>

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

### <span data-ttu-id="dac34-116">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="dac34-116">-DatabaseName</span></span>
<span data-ttu-id="dac34-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dac34-117">Database name.</span></span>

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

### <span data-ttu-id="dac34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac34-118">-DefaultProfile</span></span>
<span data-ttu-id="dac34-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dac34-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dac34-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="dac34-120">-Name</span></span>
<span data-ttu-id="dac34-121">Nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="dac34-121">Trigger name.</span></span>

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

### <span data-ttu-id="dac34-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dac34-122">-ParentObject</span></span>
<span data-ttu-id="dac34-123">Objeto Contêiner Sql.</span><span class="sxs-lookup"><span data-stu-id="dac34-123">Sql Container object.</span></span>

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

### <span data-ttu-id="dac34-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dac34-124">-ResourceGroupName</span></span>
<span data-ttu-id="dac34-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dac34-125">Name of resource group.</span></span>

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

### <span data-ttu-id="dac34-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac34-126">CommonParameters</span></span>
<span data-ttu-id="dac34-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dac34-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac34-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dac34-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac34-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="dac34-129">INPUTS</span></span>

### <span data-ttu-id="dac34-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dac34-130">None</span></span>

## <span data-ttu-id="dac34-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="dac34-131">OUTPUTS</span></span>

### <span data-ttu-id="dac34-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTrigetResults</span><span class="sxs-lookup"><span data-stu-id="dac34-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="dac34-133">Notas</span><span class="sxs-lookup"><span data-stu-id="dac34-133">NOTES</span></span>

## <span data-ttu-id="dac34-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dac34-134">RELATED LINKS</span></span>
