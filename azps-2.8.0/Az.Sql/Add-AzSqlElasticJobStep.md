---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 79b26156ae99bfcdd94671649b403b495377af30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773170"
---
# <span data-ttu-id="ecf0e-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="ecf0e-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="ecf0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ecf0e-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf0e-103">Adiciona uma etapa de trabalho a um trabalho</span><span class="sxs-lookup"><span data-stu-id="ecf0e-103">Adds a job step to a job</span></span>

## <span data-ttu-id="ecf0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecf0e-104">SYNTAX</span></span>

### <span data-ttu-id="ecf0e-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="ecf0e-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf0e-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="ecf0e-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecf0e-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="ecf0e-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecf0e-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ecf0e-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecf0e-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ecf0e-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf0e-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ecf0e-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf0e-111">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="ecf0e-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecf0e-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ecf0e-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf0e-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ecf0e-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf0e-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ecf0e-114">DESCRIPTION</span></span>
<span data-ttu-id="ecf0e-115">O cmdlet Add-AzSqlElasticJobStep adiciona uma etapa de trabalho a um trabalho</span><span class="sxs-lookup"><span data-stu-id="ecf0e-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="ecf0e-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecf0e-116">EXAMPLES</span></span>

### <span data-ttu-id="ecf0e-117">Exemplo 1-adiciona uma etapa a um trabalho</span><span class="sxs-lookup"><span data-stu-id="ecf0e-117">Example 1 - Adds a step to a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="ecf0e-118">Adiciona uma etapa de trabalho a um trabalho</span><span class="sxs-lookup"><span data-stu-id="ecf0e-118">Adds a job step to a job</span></span>

## <span data-ttu-id="ecf0e-119">OS</span><span class="sxs-lookup"><span data-stu-id="ecf0e-119">PARAMETERS</span></span>

### <span data-ttu-id="ecf0e-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ecf0e-120">-AgentName</span></span>
<span data-ttu-id="ecf0e-121">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="ecf0e-121">The agent name</span></span>

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

### <span data-ttu-id="ecf0e-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="ecf0e-122">-CommandText</span></span>
<span data-ttu-id="ecf0e-123">O texto do comando</span><span class="sxs-lookup"><span data-stu-id="ecf0e-123">The command text</span></span>

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

### <span data-ttu-id="ecf0e-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ecf0e-124">-CredentialName</span></span>
<span data-ttu-id="ecf0e-125">O nome da credencial</span><span class="sxs-lookup"><span data-stu-id="ecf0e-125">The credential name</span></span>

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

### <span data-ttu-id="ecf0e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf0e-126">-DefaultProfile</span></span>
<span data-ttu-id="ecf0e-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf0e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecf0e-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="ecf0e-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="ecf0e-129">O intervalo inicial de segundos de repetição</span><span class="sxs-lookup"><span data-stu-id="ecf0e-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="ecf0e-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="ecf0e-130">-JobName</span></span>
<span data-ttu-id="ecf0e-131">O nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="ecf0e-131">The job name</span></span>

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

### <span data-ttu-id="ecf0e-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="ecf0e-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="ecf0e-133">O intervalo de repetição máximo de segundos</span><span class="sxs-lookup"><span data-stu-id="ecf0e-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="ecf0e-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecf0e-134">-Name</span></span>
<span data-ttu-id="ecf0e-135">O nome da etapa do trabalho</span><span class="sxs-lookup"><span data-stu-id="ecf0e-135">The job step name</span></span>

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

### <span data-ttu-id="ecf0e-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="ecf0e-136">-OutputCredentialName</span></span>
<span data-ttu-id="ecf0e-137">O nome da credencial de saída</span><span class="sxs-lookup"><span data-stu-id="ecf0e-137">The output credential name</span></span>

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

### <span data-ttu-id="ecf0e-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ecf0e-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="ecf0e-139">O objeto de banco de dados de saída</span><span class="sxs-lookup"><span data-stu-id="ecf0e-139">The output database object</span></span>

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

### <span data-ttu-id="ecf0e-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="ecf0e-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="ecf0e-141">A ID do recurso de banco de dados de saída</span><span class="sxs-lookup"><span data-stu-id="ecf0e-141">The output database resource id</span></span>

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

### <span data-ttu-id="ecf0e-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="ecf0e-142">-OutputSchemaName</span></span>
<span data-ttu-id="ecf0e-143">O nome do esquema de saída</span><span class="sxs-lookup"><span data-stu-id="ecf0e-143">The output schema name</span></span>

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

### <span data-ttu-id="ecf0e-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="ecf0e-144">-OutputTableName</span></span>
<span data-ttu-id="ecf0e-145">O nome da tabela de saída</span><span class="sxs-lookup"><span data-stu-id="ecf0e-145">The output table name</span></span>

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

### <span data-ttu-id="ecf0e-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ecf0e-146">-ParentObject</span></span>
<span data-ttu-id="ecf0e-147">O objeto de trabalho</span><span class="sxs-lookup"><span data-stu-id="ecf0e-147">The job object</span></span>

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

### <span data-ttu-id="ecf0e-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ecf0e-148">-ParentResourceId</span></span>
<span data-ttu-id="ecf0e-149">A ID do recurso do trabalho</span><span class="sxs-lookup"><span data-stu-id="ecf0e-149">The job resource id</span></span>

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

### <span data-ttu-id="ecf0e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf0e-150">-ResourceGroupName</span></span>
<span data-ttu-id="ecf0e-151">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ecf0e-151">The resource group name</span></span>

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

### <span data-ttu-id="ecf0e-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="ecf0e-152">-RetryAttempts</span></span>
<span data-ttu-id="ecf0e-153">As tentativas de repetição</span><span class="sxs-lookup"><span data-stu-id="ecf0e-153">The retry attempts</span></span>

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

### <span data-ttu-id="ecf0e-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="ecf0e-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="ecf0e-155">O intervalo de repetição desliga o multiplicador</span><span class="sxs-lookup"><span data-stu-id="ecf0e-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="ecf0e-156">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ecf0e-156">-ServerName</span></span>
<span data-ttu-id="ecf0e-157">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="ecf0e-157">The server name</span></span>

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

### <span data-ttu-id="ecf0e-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="ecf0e-158">-StepId</span></span>
<span data-ttu-id="ecf0e-159">A ID da etapa</span><span class="sxs-lookup"><span data-stu-id="ecf0e-159">The step id</span></span>

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

### <span data-ttu-id="ecf0e-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf0e-160">-TargetGroupName</span></span>
<span data-ttu-id="ecf0e-161">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="ecf0e-161">The target group name</span></span>

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

### <span data-ttu-id="ecf0e-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="ecf0e-162">-TimeoutSeconds</span></span>
<span data-ttu-id="ecf0e-163">O tempo limite em segundos</span><span class="sxs-lookup"><span data-stu-id="ecf0e-163">The time out seconds</span></span>

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

### <span data-ttu-id="ecf0e-164">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ecf0e-164">-Confirm</span></span>
<span data-ttu-id="ecf0e-165">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecf0e-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecf0e-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf0e-166">-WhatIf</span></span>
<span data-ttu-id="ecf0e-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ecf0e-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecf0e-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ecf0e-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecf0e-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf0e-169">CommonParameters</span></span>
<span data-ttu-id="ecf0e-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecf0e-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf0e-171">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecf0e-171">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf0e-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ecf0e-172">INPUTS</span></span>

### <span data-ttu-id="ecf0e-173">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="ecf0e-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="ecf0e-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ecf0e-174">OUTPUTS</span></span>

### <span data-ttu-id="ecf0e-175">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="ecf0e-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="ecf0e-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ecf0e-176">NOTES</span></span>

## <span data-ttu-id="ecf0e-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecf0e-177">RELATED LINKS</span></span>
