---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117101"
---
# <span data-ttu-id="0da9e-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="0da9e-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="0da9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0da9e-102">SYNOPSIS</span></span>
<span data-ttu-id="0da9e-103">Obtém uma ou mais etapas de trabalho</span><span class="sxs-lookup"><span data-stu-id="0da9e-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="0da9e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0da9e-104">SYNTAX</span></span>

### <span data-ttu-id="0da9e-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0da9e-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0da9e-106">WithStepName</span><span class="sxs-lookup"><span data-stu-id="0da9e-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0da9e-107">Objectset</span><span class="sxs-lookup"><span data-stu-id="0da9e-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0da9e-108">WithStepStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="0da9e-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0da9e-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0da9e-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0da9e-110">WithStepStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0da9e-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0da9e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0da9e-111">DESCRIPTION</span></span>
<span data-ttu-id="0da9e-112">O Get-AzSqlElasticJobStepExecution cmdlet obtém uma ou mais execuções de uma etapa de trabalho de uma execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="0da9e-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="0da9e-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0da9e-113">EXAMPLES</span></span>

### <span data-ttu-id="0da9e-114">Exemplo 1 - Obtém uma ou mais execuções de uma etapa de trabalho a partir de execuções de um trabalho</span><span class="sxs-lookup"><span data-stu-id="0da9e-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="0da9e-115">Exemplo 2 - Obtém uma ou mais execuções de uma etapa de trabalho de uma execução de trabalho, filtrando por nome da etapa</span><span class="sxs-lookup"><span data-stu-id="0da9e-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="0da9e-116">Obtém uma ou mais etapas de trabalho</span><span class="sxs-lookup"><span data-stu-id="0da9e-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="0da9e-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0da9e-117">PARAMETERS</span></span>

### <span data-ttu-id="0da9e-118">-Ativo</span><span class="sxs-lookup"><span data-stu-id="0da9e-118">-Active</span></span>
<span data-ttu-id="0da9e-119">Sinalizar para filtrar por execuções ativas.</span><span class="sxs-lookup"><span data-stu-id="0da9e-119">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="0da9e-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0da9e-120">-AgentName</span></span>
<span data-ttu-id="0da9e-121">O nome do agente.</span><span class="sxs-lookup"><span data-stu-id="0da9e-121">The agent name.</span></span>

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

### <span data-ttu-id="0da9e-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="0da9e-122">-CreateTimeMax</span></span>
<span data-ttu-id="0da9e-123">Filtrar por criar tempo máximo</span><span class="sxs-lookup"><span data-stu-id="0da9e-123">Filter by create time max</span></span>

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

### <span data-ttu-id="0da9e-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="0da9e-124">-CreateTimeMin</span></span>
<span data-ttu-id="0da9e-125">Filtrar por criar min de tempo</span><span class="sxs-lookup"><span data-stu-id="0da9e-125">Filter by create time min</span></span>

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

### <span data-ttu-id="0da9e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da9e-126">-DefaultProfile</span></span>
<span data-ttu-id="0da9e-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0da9e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da9e-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="0da9e-128">-EndTimeMax</span></span>
<span data-ttu-id="0da9e-129">Filtrar por hora de término, no máximo.</span><span class="sxs-lookup"><span data-stu-id="0da9e-129">Filter by end time max.</span></span>

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

### <span data-ttu-id="0da9e-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="0da9e-130">-EndTimeMin</span></span>
<span data-ttu-id="0da9e-131">Filtrar por hora de término.</span><span class="sxs-lookup"><span data-stu-id="0da9e-131">Filter by end time min.</span></span>

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

### <span data-ttu-id="0da9e-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="0da9e-132">-JobExecutionId</span></span>
<span data-ttu-id="0da9e-133">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="0da9e-133">The job execution id.</span></span>

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

### <span data-ttu-id="0da9e-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="0da9e-134">-JobName</span></span>
<span data-ttu-id="0da9e-135">O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="0da9e-135">The job name.</span></span>

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

### <span data-ttu-id="0da9e-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0da9e-136">-ParentObject</span></span>
<span data-ttu-id="0da9e-137">O objeto do agente.</span><span class="sxs-lookup"><span data-stu-id="0da9e-137">The agent object.</span></span>

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

### <span data-ttu-id="0da9e-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0da9e-138">-ParentResourceId</span></span>
<span data-ttu-id="0da9e-139">A ID do recurso de execução de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0da9e-139">The job execution resource id.</span></span>

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

### <span data-ttu-id="0da9e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da9e-140">-ResourceGroupName</span></span>
<span data-ttu-id="0da9e-141">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0da9e-141">The resource group name.</span></span>

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

### <span data-ttu-id="0da9e-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0da9e-142">-ServerName</span></span>
<span data-ttu-id="0da9e-143">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0da9e-143">The server name.</span></span>

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

### <span data-ttu-id="0da9e-144">-NomeDoEsinado</span><span class="sxs-lookup"><span data-stu-id="0da9e-144">-StepName</span></span>
<span data-ttu-id="0da9e-145">O nome da etapa do trabalho.</span><span class="sxs-lookup"><span data-stu-id="0da9e-145">The job step name.</span></span>

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

### <span data-ttu-id="0da9e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da9e-146">CommonParameters</span></span>
<span data-ttu-id="0da9e-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da9e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da9e-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0da9e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da9e-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="0da9e-149">INPUTS</span></span>

### <span data-ttu-id="0da9e-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="0da9e-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="0da9e-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="0da9e-151">OUTPUTS</span></span>

### <span data-ttu-id="0da9e-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="0da9e-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="0da9e-153">Notas</span><span class="sxs-lookup"><span data-stu-id="0da9e-153">NOTES</span></span>

## <span data-ttu-id="0da9e-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0da9e-154">RELATED LINKS</span></span>
