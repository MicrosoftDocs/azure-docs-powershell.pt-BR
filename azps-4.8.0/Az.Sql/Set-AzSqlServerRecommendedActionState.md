---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: 78366f70db7bd586e1e35566f167c7cae2c2dbf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113854"
---
# <span data-ttu-id="323fb-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="323fb-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="323fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="323fb-102">SYNOPSIS</span></span>
<span data-ttu-id="323fb-103">Atualiza o estado de uma ação recomendada do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="323fb-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="323fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="323fb-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="323fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="323fb-105">DESCRIPTION</span></span>
<span data-ttu-id="323fb-106">O cmdlet **set-AzSqlServerRecommendedActionState** atualiza o estado de uma ação recomendada do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="323fb-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="323fb-107">Esse cmdlet aplica, reverte ou descarta a ação recomendada com base no novo estado.</span><span class="sxs-lookup"><span data-stu-id="323fb-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="323fb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="323fb-108">EXAMPLES</span></span>

### <span data-ttu-id="323fb-109">Example1: atualiza o estado da ação recomendada especificada para pendente</span><span class="sxs-lookup"><span data-stu-id="323fb-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="323fb-110">Atualiza o estado da ação recomendada do servidor chamada "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" para "pendente"</span><span class="sxs-lookup"><span data-stu-id="323fb-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="323fb-111">OS</span><span class="sxs-lookup"><span data-stu-id="323fb-111">PARAMETERS</span></span>

### <span data-ttu-id="323fb-112">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="323fb-112">-AdvisorName</span></span>
<span data-ttu-id="323fb-113">Especifica o nome do supervisor que contém a ação recomendada.</span><span class="sxs-lookup"><span data-stu-id="323fb-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="323fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="323fb-114">-DefaultProfile</span></span>
<span data-ttu-id="323fb-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="323fb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="323fb-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="323fb-116">-RecommendedActionName</span></span>
<span data-ttu-id="323fb-117">Especifica o nome da ação recomendada para a qual esse cmdlet atualiza o estado.</span><span class="sxs-lookup"><span data-stu-id="323fb-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="323fb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="323fb-118">-ResourceGroupName</span></span>
<span data-ttu-id="323fb-119">Especifica o nome do grupo de recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="323fb-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="323fb-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="323fb-120">-ServerName</span></span>
<span data-ttu-id="323fb-121">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="323fb-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="323fb-122">-Estado</span><span class="sxs-lookup"><span data-stu-id="323fb-122">-State</span></span>
<span data-ttu-id="323fb-123">Especifica o novo valor para o qual esse cmdlet atualiza o estado de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="323fb-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="323fb-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="323fb-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="323fb-125">Maneira</span><span class="sxs-lookup"><span data-stu-id="323fb-125">Active</span></span>
- <span data-ttu-id="323fb-126">Pending</span><span class="sxs-lookup"><span data-stu-id="323fb-126">Pending</span></span>
- <span data-ttu-id="323fb-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="323fb-127">PendingRevert</span></span>
- <span data-ttu-id="323fb-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="323fb-128">RevertCancelled</span></span>
- <span data-ttu-id="323fb-129">Aceita</span><span class="sxs-lookup"><span data-stu-id="323fb-129">Ignored</span></span>
- <span data-ttu-id="323fb-130">Interpretar</span><span class="sxs-lookup"><span data-stu-id="323fb-130">Resolved</span></span>

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

### <span data-ttu-id="323fb-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="323fb-131">-Confirm</span></span>
<span data-ttu-id="323fb-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="323fb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="323fb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="323fb-133">-WhatIf</span></span>
<span data-ttu-id="323fb-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="323fb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="323fb-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="323fb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="323fb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="323fb-136">CommonParameters</span></span>
<span data-ttu-id="323fb-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="323fb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="323fb-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="323fb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="323fb-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="323fb-139">INPUTS</span></span>

### <span data-ttu-id="323fb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="323fb-140">System.String</span></span>

### <span data-ttu-id="323fb-141">Microsoft. Azure. Commands. Sql. Recomendadoaction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="323fb-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="323fb-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="323fb-142">OUTPUTS</span></span>

### <span data-ttu-id="323fb-143">Microsoft. Azure. Commands. Sql. Recomendadoaction. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="323fb-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="323fb-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="323fb-144">NOTES</span></span>
* <span data-ttu-id="323fb-145">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Server, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="323fb-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="323fb-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="323fb-146">RELATED LINKS</span></span>

[<span data-ttu-id="323fb-147">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="323fb-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="323fb-148">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="323fb-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="323fb-149">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="323fb-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="323fb-150">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="323fb-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="323fb-151">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="323fb-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
