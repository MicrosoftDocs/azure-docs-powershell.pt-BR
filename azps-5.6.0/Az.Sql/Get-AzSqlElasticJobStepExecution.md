---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 9918c314d239bf822fa789bcab6a9de923b8c2e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891606"
---
# <span data-ttu-id="33a37-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="33a37-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="33a37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33a37-102">SYNOPSIS</span></span>
<span data-ttu-id="33a37-103">Obtém uma ou mais execuções de etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="33a37-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="33a37-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="33a37-104">SYNTAX</span></span>

### <span data-ttu-id="33a37-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="33a37-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33a37-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="33a37-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33a37-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="33a37-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33a37-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="33a37-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33a37-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="33a37-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33a37-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="33a37-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33a37-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="33a37-111">DESCRIPTION</span></span>
<span data-ttu-id="33a37-112">O Get-AzSqlElasticJobStepExecution cmdlet obtém uma ou mais execuções de etapa de trabalho de uma execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="33a37-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="33a37-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33a37-113">EXAMPLES</span></span>

### <span data-ttu-id="33a37-114">Exemplo 1 - Obtém uma ou mais execuções de etapa de trabalho de execuções de trabalho</span><span class="sxs-lookup"><span data-stu-id="33a37-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="33a37-115">Exemplo 2 - Obtém uma ou mais execuções de etapa de trabalho de uma execução de trabalho, filtragem por nome de etapa</span><span class="sxs-lookup"><span data-stu-id="33a37-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="33a37-116">Obtém uma ou mais execuções de etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="33a37-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="33a37-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="33a37-117">PARAMETERS</span></span>

### <span data-ttu-id="33a37-118">-Active</span><span class="sxs-lookup"><span data-stu-id="33a37-118">-Active</span></span>
<span data-ttu-id="33a37-119">Sinalizar para filtrar por execuções ativas.</span><span class="sxs-lookup"><span data-stu-id="33a37-119">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="33a37-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="33a37-120">-AgentName</span></span>
<span data-ttu-id="33a37-121">O nome do agente.</span><span class="sxs-lookup"><span data-stu-id="33a37-121">The agent name.</span></span>

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

### <span data-ttu-id="33a37-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="33a37-122">-CreateTimeMax</span></span>
<span data-ttu-id="33a37-123">Filtrar por criar tempo máximo</span><span class="sxs-lookup"><span data-stu-id="33a37-123">Filter by create time max</span></span>

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

### <span data-ttu-id="33a37-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="33a37-124">-CreateTimeMin</span></span>
<span data-ttu-id="33a37-125">Filtrar por criar tempo mínimo</span><span class="sxs-lookup"><span data-stu-id="33a37-125">Filter by create time min</span></span>

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

### <span data-ttu-id="33a37-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a37-126">-DefaultProfile</span></span>
<span data-ttu-id="33a37-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33a37-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33a37-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="33a37-128">-EndTimeMax</span></span>
<span data-ttu-id="33a37-129">Filtrar por tempo máximo de término.</span><span class="sxs-lookup"><span data-stu-id="33a37-129">Filter by end time max.</span></span>

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

### <span data-ttu-id="33a37-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="33a37-130">-EndTimeMin</span></span>
<span data-ttu-id="33a37-131">Filtrar por tempo mínimo de término.</span><span class="sxs-lookup"><span data-stu-id="33a37-131">Filter by end time min.</span></span>

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

### <span data-ttu-id="33a37-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="33a37-132">-JobExecutionId</span></span>
<span data-ttu-id="33a37-133">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="33a37-133">The job execution id.</span></span>

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

### <span data-ttu-id="33a37-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="33a37-134">-JobName</span></span>
<span data-ttu-id="33a37-135">O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="33a37-135">The job name.</span></span>

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

### <span data-ttu-id="33a37-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="33a37-136">-ParentObject</span></span>
<span data-ttu-id="33a37-137">O objeto agent.</span><span class="sxs-lookup"><span data-stu-id="33a37-137">The agent object.</span></span>

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

### <span data-ttu-id="33a37-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="33a37-138">-ParentResourceId</span></span>
<span data-ttu-id="33a37-139">A ID do recurso de execução de trabalho.</span><span class="sxs-lookup"><span data-stu-id="33a37-139">The job execution resource id.</span></span>

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

### <span data-ttu-id="33a37-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33a37-140">-ResourceGroupName</span></span>
<span data-ttu-id="33a37-141">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="33a37-141">The resource group name.</span></span>

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

### <span data-ttu-id="33a37-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="33a37-142">-ServerName</span></span>
<span data-ttu-id="33a37-143">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="33a37-143">The server name.</span></span>

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

### <span data-ttu-id="33a37-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="33a37-144">-StepName</span></span>
<span data-ttu-id="33a37-145">O nome da etapa de trabalho.</span><span class="sxs-lookup"><span data-stu-id="33a37-145">The job step name.</span></span>

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

### <span data-ttu-id="33a37-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a37-146">CommonParameters</span></span>
<span data-ttu-id="33a37-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a37-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a37-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33a37-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a37-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33a37-149">INPUTS</span></span>

### <span data-ttu-id="33a37-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="33a37-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="33a37-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="33a37-151">OUTPUTS</span></span>

### <span data-ttu-id="33a37-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="33a37-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="33a37-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="33a37-153">NOTES</span></span>

## <span data-ttu-id="33a37-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33a37-154">RELATED LINKS</span></span>
