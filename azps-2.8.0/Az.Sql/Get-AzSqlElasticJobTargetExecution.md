---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 95cd4cdfb9cc21207e336a514e91d56193119e8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773627"
---
# <span data-ttu-id="928c8-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="928c8-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="928c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="928c8-102">SYNOPSIS</span></span>
<span data-ttu-id="928c8-103">Obtém uma ou mais execuções de destino do trabalho</span><span class="sxs-lookup"><span data-stu-id="928c8-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="928c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="928c8-104">SYNTAX</span></span>

### <span data-ttu-id="928c8-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="928c8-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="928c8-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="928c8-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="928c8-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="928c8-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="928c8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="928c8-108">DESCRIPTION</span></span>
<span data-ttu-id="928c8-109">O cmdlet Get-AzSqlElasticJobTargetExecution Obtém uma ou mais execuções de destino do trabalho a partir de uma execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="928c8-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="928c8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="928c8-110">EXAMPLES</span></span>

### <span data-ttu-id="928c8-111">Exemplo 1-Obtém uma ou mais execuções de destino de trabalho de uma execução de trabalho</span><span class="sxs-lookup"><span data-stu-id="928c8-111">Example 1 - Gets one or more job target executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="928c8-112">Exemplo 2-Obtém uma ou mais execuções de destino do trabalho de uma execução de trabalho – filtragem por nome da etapa</span><span class="sxs-lookup"><span data-stu-id="928c8-112">Example 2 - Gets one or more job target executions from a job executions - filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="928c8-113">Obtém uma ou mais execuções de destino do trabalho</span><span class="sxs-lookup"><span data-stu-id="928c8-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="928c8-114">OS</span><span class="sxs-lookup"><span data-stu-id="928c8-114">PARAMETERS</span></span>

### <span data-ttu-id="928c8-115">-Ativo</span><span class="sxs-lookup"><span data-stu-id="928c8-115">-Active</span></span>
<span data-ttu-id="928c8-116">Sinalizar para filtrar por execuções ativas.</span><span class="sxs-lookup"><span data-stu-id="928c8-116">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="928c8-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="928c8-117">-AgentName</span></span>
<span data-ttu-id="928c8-118">O nome do agente.</span><span class="sxs-lookup"><span data-stu-id="928c8-118">The agent name.</span></span>

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

### <span data-ttu-id="928c8-119">-Contagem</span><span class="sxs-lookup"><span data-stu-id="928c8-119">-Count</span></span>
<span data-ttu-id="928c8-120">Count retorna o número superior de execuções.</span><span class="sxs-lookup"><span data-stu-id="928c8-120">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="928c8-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="928c8-121">-CreateTimeMax</span></span>
<span data-ttu-id="928c8-122">Filtrar por criar tempo máx</span><span class="sxs-lookup"><span data-stu-id="928c8-122">Filter by create time max</span></span>

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

### <span data-ttu-id="928c8-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="928c8-123">-CreateTimeMin</span></span>
<span data-ttu-id="928c8-124">Filtrar por tempo de criação min</span><span class="sxs-lookup"><span data-stu-id="928c8-124">Filter by create time min</span></span>

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

### <span data-ttu-id="928c8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="928c8-125">-DefaultProfile</span></span>
<span data-ttu-id="928c8-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="928c8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="928c8-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="928c8-127">-EndTimeMax</span></span>
<span data-ttu-id="928c8-128">Filtrar por hora de término máx.</span><span class="sxs-lookup"><span data-stu-id="928c8-128">Filter by end time max.</span></span>

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

### <span data-ttu-id="928c8-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="928c8-129">-EndTimeMin</span></span>
<span data-ttu-id="928c8-130">Filtrar por hora de término mín.</span><span class="sxs-lookup"><span data-stu-id="928c8-130">Filter by end time min.</span></span>

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

### <span data-ttu-id="928c8-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="928c8-131">-JobExecutionId</span></span>
<span data-ttu-id="928c8-132">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="928c8-132">The job execution id.</span></span>

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

### <span data-ttu-id="928c8-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="928c8-133">-JobName</span></span>
<span data-ttu-id="928c8-134">O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="928c8-134">The job name.</span></span>

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

### <span data-ttu-id="928c8-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="928c8-135">-ParentObject</span></span>
<span data-ttu-id="928c8-136">O objeto de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="928c8-136">The job execution object.</span></span>

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

### <span data-ttu-id="928c8-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="928c8-137">-ParentResourceId</span></span>
<span data-ttu-id="928c8-138">A ID do recurso de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="928c8-138">The job execution resource id.</span></span>

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

### <span data-ttu-id="928c8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="928c8-139">-ResourceGroupName</span></span>
<span data-ttu-id="928c8-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="928c8-140">The resource group name.</span></span>

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

### <span data-ttu-id="928c8-141">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="928c8-141">-ServerName</span></span>
<span data-ttu-id="928c8-142">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="928c8-142">The server name.</span></span>

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

### <span data-ttu-id="928c8-143">-Stepname</span><span class="sxs-lookup"><span data-stu-id="928c8-143">-StepName</span></span>
<span data-ttu-id="928c8-144">O nome da etapa do trabalho.</span><span class="sxs-lookup"><span data-stu-id="928c8-144">The job step name.</span></span>

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

### <span data-ttu-id="928c8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928c8-145">CommonParameters</span></span>
<span data-ttu-id="928c8-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="928c8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928c8-147">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="928c8-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928c8-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="928c8-148">INPUTS</span></span>

### <span data-ttu-id="928c8-149">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="928c8-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="928c8-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="928c8-150">OUTPUTS</span></span>

### <span data-ttu-id="928c8-151">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="928c8-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="928c8-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="928c8-152">NOTES</span></span>

## <span data-ttu-id="928c8-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="928c8-153">RELATED LINKS</span></span>