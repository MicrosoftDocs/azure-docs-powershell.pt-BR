---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281377"
---
# <span data-ttu-id="f5031-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="f5031-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="f5031-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5031-102">SYNOPSIS</span></span>
<span data-ttu-id="f5031-103">Obtém o gatilho SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f5031-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="f5031-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5031-104">SYNTAX</span></span>

### <span data-ttu-id="f5031-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5031-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5031-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5031-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5031-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5031-107">DESCRIPTION</span></span>
<span data-ttu-id="f5031-108">O cmdlet **Get-AzCosmosDBSqlTrigger** Obtém a lista de todos os gatilhos SQL existentes do CosmosDB para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName e Obtém um gatilho SQL único CosmosDB para um determinado ResourceGroupName, AccountName, DatabaseName, ContainerName e triggername.</span><span class="sxs-lookup"><span data-stu-id="f5031-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="f5031-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5031-109">EXAMPLES</span></span>

### <span data-ttu-id="f5031-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f5031-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="f5031-111">OS</span><span class="sxs-lookup"><span data-stu-id="f5031-111">PARAMETERS</span></span>

### <span data-ttu-id="f5031-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5031-112">-AccountName</span></span>
<span data-ttu-id="f5031-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="f5031-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f5031-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f5031-114">-ContainerName</span></span>
<span data-ttu-id="f5031-115">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f5031-115">Container name.</span></span>

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

### <span data-ttu-id="f5031-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f5031-116">-DatabaseName</span></span>
<span data-ttu-id="f5031-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f5031-117">Database name.</span></span>

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

### <span data-ttu-id="f5031-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5031-118">-DefaultProfile</span></span>
<span data-ttu-id="f5031-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5031-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5031-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5031-120">-Name</span></span>
<span data-ttu-id="f5031-121">Nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="f5031-121">Trigger name.</span></span>

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

### <span data-ttu-id="f5031-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f5031-122">-ParentObject</span></span>
<span data-ttu-id="f5031-123">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="f5031-123">Sql Container object.</span></span>

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

### <span data-ttu-id="f5031-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5031-124">-ResourceGroupName</span></span>
<span data-ttu-id="f5031-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5031-125">Name of resource group.</span></span>

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

### <span data-ttu-id="f5031-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5031-126">CommonParameters</span></span>
<span data-ttu-id="f5031-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5031-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5031-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5031-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5031-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5031-129">INPUTS</span></span>

### <span data-ttu-id="f5031-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f5031-130">None</span></span>

## <span data-ttu-id="f5031-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5031-131">OUTPUTS</span></span>

### <span data-ttu-id="f5031-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="f5031-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="f5031-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5031-133">NOTES</span></span>

## <span data-ttu-id="f5031-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5031-134">RELATED LINKS</span></span>
