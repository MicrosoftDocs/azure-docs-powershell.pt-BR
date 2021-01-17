---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432987"
---
# <span data-ttu-id="8f28f-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="8f28f-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="8f28f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f28f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f28f-103">Obtém uma ou mais execuções de etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="8f28f-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="8f28f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f28f-104">SYNTAX</span></span>

### <span data-ttu-id="8f28f-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="8f28f-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f28f-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="8f28f-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f28f-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="8f28f-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f28f-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8f28f-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f28f-109">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="8f28f-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f28f-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8f28f-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f28f-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f28f-111">DESCRIPTION</span></span>
<span data-ttu-id="8f28f-112">O cmdlet Get-AzSqlElasticJobStepExecution Obtém uma ou mais execuções de etapa do trabalho de uma execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="8f28f-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="8f28f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f28f-113">EXAMPLES</span></span>

### <span data-ttu-id="8f28f-114">Exemplo 1-Obtém uma ou mais execuções de etapa do trabalho de uma execuções de trabalho</span><span class="sxs-lookup"><span data-stu-id="8f28f-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="8f28f-115">Exemplo 2-Obtém uma ou mais execuções de etapa do trabalho de uma execução de trabalho, filtrando por nome da etapa</span><span class="sxs-lookup"><span data-stu-id="8f28f-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="8f28f-116">Obtém uma ou mais execuções de etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="8f28f-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="8f28f-117">OS</span><span class="sxs-lookup"><span data-stu-id="8f28f-117">PARAMETERS</span></span>

### <span data-ttu-id="8f28f-118">-Ativo</span><span class="sxs-lookup"><span data-stu-id="8f28f-118">-Active</span></span>
<span data-ttu-id="8f28f-119">Sinalizar para filtrar por execuções ativas.</span><span class="sxs-lookup"><span data-stu-id="8f28f-119">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="8f28f-120">-AgentName</span></span>
<span data-ttu-id="8f28f-121">O nome do agente.</span><span class="sxs-lookup"><span data-stu-id="8f28f-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="8f28f-122">-CreateTimeMax</span></span>
<span data-ttu-id="8f28f-123">Filtrar por criar tempo máx</span><span class="sxs-lookup"><span data-stu-id="8f28f-123">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="8f28f-124">-CreateTimeMin</span></span>
<span data-ttu-id="8f28f-125">Filtrar por tempo de criação min</span><span class="sxs-lookup"><span data-stu-id="8f28f-125">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f28f-126">-DefaultProfile</span></span>
<span data-ttu-id="8f28f-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f28f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f28f-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="8f28f-128">-EndTimeMax</span></span>
<span data-ttu-id="8f28f-129">Filtrar por hora de término máx.</span><span class="sxs-lookup"><span data-stu-id="8f28f-129">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="8f28f-130">-EndTimeMin</span></span>
<span data-ttu-id="8f28f-131">Filtrar por hora de término mín.</span><span class="sxs-lookup"><span data-stu-id="8f28f-131">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="8f28f-132">-JobExecutionId</span></span>
<span data-ttu-id="8f28f-133">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8f28f-133">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="8f28f-134">-JobName</span></span>
<span data-ttu-id="8f28f-135">O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8f28f-135">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8f28f-136">-ParentObject</span></span>
<span data-ttu-id="8f28f-137">O objeto agente.</span><span class="sxs-lookup"><span data-stu-id="8f28f-137">The agent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet, WithJobStepNameUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8f28f-138">-ParentResourceId</span></span>
<span data-ttu-id="8f28f-139">A ID do recurso de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8f28f-139">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f28f-140">-ResourceGroupName</span></span>
<span data-ttu-id="8f28f-141">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f28f-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-142">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="8f28f-142">-ServerName</span></span>
<span data-ttu-id="8f28f-143">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="8f28f-143">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-144">-Stepname</span><span class="sxs-lookup"><span data-stu-id="8f28f-144">-StepName</span></span>
<span data-ttu-id="8f28f-145">O nome da etapa do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8f28f-145">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobStepName, WithJobStepNameUsingParentObject, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f28f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f28f-146">CommonParameters</span></span>
<span data-ttu-id="8f28f-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f28f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f28f-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f28f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f28f-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f28f-149">INPUTS</span></span>

### <span data-ttu-id="8f28f-150">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="8f28f-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="8f28f-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f28f-151">OUTPUTS</span></span>

### <span data-ttu-id="8f28f-152">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="8f28f-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="8f28f-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f28f-153">NOTES</span></span>

## <span data-ttu-id="8f28f-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f28f-154">RELATED LINKS</span></span>
