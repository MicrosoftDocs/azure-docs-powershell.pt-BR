---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115711"
---
# <span data-ttu-id="4fdce-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="4fdce-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="4fdce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fdce-102">SYNOPSIS</span></span>
<span data-ttu-id="4fdce-103">Atualiza um trabalho</span><span class="sxs-lookup"><span data-stu-id="4fdce-103">Updates a job</span></span>

## <span data-ttu-id="4fdce-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4fdce-104">SYNTAX</span></span>

### <span data-ttu-id="4fdce-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4fdce-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fdce-106">Runonce</span><span class="sxs-lookup"><span data-stu-id="4fdce-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fdce-107">Recorrente</span><span class="sxs-lookup"><span data-stu-id="4fdce-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fdce-108">Objectset</span><span class="sxs-lookup"><span data-stu-id="4fdce-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fdce-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4fdce-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fdce-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4fdce-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fdce-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4fdce-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fdce-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4fdce-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fdce-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4fdce-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fdce-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4fdce-114">DESCRIPTION</span></span>
<span data-ttu-id="4fdce-115">O Set-AzSqlElasticJob cmdlet atualiza um trabalho</span><span class="sxs-lookup"><span data-stu-id="4fdce-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="4fdce-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4fdce-116">EXAMPLES</span></span>

### <span data-ttu-id="4fdce-117">Exemplo 1: atualiza um trabalho para iniciar uma hora a partir de agora e repetir a cada 1 hora</span><span class="sxs-lookup"><span data-stu-id="4fdce-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="4fdce-118">Atualiza um trabalho</span><span class="sxs-lookup"><span data-stu-id="4fdce-118">Updates a job</span></span>

### <span data-ttu-id="4fdce-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4fdce-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="4fdce-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4fdce-120">PARAMETERS</span></span>

### <span data-ttu-id="4fdce-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4fdce-121">-AgentName</span></span>
<span data-ttu-id="4fdce-122">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="4fdce-122">The agent name</span></span>

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

### <span data-ttu-id="4fdce-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fdce-123">-DefaultProfile</span></span>
<span data-ttu-id="4fdce-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fdce-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fdce-125">-Descrição</span><span class="sxs-lookup"><span data-stu-id="4fdce-125">-Description</span></span>
<span data-ttu-id="4fdce-126">A descrição do trabalho</span><span class="sxs-lookup"><span data-stu-id="4fdce-126">The job description</span></span>

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

### <span data-ttu-id="4fdce-127">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="4fdce-127">-Enable</span></span>
<span data-ttu-id="4fdce-128">O sinalizador para indicar que o cliente quer que esse trabalho seja habilitado.</span><span class="sxs-lookup"><span data-stu-id="4fdce-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="4fdce-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4fdce-129">-EndTime</span></span>
<span data-ttu-id="4fdce-130">Hora de término do cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="4fdce-130">The job schedule end time</span></span>

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

### <span data-ttu-id="4fdce-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fdce-131">-InputObject</span></span>
<span data-ttu-id="4fdce-132">O objeto de entrada de trabalho</span><span class="sxs-lookup"><span data-stu-id="4fdce-132">The job input object</span></span>

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

### <span data-ttu-id="4fdce-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="4fdce-133">-IntervalCount</span></span>
<span data-ttu-id="4fdce-134">A contagem de intervalos do cronograma recorrente</span><span class="sxs-lookup"><span data-stu-id="4fdce-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="4fdce-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="4fdce-135">-IntervalType</span></span>
<span data-ttu-id="4fdce-136">O tipo de intervalo do cronograma recorrente - Pode ser Minuto, Hora, Dia, Semana, Mês</span><span class="sxs-lookup"><span data-stu-id="4fdce-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="4fdce-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fdce-137">-Name</span></span>
<span data-ttu-id="4fdce-138">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="4fdce-138">The job name</span></span>

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

### <span data-ttu-id="4fdce-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fdce-139">-ResourceGroupName</span></span>
<span data-ttu-id="4fdce-140">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4fdce-140">The resource group name</span></span>

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

### <span data-ttu-id="4fdce-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fdce-141">-ResourceId</span></span>
<span data-ttu-id="4fdce-142">A ID do recurso de trabalho</span><span class="sxs-lookup"><span data-stu-id="4fdce-142">The job resource id</span></span>

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

### <span data-ttu-id="4fdce-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="4fdce-143">-RunOnce</span></span>
<span data-ttu-id="4fdce-144">O sinalizador para indicar que o trabalho será executado uma vez</span><span class="sxs-lookup"><span data-stu-id="4fdce-144">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="4fdce-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4fdce-145">-ServerName</span></span>
<span data-ttu-id="4fdce-146">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="4fdce-146">The server name</span></span>

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

### <span data-ttu-id="4fdce-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4fdce-147">-StartTime</span></span>
<span data-ttu-id="4fdce-148">A hora de início do cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="4fdce-148">The job schedule start time</span></span>

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

### <span data-ttu-id="4fdce-149">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4fdce-149">-Confirm</span></span>
<span data-ttu-id="4fdce-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fdce-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fdce-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fdce-151">-WhatIf</span></span>
<span data-ttu-id="4fdce-152">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4fdce-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fdce-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4fdce-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fdce-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fdce-154">CommonParameters</span></span>
<span data-ttu-id="4fdce-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fdce-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fdce-156">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fdce-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fdce-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="4fdce-157">INPUTS</span></span>

### <span data-ttu-id="4fdce-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="4fdce-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="4fdce-159">Saídas</span><span class="sxs-lookup"><span data-stu-id="4fdce-159">OUTPUTS</span></span>

### <span data-ttu-id="4fdce-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="4fdce-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="4fdce-161">Notas</span><span class="sxs-lookup"><span data-stu-id="4fdce-161">NOTES</span></span>

## <span data-ttu-id="4fdce-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fdce-162">RELATED LINKS</span></span>
