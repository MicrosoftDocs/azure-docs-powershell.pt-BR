---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: 05bde2ee8a5bbcae941203115c49ff6b9fbc6bae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111368"
---
# <span data-ttu-id="b949b-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="b949b-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="b949b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b949b-102">SYNOPSIS</span></span>
<span data-ttu-id="b949b-103">Obtém um ou mais conselheiros para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b949b-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="b949b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b949b-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b949b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b949b-105">DESCRIPTION</span></span>
<span data-ttu-id="b949b-106">O cmdlet **Get-AzSqlDatabaseAdvisor** Obtém um ou mais consultores de banco de dados SQL do Azure para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b949b-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="b949b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b949b-107">EXAMPLES</span></span>

### <span data-ttu-id="b949b-108">Exemplo 1: listar todos os conselheiros para o banco de dados especificado</span><span class="sxs-lookup"><span data-stu-id="b949b-108">Example 1: List all the advisors for the specified database</span></span>
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

<span data-ttu-id="b949b-109">Esse comando obtém todos os conselheiros do banco de dados denominado WIRunner que pertencem ao servidor chamado Wi-Runner-Austrália-leste.</span><span class="sxs-lookup"><span data-stu-id="b949b-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="b949b-110">Exemplo 2: obter um único supervisor para o banco de dados especificado</span><span class="sxs-lookup"><span data-stu-id="b949b-110">Example 2: Get a single advisor for the specified database</span></span>
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

<span data-ttu-id="b949b-111">Esse comando obtém o supervisor chamado CreateIndex para o banco de dados chamado WIRunner.</span><span class="sxs-lookup"><span data-stu-id="b949b-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="b949b-112">Exemplo 3: listar todos os conselheiros com as ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="b949b-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
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

<span data-ttu-id="b949b-113">Esse comando obtém todos os conselheiros para o banco de dados chamado ' WIRunner ' com as ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="b949b-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="b949b-114">Como o comando usa o parâmetro *ExpandRecommendedActions* , o cmdlet obtém as ações recomendadas com a resposta.</span><span class="sxs-lookup"><span data-stu-id="b949b-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="b949b-115">Exemplo 4: obter um único conselheiro com as ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="b949b-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
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

<span data-ttu-id="b949b-116">Esse comando obtém o supervisor chamado CreateIndex do banco de dados chamado WIRunner com suas ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="b949b-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="b949b-117">Como o comando usa o parâmetro *ExpandRecommendedActions* , o cmdlet obtém as ações recomendadas com a resposta.</span><span class="sxs-lookup"><span data-stu-id="b949b-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="b949b-118">Exemplo 5: listar todos os conselheiros do banco de dados especificado usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="b949b-118">Example 5: List all the advisors for the specified database using filtering</span></span>
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

<span data-ttu-id="b949b-119">Esse comando obtém todos os conselheiros do banco de dados denominado WIRunner que pertencem ao servidor chamado Wi-Runner-Austrália-leste e começa com a letra "d".</span><span class="sxs-lookup"><span data-stu-id="b949b-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="b949b-120">OS</span><span class="sxs-lookup"><span data-stu-id="b949b-120">PARAMETERS</span></span>

### <span data-ttu-id="b949b-121">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="b949b-121">-AdvisorName</span></span>
<span data-ttu-id="b949b-122">Especifica o nome do supervisor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b949b-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b949b-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b949b-123">-DatabaseName</span></span>
<span data-ttu-id="b949b-124">Especifica o nome do banco de dados para o qual esse cmdlet solicita o supervisor.</span><span class="sxs-lookup"><span data-stu-id="b949b-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="b949b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b949b-125">-DefaultProfile</span></span>
<span data-ttu-id="b949b-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b949b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b949b-127">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="b949b-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="b949b-128">Indica que esse cmdlet obtém as ações recomendadas com a resposta.</span><span class="sxs-lookup"><span data-stu-id="b949b-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="b949b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b949b-129">-ResourceGroupName</span></span>
<span data-ttu-id="b949b-130">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b949b-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="b949b-131">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b949b-131">-ServerName</span></span>
<span data-ttu-id="b949b-132">Especifica o nome do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b949b-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="b949b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b949b-133">CommonParameters</span></span>
<span data-ttu-id="b949b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b949b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b949b-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b949b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b949b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b949b-136">INPUTS</span></span>

### <span data-ttu-id="b949b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b949b-137">System.String</span></span>

### <span data-ttu-id="b949b-138">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b949b-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b949b-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b949b-139">OUTPUTS</span></span>

### <span data-ttu-id="b949b-140">Microsoft. Azure. Commands. Sql. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="b949b-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="b949b-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b949b-141">NOTES</span></span>
* <span data-ttu-id="b949b-142">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="b949b-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="b949b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b949b-143">RELATED LINKS</span></span>

[<span data-ttu-id="b949b-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="b949b-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="b949b-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="b949b-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="b949b-146">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b949b-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="b949b-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b949b-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="b949b-148">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b949b-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
