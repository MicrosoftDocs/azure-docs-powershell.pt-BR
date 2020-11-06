---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: 5ca6edfa811a1b73cbdaae59e8d3b0e2f76cc15f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429810"
---
# <span data-ttu-id="c3bc4-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="c3bc4-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="c3bc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="c3bc4-103">Recupera o objeto PSProjectTask associado a uma tarefa de migração do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3bc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3bc4-104">SYNTAX</span></span>

### <span data-ttu-id="c3bc4-105">ListByComponent (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3bc4-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="c3bc4-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="c3bc4-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="c3bc4-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c3bc4-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="c3bc4-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="c3bc4-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="c3bc4-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3bc4-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="c3bc4-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3bc4-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="c3bc4-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="c3bc4-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="c3bc4-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="c3bc4-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="c3bc4-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="c3bc4-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="c3bc4-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3bc4-114">DESCRIPTION</span></span>
<span data-ttu-id="c3bc4-115">O cmdlet Get-AzureRmDataMigrationTask recupera as propriedades associadas a uma tarefa de migração do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="c3bc4-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3bc4-116">EXAMPLES</span></span>

### <span data-ttu-id="c3bc4-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3bc4-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="c3bc4-118">O exemplo acima ilustra o uso do cmdlet Get-AzureRmDataMigrationTask para recuperar as propriedades associadas a uma tarefa de migração do serviço de migração de banco de dados do Azure com base no nome da tarefa passado como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="c3bc4-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="c3bc4-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c3bc4-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="c3bc4-120">O exemplo acima ilustra o uso do cmdlet Get-AzureRmDataMigrationTask para recuperar todas as tarefas de migração associadas ao objeto PSProject passado como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="c3bc4-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="c3bc4-121">OS</span><span class="sxs-lookup"><span data-stu-id="c3bc4-121">PARAMETERS</span></span>

### <span data-ttu-id="c3bc4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3bc4-122">-DefaultProfile</span></span>
<span data-ttu-id="c3bc4-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bc4-124">-Expandir</span><span class="sxs-lookup"><span data-stu-id="c3bc4-124">-Expand</span></span>
<span data-ttu-id="c3bc4-125">Expandir saída</span><span class="sxs-lookup"><span data-stu-id="c3bc4-125">Expand output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bc4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3bc4-126">-InputObject</span></span>
<span data-ttu-id="c3bc4-127">Objeto PSProject.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-127">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3bc4-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3bc4-128">-Name</span></span>
<span data-ttu-id="c3bc4-129">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-129">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bc4-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="c3bc4-130">-ProjectName</span></span>
<span data-ttu-id="c3bc4-131">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-131">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bc4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3bc4-132">-ResourceGroupName</span></span>
<span data-ttu-id="c3bc4-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-133">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bc4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3bc4-134">-ResourceId</span></span>
<span data-ttu-id="c3bc4-135">ID do recurso do projeto.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-135">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3bc4-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="c3bc4-136">-ResultType</span></span>
<span data-ttu-id="c3bc4-137">Expandir a saída do tipo de resultado determinado.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-137">Expand output of given result type.</span></span>

```yaml
Type: ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bc4-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c3bc4-138">-ServiceName</span></span>
<span data-ttu-id="c3bc4-139">Nome do serviço de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-139">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bc4-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="c3bc4-140">-TaskType</span></span>
<span data-ttu-id="c3bc4-141">Filtrar por TaskType.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-141">Filter by TaskType.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="c3bc4-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3bc4-142">INPUTS</span></span>

### <span data-ttu-id="c3bc4-143">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="c3bc4-143">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="c3bc4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c3bc4-144">System.String</span></span>

## <span data-ttu-id="c3bc4-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3bc4-145">OUTPUTS</span></span>

### <span data-ttu-id="c3bc4-146">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. datamigration. Models. PSProjectTask, Microsoft. Azure. Commands. datamigration, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c3bc4-146">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c3bc4-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3bc4-147">NOTES</span></span>

## <span data-ttu-id="c3bc4-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3bc4-148">RELATED LINKS</span></span>

