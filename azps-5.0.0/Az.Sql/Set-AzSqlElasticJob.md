---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125533"
---
# <span data-ttu-id="0a28e-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="0a28e-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="0a28e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a28e-102">SYNOPSIS</span></span>
<span data-ttu-id="0a28e-103">Atualiza um trabalho</span><span class="sxs-lookup"><span data-stu-id="0a28e-103">Updates a job</span></span>

## <span data-ttu-id="0a28e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a28e-104">SYNTAX</span></span>

### <span data-ttu-id="0a28e-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="0a28e-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a28e-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="0a28e-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a28e-107">Recorrente</span><span class="sxs-lookup"><span data-stu-id="0a28e-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a28e-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="0a28e-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a28e-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="0a28e-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a28e-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="0a28e-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a28e-111">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="0a28e-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a28e-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0a28e-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a28e-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0a28e-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a28e-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a28e-114">DESCRIPTION</span></span>
<span data-ttu-id="0a28e-115">O cmdlet Set-AzSqlElasticJob atualiza um trabalho</span><span class="sxs-lookup"><span data-stu-id="0a28e-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="0a28e-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a28e-116">EXAMPLES</span></span>

### <span data-ttu-id="0a28e-117">Exemplo 1: atualiza um trabalho para iniciar uma hora a partir de agora e repetir a cada 1 hora</span><span class="sxs-lookup"><span data-stu-id="0a28e-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="0a28e-118">Atualiza um trabalho</span><span class="sxs-lookup"><span data-stu-id="0a28e-118">Updates a job</span></span>

### <span data-ttu-id="0a28e-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0a28e-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="0a28e-120">OS</span><span class="sxs-lookup"><span data-stu-id="0a28e-120">PARAMETERS</span></span>

### <span data-ttu-id="0a28e-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0a28e-121">-AgentName</span></span>
<span data-ttu-id="0a28e-122">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="0a28e-122">The agent name</span></span>

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

### <span data-ttu-id="0a28e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a28e-123">-DefaultProfile</span></span>
<span data-ttu-id="0a28e-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a28e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a28e-125">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0a28e-125">-Description</span></span>
<span data-ttu-id="0a28e-126">A descrição do trabalho</span><span class="sxs-lookup"><span data-stu-id="0a28e-126">The job description</span></span>

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

### <span data-ttu-id="0a28e-127">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="0a28e-127">-Enable</span></span>
<span data-ttu-id="0a28e-128">O sinalizador para indicar que o cliente deseja habilitar esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="0a28e-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="0a28e-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0a28e-129">-EndTime</span></span>
<span data-ttu-id="0a28e-130">A hora de término do agendamento do trabalho</span><span class="sxs-lookup"><span data-stu-id="0a28e-130">The job schedule end time</span></span>

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

### <span data-ttu-id="0a28e-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a28e-131">-InputObject</span></span>
<span data-ttu-id="0a28e-132">O objeto de entrada de trabalho</span><span class="sxs-lookup"><span data-stu-id="0a28e-132">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a28e-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="0a28e-133">-IntervalCount</span></span>
<span data-ttu-id="0a28e-134">A contagem de intervalos do cronograma recorrente</span><span class="sxs-lookup"><span data-stu-id="0a28e-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="0a28e-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="0a28e-135">-IntervalType</span></span>
<span data-ttu-id="0a28e-136">O tipo de intervalo do cronograma recorrente-pode ser minuto, hora, dia, semana, mês</span><span class="sxs-lookup"><span data-stu-id="0a28e-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="0a28e-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a28e-137">-Name</span></span>
<span data-ttu-id="0a28e-138">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="0a28e-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a28e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a28e-139">-ResourceGroupName</span></span>
<span data-ttu-id="0a28e-140">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0a28e-140">The resource group name</span></span>

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

### <span data-ttu-id="0a28e-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a28e-141">-ResourceId</span></span>
<span data-ttu-id="0a28e-142">A ID do recurso do trabalho</span><span class="sxs-lookup"><span data-stu-id="0a28e-142">The job resource id</span></span>

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

### <span data-ttu-id="0a28e-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="0a28e-143">-RunOnce</span></span>
<span data-ttu-id="0a28e-144">O sinalizador para indicar que o trabalho será executado uma vez</span><span class="sxs-lookup"><span data-stu-id="0a28e-144">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="0a28e-145">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0a28e-145">-ServerName</span></span>
<span data-ttu-id="0a28e-146">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="0a28e-146">The server name</span></span>

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

### <span data-ttu-id="0a28e-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0a28e-147">-StartTime</span></span>
<span data-ttu-id="0a28e-148">A hora de início do agendamento do trabalho</span><span class="sxs-lookup"><span data-stu-id="0a28e-148">The job schedule start time</span></span>

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

### <span data-ttu-id="0a28e-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0a28e-149">-Confirm</span></span>
<span data-ttu-id="0a28e-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a28e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a28e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a28e-151">-WhatIf</span></span>
<span data-ttu-id="0a28e-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0a28e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a28e-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a28e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a28e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a28e-154">CommonParameters</span></span>
<span data-ttu-id="0a28e-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a28e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a28e-156">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a28e-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a28e-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a28e-157">INPUTS</span></span>

### <span data-ttu-id="0a28e-158">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="0a28e-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="0a28e-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a28e-159">OUTPUTS</span></span>

### <span data-ttu-id="0a28e-160">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="0a28e-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="0a28e-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a28e-161">NOTES</span></span>

## <span data-ttu-id="0a28e-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a28e-162">RELATED LINKS</span></span>
