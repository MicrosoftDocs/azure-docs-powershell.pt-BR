---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: bcc1c39af722d5f12c333152e8458228f583a842
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112295"
---
# <span data-ttu-id="2da68-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2da68-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="2da68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2da68-102">SYNOPSIS</span></span>
<span data-ttu-id="2da68-103">Recupera o objeto PSProjectTask associado a uma tarefa de migração do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2da68-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="2da68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2da68-104">SYNTAX</span></span>

### <span data-ttu-id="2da68-105">ListByComponent (padrão)</span><span class="sxs-lookup"><span data-stu-id="2da68-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da68-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="2da68-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da68-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2da68-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da68-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="2da68-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da68-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="2da68-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da68-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2da68-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da68-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="2da68-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da68-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="2da68-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da68-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="2da68-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2da68-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2da68-114">DESCRIPTION</span></span>
<span data-ttu-id="2da68-115">O cmdlet Get-AzDataMigrationTask recupera as propriedades associadas a uma tarefa de migração do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2da68-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="2da68-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2da68-116">EXAMPLES</span></span>

### <span data-ttu-id="2da68-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2da68-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="2da68-118">O exemplo acima ilustra o uso do cmdlet Get-AzDataMigrationTask para recuperar as propriedades associadas a uma tarefa de migração do serviço de migração de banco de dados do Azure com base no nome da tarefa passado como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="2da68-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="2da68-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2da68-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="2da68-120">O exemplo acima ilustra o uso do cmdlet Get-AzDataMigrationTask para recuperar todas as tarefas de migração associadas ao objeto PSProject passado como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="2da68-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="2da68-121">OS</span><span class="sxs-lookup"><span data-stu-id="2da68-121">PARAMETERS</span></span>

### <span data-ttu-id="2da68-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da68-122">-DefaultProfile</span></span>
<span data-ttu-id="2da68-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2da68-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2da68-124">-Expandir</span><span class="sxs-lookup"><span data-stu-id="2da68-124">-Expand</span></span>
<span data-ttu-id="2da68-125">Expandir saída</span><span class="sxs-lookup"><span data-stu-id="2da68-125">Expand output</span></span>

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

### <span data-ttu-id="2da68-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2da68-126">-InputObject</span></span>
<span data-ttu-id="2da68-127">Objeto PSProject.</span><span class="sxs-lookup"><span data-stu-id="2da68-127">PSProject Object.</span></span>

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

### <span data-ttu-id="2da68-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2da68-128">-Name</span></span>
<span data-ttu-id="2da68-129">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="2da68-129">The name of the task.</span></span>

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

### <span data-ttu-id="2da68-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="2da68-130">-ProjectName</span></span>
<span data-ttu-id="2da68-131">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="2da68-131">The name of the project.</span></span>

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

### <span data-ttu-id="2da68-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da68-132">-ResourceGroupName</span></span>
<span data-ttu-id="2da68-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2da68-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="2da68-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2da68-134">-ResourceId</span></span>
<span data-ttu-id="2da68-135">ID do recurso do projeto.</span><span class="sxs-lookup"><span data-stu-id="2da68-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="2da68-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="2da68-136">-ResultType</span></span>
<span data-ttu-id="2da68-137">Expandir a saída do tipo de resultado determinado.</span><span class="sxs-lookup"><span data-stu-id="2da68-137">Expand output of given result type.</span></span>

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

### <span data-ttu-id="2da68-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2da68-138">-ServiceName</span></span>
<span data-ttu-id="2da68-139">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2da68-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="2da68-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="2da68-140">-TaskType</span></span>
<span data-ttu-id="2da68-141">Filtrar por TaskType.</span><span class="sxs-lookup"><span data-stu-id="2da68-141">Filter by TaskType.</span></span>

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

### <span data-ttu-id="2da68-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da68-142">CommonParameters</span></span>
<span data-ttu-id="2da68-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2da68-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da68-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2da68-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da68-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2da68-145">INPUTS</span></span>

### <span data-ttu-id="2da68-146">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="2da68-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="2da68-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2da68-147">System.String</span></span>

## <span data-ttu-id="2da68-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2da68-148">OUTPUTS</span></span>

### <span data-ttu-id="2da68-149">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="2da68-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="2da68-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2da68-150">NOTES</span></span>

## <span data-ttu-id="2da68-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2da68-151">RELATED LINKS</span></span>
