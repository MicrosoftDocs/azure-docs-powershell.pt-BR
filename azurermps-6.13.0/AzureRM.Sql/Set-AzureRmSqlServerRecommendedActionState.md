---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
ms.openlocfilehash: ec44664db9a0e07d963a8db289b6e91b4e76b13a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429301"
---
# <span data-ttu-id="56022-101">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="56022-101">Set-AzureRmSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="56022-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56022-102">SYNOPSIS</span></span>
<span data-ttu-id="56022-103">Atualiza o estado de uma ação recomendada do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="56022-103">Updates the state of an Azure SQL Server recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56022-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56022-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56022-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56022-105">DESCRIPTION</span></span>
<span data-ttu-id="56022-106">O cmdlet **set-AzureRmSqlServerRecommendedActionState** atualiza o estado de uma ação recomendada do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="56022-106">The **Set-AzureRmSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="56022-107">Esse cmdlet aplica, reverte ou descarta a ação recomendada com base no novo estado.</span><span class="sxs-lookup"><span data-stu-id="56022-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="56022-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56022-108">EXAMPLES</span></span>

### <span data-ttu-id="56022-109">Example1: atualiza o estado da ação recomendada especificada para pendente</span><span class="sxs-lookup"><span data-stu-id="56022-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="56022-110">Atualiza o estado da ação recomendada do servidor chamada "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" para "pendente"</span><span class="sxs-lookup"><span data-stu-id="56022-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="56022-111">OS</span><span class="sxs-lookup"><span data-stu-id="56022-111">PARAMETERS</span></span>

### <span data-ttu-id="56022-112">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="56022-112">-AdvisorName</span></span>
<span data-ttu-id="56022-113">Especifica o nome do supervisor que contém a ação recomendada.</span><span class="sxs-lookup"><span data-stu-id="56022-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="56022-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56022-114">-DefaultProfile</span></span>
<span data-ttu-id="56022-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="56022-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56022-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="56022-116">-RecommendedActionName</span></span>
<span data-ttu-id="56022-117">Especifica o nome da ação recomendada para a qual esse cmdlet atualiza o estado.</span><span class="sxs-lookup"><span data-stu-id="56022-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="56022-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56022-118">-ResourceGroupName</span></span>
<span data-ttu-id="56022-119">Especifica o nome do grupo de recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="56022-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="56022-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="56022-120">-ServerName</span></span>
<span data-ttu-id="56022-121">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="56022-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="56022-122">-Estado</span><span class="sxs-lookup"><span data-stu-id="56022-122">-State</span></span>
<span data-ttu-id="56022-123">Especifica o novo valor para o qual esse cmdlet atualiza o estado de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="56022-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="56022-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="56022-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56022-125">Maneira</span><span class="sxs-lookup"><span data-stu-id="56022-125">Active</span></span>
- <span data-ttu-id="56022-126">Pending</span><span class="sxs-lookup"><span data-stu-id="56022-126">Pending</span></span>
- <span data-ttu-id="56022-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="56022-127">PendingRevert</span></span>
- <span data-ttu-id="56022-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="56022-128">RevertCancelled</span></span>
- <span data-ttu-id="56022-129">Aceita</span><span class="sxs-lookup"><span data-stu-id="56022-129">Ignored</span></span>
- <span data-ttu-id="56022-130">Interpretar</span><span class="sxs-lookup"><span data-stu-id="56022-130">Resolved</span></span>

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

### <span data-ttu-id="56022-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="56022-131">-Confirm</span></span>
<span data-ttu-id="56022-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56022-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56022-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56022-133">-WhatIf</span></span>
<span data-ttu-id="56022-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="56022-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56022-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56022-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56022-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56022-136">CommonParameters</span></span>
<span data-ttu-id="56022-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56022-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56022-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56022-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56022-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56022-139">INPUTS</span></span>

### <span data-ttu-id="56022-140">System. String</span><span class="sxs-lookup"><span data-stu-id="56022-140">System.String</span></span>

### <span data-ttu-id="56022-141">Microsoft. Azure. Commands. Sql. Recomendadoaction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="56022-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="56022-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56022-142">OUTPUTS</span></span>

### <span data-ttu-id="56022-143">Microsoft. Azure. Commands. Sql. Recomendadoaction. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="56022-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="56022-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56022-144">NOTES</span></span>
* <span data-ttu-id="56022-145">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Server, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="56022-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="56022-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56022-146">RELATED LINKS</span></span>

[<span data-ttu-id="56022-147">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="56022-147">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="56022-148">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="56022-148">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="56022-149">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="56022-149">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="56022-150">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="56022-150">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="56022-151">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="56022-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)