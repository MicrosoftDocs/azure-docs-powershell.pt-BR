---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: d946b6b324247a46760f762c4631419b6c6aac59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887329"
---
# <span data-ttu-id="9c09a-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="9c09a-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="9c09a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c09a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c09a-103">Obtém um ou mais Consultores para um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9c09a-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="9c09a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9c09a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c09a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9c09a-105">DESCRIPTION</span></span>
<span data-ttu-id="9c09a-106">O cmdlet **Get-AzSqlDatabaseAdvisor** obtém um ou mais Consultores de Banco de Dados do Azure SQL para um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9c09a-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="9c09a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c09a-107">EXAMPLES</span></span>

### <span data-ttu-id="9c09a-108">Exemplo 1: listar todos os consultores do banco de dados especificado</span><span class="sxs-lookup"><span data-stu-id="9c09a-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
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

<span data-ttu-id="9c09a-109">Este comando obtém lista todos os consultores do banco de dados chamado WIRunner que pertence ao servidor chamado wi-runner-australia-east.</span><span class="sxs-lookup"><span data-stu-id="9c09a-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="9c09a-110">Exemplo 2: obter um único consultor para o banco de dados especificado</span><span class="sxs-lookup"><span data-stu-id="9c09a-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
DatabaseName                   : WIRunner
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

<span data-ttu-id="9c09a-111">Este comando obtém o Advisor chamado CreateIndex para o banco de dados chamado WIRunner.</span><span class="sxs-lookup"><span data-stu-id="9c09a-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="9c09a-112">Exemplo 3: listar todos os consultores com suas ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="9c09a-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
DatabaseName                   : WIRunner
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

DatabaseName                   : WIRunner
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

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
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

<span data-ttu-id="9c09a-113">Esse comando obtém todos os consultores do banco de dados chamado 'WIRunner' com suas ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="9c09a-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="9c09a-114">Como o comando usa o *parâmetro ExpandRecommendedActions,* o cmdlet obtém as ações recomendadas com a resposta.</span><span class="sxs-lookup"><span data-stu-id="9c09a-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="9c09a-115">Exemplo 4: obter um único consultor com suas ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="9c09a-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
DatabaseName                   : WIRunner
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

<span data-ttu-id="9c09a-116">Este comando obtém o Advisor chamado CreateIndex do banco de dados chamado WIRunner com suas ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="9c09a-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="9c09a-117">Como o comando usa o *parâmetro ExpandRecommendedActions,* o cmdlet obtém as ações recomendadas com a resposta.</span><span class="sxs-lookup"><span data-stu-id="9c09a-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="9c09a-118">Exemplo 5: listar todos os consultores para o banco de dados especificado usando filtragem</span><span class="sxs-lookup"><span data-stu-id="9c09a-118">Example 5: List all the advisors for the specified database using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName d*
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
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

<span data-ttu-id="9c09a-119">Este comando obtém lista todos os consultores do banco de dados chamado WIRunner que pertence ao servidor chamado wi-runner-australia-east e comece com a letra "d".</span><span class="sxs-lookup"><span data-stu-id="9c09a-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="9c09a-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9c09a-120">PARAMETERS</span></span>

### <span data-ttu-id="9c09a-121">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="9c09a-121">-AdvisorName</span></span>
<span data-ttu-id="9c09a-122">Especifica o nome do consultor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9c09a-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9c09a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9c09a-123">-DatabaseName</span></span>
<span data-ttu-id="9c09a-124">Especifica o nome do banco de dados para o qual este cmdlet solicita o Advisor.</span><span class="sxs-lookup"><span data-stu-id="9c09a-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="9c09a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c09a-125">-DefaultProfile</span></span>
<span data-ttu-id="9c09a-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9c09a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c09a-127">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="9c09a-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="9c09a-128">Indica que esse cmdlet obtém as ações recomendadas com a resposta.</span><span class="sxs-lookup"><span data-stu-id="9c09a-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="9c09a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c09a-129">-ResourceGroupName</span></span>
<span data-ttu-id="9c09a-130">Especifica o nome do grupo de recursos do servidor que contém esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9c09a-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="9c09a-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9c09a-131">-ServerName</span></span>
<span data-ttu-id="9c09a-132">Especifica o nome do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9c09a-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="9c09a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c09a-133">CommonParameters</span></span>
<span data-ttu-id="9c09a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c09a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c09a-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c09a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c09a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c09a-136">INPUTS</span></span>

### <span data-ttu-id="9c09a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9c09a-137">System.String</span></span>

### <span data-ttu-id="9c09a-138">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9c09a-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9c09a-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9c09a-139">OUTPUTS</span></span>

### <span data-ttu-id="9c09a-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="9c09a-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="9c09a-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="9c09a-141">NOTES</span></span>
* <span data-ttu-id="9c09a-142">Palavras-chave: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="9c09a-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="9c09a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c09a-143">RELATED LINKS</span></span>

[<span data-ttu-id="9c09a-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="9c09a-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="9c09a-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="9c09a-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="9c09a-146">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="9c09a-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="9c09a-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="9c09a-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="9c09a-148">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="9c09a-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
