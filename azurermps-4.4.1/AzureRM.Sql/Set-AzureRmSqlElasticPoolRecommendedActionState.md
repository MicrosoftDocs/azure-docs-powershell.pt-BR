---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 1bc5d89a381027bd72697d873308eb85807a6e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609544"
---
# <span data-ttu-id="ee75c-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ee75c-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="ee75c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee75c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee75c-103">Atualiza o estado de uma ação recomendada do pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ee75c-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee75c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee75c-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee75c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee75c-105">DESCRIPTION</span></span>
<span data-ttu-id="ee75c-106">O cmdlet **set-AzureRmSqlElasticPoolRecommendedActionState** atualiza o estado de uma ação recomendada do pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ee75c-106">The **Set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="ee75c-107">Este cmdlet aplica uma ação recomendada, revertida ou descartada com base no novo estado.</span><span class="sxs-lookup"><span data-stu-id="ee75c-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="ee75c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee75c-108">EXAMPLES</span></span>

### <span data-ttu-id="ee75c-109">Exemplo 1: atualizar o estado de uma ação recomendada para pendente</span><span class="sxs-lookup"><span data-stu-id="ee75c-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="ee75c-110">Este comando atualiza o estado da ação recomendada do pool elástico chamado IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 como pendente.</span><span class="sxs-lookup"><span data-stu-id="ee75c-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="ee75c-111">OS</span><span class="sxs-lookup"><span data-stu-id="ee75c-111">PARAMETERS</span></span>

### <span data-ttu-id="ee75c-112">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="ee75c-112">-AdvisorName</span></span>
<span data-ttu-id="ee75c-113">Especifica o nome do supervisor ao qual esta ação recomendada pertence.</span><span class="sxs-lookup"><span data-stu-id="ee75c-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="ee75c-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ee75c-114">-ElasticPoolName</span></span>
<span data-ttu-id="ee75c-115">Especifica o nome do pool elástico.</span><span class="sxs-lookup"><span data-stu-id="ee75c-115">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="ee75c-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="ee75c-116">-RecommendedActionName</span></span>
<span data-ttu-id="ee75c-117">Especifica o nome da ação recomendada para a qual esse cmdlet atualiza o estado.</span><span class="sxs-lookup"><span data-stu-id="ee75c-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="ee75c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee75c-118">-ResourceGroupName</span></span>
<span data-ttu-id="ee75c-119">Especifica o nome do grupo de recursos do servidor que contém esse pool elástico.</span><span class="sxs-lookup"><span data-stu-id="ee75c-119">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="ee75c-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ee75c-120">-ServerName</span></span>
<span data-ttu-id="ee75c-121">Especifica o nome do servidor no qual o pool elástico está.</span><span class="sxs-lookup"><span data-stu-id="ee75c-121">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="ee75c-122">-Estado</span><span class="sxs-lookup"><span data-stu-id="ee75c-122">-State</span></span>
<span data-ttu-id="ee75c-123">Especifica o valor para o qual esse cmdlet atualiza o estado de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="ee75c-123">Specifies the value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="ee75c-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ee75c-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ee75c-125">Maneira</span><span class="sxs-lookup"><span data-stu-id="ee75c-125">Active</span></span>
- <span data-ttu-id="ee75c-126">Pending</span><span class="sxs-lookup"><span data-stu-id="ee75c-126">Pending</span></span>
- <span data-ttu-id="ee75c-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="ee75c-127">PendingRevert</span></span>
- <span data-ttu-id="ee75c-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="ee75c-128">RevertCancelled</span></span>
- <span data-ttu-id="ee75c-129">Aceita</span><span class="sxs-lookup"><span data-stu-id="ee75c-129">Ignored</span></span>
- <span data-ttu-id="ee75c-130">Interpretar</span><span class="sxs-lookup"><span data-stu-id="ee75c-130">Resolved</span></span>

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

### <span data-ttu-id="ee75c-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ee75c-131">-Confirm</span></span>
<span data-ttu-id="ee75c-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee75c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee75c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee75c-133">-WhatIf</span></span>
<span data-ttu-id="ee75c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee75c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee75c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee75c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee75c-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee75c-136">-DefaultProfile</span></span>
<span data-ttu-id="ee75c-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee75c-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee75c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee75c-138">CommonParameters</span></span>
<span data-ttu-id="ee75c-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee75c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee75c-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee75c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee75c-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee75c-141">INPUTS</span></span>

## <span data-ttu-id="ee75c-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee75c-142">OUTPUTS</span></span>

## <span data-ttu-id="ee75c-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee75c-143">NOTES</span></span>
* <span data-ttu-id="ee75c-144">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="ee75c-144">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="ee75c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee75c-145">RELATED LINKS</span></span>

[<span data-ttu-id="ee75c-146">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="ee75c-146">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="ee75c-147">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ee75c-147">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="ee75c-148">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ee75c-148">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="ee75c-149">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ee75c-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
