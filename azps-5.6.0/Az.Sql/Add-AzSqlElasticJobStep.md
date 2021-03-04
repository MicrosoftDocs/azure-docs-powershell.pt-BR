---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 41314cb2a65912e2973e91b27036fc099d2cbca6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886578"
---
# <span data-ttu-id="c52a8-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="c52a8-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="c52a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c52a8-102">SYNOPSIS</span></span>
<span data-ttu-id="c52a8-103">Adiciona uma etapa de trabalho a um trabalho</span><span class="sxs-lookup"><span data-stu-id="c52a8-103">Adds a job step to a job</span></span>

## <span data-ttu-id="c52a8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c52a8-104">SYNTAX</span></span>

### <span data-ttu-id="c52a8-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c52a8-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c52a8-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="c52a8-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c52a8-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="c52a8-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c52a8-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c52a8-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c52a8-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c52a8-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c52a8-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c52a8-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c52a8-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c52a8-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c52a8-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c52a8-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c52a8-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c52a8-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c52a8-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c52a8-114">DESCRIPTION</span></span>
<span data-ttu-id="c52a8-115">O Add-AzSqlElasticJobStep cmdlet adiciona uma etapa de trabalho a um trabalho</span><span class="sxs-lookup"><span data-stu-id="c52a8-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="c52a8-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c52a8-116">EXAMPLES</span></span>

### <span data-ttu-id="c52a8-117">Exemplo 1: adiciona uma etapa a um trabalho</span><span class="sxs-lookup"><span data-stu-id="c52a8-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="c52a8-118">Adiciona uma etapa de trabalho a um trabalho</span><span class="sxs-lookup"><span data-stu-id="c52a8-118">Adds a job step to a job</span></span>

## <span data-ttu-id="c52a8-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c52a8-119">PARAMETERS</span></span>

### <span data-ttu-id="c52a8-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c52a8-120">-AgentName</span></span>
<span data-ttu-id="c52a8-121">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="c52a8-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="c52a8-122">-CommandText</span></span>
<span data-ttu-id="c52a8-123">O texto do comando</span><span class="sxs-lookup"><span data-stu-id="c52a8-123">The command text</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="c52a8-124">-CredentialName</span></span>
<span data-ttu-id="c52a8-125">O nome da credencial</span><span class="sxs-lookup"><span data-stu-id="c52a8-125">The credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c52a8-126">-DefaultProfile</span></span>
<span data-ttu-id="c52a8-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c52a8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c52a8-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="c52a8-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="c52a8-129">Os segundos iniciais de intervalo de repetir</span><span class="sxs-lookup"><span data-stu-id="c52a8-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="c52a8-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="c52a8-130">-JobName</span></span>
<span data-ttu-id="c52a8-131">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="c52a8-131">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="c52a8-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="c52a8-133">O intervalo máximo de repetir segundos</span><span class="sxs-lookup"><span data-stu-id="c52a8-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="c52a8-134">-Name</span><span class="sxs-lookup"><span data-stu-id="c52a8-134">-Name</span></span>
<span data-ttu-id="c52a8-135">O nome da etapa de trabalho</span><span class="sxs-lookup"><span data-stu-id="c52a8-135">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="c52a8-136">-OutputCredentialName</span></span>
<span data-ttu-id="c52a8-137">O nome da credencial de saída</span><span class="sxs-lookup"><span data-stu-id="c52a8-137">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c52a8-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="c52a8-139">O objeto de banco de dados de saída</span><span class="sxs-lookup"><span data-stu-id="c52a8-139">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: WithOutputDb, WithOutputDbUsingParentObject, WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="c52a8-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="c52a8-141">A ID do recurso de banco de dados de saída</span><span class="sxs-lookup"><span data-stu-id="c52a8-141">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDbId, WithOutputDbIdUsingParentObject, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="c52a8-142">-OutputSchemaName</span></span>
<span data-ttu-id="c52a8-143">O nome do esquema de saída</span><span class="sxs-lookup"><span data-stu-id="c52a8-143">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="c52a8-144">-OutputTableName</span></span>
<span data-ttu-id="c52a8-145">O nome da tabela de saída</span><span class="sxs-lookup"><span data-stu-id="c52a8-145">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c52a8-146">-ParentObject</span></span>
<span data-ttu-id="c52a8-147">O objeto job</span><span class="sxs-lookup"><span data-stu-id="c52a8-147">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c52a8-148">-ParentResourceId</span></span>
<span data-ttu-id="c52a8-149">A ID do recurso de trabalho</span><span class="sxs-lookup"><span data-stu-id="c52a8-149">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c52a8-150">-ResourceGroupName</span></span>
<span data-ttu-id="c52a8-151">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c52a8-151">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="c52a8-152">-RetryAttempts</span></span>
<span data-ttu-id="c52a8-153">As tentativas de repetir</span><span class="sxs-lookup"><span data-stu-id="c52a8-153">The retry attempts</span></span>

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

### <span data-ttu-id="c52a8-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="c52a8-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="c52a8-155">O intervalo de tentativa de retorno do multiplicador</span><span class="sxs-lookup"><span data-stu-id="c52a8-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="c52a8-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c52a8-156">-ServerName</span></span>
<span data-ttu-id="c52a8-157">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="c52a8-157">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="c52a8-158">-StepId</span></span>
<span data-ttu-id="c52a8-159">A id da etapa</span><span class="sxs-lookup"><span data-stu-id="c52a8-159">The step id</span></span>

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

### <span data-ttu-id="c52a8-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="c52a8-160">-TargetGroupName</span></span>
<span data-ttu-id="c52a8-161">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="c52a8-161">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId, ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, ResourceIdSet, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a8-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="c52a8-162">-TimeoutSeconds</span></span>
<span data-ttu-id="c52a8-163">Os segundos de tempo de tempo</span><span class="sxs-lookup"><span data-stu-id="c52a8-163">The time out seconds</span></span>

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

### <span data-ttu-id="c52a8-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c52a8-164">-Confirm</span></span>
<span data-ttu-id="c52a8-165">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c52a8-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c52a8-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c52a8-166">-WhatIf</span></span>
<span data-ttu-id="c52a8-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c52a8-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c52a8-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c52a8-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c52a8-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c52a8-169">CommonParameters</span></span>
<span data-ttu-id="c52a8-170">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c52a8-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c52a8-171">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c52a8-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c52a8-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c52a8-172">INPUTS</span></span>

### <span data-ttu-id="c52a8-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="c52a8-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="c52a8-174">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c52a8-174">OUTPUTS</span></span>

### <span data-ttu-id="c52a8-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="c52a8-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="c52a8-176">NOTES</span><span class="sxs-lookup"><span data-stu-id="c52a8-176">NOTES</span></span>

## <span data-ttu-id="c52a8-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c52a8-177">RELATED LINKS</span></span>
