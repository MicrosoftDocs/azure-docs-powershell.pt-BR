---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3FC9E586-3962-437E-B89F-BB4EA1FBF403
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendedAction.md
ms.openlocfilehash: 83abaaceffd58ea3e1d6277cc0142bf36deb2cae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258674"
---
# <span data-ttu-id="b35a5-101">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b35a5-101">Get-AzSqlElasticPoolRecommendedAction</span></span>

## <span data-ttu-id="b35a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b35a5-102">SYNOPSIS</span></span>
<span data-ttu-id="b35a5-103">Obtém uma ou mais ações recomendadas para um conselheiro de pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b35a5-103">Gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="b35a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b35a5-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b35a5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b35a5-105">DESCRIPTION</span></span>
<span data-ttu-id="b35a5-106">O cmdlet **Get-AzSqlElasticPoolRecommendedAction** Obtém uma ou mais ações recomendadas para um conselheiro de pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b35a5-106">The **Get-AzSqlElasticPoolRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="b35a5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b35a5-107">EXAMPLES</span></span>

### <span data-ttu-id="b35a5-108">Exemplo 1: listar todas as ações recomendadas para um conselheiro</span><span class="sxs-lookup"><span data-stu-id="b35a5-108">Example 1: List all recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
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

ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.236046_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.236046]]...} 
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
ObservedImpact             : {SpaceChange}
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM

ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.239359_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.239359]]...} 
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
RevertActionDuration       : PT10S
RevertActionInitiatedBy    : System
RevertActionInitiatedTime  : 4/21/2016 3:24:47 PM
RevertActionStartTime      : 4/21/2016 3:24:47 PM
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="b35a5-109">Esse comando obtém uma lista de todas as ações recomendadas do supervisor chamada CreateIndex disponível para o pool elástico chamado WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="b35a5-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="b35a5-110">Exemplo 2: obter uma única ação recomendada para um conselheiro</span><span class="sxs-lookup"><span data-stu-id="b35a5-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
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

<span data-ttu-id="b35a5-111">Esse comando obtém a ação recomendada chamada IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 do conselheiro chamado CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="b35a5-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="b35a5-112">OS</span><span class="sxs-lookup"><span data-stu-id="b35a5-112">PARAMETERS</span></span>

### <span data-ttu-id="b35a5-113">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="b35a5-113">-AdvisorName</span></span>
<span data-ttu-id="b35a5-114">Especifica o nome do supervisor para o qual este cmdlet solicita ações recomendadas.</span><span class="sxs-lookup"><span data-stu-id="b35a5-114">Specifies the name of the advisor for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="b35a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35a5-115">-DefaultProfile</span></span>
<span data-ttu-id="b35a5-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b35a5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b35a5-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b35a5-117">-ElasticPoolName</span></span>
<span data-ttu-id="b35a5-118">Especifica o nome do pool elástico para o qual este cmdlet solicita ações recomendadas.</span><span class="sxs-lookup"><span data-stu-id="b35a5-118">Specifies the name of the elastic pool for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="b35a5-119">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="b35a5-119">-RecommendedActionName</span></span>
<span data-ttu-id="b35a5-120">Especifica o nome da ação recomendada que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b35a5-120">Specifies the name of the recommended action that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b35a5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b35a5-121">-ResourceGroupName</span></span>
<span data-ttu-id="b35a5-122">Especifica o nome do grupo de recursos do servidor que contém esse pool elástico.</span><span class="sxs-lookup"><span data-stu-id="b35a5-122">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="b35a5-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b35a5-123">-ServerName</span></span>
<span data-ttu-id="b35a5-124">Especifica o nome do servidor no qual o pool elástico está.</span><span class="sxs-lookup"><span data-stu-id="b35a5-124">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="b35a5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35a5-125">CommonParameters</span></span>
<span data-ttu-id="b35a5-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b35a5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35a5-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b35a5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35a5-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b35a5-128">INPUTS</span></span>

### <span data-ttu-id="b35a5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b35a5-129">System.String</span></span>

## <span data-ttu-id="b35a5-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b35a5-130">OUTPUTS</span></span>

### <span data-ttu-id="b35a5-131">Microsoft. Azure. Commands. Sql. Recomendadoaction. Model. AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="b35a5-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="b35a5-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b35a5-132">NOTES</span></span>
* <span data-ttu-id="b35a5-133">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="b35a5-133">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="b35a5-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b35a5-134">RELATED LINKS</span></span>

[<span data-ttu-id="b35a5-135">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b35a5-135">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="b35a5-136">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="b35a5-136">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="b35a5-137">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b35a5-137">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="b35a5-138">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b35a5-138">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="b35a5-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b35a5-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
