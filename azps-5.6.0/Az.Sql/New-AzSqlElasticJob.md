---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 961f37db94cff87952b2811a528a94cc71ffabff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892922"
---
# <span data-ttu-id="8f1c7-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="8f1c7-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="8f1c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f1c7-102">SYNOPSIS</span></span>
<span data-ttu-id="8f1c7-103">Cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="8f1c7-103">Creates a new job</span></span>

## <span data-ttu-id="8f1c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8f1c7-104">SYNTAX</span></span>

### <span data-ttu-id="8f1c7-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f1c7-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f1c7-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="8f1c7-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1c7-107">Recorrente</span><span class="sxs-lookup"><span data-stu-id="8f1c7-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f1c7-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="8f1c7-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1c7-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8f1c7-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1c7-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8f1c7-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1c7-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8f1c7-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1c7-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8f1c7-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f1c7-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8f1c7-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f1c7-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8f1c7-114">DESCRIPTION</span></span>
<span data-ttu-id="8f1c7-115">O New-AzSqlElasticJob cmdlet cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="8f1c7-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="8f1c7-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f1c7-116">EXAMPLES</span></span>

### <span data-ttu-id="8f1c7-117">Exemplo 1: cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="8f1c7-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="8f1c7-118">Cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="8f1c7-118">Creates a new job</span></span>

### <span data-ttu-id="8f1c7-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8f1c7-119">Example 2</span></span>

<span data-ttu-id="8f1c7-120">Cria um novo trabalho.</span><span class="sxs-lookup"><span data-stu-id="8f1c7-120">Creates a new job.</span></span> <span data-ttu-id="8f1c7-121">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="8f1c7-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="8f1c7-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8f1c7-122">PARAMETERS</span></span>

### <span data-ttu-id="8f1c7-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="8f1c7-123">-AgentName</span></span>
<span data-ttu-id="8f1c7-124">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="8f1c7-124">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f1c7-125">-DefaultProfile</span></span>
<span data-ttu-id="8f1c7-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f1c7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f1c7-127">-Description</span><span class="sxs-lookup"><span data-stu-id="8f1c7-127">-Description</span></span>
<span data-ttu-id="8f1c7-128">A descrição do trabalho</span><span class="sxs-lookup"><span data-stu-id="8f1c7-128">The job description</span></span>

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

### <span data-ttu-id="8f1c7-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="8f1c7-129">-Enable</span></span>
<span data-ttu-id="8f1c7-130">O sinalizador para indicar que o cliente deseja que esse trabalho seja habilitado.</span><span class="sxs-lookup"><span data-stu-id="8f1c7-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="8f1c7-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8f1c7-131">-EndTime</span></span>
<span data-ttu-id="8f1c7-132">Hora de término do agendamento do trabalho</span><span class="sxs-lookup"><span data-stu-id="8f1c7-132">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="8f1c7-133">-IntervalCount</span></span>
<span data-ttu-id="8f1c7-134">A contagem de intervalos de agendamento recorrente</span><span class="sxs-lookup"><span data-stu-id="8f1c7-134">The recurring schedule interval count</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="8f1c7-135">-IntervalType</span></span>
<span data-ttu-id="8f1c7-136">O tipo de intervalo de agenda recorrente - Pode ser Minuto, Hora, Dia, Semana, Mês</span><span class="sxs-lookup"><span data-stu-id="8f1c7-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

```yaml
Type: System.String
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-137">-Name</span><span class="sxs-lookup"><span data-stu-id="8f1c7-137">-Name</span></span>
<span data-ttu-id="8f1c7-138">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="8f1c7-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8f1c7-139">-ParentObject</span></span>
<span data-ttu-id="8f1c7-140">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="8f1c7-140">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8f1c7-141">-ParentResourceId</span></span>
<span data-ttu-id="8f1c7-142">A ID de recurso do agente</span><span class="sxs-lookup"><span data-stu-id="8f1c7-142">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f1c7-143">-ResourceGroupName</span></span>
<span data-ttu-id="8f1c7-144">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8f1c7-144">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="8f1c7-145">-RunOnce</span></span>
<span data-ttu-id="8f1c7-146">O sinalizador para indicar que o trabalho será executado uma vez</span><span class="sxs-lookup"><span data-stu-id="8f1c7-146">The flag to indicate job will be run once</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RunOnce, RunOnceUsingParentObject, RunOnceUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8f1c7-147">-ServerName</span></span>
<span data-ttu-id="8f1c7-148">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="8f1c7-148">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8f1c7-149">-StartTime</span></span>
<span data-ttu-id="8f1c7-150">Hora de início do agendamento do trabalho</span><span class="sxs-lookup"><span data-stu-id="8f1c7-150">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RunOnce, Recurring, RunOnceUsingParentObject, RecurringUsingParentObject, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f1c7-151">-Confirm</span></span>
<span data-ttu-id="8f1c7-152">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f1c7-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f1c7-153">-WhatIf</span></span>
<span data-ttu-id="8f1c7-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f1c7-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f1c7-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f1c7-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1c7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f1c7-156">CommonParameters</span></span>
<span data-ttu-id="8f1c7-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f1c7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f1c7-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f1c7-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f1c7-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f1c7-159">INPUTS</span></span>

### <span data-ttu-id="8f1c7-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="8f1c7-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="8f1c7-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8f1c7-161">OUTPUTS</span></span>

### <span data-ttu-id="8f1c7-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="8f1c7-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="8f1c7-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="8f1c7-163">NOTES</span></span>

## <span data-ttu-id="8f1c7-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f1c7-164">RELATED LINKS</span></span>
