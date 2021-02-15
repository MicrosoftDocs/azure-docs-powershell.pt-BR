---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
ms.openlocfilehash: 3032824d51e7892c21830decbdb1c92d03d7a2e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118939"
---
# <span data-ttu-id="b6431-101">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="b6431-101">Get-AzSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="b6431-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6431-102">SYNOPSIS</span></span>
<span data-ttu-id="b6431-103">Recebe um ou mais Consultores para um Pool Elástica SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b6431-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="b6431-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6431-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6431-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6431-105">DESCRIPTION</span></span>
<span data-ttu-id="b6431-106">O cmdlet **Get-AzSqlElasticPoolAdvisor** obtém um ou mais Supervisores de Pool Elástica SQL do Azure para um Pool Elástica SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b6431-106">The **Get-AzSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="b6431-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6431-107">EXAMPLES</span></span>

### <span data-ttu-id="b6431-108">Exemplo 1: Listar todos os consultores do pool elástica especificado</span><span class="sxs-lookup"><span data-stu-id="b6431-108">Example 1: List all the advisors for the specified elastic pool</span></span>
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

<span data-ttu-id="b6431-109">O comando obtém listas de todos os consultores do pool elástica chamado WIPoolPool.</span><span class="sxs-lookup"><span data-stu-id="b6431-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="b6431-110">Exemplo 2: Obter um único consultor para o pool elástica especificado</span><span class="sxs-lookup"><span data-stu-id="b6431-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
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

<span data-ttu-id="b6431-111">Esse comando obtém o Consultor chamado CreateIndex para o pool elástica chamado WIPoolPool.</span><span class="sxs-lookup"><span data-stu-id="b6431-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="b6431-112">Exemplo 3: Listar todos os consultores com suas ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="b6431-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
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

<span data-ttu-id="b6431-113">Esse comando obtém todos os consultores do pool elástica com suas ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="b6431-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="b6431-114">Exemplo 4: Obter um único consultor com suas ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="b6431-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
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

<span data-ttu-id="b6431-115">Esse comando recebe o consultor CreateIndex do servidor chamado wi-runner-australia-east com suas ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="b6431-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="b6431-116">Exemplo 5: Listar todos os consultores para o pool elástica especificado usando filtragem</span><span class="sxs-lookup"><span data-stu-id="b6431-116">Example 5: List all the advisors for the specified elastic pool using filtering</span></span>
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

<span data-ttu-id="b6431-117">O comando obtém listas de todos os consultores do pool elástica chamado WIPoolPool que começam com a letra "d".</span><span class="sxs-lookup"><span data-stu-id="b6431-117">The command gets lists all the advisors for the elastic pool named WIRunnerPool that start with the letter "d".</span></span>

## <span data-ttu-id="b6431-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6431-118">PARAMETERS</span></span>

### <span data-ttu-id="b6431-119">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="b6431-119">-AdvisorName</span></span>
<span data-ttu-id="b6431-120">Especifica o nome do Consultor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b6431-120">Specifies the name of the Advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b6431-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6431-121">-DefaultProfile</span></span>
<span data-ttu-id="b6431-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b6431-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6431-123">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b6431-123">-ElasticPoolName</span></span>
<span data-ttu-id="b6431-124">Especifica o nome do pool elástica para o qual este cmdlet solicita ao Consultor.</span><span class="sxs-lookup"><span data-stu-id="b6431-124">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="b6431-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="b6431-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="b6431-126">Indica que o cmdlet inclui as ações recomendadas do Consultor na resposta.</span><span class="sxs-lookup"><span data-stu-id="b6431-126">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

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

### <span data-ttu-id="b6431-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6431-127">-ResourceGroupName</span></span>
<span data-ttu-id="b6431-128">Especifica o nome do grupo de recursos do servidor que contém esse pool elástica.</span><span class="sxs-lookup"><span data-stu-id="b6431-128">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="b6431-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b6431-129">-ServerName</span></span>
<span data-ttu-id="b6431-130">Especifica o nome do servidor em que o pool elástica está.</span><span class="sxs-lookup"><span data-stu-id="b6431-130">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="b6431-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6431-131">CommonParameters</span></span>
<span data-ttu-id="b6431-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6431-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6431-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6431-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6431-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="b6431-134">INPUTS</span></span>

### <span data-ttu-id="b6431-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b6431-135">System.String</span></span>

### <span data-ttu-id="b6431-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b6431-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b6431-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="b6431-137">OUTPUTS</span></span>

### <span data-ttu-id="b6431-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="b6431-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="b6431-139">Notas</span><span class="sxs-lookup"><span data-stu-id="b6431-139">NOTES</span></span>
* <span data-ttu-id="b6431-140">Palavras-chave: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="b6431-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="b6431-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6431-141">RELATED LINKS</span></span>

[<span data-ttu-id="b6431-142">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="b6431-142">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="b6431-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="b6431-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="b6431-144">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b6431-144">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="b6431-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b6431-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="b6431-146">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b6431-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
