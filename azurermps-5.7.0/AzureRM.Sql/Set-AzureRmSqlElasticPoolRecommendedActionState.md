---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 992dc949ec4c17529415beeeb2cf2a831d4d2a68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428698"
---
# <span data-ttu-id="16089-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="16089-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="16089-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16089-102">SYNOPSIS</span></span>
<span data-ttu-id="16089-103">Atualiza o estado de uma ação recomendada do pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="16089-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16089-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16089-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16089-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16089-105">DESCRIPTION</span></span>
<span data-ttu-id="16089-106">O cmdlet **set-AzureRmSqlElasticPoolRecommendedActionState** atualiza o estado de uma ação recomendada do pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="16089-106">The **Set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="16089-107">Este cmdlet aplica uma ação recomendada, revertida ou descartada com base no novo estado.</span><span class="sxs-lookup"><span data-stu-id="16089-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="16089-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16089-108">EXAMPLES</span></span>

### <span data-ttu-id="16089-109">Exemplo 1: atualizar o estado de uma ação recomendada para pendente</span><span class="sxs-lookup"><span data-stu-id="16089-109">Example 1: Update the state of a recommended action to Pending</span></span>
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

<span data-ttu-id="16089-110">Este comando atualiza o estado da ação recomendada do pool elástico chamado IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 como pendente.</span><span class="sxs-lookup"><span data-stu-id="16089-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="16089-111">OS</span><span class="sxs-lookup"><span data-stu-id="16089-111">PARAMETERS</span></span>

### <span data-ttu-id="16089-112">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="16089-112">-AdvisorName</span></span>
<span data-ttu-id="16089-113">Especifica o nome do supervisor ao qual esta ação recomendada pertence.</span><span class="sxs-lookup"><span data-stu-id="16089-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="16089-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16089-114">-DefaultProfile</span></span>
<span data-ttu-id="16089-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="16089-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16089-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="16089-116">-ElasticPoolName</span></span>
<span data-ttu-id="16089-117">Especifica o nome do pool elástico.</span><span class="sxs-lookup"><span data-stu-id="16089-117">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="16089-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="16089-118">-RecommendedActionName</span></span>
<span data-ttu-id="16089-119">Especifica o nome da ação recomendada para a qual esse cmdlet atualiza o estado.</span><span class="sxs-lookup"><span data-stu-id="16089-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="16089-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16089-120">-ResourceGroupName</span></span>
<span data-ttu-id="16089-121">Especifica o nome do grupo de recursos do servidor que contém esse pool elástico.</span><span class="sxs-lookup"><span data-stu-id="16089-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="16089-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="16089-122">-ServerName</span></span>
<span data-ttu-id="16089-123">Especifica o nome do servidor no qual o pool elástico está.</span><span class="sxs-lookup"><span data-stu-id="16089-123">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="16089-124">-Estado</span><span class="sxs-lookup"><span data-stu-id="16089-124">-State</span></span>
<span data-ttu-id="16089-125">Especifica o valor para o qual esse cmdlet atualiza o estado de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="16089-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="16089-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="16089-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="16089-127">Maneira</span><span class="sxs-lookup"><span data-stu-id="16089-127">Active</span></span>
- <span data-ttu-id="16089-128">Pending</span><span class="sxs-lookup"><span data-stu-id="16089-128">Pending</span></span>
- <span data-ttu-id="16089-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="16089-129">PendingRevert</span></span>
- <span data-ttu-id="16089-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="16089-130">RevertCancelled</span></span>
- <span data-ttu-id="16089-131">Aceita</span><span class="sxs-lookup"><span data-stu-id="16089-131">Ignored</span></span>
- <span data-ttu-id="16089-132">Interpretar</span><span class="sxs-lookup"><span data-stu-id="16089-132">Resolved</span></span>

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

### <span data-ttu-id="16089-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="16089-133">-Confirm</span></span>
<span data-ttu-id="16089-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16089-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16089-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16089-135">-WhatIf</span></span>
<span data-ttu-id="16089-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16089-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16089-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16089-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16089-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16089-138">CommonParameters</span></span>
<span data-ttu-id="16089-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16089-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16089-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16089-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16089-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16089-141">INPUTS</span></span>

### <span data-ttu-id="16089-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="16089-142">None</span></span>
<span data-ttu-id="16089-143">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="16089-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16089-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16089-144">OUTPUTS</span></span>

## <span data-ttu-id="16089-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16089-145">NOTES</span></span>
* <span data-ttu-id="16089-146">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="16089-146">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="16089-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16089-147">RELATED LINKS</span></span>

[<span data-ttu-id="16089-148">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="16089-148">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="16089-149">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="16089-149">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="16089-150">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="16089-150">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="16089-151">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="16089-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
