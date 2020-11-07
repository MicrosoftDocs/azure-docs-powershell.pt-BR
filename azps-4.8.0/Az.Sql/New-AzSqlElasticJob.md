---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954589"
---
# <span data-ttu-id="efa5e-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="efa5e-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="efa5e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efa5e-102">SYNOPSIS</span></span>
<span data-ttu-id="efa5e-103">Cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="efa5e-103">Creates a new job</span></span>

## <span data-ttu-id="efa5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efa5e-104">SYNTAX</span></span>

### <span data-ttu-id="efa5e-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="efa5e-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efa5e-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="efa5e-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa5e-107">Recorrente</span><span class="sxs-lookup"><span data-stu-id="efa5e-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efa5e-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="efa5e-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa5e-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="efa5e-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa5e-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="efa5e-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa5e-111">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="efa5e-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa5e-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="efa5e-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efa5e-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="efa5e-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efa5e-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="efa5e-114">DESCRIPTION</span></span>
<span data-ttu-id="efa5e-115">O cmdlet New-AzSqlElasticJob cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="efa5e-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="efa5e-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="efa5e-116">EXAMPLES</span></span>

### <span data-ttu-id="efa5e-117">Exemplo 1: cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="efa5e-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="efa5e-118">Cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="efa5e-118">Creates a new job</span></span>

### <span data-ttu-id="efa5e-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="efa5e-119">Example 2</span></span>

<span data-ttu-id="efa5e-120">Cria um novo trabalho.</span><span class="sxs-lookup"><span data-stu-id="efa5e-120">Creates a new job.</span></span> <span data-ttu-id="efa5e-121">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="efa5e-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="efa5e-122">OS</span><span class="sxs-lookup"><span data-stu-id="efa5e-122">PARAMETERS</span></span>

### <span data-ttu-id="efa5e-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="efa5e-123">-AgentName</span></span>
<span data-ttu-id="efa5e-124">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="efa5e-124">The agent name</span></span>

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

### <span data-ttu-id="efa5e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa5e-125">-DefaultProfile</span></span>
<span data-ttu-id="efa5e-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="efa5e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efa5e-127">-Descrição</span><span class="sxs-lookup"><span data-stu-id="efa5e-127">-Description</span></span>
<span data-ttu-id="efa5e-128">A descrição do trabalho</span><span class="sxs-lookup"><span data-stu-id="efa5e-128">The job description</span></span>

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

### <span data-ttu-id="efa5e-129">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="efa5e-129">-Enable</span></span>
<span data-ttu-id="efa5e-130">O sinalizador para indicar que o cliente deseja habilitar esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="efa5e-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="efa5e-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="efa5e-131">-EndTime</span></span>
<span data-ttu-id="efa5e-132">A hora de término do agendamento do trabalho</span><span class="sxs-lookup"><span data-stu-id="efa5e-132">The job schedule end time</span></span>

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

### <span data-ttu-id="efa5e-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="efa5e-133">-IntervalCount</span></span>
<span data-ttu-id="efa5e-134">A contagem de intervalos do cronograma recorrente</span><span class="sxs-lookup"><span data-stu-id="efa5e-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="efa5e-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="efa5e-135">-IntervalType</span></span>
<span data-ttu-id="efa5e-136">O tipo de intervalo do cronograma recorrente-pode ser minuto, hora, dia, semana, mês</span><span class="sxs-lookup"><span data-stu-id="efa5e-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="efa5e-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="efa5e-137">-Name</span></span>
<span data-ttu-id="efa5e-138">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="efa5e-138">The job name</span></span>

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

### <span data-ttu-id="efa5e-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="efa5e-139">-ParentObject</span></span>
<span data-ttu-id="efa5e-140">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="efa5e-140">The agent input object</span></span>

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

### <span data-ttu-id="efa5e-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="efa5e-141">-ParentResourceId</span></span>
<span data-ttu-id="efa5e-142">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="efa5e-142">The agent resource id</span></span>

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

### <span data-ttu-id="efa5e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa5e-143">-ResourceGroupName</span></span>
<span data-ttu-id="efa5e-144">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="efa5e-144">The resource group name</span></span>

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

### <span data-ttu-id="efa5e-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="efa5e-145">-RunOnce</span></span>
<span data-ttu-id="efa5e-146">O sinalizador para indicar que o trabalho será executado uma vez</span><span class="sxs-lookup"><span data-stu-id="efa5e-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="efa5e-147">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="efa5e-147">-ServerName</span></span>
<span data-ttu-id="efa5e-148">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="efa5e-148">The server name</span></span>

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

### <span data-ttu-id="efa5e-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="efa5e-149">-StartTime</span></span>
<span data-ttu-id="efa5e-150">A hora de início do agendamento do trabalho</span><span class="sxs-lookup"><span data-stu-id="efa5e-150">The job schedule start time</span></span>

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

### <span data-ttu-id="efa5e-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="efa5e-151">-Confirm</span></span>
<span data-ttu-id="efa5e-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efa5e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efa5e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa5e-153">-WhatIf</span></span>
<span data-ttu-id="efa5e-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="efa5e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efa5e-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="efa5e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efa5e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa5e-156">CommonParameters</span></span>
<span data-ttu-id="efa5e-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efa5e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa5e-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efa5e-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa5e-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="efa5e-159">INPUTS</span></span>

### <span data-ttu-id="efa5e-160">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="efa5e-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="efa5e-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="efa5e-161">OUTPUTS</span></span>

### <span data-ttu-id="efa5e-162">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="efa5e-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="efa5e-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="efa5e-163">NOTES</span></span>

## <span data-ttu-id="efa5e-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efa5e-164">RELATED LINKS</span></span>
