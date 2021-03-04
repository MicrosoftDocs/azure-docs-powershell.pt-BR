---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: 08f87d40eec10f10b12f568cae8e899f5b7468d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886980"
---
# <span data-ttu-id="580d0-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="580d0-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="580d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="580d0-102">SYNOPSIS</span></span>
<span data-ttu-id="580d0-103">Recupera o objeto PSProjectTask associado a uma tarefa de migração do Serviço de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="580d0-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="580d0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="580d0-104">SYNTAX</span></span>

### <span data-ttu-id="580d0-105">ListByComponent (Padrão)</span><span class="sxs-lookup"><span data-stu-id="580d0-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="580d0-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="580d0-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="580d0-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="580d0-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="580d0-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="580d0-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="580d0-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="580d0-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="580d0-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="580d0-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="580d0-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="580d0-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="580d0-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="580d0-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="580d0-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="580d0-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="580d0-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="580d0-114">DESCRIPTION</span></span>
<span data-ttu-id="580d0-115">O Get-AzDataMigrationTask cmdlet recupera as propriedades associadas a uma tarefa de migração do Serviço de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="580d0-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="580d0-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="580d0-116">EXAMPLES</span></span>

### <span data-ttu-id="580d0-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="580d0-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="580d0-118">O exemplo acima ilustra o uso de um cmdlet Get-AzDataMigrationTask para recuperar as propriedades associadas a uma tarefa de migração do Serviço de Migração de Banco de Dados do Azure com base no nome da tarefa passada como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="580d0-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="580d0-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="580d0-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="580d0-120">O exemplo acima ilustra o uso de um cmdlet Get-AzDataMigrationTask para recuperar todas as tarefas de migração associadas ao objeto PSProject passadas como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="580d0-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="580d0-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="580d0-121">PARAMETERS</span></span>

### <span data-ttu-id="580d0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="580d0-122">-DefaultProfile</span></span>
<span data-ttu-id="580d0-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="580d0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580d0-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="580d0-124">-Expand</span></span>
<span data-ttu-id="580d0-125">Expandir saída</span><span class="sxs-lookup"><span data-stu-id="580d0-125">Expand output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580d0-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="580d0-126">-InputObject</span></span>
<span data-ttu-id="580d0-127">Objeto PSProject.</span><span class="sxs-lookup"><span data-stu-id="580d0-127">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="580d0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="580d0-128">-Name</span></span>
<span data-ttu-id="580d0-129">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="580d0-129">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580d0-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="580d0-130">-ProjectName</span></span>
<span data-ttu-id="580d0-131">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="580d0-131">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580d0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="580d0-132">-ResourceGroupName</span></span>
<span data-ttu-id="580d0-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="580d0-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580d0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="580d0-134">-ResourceId</span></span>
<span data-ttu-id="580d0-135">ID do Recurso do Project.</span><span class="sxs-lookup"><span data-stu-id="580d0-135">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="580d0-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="580d0-136">-ResultType</span></span>
<span data-ttu-id="580d0-137">Expanda a saída de determinado tipo de resultado.</span><span class="sxs-lookup"><span data-stu-id="580d0-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput, Command

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580d0-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="580d0-138">-ServiceName</span></span>
<span data-ttu-id="580d0-139">Nome do Serviço de Migração de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="580d0-139">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580d0-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="580d0-140">-TaskType</span></span>
<span data-ttu-id="580d0-141">Filtrar por TaskType.</span><span class="sxs-lookup"><span data-stu-id="580d0-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580d0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="580d0-142">CommonParameters</span></span>
<span data-ttu-id="580d0-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="580d0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="580d0-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="580d0-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="580d0-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="580d0-145">INPUTS</span></span>

### <span data-ttu-id="580d0-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="580d0-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="580d0-147">System.String</span><span class="sxs-lookup"><span data-stu-id="580d0-147">System.String</span></span>

## <span data-ttu-id="580d0-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="580d0-148">OUTPUTS</span></span>

### <span data-ttu-id="580d0-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="580d0-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="580d0-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="580d0-150">NOTES</span></span>

## <span data-ttu-id="580d0-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="580d0-151">RELATED LINKS</span></span>
