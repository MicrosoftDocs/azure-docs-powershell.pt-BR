---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284010"
---
# <span data-ttu-id="1c2dc-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="1c2dc-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="1c2dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c2dc-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2dc-103">Atualiza uma etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="1c2dc-103">Updates a job step</span></span>

## <span data-ttu-id="1c2dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c2dc-104">SYNTAX</span></span>

### <span data-ttu-id="1c2dc-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="1c2dc-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c2dc-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="1c2dc-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c2dc-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="1c2dc-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c2dc-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="1c2dc-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c2dc-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="1c2dc-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c2dc-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="1c2dc-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c2dc-111">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="1c2dc-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c2dc-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1c2dc-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c2dc-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1c2dc-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c2dc-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c2dc-114">DESCRIPTION</span></span>
<span data-ttu-id="1c2dc-115">O cmdlet Set-AzSqlElasticJobStep atualiza uma etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="1c2dc-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="1c2dc-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c2dc-116">EXAMPLES</span></span>

### <span data-ttu-id="1c2dc-117">Exemplo 1: atualiza o grupo de destino de uma etapa de trabalho para um trabalho</span><span class="sxs-lookup"><span data-stu-id="1c2dc-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="1c2dc-118">Exemplo 2: atualiza um script T-SQL de etapa do trabalho para um trabalho</span><span class="sxs-lookup"><span data-stu-id="1c2dc-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="1c2dc-119">Atualiza uma etapa de trabalho a partir de um trabalho</span><span class="sxs-lookup"><span data-stu-id="1c2dc-119">Updates a job step from a job</span></span>

### <span data-ttu-id="1c2dc-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1c2dc-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="1c2dc-121">OS</span><span class="sxs-lookup"><span data-stu-id="1c2dc-121">PARAMETERS</span></span>

### <span data-ttu-id="1c2dc-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="1c2dc-122">-AgentName</span></span>
<span data-ttu-id="1c2dc-123">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="1c2dc-123">The agent name</span></span>

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

### <span data-ttu-id="1c2dc-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="1c2dc-124">-CommandText</span></span>
<span data-ttu-id="1c2dc-125">O texto do comando</span><span class="sxs-lookup"><span data-stu-id="1c2dc-125">The command text</span></span>

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

### <span data-ttu-id="1c2dc-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="1c2dc-126">-CredentialName</span></span>
<span data-ttu-id="1c2dc-127">O nome da credencial</span><span class="sxs-lookup"><span data-stu-id="1c2dc-127">The credential name</span></span>

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

### <span data-ttu-id="1c2dc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2dc-128">-DefaultProfile</span></span>
<span data-ttu-id="1c2dc-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c2dc-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c2dc-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="1c2dc-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="1c2dc-131">O intervalo inicial de segundos de repetição</span><span class="sxs-lookup"><span data-stu-id="1c2dc-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="1c2dc-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c2dc-132">-InputObject</span></span>
<span data-ttu-id="1c2dc-133">O objeto da etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="1c2dc-133">The job step object</span></span>

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

### <span data-ttu-id="1c2dc-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="1c2dc-134">-JobName</span></span>
<span data-ttu-id="1c2dc-135">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="1c2dc-135">The job name</span></span>

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

### <span data-ttu-id="1c2dc-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="1c2dc-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="1c2dc-137">O intervalo de repetição máximo de segundos</span><span class="sxs-lookup"><span data-stu-id="1c2dc-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="1c2dc-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c2dc-138">-Name</span></span>
<span data-ttu-id="1c2dc-139">O nome da etapa</span><span class="sxs-lookup"><span data-stu-id="1c2dc-139">The step name</span></span>

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

### <span data-ttu-id="1c2dc-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="1c2dc-140">-OutputCredentialName</span></span>
<span data-ttu-id="1c2dc-141">O nome da credencial de saída</span><span class="sxs-lookup"><span data-stu-id="1c2dc-141">The output credential name</span></span>

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

### <span data-ttu-id="1c2dc-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="1c2dc-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="1c2dc-143">O objeto de banco de dados de saída</span><span class="sxs-lookup"><span data-stu-id="1c2dc-143">The output database object</span></span>

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

### <span data-ttu-id="1c2dc-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="1c2dc-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="1c2dc-145">A ID do recurso de banco de dados de saída</span><span class="sxs-lookup"><span data-stu-id="1c2dc-145">The output database resource id</span></span>

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

### <span data-ttu-id="1c2dc-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="1c2dc-146">-OutputSchemaName</span></span>
<span data-ttu-id="1c2dc-147">O nome do esquema de saída</span><span class="sxs-lookup"><span data-stu-id="1c2dc-147">The output schema name</span></span>

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

### <span data-ttu-id="1c2dc-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="1c2dc-148">-OutputTableName</span></span>
<span data-ttu-id="1c2dc-149">O nome da tabela de saída</span><span class="sxs-lookup"><span data-stu-id="1c2dc-149">The output table name</span></span>

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

### <span data-ttu-id="1c2dc-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="1c2dc-150">-RemoveOutput</span></span>
<span data-ttu-id="1c2dc-151">O sinalizador para indicar se a saída deve ser removida</span><span class="sxs-lookup"><span data-stu-id="1c2dc-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="1c2dc-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c2dc-152">-ResourceGroupName</span></span>
<span data-ttu-id="1c2dc-153">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1c2dc-153">The resource group name</span></span>

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

### <span data-ttu-id="1c2dc-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c2dc-154">-ResourceId</span></span>
<span data-ttu-id="1c2dc-155">A ID do recurso etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="1c2dc-155">The job step resource id</span></span>

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

### <span data-ttu-id="1c2dc-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="1c2dc-156">-RetryAttempts</span></span>
<span data-ttu-id="1c2dc-157">O attemps de repetição</span><span class="sxs-lookup"><span data-stu-id="1c2dc-157">The retry attemps</span></span>

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

### <span data-ttu-id="1c2dc-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="1c2dc-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="1c2dc-159">O multiplicador de retrocesso do intervalo de repetição</span><span class="sxs-lookup"><span data-stu-id="1c2dc-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="1c2dc-160">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="1c2dc-160">-ServerName</span></span>
<span data-ttu-id="1c2dc-161">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="1c2dc-161">The server name</span></span>

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

### <span data-ttu-id="1c2dc-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="1c2dc-162">-StepId</span></span>
<span data-ttu-id="1c2dc-163">O texto da identificação da etapa</span><span class="sxs-lookup"><span data-stu-id="1c2dc-163">The step id text</span></span>

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

### <span data-ttu-id="1c2dc-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="1c2dc-164">-TargetGroupName</span></span>
<span data-ttu-id="1c2dc-165">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="1c2dc-165">The target group name</span></span>

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

### <span data-ttu-id="1c2dc-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="1c2dc-166">-TimeoutSeconds</span></span>
<span data-ttu-id="1c2dc-167">O tempo limite em segundos</span><span class="sxs-lookup"><span data-stu-id="1c2dc-167">The timeout seconds</span></span>

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

### <span data-ttu-id="1c2dc-168">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1c2dc-168">-Confirm</span></span>
<span data-ttu-id="1c2dc-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c2dc-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c2dc-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c2dc-170">-WhatIf</span></span>
<span data-ttu-id="1c2dc-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c2dc-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c2dc-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c2dc-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c2dc-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2dc-173">CommonParameters</span></span>
<span data-ttu-id="1c2dc-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c2dc-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2dc-175">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c2dc-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2dc-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c2dc-176">INPUTS</span></span>

### <span data-ttu-id="1c2dc-177">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="1c2dc-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="1c2dc-178">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c2dc-178">OUTPUTS</span></span>

### <span data-ttu-id="1c2dc-179">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="1c2dc-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="1c2dc-180">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c2dc-180">NOTES</span></span>

## <span data-ttu-id="1c2dc-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c2dc-181">RELATED LINKS</span></span>
