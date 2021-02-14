---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110907"
---
# <span data-ttu-id="058ca-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="058ca-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="058ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="058ca-102">SYNOPSIS</span></span>
<span data-ttu-id="058ca-103">Atualiza uma etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="058ca-103">Updates a job step</span></span>

## <span data-ttu-id="058ca-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="058ca-104">SYNTAX</span></span>

### <span data-ttu-id="058ca-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="058ca-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="058ca-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="058ca-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="058ca-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="058ca-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="058ca-108">Objectset</span><span class="sxs-lookup"><span data-stu-id="058ca-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="058ca-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="058ca-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="058ca-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="058ca-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="058ca-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="058ca-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="058ca-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="058ca-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="058ca-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="058ca-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="058ca-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="058ca-114">DESCRIPTION</span></span>
<span data-ttu-id="058ca-115">O Set-AzSqlElasticJobStep cmdlet atualiza uma etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="058ca-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="058ca-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="058ca-116">EXAMPLES</span></span>

### <span data-ttu-id="058ca-117">Exemplo 1: atualiza o grupo de destino de uma etapa de trabalho para um trabalho</span><span class="sxs-lookup"><span data-stu-id="058ca-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="058ca-118">Exemplo 2: atualiza o script T-SQL de uma etapa de trabalho para um trabalho</span><span class="sxs-lookup"><span data-stu-id="058ca-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="058ca-119">Atualiza uma etapa de trabalho de um trabalho</span><span class="sxs-lookup"><span data-stu-id="058ca-119">Updates a job step from a job</span></span>

### <span data-ttu-id="058ca-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="058ca-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="058ca-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="058ca-121">PARAMETERS</span></span>

### <span data-ttu-id="058ca-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="058ca-122">-AgentName</span></span>
<span data-ttu-id="058ca-123">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="058ca-123">The agent name</span></span>

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

### <span data-ttu-id="058ca-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="058ca-124">-CommandText</span></span>
<span data-ttu-id="058ca-125">O texto do comando</span><span class="sxs-lookup"><span data-stu-id="058ca-125">The command text</span></span>

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

### <span data-ttu-id="058ca-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="058ca-126">-CredentialName</span></span>
<span data-ttu-id="058ca-127">O nome da credencial</span><span class="sxs-lookup"><span data-stu-id="058ca-127">The credential name</span></span>

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

### <span data-ttu-id="058ca-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="058ca-128">-DefaultProfile</span></span>
<span data-ttu-id="058ca-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="058ca-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="058ca-130">-InitialEsryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="058ca-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="058ca-131">O intervalo inicial de tentativa de segundos</span><span class="sxs-lookup"><span data-stu-id="058ca-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="058ca-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="058ca-132">-InputObject</span></span>
<span data-ttu-id="058ca-133">O objeto de etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="058ca-133">The job step object</span></span>

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

### <span data-ttu-id="058ca-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="058ca-134">-JobName</span></span>
<span data-ttu-id="058ca-135">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="058ca-135">The job name</span></span>

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

### <span data-ttu-id="058ca-136">-MaximumEscondsIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="058ca-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="058ca-137">O intervalo máximo de tentar segundos</span><span class="sxs-lookup"><span data-stu-id="058ca-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="058ca-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="058ca-138">-Name</span></span>
<span data-ttu-id="058ca-139">O nome da etapa</span><span class="sxs-lookup"><span data-stu-id="058ca-139">The step name</span></span>

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

### <span data-ttu-id="058ca-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="058ca-140">-OutputCredentialName</span></span>
<span data-ttu-id="058ca-141">O nome da credencial de saída</span><span class="sxs-lookup"><span data-stu-id="058ca-141">The output credential name</span></span>

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

### <span data-ttu-id="058ca-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="058ca-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="058ca-143">O objeto de banco de dados de saída</span><span class="sxs-lookup"><span data-stu-id="058ca-143">The output database object</span></span>

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

### <span data-ttu-id="058ca-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="058ca-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="058ca-145">A ID de recurso de banco de dados de saída</span><span class="sxs-lookup"><span data-stu-id="058ca-145">The output database resource id</span></span>

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

### <span data-ttu-id="058ca-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="058ca-146">-OutputSchemaName</span></span>
<span data-ttu-id="058ca-147">O nome do esquema de saída</span><span class="sxs-lookup"><span data-stu-id="058ca-147">The output schema name</span></span>

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

### <span data-ttu-id="058ca-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="058ca-148">-OutputTableName</span></span>
<span data-ttu-id="058ca-149">O nome da tabela de saída</span><span class="sxs-lookup"><span data-stu-id="058ca-149">The output table name</span></span>

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

### <span data-ttu-id="058ca-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="058ca-150">-RemoveOutput</span></span>
<span data-ttu-id="058ca-151">O sinalizador para indicar se você deve remover a saída</span><span class="sxs-lookup"><span data-stu-id="058ca-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="058ca-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="058ca-152">-ResourceGroupName</span></span>
<span data-ttu-id="058ca-153">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="058ca-153">The resource group name</span></span>

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

### <span data-ttu-id="058ca-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="058ca-154">-ResourceId</span></span>
<span data-ttu-id="058ca-155">A ID do recurso de etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="058ca-155">The job step resource id</span></span>

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

### <span data-ttu-id="058ca-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="058ca-156">-RetryAttempts</span></span>
<span data-ttu-id="058ca-157">Os attemps de tentar novamente</span><span class="sxs-lookup"><span data-stu-id="058ca-157">The retry attemps</span></span>

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

### <span data-ttu-id="058ca-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="058ca-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="058ca-159">O multiplicador de backoff do intervalo de tentativa</span><span class="sxs-lookup"><span data-stu-id="058ca-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="058ca-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="058ca-160">-ServerName</span></span>
<span data-ttu-id="058ca-161">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="058ca-161">The server name</span></span>

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

### <span data-ttu-id="058ca-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="058ca-162">-StepId</span></span>
<span data-ttu-id="058ca-163">O texto de ID da etapa</span><span class="sxs-lookup"><span data-stu-id="058ca-163">The step id text</span></span>

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

### <span data-ttu-id="058ca-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="058ca-164">-TargetGroupName</span></span>
<span data-ttu-id="058ca-165">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="058ca-165">The target group name</span></span>

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

### <span data-ttu-id="058ca-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="058ca-166">-TimeoutSeconds</span></span>
<span data-ttu-id="058ca-167">Os segundos de tempo de tempo</span><span class="sxs-lookup"><span data-stu-id="058ca-167">The timeout seconds</span></span>

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

### <span data-ttu-id="058ca-168">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="058ca-168">-Confirm</span></span>
<span data-ttu-id="058ca-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="058ca-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="058ca-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="058ca-170">-WhatIf</span></span>
<span data-ttu-id="058ca-171">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="058ca-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="058ca-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="058ca-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="058ca-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="058ca-173">CommonParameters</span></span>
<span data-ttu-id="058ca-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="058ca-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="058ca-175">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="058ca-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="058ca-176">Entradas</span><span class="sxs-lookup"><span data-stu-id="058ca-176">INPUTS</span></span>

### <span data-ttu-id="058ca-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticStepModel</span><span class="sxs-lookup"><span data-stu-id="058ca-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="058ca-178">Saídas</span><span class="sxs-lookup"><span data-stu-id="058ca-178">OUTPUTS</span></span>

### <span data-ttu-id="058ca-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticStepModel</span><span class="sxs-lookup"><span data-stu-id="058ca-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="058ca-180">Notas</span><span class="sxs-lookup"><span data-stu-id="058ca-180">NOTES</span></span>

## <span data-ttu-id="058ca-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="058ca-181">RELATED LINKS</span></span>
