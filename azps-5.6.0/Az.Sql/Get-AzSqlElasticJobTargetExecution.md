---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: bd0d7f13e5391345e25111b727ac6779a924260a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891605"
---
# <span data-ttu-id="93bb0-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="93bb0-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="93bb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="93bb0-103">Obtém uma ou mais execuções de destino de trabalho</span><span class="sxs-lookup"><span data-stu-id="93bb0-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="93bb0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="93bb0-104">SYNTAX</span></span>

### <span data-ttu-id="93bb0-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="93bb0-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93bb0-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="93bb0-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93bb0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="93bb0-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93bb0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93bb0-108">DESCRIPTION</span></span>
<span data-ttu-id="93bb0-109">O Get-AzSqlElasticJobTargetExecution cmdlet obtém uma ou mais execuções de destino de trabalho de uma execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="93bb0-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="93bb0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93bb0-110">EXAMPLES</span></span>

### <span data-ttu-id="93bb0-111">Exemplo 1: obtém uma ou mais execuções de destino de trabalho de execuções de trabalho</span><span class="sxs-lookup"><span data-stu-id="93bb0-111">Example 1: Gets one or more job target executions from a job executions</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="93bb0-112">Exemplo 2: obtém uma ou mais execuções de destino de trabalho de execuções de trabalho - filtragem por nome de etapa</span><span class="sxs-lookup"><span data-stu-id="93bb0-112">Example 2: Gets one or more job target executions from a job executions - filtering by step name</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="93bb0-113">Obtém uma ou mais execuções de destino de trabalho</span><span class="sxs-lookup"><span data-stu-id="93bb0-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="93bb0-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="93bb0-114">PARAMETERS</span></span>

### <span data-ttu-id="93bb0-115">-Active</span><span class="sxs-lookup"><span data-stu-id="93bb0-115">-Active</span></span>
<span data-ttu-id="93bb0-116">Sinalizar para filtrar por execuções ativas.</span><span class="sxs-lookup"><span data-stu-id="93bb0-116">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="93bb0-117">-AgentName</span></span>
<span data-ttu-id="93bb0-118">O nome do agente.</span><span class="sxs-lookup"><span data-stu-id="93bb0-118">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-119">-Count</span><span class="sxs-lookup"><span data-stu-id="93bb0-119">-Count</span></span>
<span data-ttu-id="93bb0-120">Count retorna o número superior de execuções.</span><span class="sxs-lookup"><span data-stu-id="93bb0-120">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="93bb0-121">-CreateTimeMax</span></span>
<span data-ttu-id="93bb0-122">Filtrar por criar tempo máximo</span><span class="sxs-lookup"><span data-stu-id="93bb0-122">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="93bb0-123">-CreateTimeMin</span></span>
<span data-ttu-id="93bb0-124">Filtrar por criar tempo mínimo</span><span class="sxs-lookup"><span data-stu-id="93bb0-124">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93bb0-125">-DefaultProfile</span></span>
<span data-ttu-id="93bb0-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93bb0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93bb0-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="93bb0-127">-EndTimeMax</span></span>
<span data-ttu-id="93bb0-128">Filtrar por tempo máximo de término.</span><span class="sxs-lookup"><span data-stu-id="93bb0-128">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="93bb0-129">-EndTimeMin</span></span>
<span data-ttu-id="93bb0-130">Filtrar por tempo mínimo de término.</span><span class="sxs-lookup"><span data-stu-id="93bb0-130">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="93bb0-131">-JobExecutionId</span></span>
<span data-ttu-id="93bb0-132">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="93bb0-132">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="93bb0-133">-JobName</span></span>
<span data-ttu-id="93bb0-134">O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="93bb0-134">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="93bb0-135">-ParentObject</span></span>
<span data-ttu-id="93bb0-136">O objeto de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="93bb0-136">The job execution object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="93bb0-137">-ParentResourceId</span></span>
<span data-ttu-id="93bb0-138">A ID do recurso de execução de trabalho.</span><span class="sxs-lookup"><span data-stu-id="93bb0-138">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93bb0-139">-ResourceGroupName</span></span>
<span data-ttu-id="93bb0-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="93bb0-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="93bb0-141">-ServerName</span></span>
<span data-ttu-id="93bb0-142">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="93bb0-142">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-143">-StepName</span><span class="sxs-lookup"><span data-stu-id="93bb0-143">-StepName</span></span>
<span data-ttu-id="93bb0-144">O nome da etapa de trabalho.</span><span class="sxs-lookup"><span data-stu-id="93bb0-144">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bb0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93bb0-145">CommonParameters</span></span>
<span data-ttu-id="93bb0-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93bb0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93bb0-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93bb0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93bb0-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93bb0-148">INPUTS</span></span>

### <span data-ttu-id="93bb0-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="93bb0-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="93bb0-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="93bb0-150">OUTPUTS</span></span>

### <span data-ttu-id="93bb0-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="93bb0-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="93bb0-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="93bb0-152">NOTES</span></span>

## <span data-ttu-id="93bb0-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93bb0-153">RELATED LINKS</span></span>
