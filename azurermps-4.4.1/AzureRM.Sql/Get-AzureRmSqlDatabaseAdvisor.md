---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
ms.openlocfilehash: bc66e944a71cdd354bd102969ed2914c496bcfe8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440543"
---
# <span data-ttu-id="fade1-101">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="fade1-101">Get-AzureRmSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="fade1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fade1-102">SYNOPSIS</span></span>
<span data-ttu-id="fade1-103">Obtém um ou mais conselheiros para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fade1-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fade1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fade1-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fade1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fade1-105">DESCRIPTION</span></span>
<span data-ttu-id="fade1-106">O cmdlet **Get-AzureRmSqlDatabaseAdvisor** Obtém um ou mais consultores de banco de dados SQL do Azure para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fade1-106">The **Get-AzureRmSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="fade1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fade1-107">EXAMPLES</span></span>

### <span data-ttu-id="fade1-108">Exemplo 1: listar todos os conselheiros para o banco de dados especificado</span><span class="sxs-lookup"><span data-stu-id="fade1-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
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

<span data-ttu-id="fade1-109">Esse comando obtém todos os conselheiros do banco de dados denominado WIRunner que pertencem ao servidor chamado Wi-Runner-Austrália-leste.</span><span class="sxs-lookup"><span data-stu-id="fade1-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="fade1-110">Exemplo 2: obter um único supervisor para o banco de dados especificado</span><span class="sxs-lookup"><span data-stu-id="fade1-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

<span data-ttu-id="fade1-111">Esse comando obtém o supervisor chamado CreateIndex para o banco de dados chamado WIRunner.</span><span class="sxs-lookup"><span data-stu-id="fade1-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="fade1-112">Exemplo 3: listar todos os conselheiros com as ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="fade1-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
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

<span data-ttu-id="fade1-113">Esse comando obtém todos os conselheiros para o banco de dados chamado ' WIRunner ' com as ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="fade1-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="fade1-114">Como o comando usa o parâmetro *ExpandRecommendedActions* , o cmdlet obtém as ações recomendadas com a resposta.</span><span class="sxs-lookup"><span data-stu-id="fade1-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="fade1-115">Exemplo 4: obter um único conselheiro com as ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="fade1-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="fade1-116">Esse comando obtém o supervisor chamado CreateIndex do banco de dados chamado WIRunner com suas ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="fade1-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="fade1-117">Como o comando usa o parâmetro *ExpandRecommendedActions* , o cmdlet obtém as ações recomendadas com a resposta.</span><span class="sxs-lookup"><span data-stu-id="fade1-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

## <span data-ttu-id="fade1-118">OS</span><span class="sxs-lookup"><span data-stu-id="fade1-118">PARAMETERS</span></span>

### <span data-ttu-id="fade1-119">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="fade1-119">-AdvisorName</span></span>
<span data-ttu-id="fade1-120">Especifica o nome do supervisor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="fade1-120">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fade1-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fade1-121">-DatabaseName</span></span>
<span data-ttu-id="fade1-122">Especifica o nome do banco de dados para o qual esse cmdlet solicita o supervisor.</span><span class="sxs-lookup"><span data-stu-id="fade1-122">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="fade1-123">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="fade1-123">-ExpandRecommendedActions</span></span>
<span data-ttu-id="fade1-124">Indica que esse cmdlet obtém as ações recomendadas com a resposta.</span><span class="sxs-lookup"><span data-stu-id="fade1-124">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="fade1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fade1-125">-ResourceGroupName</span></span>
<span data-ttu-id="fade1-126">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fade1-126">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="fade1-127">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="fade1-127">-ServerName</span></span>
<span data-ttu-id="fade1-128">Especifica o nome do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fade1-128">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="fade1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fade1-129">-DefaultProfile</span></span>
<span data-ttu-id="fade1-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fade1-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fade1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fade1-131">CommonParameters</span></span>
<span data-ttu-id="fade1-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fade1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fade1-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fade1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fade1-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fade1-134">INPUTS</span></span>

## <span data-ttu-id="fade1-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fade1-135">OUTPUTS</span></span>

### <span data-ttu-id="fade1-136">Microsoft. Azure. Commands. Sql. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="fade1-136">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="fade1-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fade1-137">NOTES</span></span>
* <span data-ttu-id="fade1-138">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="fade1-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="fade1-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fade1-139">RELATED LINKS</span></span>

[<span data-ttu-id="fade1-140">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="fade1-140">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="fade1-141">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="fade1-141">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="fade1-142">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="fade1-142">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="fade1-143">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="fade1-143">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="fade1-144">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="fade1-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
