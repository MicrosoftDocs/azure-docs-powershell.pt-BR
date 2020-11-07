---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 04f182cb410e77a9ca61aa6f80da14c08e517406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773710"
---
# <span data-ttu-id="461be-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="461be-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="461be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="461be-102">SYNOPSIS</span></span>
<span data-ttu-id="461be-103">Atualiza um trabalho</span><span class="sxs-lookup"><span data-stu-id="461be-103">Updates a job</span></span>

## <span data-ttu-id="461be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="461be-104">SYNTAX</span></span>

### <span data-ttu-id="461be-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="461be-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="461be-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="461be-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="461be-107">Recorrente</span><span class="sxs-lookup"><span data-stu-id="461be-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="461be-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="461be-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="461be-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="461be-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="461be-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="461be-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="461be-111">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="461be-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="461be-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="461be-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="461be-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="461be-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="461be-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="461be-114">DESCRIPTION</span></span>
<span data-ttu-id="461be-115">O cmdlet Set-AzSqlElasticJob atualiza um trabalho</span><span class="sxs-lookup"><span data-stu-id="461be-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="461be-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="461be-116">EXAMPLES</span></span>

### <span data-ttu-id="461be-117">Exemplo 1: atualiza um trabalho para iniciar uma hora a partir de agora e repetir a cada 1 hora</span><span class="sxs-lookup"><span data-stu-id="461be-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="461be-118">Atualiza um trabalho</span><span class="sxs-lookup"><span data-stu-id="461be-118">Updates a job</span></span>

## <span data-ttu-id="461be-119">OS</span><span class="sxs-lookup"><span data-stu-id="461be-119">PARAMETERS</span></span>

### <span data-ttu-id="461be-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="461be-120">-AgentName</span></span>
<span data-ttu-id="461be-121">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="461be-121">The agent name</span></span>

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

### <span data-ttu-id="461be-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="461be-122">-DefaultProfile</span></span>
<span data-ttu-id="461be-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="461be-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="461be-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="461be-124">-Description</span></span>
<span data-ttu-id="461be-125">A descrição do trabalho</span><span class="sxs-lookup"><span data-stu-id="461be-125">The job description</span></span>

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

### <span data-ttu-id="461be-126">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="461be-126">-Enable</span></span>
<span data-ttu-id="461be-127">O sinalizador para indicar que o cliente deseja habilitar esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="461be-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="461be-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="461be-128">-EndTime</span></span>
<span data-ttu-id="461be-129">A hora de término do agendamento do trabalho</span><span class="sxs-lookup"><span data-stu-id="461be-129">The job schedule end time</span></span>

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

### <span data-ttu-id="461be-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="461be-130">-InputObject</span></span>
<span data-ttu-id="461be-131">O objeto de entrada de trabalho</span><span class="sxs-lookup"><span data-stu-id="461be-131">The job input object</span></span>

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

### <span data-ttu-id="461be-132">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="461be-132">-IntervalCount</span></span>
<span data-ttu-id="461be-133">A contagem de intervalos do cronograma recorrente</span><span class="sxs-lookup"><span data-stu-id="461be-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="461be-134">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="461be-134">-IntervalType</span></span>
<span data-ttu-id="461be-135">O tipo de intervalo do cronograma recorrente-pode ser minuto, hora, dia, semana, mês</span><span class="sxs-lookup"><span data-stu-id="461be-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="461be-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="461be-136">-Name</span></span>
<span data-ttu-id="461be-137">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="461be-137">The job name</span></span>

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

### <span data-ttu-id="461be-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="461be-138">-ResourceGroupName</span></span>
<span data-ttu-id="461be-139">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="461be-139">The resource group name</span></span>

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

### <span data-ttu-id="461be-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="461be-140">-ResourceId</span></span>
<span data-ttu-id="461be-141">A ID do recurso do trabalho</span><span class="sxs-lookup"><span data-stu-id="461be-141">The job resource id</span></span>

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

### <span data-ttu-id="461be-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="461be-142">-RunOnce</span></span>
<span data-ttu-id="461be-143">O sinalizador para indicar que o trabalho será executado uma vez</span><span class="sxs-lookup"><span data-stu-id="461be-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="461be-144">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="461be-144">-ServerName</span></span>
<span data-ttu-id="461be-145">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="461be-145">The server name</span></span>

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

### <span data-ttu-id="461be-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="461be-146">-StartTime</span></span>
<span data-ttu-id="461be-147">A hora de início do agendamento do trabalho</span><span class="sxs-lookup"><span data-stu-id="461be-147">The job schedule start time</span></span>

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

### <span data-ttu-id="461be-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="461be-148">-Confirm</span></span>
<span data-ttu-id="461be-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="461be-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="461be-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="461be-150">-WhatIf</span></span>
<span data-ttu-id="461be-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="461be-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="461be-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="461be-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="461be-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="461be-153">CommonParameters</span></span>
<span data-ttu-id="461be-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="461be-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="461be-155">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="461be-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="461be-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="461be-156">INPUTS</span></span>

### <span data-ttu-id="461be-157">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="461be-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="461be-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="461be-158">OUTPUTS</span></span>

### <span data-ttu-id="461be-159">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="461be-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="461be-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="461be-160">NOTES</span></span>

## <span data-ttu-id="461be-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="461be-161">RELATED LINKS</span></span>
