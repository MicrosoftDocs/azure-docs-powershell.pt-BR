---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 7e1c03b176974c85802451980df24f5a7fdf9b1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773768"
---
# <span data-ttu-id="066a3-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="066a3-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="066a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="066a3-102">SYNOPSIS</span></span>
<span data-ttu-id="066a3-103">Atualiza uma etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="066a3-103">Updates a job step</span></span>

## <span data-ttu-id="066a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="066a3-104">SYNTAX</span></span>

### <span data-ttu-id="066a3-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="066a3-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="066a3-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="066a3-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="066a3-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="066a3-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="066a3-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="066a3-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="066a3-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="066a3-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="066a3-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="066a3-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="066a3-111">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="066a3-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="066a3-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="066a3-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="066a3-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="066a3-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="066a3-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="066a3-114">DESCRIPTION</span></span>
<span data-ttu-id="066a3-115">O cmdlet Set-AzSqlElasticJobStep atualiza uma etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="066a3-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="066a3-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="066a3-116">EXAMPLES</span></span>

### <span data-ttu-id="066a3-117">Exemplo 1-atualiza o grupo de destino de uma etapa de trabalho para um trabalho</span><span class="sxs-lookup"><span data-stu-id="066a3-117">Example 1 - Updates a job step's target group for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="066a3-118">Exemplo 2-atualiza um script T-SQL de etapa do trabalho para um trabalho</span><span class="sxs-lookup"><span data-stu-id="066a3-118">Example 2 - Updates a job step's T-SQL script for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="066a3-119">Atualiza uma etapa de trabalho a partir de um trabalho</span><span class="sxs-lookup"><span data-stu-id="066a3-119">Updates a job step from a job</span></span>

## <span data-ttu-id="066a3-120">OS</span><span class="sxs-lookup"><span data-stu-id="066a3-120">PARAMETERS</span></span>

### <span data-ttu-id="066a3-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="066a3-121">-AgentName</span></span>
<span data-ttu-id="066a3-122">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="066a3-122">The agent name</span></span>

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

### <span data-ttu-id="066a3-123">-CommandText</span><span class="sxs-lookup"><span data-stu-id="066a3-123">-CommandText</span></span>
<span data-ttu-id="066a3-124">O texto do comando</span><span class="sxs-lookup"><span data-stu-id="066a3-124">The command text</span></span>

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

### <span data-ttu-id="066a3-125">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="066a3-125">-CredentialName</span></span>
<span data-ttu-id="066a3-126">O nome da credencial</span><span class="sxs-lookup"><span data-stu-id="066a3-126">The credential name</span></span>

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

### <span data-ttu-id="066a3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="066a3-127">-DefaultProfile</span></span>
<span data-ttu-id="066a3-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="066a3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="066a3-129">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="066a3-129">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="066a3-130">O intervalo inicial de segundos de repetição</span><span class="sxs-lookup"><span data-stu-id="066a3-130">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="066a3-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="066a3-131">-InputObject</span></span>
<span data-ttu-id="066a3-132">O objeto da etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="066a3-132">The job step object</span></span>

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

### <span data-ttu-id="066a3-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="066a3-133">-JobName</span></span>
<span data-ttu-id="066a3-134">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="066a3-134">The job name</span></span>

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

### <span data-ttu-id="066a3-135">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="066a3-135">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="066a3-136">O intervalo de repetição máximo de segundos</span><span class="sxs-lookup"><span data-stu-id="066a3-136">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="066a3-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="066a3-137">-Name</span></span>
<span data-ttu-id="066a3-138">O nome da etapa</span><span class="sxs-lookup"><span data-stu-id="066a3-138">The step name</span></span>

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

### <span data-ttu-id="066a3-139">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="066a3-139">-OutputCredentialName</span></span>
<span data-ttu-id="066a3-140">O nome da credencial de saída</span><span class="sxs-lookup"><span data-stu-id="066a3-140">The output credential name</span></span>

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

### <span data-ttu-id="066a3-141">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="066a3-141">-OutputDatabaseObject</span></span>
<span data-ttu-id="066a3-142">O objeto de banco de dados de saída</span><span class="sxs-lookup"><span data-stu-id="066a3-142">The output database object</span></span>

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

### <span data-ttu-id="066a3-143">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="066a3-143">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="066a3-144">A ID do recurso de banco de dados de saída</span><span class="sxs-lookup"><span data-stu-id="066a3-144">The output database resource id</span></span>

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

### <span data-ttu-id="066a3-145">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="066a3-145">-OutputSchemaName</span></span>
<span data-ttu-id="066a3-146">O nome do esquema de saída</span><span class="sxs-lookup"><span data-stu-id="066a3-146">The output schema name</span></span>

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

### <span data-ttu-id="066a3-147">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="066a3-147">-OutputTableName</span></span>
<span data-ttu-id="066a3-148">O nome da tabela de saída</span><span class="sxs-lookup"><span data-stu-id="066a3-148">The output table name</span></span>

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

### <span data-ttu-id="066a3-149">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="066a3-149">-RemoveOutput</span></span>
<span data-ttu-id="066a3-150">O sinalizador para indicar se a saída deve ser removida</span><span class="sxs-lookup"><span data-stu-id="066a3-150">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="066a3-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="066a3-151">-ResourceGroupName</span></span>
<span data-ttu-id="066a3-152">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="066a3-152">The resource group name</span></span>

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

### <span data-ttu-id="066a3-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="066a3-153">-ResourceId</span></span>
<span data-ttu-id="066a3-154">A ID do recurso etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="066a3-154">The job step resource id</span></span>

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

### <span data-ttu-id="066a3-155">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="066a3-155">-RetryAttempts</span></span>
<span data-ttu-id="066a3-156">O attemps de repetição</span><span class="sxs-lookup"><span data-stu-id="066a3-156">The retry attemps</span></span>

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

### <span data-ttu-id="066a3-157">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="066a3-157">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="066a3-158">O multiplicador de retrocesso do intervalo de repetição</span><span class="sxs-lookup"><span data-stu-id="066a3-158">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="066a3-159">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="066a3-159">-ServerName</span></span>
<span data-ttu-id="066a3-160">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="066a3-160">The server name</span></span>

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

### <span data-ttu-id="066a3-161">-StepId</span><span class="sxs-lookup"><span data-stu-id="066a3-161">-StepId</span></span>
<span data-ttu-id="066a3-162">O texto da identificação da etapa</span><span class="sxs-lookup"><span data-stu-id="066a3-162">The step id text</span></span>

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

### <span data-ttu-id="066a3-163">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="066a3-163">-TargetGroupName</span></span>
<span data-ttu-id="066a3-164">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="066a3-164">The target group name</span></span>

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

### <span data-ttu-id="066a3-165">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="066a3-165">-TimeoutSeconds</span></span>
<span data-ttu-id="066a3-166">O tempo limite em segundos</span><span class="sxs-lookup"><span data-stu-id="066a3-166">The timeout seconds</span></span>

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

### <span data-ttu-id="066a3-167">-Confirme</span><span class="sxs-lookup"><span data-stu-id="066a3-167">-Confirm</span></span>
<span data-ttu-id="066a3-168">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="066a3-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="066a3-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="066a3-169">-WhatIf</span></span>
<span data-ttu-id="066a3-170">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="066a3-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="066a3-171">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="066a3-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="066a3-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066a3-172">CommonParameters</span></span>
<span data-ttu-id="066a3-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="066a3-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066a3-174">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="066a3-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066a3-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="066a3-175">INPUTS</span></span>

### <span data-ttu-id="066a3-176">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="066a3-176">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="066a3-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="066a3-177">OUTPUTS</span></span>

### <span data-ttu-id="066a3-178">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="066a3-178">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="066a3-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="066a3-179">NOTES</span></span>

## <span data-ttu-id="066a3-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="066a3-180">RELATED LINKS</span></span>
