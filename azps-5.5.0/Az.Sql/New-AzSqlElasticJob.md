---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112540"
---
# <span data-ttu-id="3cb69-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="3cb69-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="3cb69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3cb69-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb69-103">Cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="3cb69-103">Creates a new job</span></span>

## <span data-ttu-id="3cb69-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cb69-104">SYNTAX</span></span>

### <span data-ttu-id="3cb69-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3cb69-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cb69-106">Runonce</span><span class="sxs-lookup"><span data-stu-id="3cb69-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb69-107">Recorrente</span><span class="sxs-lookup"><span data-stu-id="3cb69-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cb69-108">Objectset</span><span class="sxs-lookup"><span data-stu-id="3cb69-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb69-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="3cb69-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb69-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="3cb69-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb69-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3cb69-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb69-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3cb69-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cb69-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3cb69-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cb69-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3cb69-114">DESCRIPTION</span></span>
<span data-ttu-id="3cb69-115">O New-AzSqlElasticJob cmdlet cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="3cb69-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="3cb69-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3cb69-116">EXAMPLES</span></span>

### <span data-ttu-id="3cb69-117">Exemplo 1: cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="3cb69-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="3cb69-118">Cria um novo trabalho</span><span class="sxs-lookup"><span data-stu-id="3cb69-118">Creates a new job</span></span>

### <span data-ttu-id="3cb69-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3cb69-119">Example 2</span></span>

<span data-ttu-id="3cb69-120">Cria um novo trabalho.</span><span class="sxs-lookup"><span data-stu-id="3cb69-120">Creates a new job.</span></span> <span data-ttu-id="3cb69-121">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="3cb69-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="3cb69-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cb69-122">PARAMETERS</span></span>

### <span data-ttu-id="3cb69-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3cb69-123">-AgentName</span></span>
<span data-ttu-id="3cb69-124">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="3cb69-124">The agent name</span></span>

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

### <span data-ttu-id="3cb69-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb69-125">-DefaultProfile</span></span>
<span data-ttu-id="3cb69-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3cb69-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cb69-127">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3cb69-127">-Description</span></span>
<span data-ttu-id="3cb69-128">A descrição do trabalho</span><span class="sxs-lookup"><span data-stu-id="3cb69-128">The job description</span></span>

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

### <span data-ttu-id="3cb69-129">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="3cb69-129">-Enable</span></span>
<span data-ttu-id="3cb69-130">O sinalizador para indicar que o cliente quer que esse trabalho seja habilitado.</span><span class="sxs-lookup"><span data-stu-id="3cb69-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="3cb69-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3cb69-131">-EndTime</span></span>
<span data-ttu-id="3cb69-132">Hora de término do cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="3cb69-132">The job schedule end time</span></span>

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

### <span data-ttu-id="3cb69-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="3cb69-133">-IntervalCount</span></span>
<span data-ttu-id="3cb69-134">A contagem de intervalos do cronograma recorrente</span><span class="sxs-lookup"><span data-stu-id="3cb69-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="3cb69-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="3cb69-135">-IntervalType</span></span>
<span data-ttu-id="3cb69-136">O tipo de intervalo do cronograma recorrente - Pode ser Minuto, Hora, Dia, Semana, Mês</span><span class="sxs-lookup"><span data-stu-id="3cb69-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="3cb69-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="3cb69-137">-Name</span></span>
<span data-ttu-id="3cb69-138">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="3cb69-138">The job name</span></span>

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

### <span data-ttu-id="3cb69-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3cb69-139">-ParentObject</span></span>
<span data-ttu-id="3cb69-140">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="3cb69-140">The agent input object</span></span>

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

### <span data-ttu-id="3cb69-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3cb69-141">-ParentResourceId</span></span>
<span data-ttu-id="3cb69-142">A ID de recurso do agente</span><span class="sxs-lookup"><span data-stu-id="3cb69-142">The agent resource id</span></span>

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

### <span data-ttu-id="3cb69-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb69-143">-ResourceGroupName</span></span>
<span data-ttu-id="3cb69-144">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3cb69-144">The resource group name</span></span>

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

### <span data-ttu-id="3cb69-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="3cb69-145">-RunOnce</span></span>
<span data-ttu-id="3cb69-146">O sinalizador para indicar que o trabalho será executado uma vez</span><span class="sxs-lookup"><span data-stu-id="3cb69-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="3cb69-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3cb69-147">-ServerName</span></span>
<span data-ttu-id="3cb69-148">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="3cb69-148">The server name</span></span>

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

### <span data-ttu-id="3cb69-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3cb69-149">-StartTime</span></span>
<span data-ttu-id="3cb69-150">A hora de início do cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="3cb69-150">The job schedule start time</span></span>

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

### <span data-ttu-id="3cb69-151">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3cb69-151">-Confirm</span></span>
<span data-ttu-id="3cb69-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cb69-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cb69-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb69-153">-WhatIf</span></span>
<span data-ttu-id="3cb69-154">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3cb69-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cb69-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3cb69-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cb69-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb69-156">CommonParameters</span></span>
<span data-ttu-id="3cb69-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb69-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb69-158">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cb69-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb69-159">Entradas</span><span class="sxs-lookup"><span data-stu-id="3cb69-159">INPUTS</span></span>

### <span data-ttu-id="3cb69-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="3cb69-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="3cb69-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="3cb69-161">OUTPUTS</span></span>

### <span data-ttu-id="3cb69-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="3cb69-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="3cb69-163">Notas</span><span class="sxs-lookup"><span data-stu-id="3cb69-163">NOTES</span></span>

## <span data-ttu-id="3cb69-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3cb69-164">RELATED LINKS</span></span>
