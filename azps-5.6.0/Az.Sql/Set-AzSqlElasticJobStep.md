---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: ec2f9174cc0ca8781b56784836a4583b0568128e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889081"
---
# <span data-ttu-id="4c482-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="4c482-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="4c482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c482-102">SYNOPSIS</span></span>
<span data-ttu-id="4c482-103">Atualiza uma etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="4c482-103">Updates a job step</span></span>

## <span data-ttu-id="4c482-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4c482-104">SYNTAX</span></span>

### <span data-ttu-id="4c482-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4c482-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c482-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="4c482-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c482-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="4c482-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c482-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4c482-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c482-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4c482-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c482-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4c482-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c482-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4c482-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c482-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4c482-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c482-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4c482-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c482-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4c482-114">DESCRIPTION</span></span>
<span data-ttu-id="4c482-115">O Set-AzSqlElasticJobStep cmdlet atualiza uma etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="4c482-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="4c482-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c482-116">EXAMPLES</span></span>

### <span data-ttu-id="4c482-117">Exemplo 1: atualiza o grupo de destino de uma etapa de trabalho para um trabalho</span><span class="sxs-lookup"><span data-stu-id="4c482-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="4c482-118">Exemplo 2: atualiza o script T-SQL de uma etapa de trabalho para um trabalho</span><span class="sxs-lookup"><span data-stu-id="4c482-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="4c482-119">Atualiza uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="4c482-119">Updates a job step from a job</span></span>

### <span data-ttu-id="4c482-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4c482-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="4c482-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4c482-121">PARAMETERS</span></span>

### <span data-ttu-id="4c482-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4c482-122">-AgentName</span></span>
<span data-ttu-id="4c482-123">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="4c482-123">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="4c482-124">-CommandText</span></span>
<span data-ttu-id="4c482-125">O texto do comando</span><span class="sxs-lookup"><span data-stu-id="4c482-125">The command text</span></span>

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

### <span data-ttu-id="4c482-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="4c482-126">-CredentialName</span></span>
<span data-ttu-id="4c482-127">O nome da credencial</span><span class="sxs-lookup"><span data-stu-id="4c482-127">The credential name</span></span>

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

### <span data-ttu-id="4c482-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c482-128">-DefaultProfile</span></span>
<span data-ttu-id="4c482-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c482-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c482-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="4c482-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="4c482-131">Os segundos iniciais de intervalo de repetir</span><span class="sxs-lookup"><span data-stu-id="4c482-131">The initial retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c482-132">-InputObject</span></span>
<span data-ttu-id="4c482-133">O objeto de etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="4c482-133">The job step object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet, WithRemoveOutputUsingParentObject, WithAddOutputUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="4c482-134">-JobName</span></span>
<span data-ttu-id="4c482-135">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="4c482-135">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="4c482-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="4c482-137">O intervalo máximo de repetir segundos</span><span class="sxs-lookup"><span data-stu-id="4c482-137">The maximum retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-138">-Name</span><span class="sxs-lookup"><span data-stu-id="4c482-138">-Name</span></span>
<span data-ttu-id="4c482-139">O nome da etapa</span><span class="sxs-lookup"><span data-stu-id="4c482-139">The step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="4c482-140">-OutputCredentialName</span></span>
<span data-ttu-id="4c482-141">O nome da credencial de saída</span><span class="sxs-lookup"><span data-stu-id="4c482-141">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="4c482-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="4c482-143">O objeto de banco de dados de saída</span><span class="sxs-lookup"><span data-stu-id="4c482-143">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="4c482-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="4c482-145">A ID do recurso de banco de dados de saída</span><span class="sxs-lookup"><span data-stu-id="4c482-145">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithAddOutput, WithAddOutputUsingParentObject, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="4c482-146">-OutputSchemaName</span></span>
<span data-ttu-id="4c482-147">O nome do esquema de saída</span><span class="sxs-lookup"><span data-stu-id="4c482-147">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="4c482-148">-OutputTableName</span></span>
<span data-ttu-id="4c482-149">O nome da tabela de saída</span><span class="sxs-lookup"><span data-stu-id="4c482-149">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="4c482-150">-RemoveOutput</span></span>
<span data-ttu-id="4c482-151">O sinalizador para indicar se deve remover a saída</span><span class="sxs-lookup"><span data-stu-id="4c482-151">The flag to indicate whether to remove output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WithRemoveOutput, WithRemoveOutputUsingParentObject, WithRemoveOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c482-152">-ResourceGroupName</span></span>
<span data-ttu-id="4c482-153">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4c482-153">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c482-154">-ResourceId</span></span>
<span data-ttu-id="4c482-155">A ID do recurso de etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="4c482-155">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithRemoveOutputUsingParentResourceId, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="4c482-156">-RetryAttempts</span></span>
<span data-ttu-id="4c482-157">Os attemps de repetir</span><span class="sxs-lookup"><span data-stu-id="4c482-157">The retry attemps</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="4c482-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="4c482-159">O multiplicador de backoff de intervalo de tentativa</span><span class="sxs-lookup"><span data-stu-id="4c482-159">The retry interval backoff multiplier</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4c482-160">-ServerName</span></span>
<span data-ttu-id="4c482-161">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="4c482-161">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="4c482-162">-StepId</span></span>
<span data-ttu-id="4c482-163">O texto de id de etapa</span><span class="sxs-lookup"><span data-stu-id="4c482-163">The step id text</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="4c482-164">-TargetGroupName</span></span>
<span data-ttu-id="4c482-165">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="4c482-165">The target group name</span></span>

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

### <span data-ttu-id="4c482-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="4c482-166">-TimeoutSeconds</span></span>
<span data-ttu-id="4c482-167">Os segundos de tempo decoro</span><span class="sxs-lookup"><span data-stu-id="4c482-167">The timeout seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c482-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c482-168">-Confirm</span></span>
<span data-ttu-id="4c482-169">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c482-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c482-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c482-170">-WhatIf</span></span>
<span data-ttu-id="4c482-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c482-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c482-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c482-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c482-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c482-173">CommonParameters</span></span>
<span data-ttu-id="4c482-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c482-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c482-175">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c482-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c482-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c482-176">INPUTS</span></span>

### <span data-ttu-id="4c482-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="4c482-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="4c482-178">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4c482-178">OUTPUTS</span></span>

### <span data-ttu-id="4c482-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="4c482-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="4c482-180">NOTES</span><span class="sxs-lookup"><span data-stu-id="4c482-180">NOTES</span></span>

## <span data-ttu-id="4c482-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c482-181">RELATED LINKS</span></span>
