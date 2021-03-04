---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: b3efbc4fdfcc5869e44d1044648152c22b679639
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889152"
---
# <span data-ttu-id="8c715-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="8c715-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="8c715-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c715-102">SYNOPSIS</span></span>
<span data-ttu-id="8c715-103">Obtém um ou mais Consultores para um Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8c715-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="8c715-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8c715-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c715-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8c715-105">DESCRIPTION</span></span>
<span data-ttu-id="8c715-106">O cmdlet **Get-AzSqlServerAdvisor** obtém um ou mais Consultores do Azure SQL Server para um Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8c715-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="8c715-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c715-107">EXAMPLES</span></span>

### <span data-ttu-id="8c715-108">Exemplo 1: listar todos os consultores do servidor</span><span class="sxs-lookup"><span data-stu-id="8c715-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:01:41 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="8c715-109">Este comando obtém uma lista de todos os consultores do servidor chamado wi-runner-australia-east que pertence ao grupo de recursos chamado WIRunnersProd.</span><span class="sxs-lookup"><span data-stu-id="8c715-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="8c715-110">Exemplo 2: Obter um único consultor para o servidor</span><span class="sxs-lookup"><span data-stu-id="8c715-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="8c715-111">Este comando obtém o consultor chamado CreateIndex para o servidor chamado wi-runner-australia-east.</span><span class="sxs-lookup"><span data-stu-id="8c715-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="8c715-112">Exemplo 3: listar todos os consultores com suas ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="8c715-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...} 

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0288891]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.140264]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.412191]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.442075]_38724E1DCF2178318957...} 

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:04:26 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="8c715-113">Este comando obtém todos os consultores do servidor chamado wi-runner-australia-east.</span><span class="sxs-lookup"><span data-stu-id="8c715-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="8c715-114">Como o comando usa o *parâmetro ExpandRecommendedActions,* o cmdlet obtém as ações recomendadas dos consultores incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="8c715-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="8c715-115">Exemplo 4: obter um único consultor com suas ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="8c715-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...}
```

<span data-ttu-id="8c715-116">Este comando obtém um consultor chamado CreateIndex do servidor chamado wi-runner-australia-east com suas ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="8c715-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="8c715-117">Exemplo 5: listar todos os consultores para o servidor usando filtragem</span><span class="sxs-lookup"><span data-stu-id="8c715-117">Example 5: List all the advisors for the server using filtering</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName d*
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
```

<span data-ttu-id="8c715-118">Este comando obtém uma lista de todos os consultores do servidor chamado wi-runner-australia-east que pertence ao grupo de recursos chamado WIRunnersProd que começam com a letra "d".</span><span class="sxs-lookup"><span data-stu-id="8c715-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="8c715-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8c715-119">PARAMETERS</span></span>

### <span data-ttu-id="8c715-120">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="8c715-120">-AdvisorName</span></span>
<span data-ttu-id="8c715-121">Especifica o nome do consultor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8c715-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8c715-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c715-122">-DefaultProfile</span></span>
<span data-ttu-id="8c715-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8c715-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c715-124">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="8c715-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="8c715-125">Indica que o cmdlet inclui as ações recomendadas dos consultores incluídos na resposta.</span><span class="sxs-lookup"><span data-stu-id="8c715-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c715-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c715-126">-ResourceGroupName</span></span>
<span data-ttu-id="8c715-127">Especifica o nome do grupo de recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="8c715-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="8c715-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8c715-128">-ServerName</span></span>
<span data-ttu-id="8c715-129">Especifica o nome do servidor para o consultor que este cmdlet solicita.</span><span class="sxs-lookup"><span data-stu-id="8c715-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="8c715-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c715-130">CommonParameters</span></span>
<span data-ttu-id="8c715-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c715-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c715-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c715-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c715-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c715-133">INPUTS</span></span>

### <span data-ttu-id="8c715-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8c715-134">System.String</span></span>

### <span data-ttu-id="8c715-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c715-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8c715-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8c715-136">OUTPUTS</span></span>

### <span data-ttu-id="8c715-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="8c715-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="8c715-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="8c715-138">NOTES</span></span>
* <span data-ttu-id="8c715-139">Palavras-chave: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="8c715-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="8c715-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c715-140">RELATED LINKS</span></span>

[<span data-ttu-id="8c715-141">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="8c715-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="8c715-142">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="8c715-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="8c715-143">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="8c715-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="8c715-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="8c715-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="8c715-145">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="8c715-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

