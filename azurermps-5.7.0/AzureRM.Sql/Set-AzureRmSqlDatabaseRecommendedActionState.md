---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 91d99188d1a93ff3719d9229961cbb673666c14a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602338"
---
# <span data-ttu-id="ae5f0-101">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ae5f0-101">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="ae5f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae5f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5f0-103">Atualiza o estado de uma ação recomendada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-103">Updates the state of an Azure SQL Database recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae5f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae5f0-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae5f0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae5f0-105">DESCRIPTION</span></span>
<span data-ttu-id="ae5f0-106">O cmdlet **set-AzureRmSqlDatabaseRecommendedActionState** atualiza o estado de uma ação recomendada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-106">The **Set-AzureRmSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="ae5f0-107">Isso permite que uma ação recomendada seja aplicada, revertida ou descartada com base no novo estado.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="ae5f0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae5f0-108">EXAMPLES</span></span>

### <span data-ttu-id="ae5f0-109">Exemplo 1: aplicar um estado de ação recomendado para pendente</span><span class="sxs-lookup"><span data-stu-id="ae5f0-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="ae5f0-110">Esse comando atualiza o estado da ação recomendada chamada IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 que pertence ao banco de dados chamado WIRunner para pendente.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="ae5f0-111">OS</span><span class="sxs-lookup"><span data-stu-id="ae5f0-111">PARAMETERS</span></span>

### <span data-ttu-id="ae5f0-112">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="ae5f0-112">-AdvisorName</span></span>
<span data-ttu-id="ae5f0-113">Especifica o nome do supervisor ao qual esta ação recomendada pertence.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5f0-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae5f0-114">-DatabaseName</span></span>
<span data-ttu-id="ae5f0-115">Especifica o nome do banco de dados para o qual esse cmdlet define o estado de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae5f0-116">-DefaultProfile</span></span>
<span data-ttu-id="ae5f0-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ae5f0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5f0-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="ae5f0-118">-RecommendedActionName</span></span>
<span data-ttu-id="ae5f0-119">Especifica o nome da ação recomendada para a qual o estado está sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-119">Specifies the name of the recommended action for which state is being updated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5f0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae5f0-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae5f0-121">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-121">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5f0-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ae5f0-122">-ServerName</span></span>
<span data-ttu-id="ae5f0-123">Especifica o nome do servidor no qual o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-123">Specifies the name of the server the database is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5f0-124">-Estado</span><span class="sxs-lookup"><span data-stu-id="ae5f0-124">-State</span></span>
<span data-ttu-id="ae5f0-125">Especifica o novo valor para o qual esse cmdlet atualiza o estado de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="ae5f0-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ae5f0-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae5f0-127">Maneira</span><span class="sxs-lookup"><span data-stu-id="ae5f0-127">Active</span></span>
- <span data-ttu-id="ae5f0-128">Pending</span><span class="sxs-lookup"><span data-stu-id="ae5f0-128">Pending</span></span>
- <span data-ttu-id="ae5f0-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="ae5f0-129">PendingRevert</span></span>
- <span data-ttu-id="ae5f0-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="ae5f0-130">RevertCancelled</span></span>
- <span data-ttu-id="ae5f0-131">Aceita</span><span class="sxs-lookup"><span data-stu-id="ae5f0-131">Ignored</span></span>
- <span data-ttu-id="ae5f0-132">Interpretar</span><span class="sxs-lookup"><span data-stu-id="ae5f0-132">Resolved</span></span>

```yaml
Type: RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5f0-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae5f0-133">-Confirm</span></span>
<span data-ttu-id="ae5f0-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5f0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae5f0-135">-WhatIf</span></span>
<span data-ttu-id="ae5f0-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae5f0-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5f0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5f0-138">CommonParameters</span></span>
<span data-ttu-id="ae5f0-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5f0-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae5f0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5f0-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae5f0-141">INPUTS</span></span>

### <span data-ttu-id="ae5f0-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ae5f0-142">None</span></span>
<span data-ttu-id="ae5f0-143">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ae5f0-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae5f0-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae5f0-144">OUTPUTS</span></span>

### <span data-ttu-id="ae5f0-145">Microsoft. Azure. Commands. Sql. Recomendadoaction. Model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="ae5f0-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="ae5f0-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae5f0-146">NOTES</span></span>
* <span data-ttu-id="ae5f0-147">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="ae5f0-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="ae5f0-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae5f0-148">RELATED LINKS</span></span>

[<span data-ttu-id="ae5f0-149">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="ae5f0-149">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="ae5f0-150">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="ae5f0-150">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="ae5f0-151">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="ae5f0-151">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="ae5f0-152">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="ae5f0-152">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="ae5f0-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ae5f0-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="ae5f0-154">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="ae5f0-154">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="ae5f0-155">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ae5f0-155">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="ae5f0-156">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ae5f0-156">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="ae5f0-157">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="ae5f0-157">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="ae5f0-158">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="ae5f0-158">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="ae5f0-159">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ae5f0-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
