---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 29ae424807b8648238e2cc855fb90734773e870d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773571"
---
# <span data-ttu-id="0615b-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="0615b-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="0615b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0615b-102">SYNOPSIS</span></span>
<span data-ttu-id="0615b-103">Cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="0615b-103">Creates a new job</span></span>

## <span data-ttu-id="0615b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0615b-104">SYNTAX</span></span>

### <span data-ttu-id="0615b-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="0615b-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0615b-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="0615b-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0615b-107">Recorrente</span><span class="sxs-lookup"><span data-stu-id="0615b-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0615b-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="0615b-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0615b-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="0615b-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0615b-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="0615b-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0615b-111">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="0615b-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0615b-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0615b-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0615b-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0615b-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0615b-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0615b-114">DESCRIPTION</span></span>
<span data-ttu-id="0615b-115">O cmdlet New-AzSqlElasticJob cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="0615b-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="0615b-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0615b-116">EXAMPLES</span></span>

### <span data-ttu-id="0615b-117">Exemplo 1-criar um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="0615b-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="0615b-118">Cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="0615b-118">Creates a new job</span></span>

## <span data-ttu-id="0615b-119">OS</span><span class="sxs-lookup"><span data-stu-id="0615b-119">PARAMETERS</span></span>

### <span data-ttu-id="0615b-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0615b-120">-AgentName</span></span>
<span data-ttu-id="0615b-121">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="0615b-121">The agent name</span></span>

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

### <span data-ttu-id="0615b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0615b-122">-DefaultProfile</span></span>
<span data-ttu-id="0615b-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0615b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0615b-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0615b-124">-Description</span></span>
<span data-ttu-id="0615b-125">A descrição do trabalho</span><span class="sxs-lookup"><span data-stu-id="0615b-125">The job description</span></span>

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

### <span data-ttu-id="0615b-126">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="0615b-126">-Enable</span></span>
<span data-ttu-id="0615b-127">O sinalizador para indicar que o cliente deseja habilitar esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="0615b-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="0615b-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0615b-128">-EndTime</span></span>
<span data-ttu-id="0615b-129">A hora de término do agendamento do trabalho</span><span class="sxs-lookup"><span data-stu-id="0615b-129">The job schedule end time</span></span>

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

### <span data-ttu-id="0615b-130">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="0615b-130">-IntervalCount</span></span>
<span data-ttu-id="0615b-131">A contagem de intervalos do cronograma recorrente</span><span class="sxs-lookup"><span data-stu-id="0615b-131">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="0615b-132">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="0615b-132">-IntervalType</span></span>
<span data-ttu-id="0615b-133">O tipo de intervalo do cronograma recorrente-pode ser minuto, hora, dia, semana, mês</span><span class="sxs-lookup"><span data-stu-id="0615b-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="0615b-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="0615b-134">-Name</span></span>
<span data-ttu-id="0615b-135">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="0615b-135">The job name</span></span>

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

### <span data-ttu-id="0615b-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0615b-136">-ParentObject</span></span>
<span data-ttu-id="0615b-137">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="0615b-137">The agent input object</span></span>

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

### <span data-ttu-id="0615b-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0615b-138">-ParentResourceId</span></span>
<span data-ttu-id="0615b-139">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="0615b-139">The agent resource id</span></span>

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

### <span data-ttu-id="0615b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0615b-140">-ResourceGroupName</span></span>
<span data-ttu-id="0615b-141">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0615b-141">The resource group name</span></span>

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

### <span data-ttu-id="0615b-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="0615b-142">-RunOnce</span></span>
<span data-ttu-id="0615b-143">O sinalizador para indicar que o trabalho será executado uma vez</span><span class="sxs-lookup"><span data-stu-id="0615b-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="0615b-144">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0615b-144">-ServerName</span></span>
<span data-ttu-id="0615b-145">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="0615b-145">The server name</span></span>

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

### <span data-ttu-id="0615b-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0615b-146">-StartTime</span></span>
<span data-ttu-id="0615b-147">A hora de início do agendamento do trabalho</span><span class="sxs-lookup"><span data-stu-id="0615b-147">The job schedule start time</span></span>

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

### <span data-ttu-id="0615b-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0615b-148">-Confirm</span></span>
<span data-ttu-id="0615b-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0615b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0615b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0615b-150">-WhatIf</span></span>
<span data-ttu-id="0615b-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0615b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0615b-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0615b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0615b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0615b-153">CommonParameters</span></span>
<span data-ttu-id="0615b-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0615b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0615b-155">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0615b-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0615b-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0615b-156">INPUTS</span></span>

### <span data-ttu-id="0615b-157">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="0615b-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="0615b-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0615b-158">OUTPUTS</span></span>

### <span data-ttu-id="0615b-159">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="0615b-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="0615b-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0615b-160">NOTES</span></span>

## <span data-ttu-id="0615b-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0615b-161">RELATED LINKS</span></span>
