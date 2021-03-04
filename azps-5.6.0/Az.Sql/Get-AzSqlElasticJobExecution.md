---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 2913c390620e18fb1781b235edca9e4f50715cd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891610"
---
# <span data-ttu-id="47031-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="47031-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="47031-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47031-102">SYNOPSIS</span></span>
<span data-ttu-id="47031-103">Obtém uma ou mais execuções de trabalho</span><span class="sxs-lookup"><span data-stu-id="47031-103">Gets one or more job executions</span></span>

## <span data-ttu-id="47031-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="47031-104">SYNTAX</span></span>

### <span data-ttu-id="47031-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="47031-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47031-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="47031-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47031-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="47031-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47031-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="47031-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47031-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="47031-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47031-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="47031-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47031-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="47031-111">DESCRIPTION</span></span>
<span data-ttu-id="47031-112">O Get-AzSqlElasticJobExecution cmdlet obtém uma ou mais execuções de trabalho</span><span class="sxs-lookup"><span data-stu-id="47031-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="47031-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47031-113">EXAMPLES</span></span>

### <span data-ttu-id="47031-114">Exemplo 1: obtém uma ou mais execuções de trabalho em todos os trabalhos</span><span class="sxs-lookup"><span data-stu-id="47031-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="47031-115">Exemplo 2: obtém uma ou mais execuções de trabalho para um trabalho</span><span class="sxs-lookup"><span data-stu-id="47031-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="47031-116">Obtém uma ou mais execuções de trabalho</span><span class="sxs-lookup"><span data-stu-id="47031-116">Gets one or more job executions</span></span>

### <span data-ttu-id="47031-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="47031-117">Example 3</span></span>

<span data-ttu-id="47031-118">Obtém uma ou mais execuções de trabalho.</span><span class="sxs-lookup"><span data-stu-id="47031-118">Gets one or more job executions.</span></span> <span data-ttu-id="47031-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="47031-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="47031-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="47031-120">PARAMETERS</span></span>

### <span data-ttu-id="47031-121">-Active</span><span class="sxs-lookup"><span data-stu-id="47031-121">-Active</span></span>
<span data-ttu-id="47031-122">Filtrar por criar tempo mínimo</span><span class="sxs-lookup"><span data-stu-id="47031-122">Filter by create time min</span></span>

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

### <span data-ttu-id="47031-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="47031-123">-AgentName</span></span>
<span data-ttu-id="47031-124">O nome do agente.</span><span class="sxs-lookup"><span data-stu-id="47031-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47031-125">-Count</span><span class="sxs-lookup"><span data-stu-id="47031-125">-Count</span></span>
<span data-ttu-id="47031-126">Count retorna o número superior de execuções.</span><span class="sxs-lookup"><span data-stu-id="47031-126">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47031-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="47031-127">-CreateTimeMax</span></span>
<span data-ttu-id="47031-128">Filtrar por criar tempo mínimo</span><span class="sxs-lookup"><span data-stu-id="47031-128">Filter by create time min</span></span>

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

### <span data-ttu-id="47031-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="47031-129">-CreateTimeMin</span></span>
<span data-ttu-id="47031-130">Filtrar por criar tempo mínimo</span><span class="sxs-lookup"><span data-stu-id="47031-130">Filter by create time min</span></span>

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

### <span data-ttu-id="47031-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47031-131">-DefaultProfile</span></span>
<span data-ttu-id="47031-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47031-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47031-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="47031-133">-EndTimeMax</span></span>
<span data-ttu-id="47031-134">Filtrar por criar tempo mínimo</span><span class="sxs-lookup"><span data-stu-id="47031-134">Filter by create time min</span></span>

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

### <span data-ttu-id="47031-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="47031-135">-EndTimeMin</span></span>
<span data-ttu-id="47031-136">Filtrar por criar tempo mínimo</span><span class="sxs-lookup"><span data-stu-id="47031-136">Filter by create time min</span></span>

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

### <span data-ttu-id="47031-137">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="47031-137">-JobExecutionId</span></span>
<span data-ttu-id="47031-138">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="47031-138">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47031-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="47031-139">-JobName</span></span>
<span data-ttu-id="47031-140">O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="47031-140">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47031-141">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="47031-141">-ParentObject</span></span>
<span data-ttu-id="47031-142">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="47031-142">The job execution id.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, WithJobExecutionIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47031-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="47031-143">-ParentResourceId</span></span>
<span data-ttu-id="47031-144">A ID de recurso do agente.</span><span class="sxs-lookup"><span data-stu-id="47031-144">The agent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47031-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47031-145">-ResourceGroupName</span></span>
<span data-ttu-id="47031-146">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="47031-146">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47031-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="47031-147">-ServerName</span></span>
<span data-ttu-id="47031-148">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="47031-148">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47031-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47031-149">CommonParameters</span></span>
<span data-ttu-id="47031-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47031-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47031-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47031-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47031-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47031-152">INPUTS</span></span>

### <span data-ttu-id="47031-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="47031-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="47031-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="47031-154">OUTPUTS</span></span>

### <span data-ttu-id="47031-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="47031-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="47031-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="47031-156">NOTES</span></span>

## <span data-ttu-id="47031-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47031-157">RELATED LINKS</span></span>
