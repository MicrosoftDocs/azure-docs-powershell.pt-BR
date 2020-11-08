---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112852"
---
# <span data-ttu-id="145e8-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="145e8-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="145e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="145e8-102">SYNOPSIS</span></span>
<span data-ttu-id="145e8-103">Atualiza o banco de dados SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="145e8-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="145e8-104">Executa uma operação de patch do lado do cliente lendo o banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="145e8-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="145e8-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="145e8-105">SYNTAX</span></span>

### <span data-ttu-id="145e8-106">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="145e8-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="145e8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="145e8-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="145e8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="145e8-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="145e8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="145e8-109">DESCRIPTION</span></span>
<span data-ttu-id="145e8-110">Atualiza o banco de dados SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="145e8-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="145e8-111">Executa uma operação de patch do lado do cliente lendo o banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="145e8-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="145e8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="145e8-112">EXAMPLES</span></span>

### <span data-ttu-id="145e8-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="145e8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="145e8-114">OS</span><span class="sxs-lookup"><span data-stu-id="145e8-114">PARAMETERS</span></span>

### <span data-ttu-id="145e8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="145e8-115">-AccountName</span></span>
<span data-ttu-id="145e8-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="145e8-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="145e8-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="145e8-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="145e8-118">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="145e8-118">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145e8-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="145e8-119">-Confirm</span></span>
<span data-ttu-id="145e8-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="145e8-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="145e8-121">-DefaultProfile</span></span>
<span data-ttu-id="145e8-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="145e8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="145e8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="145e8-123">-InputObject</span></span>
<span data-ttu-id="145e8-124">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="145e8-124">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="145e8-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="145e8-125">-Name</span></span>
<span data-ttu-id="145e8-126">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="145e8-126">Database name.</span></span>

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

### <span data-ttu-id="145e8-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="145e8-127">-ParentObject</span></span>
<span data-ttu-id="145e8-128">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="145e8-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="145e8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="145e8-129">-ResourceGroupName</span></span>
<span data-ttu-id="145e8-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="145e8-130">Name of resource group.</span></span>

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

### <span data-ttu-id="145e8-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="145e8-131">-Throughput</span></span>
<span data-ttu-id="145e8-132">O throughput do banco de dados SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="145e8-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="145e8-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="145e8-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145e8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="145e8-134">-WhatIf</span></span>
<span data-ttu-id="145e8-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="145e8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="145e8-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="145e8-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145e8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145e8-137">CommonParameters</span></span>
<span data-ttu-id="145e8-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="145e8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145e8-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="145e8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145e8-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="145e8-140">INPUTS</span></span>

### <span data-ttu-id="145e8-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="145e8-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="145e8-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="145e8-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="145e8-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="145e8-143">OUTPUTS</span></span>

### <span data-ttu-id="145e8-144">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="145e8-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="145e8-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="145e8-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="145e8-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="145e8-146">NOTES</span></span>

## <span data-ttu-id="145e8-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="145e8-147">RELATED LINKS</span></span>
