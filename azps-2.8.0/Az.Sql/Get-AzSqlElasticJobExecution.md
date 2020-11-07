---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 5b5837fb0c5fa56e8e8f9887b6d85bfc3a3a559c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773630"
---
# <span data-ttu-id="1cdda-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="1cdda-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="1cdda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cdda-102">SYNOPSIS</span></span>
<span data-ttu-id="1cdda-103">Obtém uma ou mais execuções de trabalho</span><span class="sxs-lookup"><span data-stu-id="1cdda-103">Gets one or more job executions</span></span>

## <span data-ttu-id="1cdda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cdda-104">SYNTAX</span></span>

### <span data-ttu-id="1cdda-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="1cdda-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1cdda-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="1cdda-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cdda-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="1cdda-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cdda-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="1cdda-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cdda-109">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="1cdda-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cdda-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1cdda-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cdda-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cdda-111">DESCRIPTION</span></span>
<span data-ttu-id="1cdda-112">O cmdlet Get-AzSqlElasticJobExecution Obtém uma ou mais execuções de trabalho</span><span class="sxs-lookup"><span data-stu-id="1cdda-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="1cdda-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cdda-113">EXAMPLES</span></span>

### <span data-ttu-id="1cdda-114">Exemplo 1-Obtém uma ou mais execuções de trabalho em todos os trabalhos</span><span class="sxs-lookup"><span data-stu-id="1cdda-114">Example 1 - Gets one or more job executions across all jobs</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="1cdda-115">Exemplo 2-Obtém uma ou mais execuções de trabalho para um trabalho</span><span class="sxs-lookup"><span data-stu-id="1cdda-115">Example 2 - Gets one or more job executions for a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="1cdda-116">Obtém uma ou mais execuções de trabalho</span><span class="sxs-lookup"><span data-stu-id="1cdda-116">Gets one or more job executions</span></span>

## <span data-ttu-id="1cdda-117">OS</span><span class="sxs-lookup"><span data-stu-id="1cdda-117">PARAMETERS</span></span>

### <span data-ttu-id="1cdda-118">-Ativo</span><span class="sxs-lookup"><span data-stu-id="1cdda-118">-Active</span></span>
<span data-ttu-id="1cdda-119">Filtrar por tempo de criação min</span><span class="sxs-lookup"><span data-stu-id="1cdda-119">Filter by create time min</span></span>

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

### <span data-ttu-id="1cdda-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="1cdda-120">-AgentName</span></span>
<span data-ttu-id="1cdda-121">O nome do agente.</span><span class="sxs-lookup"><span data-stu-id="1cdda-121">The agent name.</span></span>

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

### <span data-ttu-id="1cdda-122">-Contagem</span><span class="sxs-lookup"><span data-stu-id="1cdda-122">-Count</span></span>
<span data-ttu-id="1cdda-123">Count retorna o número superior de execuções.</span><span class="sxs-lookup"><span data-stu-id="1cdda-123">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="1cdda-124">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="1cdda-124">-CreateTimeMax</span></span>
<span data-ttu-id="1cdda-125">Filtrar por tempo de criação min</span><span class="sxs-lookup"><span data-stu-id="1cdda-125">Filter by create time min</span></span>

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

### <span data-ttu-id="1cdda-126">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="1cdda-126">-CreateTimeMin</span></span>
<span data-ttu-id="1cdda-127">Filtrar por tempo de criação min</span><span class="sxs-lookup"><span data-stu-id="1cdda-127">Filter by create time min</span></span>

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

### <span data-ttu-id="1cdda-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cdda-128">-DefaultProfile</span></span>
<span data-ttu-id="1cdda-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1cdda-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cdda-130">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="1cdda-130">-EndTimeMax</span></span>
<span data-ttu-id="1cdda-131">Filtrar por tempo de criação min</span><span class="sxs-lookup"><span data-stu-id="1cdda-131">Filter by create time min</span></span>

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

### <span data-ttu-id="1cdda-132">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="1cdda-132">-EndTimeMin</span></span>
<span data-ttu-id="1cdda-133">Filtrar por tempo de criação min</span><span class="sxs-lookup"><span data-stu-id="1cdda-133">Filter by create time min</span></span>

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

### <span data-ttu-id="1cdda-134">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="1cdda-134">-JobExecutionId</span></span>
<span data-ttu-id="1cdda-135">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="1cdda-135">The job execution id.</span></span>

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

### <span data-ttu-id="1cdda-136">-JobName</span><span class="sxs-lookup"><span data-stu-id="1cdda-136">-JobName</span></span>
<span data-ttu-id="1cdda-137">O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="1cdda-137">The job name.</span></span>

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

### <span data-ttu-id="1cdda-138">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1cdda-138">-ParentObject</span></span>
<span data-ttu-id="1cdda-139">A ID de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="1cdda-139">The job execution id.</span></span>

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

### <span data-ttu-id="1cdda-140">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1cdda-140">-ParentResourceId</span></span>
<span data-ttu-id="1cdda-141">A ID do recurso do agente.</span><span class="sxs-lookup"><span data-stu-id="1cdda-141">The agent resource id.</span></span>

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

### <span data-ttu-id="1cdda-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cdda-142">-ResourceGroupName</span></span>
<span data-ttu-id="1cdda-143">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1cdda-143">The resource group name.</span></span>

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

### <span data-ttu-id="1cdda-144">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="1cdda-144">-ServerName</span></span>
<span data-ttu-id="1cdda-145">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="1cdda-145">The server name.</span></span>

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

### <span data-ttu-id="1cdda-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cdda-146">CommonParameters</span></span>
<span data-ttu-id="1cdda-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cdda-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cdda-148">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cdda-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cdda-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cdda-149">INPUTS</span></span>

### <span data-ttu-id="1cdda-150">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="1cdda-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="1cdda-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cdda-151">OUTPUTS</span></span>

### <span data-ttu-id="1cdda-152">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="1cdda-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="1cdda-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cdda-153">NOTES</span></span>

## <span data-ttu-id="1cdda-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cdda-154">RELATED LINKS</span></span>
