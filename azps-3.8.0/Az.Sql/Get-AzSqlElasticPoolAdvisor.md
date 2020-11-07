---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
ms.openlocfilehash: 3032824d51e7892c21830decbdb1c92d03d7a2e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778427"
---
# <span data-ttu-id="1b7af-101">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="1b7af-101">Get-AzSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="1b7af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b7af-102">SYNOPSIS</span></span>
<span data-ttu-id="1b7af-103">Obtém um ou mais conselheiros para um pool elástico do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1b7af-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="1b7af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b7af-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b7af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b7af-105">DESCRIPTION</span></span>
<span data-ttu-id="1b7af-106">O cmdlet **Get-AzSqlElasticPoolAdvisor** Obtém um ou mais conselheiros de pool elástico do SQL do Azure para um pool elástico do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1b7af-106">The **Get-AzSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="1b7af-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b7af-107">EXAMPLES</span></span>

### <span data-ttu-id="1b7af-108">Exemplo 1: listar todos os conselheiros do pool elástico especificado</span><span class="sxs-lookup"><span data-stu-id="1b7af-108">Example 1: List all the advisors for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool"
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="1b7af-109">O comando obtém lista todos os conselheiros do pool elástico chamado WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="1b7af-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="1b7af-110">Exemplo 2: obter um único conselheiro para o pool elástico especificado</span><span class="sxs-lookup"><span data-stu-id="1b7af-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="1b7af-111">Esse comando obtém o supervisor chamado CreateIndex para o pool elástico chamado WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="1b7af-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="1b7af-112">Exemplo 3: listar todos os conselheiros com as ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="1b7af-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
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

ElasticPoolName                : WIRunnerPool
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

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="1b7af-113">Esse comando obtém todos os conselheiros do pool elástico com as ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="1b7af-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="1b7af-114">Exemplo 4: obter um único conselheiro com as ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="1b7af-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="1b7af-115">Este comando obtém o supervisor chamado CreateIndex do servidor chamado Wi-Runner-Austrália-leste com as ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="1b7af-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="1b7af-116">Exemplo 5: listar todos os conselheiros do pool elástico especificado usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="1b7af-116">Example 5: List all the advisors for the specified elastic pool using filtering</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName d*
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="1b7af-117">O comando obtém lista todos os conselheiros do pool elástico chamado WIRunnerPool que começam com a letra "d".</span><span class="sxs-lookup"><span data-stu-id="1b7af-117">The command gets lists all the advisors for the elastic pool named WIRunnerPool that start with the letter "d".</span></span>

## <span data-ttu-id="1b7af-118">OS</span><span class="sxs-lookup"><span data-stu-id="1b7af-118">PARAMETERS</span></span>

### <span data-ttu-id="1b7af-119">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="1b7af-119">-AdvisorName</span></span>
<span data-ttu-id="1b7af-120">Especifica o nome do supervisor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="1b7af-120">Specifies the name of the Advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1b7af-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b7af-121">-DefaultProfile</span></span>
<span data-ttu-id="1b7af-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1b7af-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b7af-123">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1b7af-123">-ElasticPoolName</span></span>
<span data-ttu-id="1b7af-124">Especifica o nome do pool elástico para o qual esse cmdlet solicita o supervisor.</span><span class="sxs-lookup"><span data-stu-id="1b7af-124">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="1b7af-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="1b7af-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="1b7af-126">Indica que o cmdlet inclui as ações recomendadas do supervisor na resposta.</span><span class="sxs-lookup"><span data-stu-id="1b7af-126">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

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

### <span data-ttu-id="1b7af-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b7af-127">-ResourceGroupName</span></span>
<span data-ttu-id="1b7af-128">Especifica o nome do grupo de recursos do servidor que contém esse pool elástico.</span><span class="sxs-lookup"><span data-stu-id="1b7af-128">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="1b7af-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="1b7af-129">-ServerName</span></span>
<span data-ttu-id="1b7af-130">Especifica o nome do servidor no qual o pool elástico está.</span><span class="sxs-lookup"><span data-stu-id="1b7af-130">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="1b7af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b7af-131">CommonParameters</span></span>
<span data-ttu-id="1b7af-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b7af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b7af-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b7af-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b7af-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b7af-134">INPUTS</span></span>

### <span data-ttu-id="1b7af-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1b7af-135">System.String</span></span>

### <span data-ttu-id="1b7af-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1b7af-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1b7af-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b7af-137">OUTPUTS</span></span>

### <span data-ttu-id="1b7af-138">Microsoft. Azure. Commands. Sql. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="1b7af-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="1b7af-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b7af-139">NOTES</span></span>
* <span data-ttu-id="1b7af-140">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="1b7af-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="1b7af-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b7af-141">RELATED LINKS</span></span>

[<span data-ttu-id="1b7af-142">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="1b7af-142">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="1b7af-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="1b7af-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="1b7af-144">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="1b7af-144">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="1b7af-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="1b7af-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="1b7af-146">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="1b7af-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
