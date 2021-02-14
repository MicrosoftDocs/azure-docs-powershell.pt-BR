---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 6e61a83d843e0ceaa7d7926060da848d80d16eae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110950"
---
# <span data-ttu-id="e19ef-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="e19ef-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="e19ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e19ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e19ef-103">Obtém uma ou mais execuções de destino de trabalho</span><span class="sxs-lookup"><span data-stu-id="e19ef-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="e19ef-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e19ef-104">SYNTAX</span></span>

### <span data-ttu-id="e19ef-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e19ef-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e19ef-106">Objectset</span><span class="sxs-lookup"><span data-stu-id="e19ef-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e19ef-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e19ef-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e19ef-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e19ef-108">DESCRIPTION</span></span>
<span data-ttu-id="e19ef-109">O Get-AzSqlElasticJobTargetExecution cmdlet obtém uma ou mais execuções de destino de trabalho de uma execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="e19ef-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="e19ef-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e19ef-110">EXAMPLES</span></span>

### <span data-ttu-id="e19ef-111">Exemplo 1: Obtém uma ou mais execuções de destino de trabalho a partir de execuções de um trabalho</span><span class="sxs-lookup"><span data-stu-id="e19ef-111">Example 1: Gets one or more job target executions from a job executions</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="e19ef-112">Exemplo 2: Obtém uma ou mais execuções de destino de trabalho a partir de execuções de um trabalho - filtragem por nome da etapa</span><span class="sxs-lookup"><span data-stu-id="e19ef-112">Example 2: Gets one or more job target executions from a job executions - filtering by step name</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="e19ef-113">Obtém uma ou mais execuções de destino de trabalho</span><span class="sxs-lookup"><span data-stu-id="e19ef-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="e19ef-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e19ef-114">PARAMETERS</span></span>

### <span data-ttu-id="e19ef-115">-Ativo</span><span class="sxs-lookup"><span data-stu-id="e19ef-115">-Active</span></span>
<span data-ttu-id="e19ef-116">Sinalizar para filtrar por execuções ativas.</span><span class="sxs-lookup"><span data-stu-id="e19ef-116">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="e19ef-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e19ef-117">-AgentName</span></span>
<span data-ttu-id="e19ef-118">O nome do agente.</span><span class="sxs-lookup"><span data-stu-id="e19ef-118">The agent name.</span></span>

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

### <span data-ttu-id="e19ef-119">-Contagem</span><span class="sxs-lookup"><span data-stu-id="e19ef-119">-Count</span></span>
<span data-ttu-id="e19ef-120">Contagem retorna o número superior de execuções.</span><span class="sxs-lookup"><span data-stu-id="e19ef-120">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="e19ef-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="e19ef-121">-CreateTimeMax</span></span>
<span data-ttu-id="e19ef-122">Filtrar por criar tempo máximo</span><span class="sxs-lookup"><span data-stu-id="e19ef-122">Filter by create time max</span></span>

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

### <span data-ttu-id="e19ef-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="e19ef-123">-CreateTimeMin</span></span>
<span data-ttu-id="e19ef-124">Filtrar por criar min de tempo</span><span class="sxs-lookup"><span data-stu-id="e19ef-124">Filter by create time min</span></span>

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

### <span data-ttu-id="e19ef-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e19ef-125">-DefaultProfile</span></span>
<span data-ttu-id="e19ef-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e19ef-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e19ef-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="e19ef-127">-EndTimeMax</span></span>
<span data-ttu-id="e19ef-128">Filtrar por hora de término, no máximo.</span><span class="sxs-lookup"><span data-stu-id="e19ef-128">Filter by end time max.</span></span>

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

### <span data-ttu-id="e19ef-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="e19ef-129">-EndTimeMin</span></span>
<span data-ttu-id="e19ef-130">Filtrar por hora de término.</span><span class="sxs-lookup"><span data-stu-id="e19ef-130">Filter by end time min.</span></span>

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

### <span data-ttu-id="e19ef-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="e19ef-131">-JobExecutionId</span></span>
<span data-ttu-id="e19ef-132">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e19ef-132">The job execution id.</span></span>

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

### <span data-ttu-id="e19ef-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="e19ef-133">-JobName</span></span>
<span data-ttu-id="e19ef-134">O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e19ef-134">The job name.</span></span>

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

### <span data-ttu-id="e19ef-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e19ef-135">-ParentObject</span></span>
<span data-ttu-id="e19ef-136">O objeto de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e19ef-136">The job execution object.</span></span>

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

### <span data-ttu-id="e19ef-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e19ef-137">-ParentResourceId</span></span>
<span data-ttu-id="e19ef-138">A ID do recurso de execução de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e19ef-138">The job execution resource id.</span></span>

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

### <span data-ttu-id="e19ef-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e19ef-139">-ResourceGroupName</span></span>
<span data-ttu-id="e19ef-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e19ef-140">The resource group name.</span></span>

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

### <span data-ttu-id="e19ef-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e19ef-141">-ServerName</span></span>
<span data-ttu-id="e19ef-142">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e19ef-142">The server name.</span></span>

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

### <span data-ttu-id="e19ef-143">-NomeDoNome</span><span class="sxs-lookup"><span data-stu-id="e19ef-143">-StepName</span></span>
<span data-ttu-id="e19ef-144">O nome da etapa do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e19ef-144">The job step name.</span></span>

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

### <span data-ttu-id="e19ef-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19ef-145">CommonParameters</span></span>
<span data-ttu-id="e19ef-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e19ef-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19ef-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e19ef-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19ef-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="e19ef-148">INPUTS</span></span>

### <span data-ttu-id="e19ef-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="e19ef-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="e19ef-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="e19ef-150">OUTPUTS</span></span>

### <span data-ttu-id="e19ef-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="e19ef-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="e19ef-152">Notas</span><span class="sxs-lookup"><span data-stu-id="e19ef-152">NOTES</span></span>

## <span data-ttu-id="e19ef-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e19ef-153">RELATED LINKS</span></span>
