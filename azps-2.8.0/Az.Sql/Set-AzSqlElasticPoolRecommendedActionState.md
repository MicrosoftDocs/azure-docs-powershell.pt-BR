---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 83785af7dc0c7bcb7286fd9c0d5a463ade5f9bf8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773712"
---
# <span data-ttu-id="9cb2d-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="9cb2d-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="9cb2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9cb2d-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb2d-103">Atualiza o estado de uma ação recomendada do pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="9cb2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9cb2d-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cb2d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9cb2d-105">DESCRIPTION</span></span>
<span data-ttu-id="9cb2d-106">O cmdlet **set-AzSqlElasticPoolRecommendedActionState** atualiza o estado de uma ação recomendada do pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="9cb2d-107">Este cmdlet aplica uma ação recomendada, revertida ou descartada com base no novo estado.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="9cb2d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9cb2d-108">EXAMPLES</span></span>

### <span data-ttu-id="9cb2d-109">Exemplo 1: atualizar o estado de uma ação recomendada para pendente</span><span class="sxs-lookup"><span data-stu-id="9cb2d-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
ElasticPoolName            : WIRunnerPool
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

<span data-ttu-id="9cb2d-110">Este comando atualiza o estado da ação recomendada do pool elástico chamado IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 como pendente.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="9cb2d-111">OS</span><span class="sxs-lookup"><span data-stu-id="9cb2d-111">PARAMETERS</span></span>

### <span data-ttu-id="9cb2d-112">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="9cb2d-112">-AdvisorName</span></span>
<span data-ttu-id="9cb2d-113">Especifica o nome do supervisor ao qual esta ação recomendada pertence.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="9cb2d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb2d-114">-DefaultProfile</span></span>
<span data-ttu-id="9cb2d-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9cb2d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cb2d-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9cb2d-116">-ElasticPoolName</span></span>
<span data-ttu-id="9cb2d-117">Especifica o nome do pool elástico.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-117">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="9cb2d-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="9cb2d-118">-RecommendedActionName</span></span>
<span data-ttu-id="9cb2d-119">Especifica o nome da ação recomendada para a qual esse cmdlet atualiza o estado.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="9cb2d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb2d-120">-ResourceGroupName</span></span>
<span data-ttu-id="9cb2d-121">Especifica o nome do grupo de recursos do servidor que contém esse pool elástico.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="9cb2d-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="9cb2d-122">-ServerName</span></span>
<span data-ttu-id="9cb2d-123">Especifica o nome do servidor no qual o pool elástico está.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-123">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="9cb2d-124">-Estado</span><span class="sxs-lookup"><span data-stu-id="9cb2d-124">-State</span></span>
<span data-ttu-id="9cb2d-125">Especifica o valor para o qual esse cmdlet atualiza o estado de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="9cb2d-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9cb2d-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9cb2d-127">Maneira</span><span class="sxs-lookup"><span data-stu-id="9cb2d-127">Active</span></span>
- <span data-ttu-id="9cb2d-128">Pending</span><span class="sxs-lookup"><span data-stu-id="9cb2d-128">Pending</span></span>
- <span data-ttu-id="9cb2d-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="9cb2d-129">PendingRevert</span></span>
- <span data-ttu-id="9cb2d-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="9cb2d-130">RevertCancelled</span></span>
- <span data-ttu-id="9cb2d-131">Aceita</span><span class="sxs-lookup"><span data-stu-id="9cb2d-131">Ignored</span></span>
- <span data-ttu-id="9cb2d-132">Interpretar</span><span class="sxs-lookup"><span data-stu-id="9cb2d-132">Resolved</span></span>

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

### <span data-ttu-id="9cb2d-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9cb2d-133">-Confirm</span></span>
<span data-ttu-id="9cb2d-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb2d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb2d-135">-WhatIf</span></span>
<span data-ttu-id="9cb2d-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cb2d-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb2d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb2d-138">CommonParameters</span></span>
<span data-ttu-id="9cb2d-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cb2d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb2d-140">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cb2d-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb2d-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9cb2d-141">INPUTS</span></span>

### <span data-ttu-id="9cb2d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9cb2d-142">System.String</span></span>

### <span data-ttu-id="9cb2d-143">Microsoft. Azure. Commands. Sql. Recomendadoaction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="9cb2d-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="9cb2d-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9cb2d-144">OUTPUTS</span></span>

### <span data-ttu-id="9cb2d-145">Microsoft. Azure. Commands. Sql. Recomendadoaction. Model. AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="9cb2d-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="9cb2d-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9cb2d-146">NOTES</span></span>
* <span data-ttu-id="9cb2d-147">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="9cb2d-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="9cb2d-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9cb2d-148">RELATED LINKS</span></span>

[<span data-ttu-id="9cb2d-149">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="9cb2d-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="9cb2d-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="9cb2d-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="9cb2d-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="9cb2d-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="9cb2d-152">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="9cb2d-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)