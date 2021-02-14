---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 6d634760080e3fb26153b747e733369b20bc8336
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117066"
---
# <span data-ttu-id="4ea87-101">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="4ea87-101">Set-AzSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="4ea87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ea87-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea87-103">Atualiza o estado de uma ação recomendada do Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea87-103">Updates the state of an Azure SQL Database recommended action.</span></span>

## <span data-ttu-id="4ea87-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ea87-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ea87-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ea87-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea87-106">O cmdlet **Set-AzSqlDatabaseRecom recommendedActionState** atualiza o estado de uma Ação Recomendada do Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea87-106">The **Set-AzSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="4ea87-107">Isso permite que uma ação recomendada seja aplicada, revertida ou descartada com base no novo estado.</span><span class="sxs-lookup"><span data-stu-id="4ea87-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="4ea87-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4ea87-108">EXAMPLES</span></span>

### <span data-ttu-id="4ea87-109">Exemplo 1: Aplicar um estado de ação recomendado a pendente</span><span class="sxs-lookup"><span data-stu-id="4ea87-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
DatabaseName               : WIRunner

ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="4ea87-110">Este comando atualiza o estado da ação recomendada chamada IR_ \[ test_schema \] _ \[ test_table_0.0361551 _6C7AE8CC9C87E7FD5893 que pertence ao banco de dados chamado WI Wifi para \] Pendente.</span><span class="sxs-lookup"><span data-stu-id="4ea87-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="4ea87-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ea87-111">PARAMETERS</span></span>

### <span data-ttu-id="4ea87-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="4ea87-112">-AdvisorName</span></span>
<span data-ttu-id="4ea87-113">Especifica o nome do consultor ao qual esta ação recomendada pertence.</span><span class="sxs-lookup"><span data-stu-id="4ea87-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea87-114">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="4ea87-114">-DatabaseName</span></span>
<span data-ttu-id="4ea87-115">Especifica o nome do banco de dados para o qual este cmdlet define o estado de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="4ea87-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea87-116">-DefaultProfile</span></span>
<span data-ttu-id="4ea87-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4ea87-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ea87-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="4ea87-118">-RecommendedActionName</span></span>
<span data-ttu-id="4ea87-119">Especifica o nome da ação recomendada para qual estado está sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="4ea87-119">Specifies the name of the recommended action for which state is being updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea87-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea87-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ea87-121">Especifica o nome do grupo de recursos do servidor que contém esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4ea87-121">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea87-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4ea87-122">-ServerName</span></span>
<span data-ttu-id="4ea87-123">Especifica o nome do servidor em que o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="4ea87-123">Specifies the name of the server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea87-124">-Estado</span><span class="sxs-lookup"><span data-stu-id="4ea87-124">-State</span></span>
<span data-ttu-id="4ea87-125">Especifica o novo valor ao qual este cmdlet atualiza o estado de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="4ea87-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="4ea87-126">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4ea87-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ea87-127">Ativo</span><span class="sxs-lookup"><span data-stu-id="4ea87-127">Active</span></span>
- <span data-ttu-id="4ea87-128">Pendente</span><span class="sxs-lookup"><span data-stu-id="4ea87-128">Pending</span></span>
- <span data-ttu-id="4ea87-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="4ea87-129">PendingRevert</span></span>
- <span data-ttu-id="4ea87-130">ReverterCancelled</span><span class="sxs-lookup"><span data-stu-id="4ea87-130">RevertCancelled</span></span>
- <span data-ttu-id="4ea87-131">Ignorado</span><span class="sxs-lookup"><span data-stu-id="4ea87-131">Ignored</span></span>
- <span data-ttu-id="4ea87-132">Resolvido</span><span class="sxs-lookup"><span data-stu-id="4ea87-132">Resolved</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea87-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4ea87-133">-Confirm</span></span>
<span data-ttu-id="4ea87-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ea87-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ea87-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea87-135">-WhatIf</span></span>
<span data-ttu-id="4ea87-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4ea87-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ea87-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ea87-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ea87-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea87-138">CommonParameters</span></span>
<span data-ttu-id="4ea87-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea87-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea87-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ea87-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea87-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="4ea87-141">INPUTS</span></span>

### <span data-ttu-id="4ea87-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4ea87-142">System.String</span></span>

### <span data-ttu-id="4ea87-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="4ea87-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="4ea87-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="4ea87-144">OUTPUTS</span></span>

### <span data-ttu-id="4ea87-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecom recommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="4ea87-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="4ea87-146">Notas</span><span class="sxs-lookup"><span data-stu-id="4ea87-146">NOTES</span></span>
* <span data-ttu-id="4ea87-147">Palavras-chave: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="4ea87-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="4ea87-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ea87-148">RELATED LINKS</span></span>

[<span data-ttu-id="4ea87-149">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="4ea87-149">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="4ea87-150">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="4ea87-150">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="4ea87-151">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="4ea87-151">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="4ea87-152">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="4ea87-152">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="4ea87-153">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="4ea87-153">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="4ea87-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="4ea87-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="4ea87-155">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="4ea87-155">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="4ea87-156">Set-AzSqlServerRecomstate</span><span class="sxs-lookup"><span data-stu-id="4ea87-156">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="4ea87-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="4ea87-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="4ea87-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="4ea87-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="4ea87-159">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4ea87-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
