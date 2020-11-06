---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: d31af9321a474c1261b2ed75138696d9f1a45461
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429037"
---
# <span data-ttu-id="c07ee-101">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="c07ee-101">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="c07ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c07ee-102">SYNOPSIS</span></span>
<span data-ttu-id="c07ee-103">Atualiza o estado de uma ação recomendada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c07ee-103">Updates the state of an Azure SQL Database recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c07ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c07ee-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c07ee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c07ee-105">DESCRIPTION</span></span>
<span data-ttu-id="c07ee-106">O cmdlet **set-AzureRmSqlDatabaseRecommendedActionState** atualiza o estado de uma ação recomendada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c07ee-106">The **Set-AzureRmSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="c07ee-107">Isso permite que uma ação recomendada seja aplicada, revertida ou descartada com base no novo estado.</span><span class="sxs-lookup"><span data-stu-id="c07ee-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="c07ee-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c07ee-108">EXAMPLES</span></span>

### <span data-ttu-id="c07ee-109">Exemplo 1: aplicar um estado de ação recomendado para pendente</span><span class="sxs-lookup"><span data-stu-id="c07ee-109">Example 1: Apply a recommended action state to pending</span></span>
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

<span data-ttu-id="c07ee-110">Esse comando atualiza o estado da ação recomendada chamada IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 que pertence ao banco de dados chamado WIRunner para pendente.</span><span class="sxs-lookup"><span data-stu-id="c07ee-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="c07ee-111">OS</span><span class="sxs-lookup"><span data-stu-id="c07ee-111">PARAMETERS</span></span>

### <span data-ttu-id="c07ee-112">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="c07ee-112">-AdvisorName</span></span>
<span data-ttu-id="c07ee-113">Especifica o nome do supervisor ao qual esta ação recomendada pertence.</span><span class="sxs-lookup"><span data-stu-id="c07ee-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="c07ee-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c07ee-114">-DatabaseName</span></span>
<span data-ttu-id="c07ee-115">Especifica o nome do banco de dados para o qual esse cmdlet define o estado de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="c07ee-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="c07ee-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="c07ee-116">-RecommendedActionName</span></span>
<span data-ttu-id="c07ee-117">Especifica o nome da ação recomendada para a qual o estado está sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="c07ee-117">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="c07ee-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c07ee-118">-ResourceGroupName</span></span>
<span data-ttu-id="c07ee-119">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c07ee-119">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="c07ee-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c07ee-120">-ServerName</span></span>
<span data-ttu-id="c07ee-121">Especifica o nome do servidor no qual o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="c07ee-121">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="c07ee-122">-Estado</span><span class="sxs-lookup"><span data-stu-id="c07ee-122">-State</span></span>
<span data-ttu-id="c07ee-123">Especifica o novo valor para o qual esse cmdlet atualiza o estado de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="c07ee-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="c07ee-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c07ee-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c07ee-125">Maneira</span><span class="sxs-lookup"><span data-stu-id="c07ee-125">Active</span></span>
- <span data-ttu-id="c07ee-126">Pending</span><span class="sxs-lookup"><span data-stu-id="c07ee-126">Pending</span></span>
- <span data-ttu-id="c07ee-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="c07ee-127">PendingRevert</span></span>
- <span data-ttu-id="c07ee-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="c07ee-128">RevertCancelled</span></span>
- <span data-ttu-id="c07ee-129">Aceita</span><span class="sxs-lookup"><span data-stu-id="c07ee-129">Ignored</span></span>
- <span data-ttu-id="c07ee-130">Interpretar</span><span class="sxs-lookup"><span data-stu-id="c07ee-130">Resolved</span></span>

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

### <span data-ttu-id="c07ee-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c07ee-131">-Confirm</span></span>
<span data-ttu-id="c07ee-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c07ee-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c07ee-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c07ee-133">-WhatIf</span></span>
<span data-ttu-id="c07ee-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c07ee-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c07ee-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c07ee-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c07ee-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c07ee-136">-DefaultProfile</span></span>
<span data-ttu-id="c07ee-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c07ee-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07ee-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07ee-138">CommonParameters</span></span>
<span data-ttu-id="c07ee-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c07ee-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07ee-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c07ee-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07ee-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c07ee-141">INPUTS</span></span>

## <span data-ttu-id="c07ee-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c07ee-142">OUTPUTS</span></span>

### <span data-ttu-id="c07ee-143">Microsoft. Azure. Commands. Sql. Recomendadoaction. Model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="c07ee-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="c07ee-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c07ee-144">NOTES</span></span>
* <span data-ttu-id="c07ee-145">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="c07ee-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="c07ee-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c07ee-146">RELATED LINKS</span></span>

[<span data-ttu-id="c07ee-147">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="c07ee-147">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="c07ee-148">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="c07ee-148">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="c07ee-149">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="c07ee-149">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="c07ee-150">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="c07ee-150">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="c07ee-151">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="c07ee-151">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="c07ee-152">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c07ee-152">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="c07ee-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="c07ee-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="c07ee-154">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="c07ee-154">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="c07ee-155">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c07ee-155">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="c07ee-156">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c07ee-156">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="c07ee-157">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="c07ee-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
