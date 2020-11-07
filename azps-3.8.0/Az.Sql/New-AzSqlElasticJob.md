---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 98c019c8dedf767fc2b75bb2133f7c545ffd03ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777416"
---
# <span data-ttu-id="59f29-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="59f29-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="59f29-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59f29-102">SYNOPSIS</span></span>
<span data-ttu-id="59f29-103">Cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="59f29-103">Creates a new job</span></span>

## <span data-ttu-id="59f29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59f29-104">SYNTAX</span></span>

### <span data-ttu-id="59f29-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="59f29-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59f29-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="59f29-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f29-107">Recorrente</span><span class="sxs-lookup"><span data-stu-id="59f29-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59f29-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="59f29-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f29-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="59f29-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f29-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="59f29-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f29-111">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="59f29-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f29-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="59f29-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59f29-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="59f29-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59f29-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59f29-114">DESCRIPTION</span></span>
<span data-ttu-id="59f29-115">O cmdlet New-AzSqlElasticJob cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="59f29-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="59f29-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59f29-116">EXAMPLES</span></span>

### <span data-ttu-id="59f29-117">Exemplo 1-criar um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="59f29-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="59f29-118">Cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="59f29-118">Creates a new job</span></span>

## <span data-ttu-id="59f29-119">OS</span><span class="sxs-lookup"><span data-stu-id="59f29-119">PARAMETERS</span></span>

### <span data-ttu-id="59f29-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="59f29-120">-AgentName</span></span>
<span data-ttu-id="59f29-121">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="59f29-121">The agent name</span></span>

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

### <span data-ttu-id="59f29-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f29-122">-DefaultProfile</span></span>
<span data-ttu-id="59f29-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59f29-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59f29-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="59f29-124">-Description</span></span>
<span data-ttu-id="59f29-125">A descrição do trabalho</span><span class="sxs-lookup"><span data-stu-id="59f29-125">The job description</span></span>

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

### <span data-ttu-id="59f29-126">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="59f29-126">-Enable</span></span>
<span data-ttu-id="59f29-127">O sinalizador para indicar que o cliente deseja habilitar esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="59f29-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="59f29-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="59f29-128">-EndTime</span></span>
<span data-ttu-id="59f29-129">A hora de término do agendamento do trabalho</span><span class="sxs-lookup"><span data-stu-id="59f29-129">The job schedule end time</span></span>

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

### <span data-ttu-id="59f29-130">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="59f29-130">-IntervalCount</span></span>
<span data-ttu-id="59f29-131">A contagem de intervalos do cronograma recorrente</span><span class="sxs-lookup"><span data-stu-id="59f29-131">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="59f29-132">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="59f29-132">-IntervalType</span></span>
<span data-ttu-id="59f29-133">O tipo de intervalo do cronograma recorrente-pode ser minuto, hora, dia, semana, mês</span><span class="sxs-lookup"><span data-stu-id="59f29-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="59f29-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="59f29-134">-Name</span></span>
<span data-ttu-id="59f29-135">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="59f29-135">The job name</span></span>

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

### <span data-ttu-id="59f29-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="59f29-136">-ParentObject</span></span>
<span data-ttu-id="59f29-137">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="59f29-137">The agent input object</span></span>

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

### <span data-ttu-id="59f29-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="59f29-138">-ParentResourceId</span></span>
<span data-ttu-id="59f29-139">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="59f29-139">The agent resource id</span></span>

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

### <span data-ttu-id="59f29-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59f29-140">-ResourceGroupName</span></span>
<span data-ttu-id="59f29-141">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="59f29-141">The resource group name</span></span>

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

### <span data-ttu-id="59f29-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="59f29-142">-RunOnce</span></span>
<span data-ttu-id="59f29-143">O sinalizador para indicar que o trabalho será executado uma vez</span><span class="sxs-lookup"><span data-stu-id="59f29-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="59f29-144">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="59f29-144">-ServerName</span></span>
<span data-ttu-id="59f29-145">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="59f29-145">The server name</span></span>

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

### <span data-ttu-id="59f29-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="59f29-146">-StartTime</span></span>
<span data-ttu-id="59f29-147">A hora de início do agendamento do trabalho</span><span class="sxs-lookup"><span data-stu-id="59f29-147">The job schedule start time</span></span>

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

### <span data-ttu-id="59f29-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="59f29-148">-Confirm</span></span>
<span data-ttu-id="59f29-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59f29-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59f29-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59f29-150">-WhatIf</span></span>
<span data-ttu-id="59f29-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="59f29-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59f29-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="59f29-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59f29-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f29-153">CommonParameters</span></span>
<span data-ttu-id="59f29-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59f29-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f29-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59f29-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f29-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59f29-156">INPUTS</span></span>

### <span data-ttu-id="59f29-157">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="59f29-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="59f29-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59f29-158">OUTPUTS</span></span>

### <span data-ttu-id="59f29-159">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="59f29-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="59f29-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59f29-160">NOTES</span></span>

## <span data-ttu-id="59f29-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59f29-161">RELATED LINKS</span></span>
