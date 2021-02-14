---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: 1d487c4397d1a7c29f0b415ee973d01e4dc6f1a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110945"
---
# <span data-ttu-id="89a3f-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="89a3f-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="89a3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="89a3f-103">Recebe um ou mais Consultores para um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="89a3f-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="89a3f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89a3f-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89a3f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="89a3f-105">DESCRIPTION</span></span>
<span data-ttu-id="89a3f-106">O cmdlet **Get-AzSqlServerAdvisor** obtém um ou mais Azure SQL Server Advisors para um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="89a3f-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="89a3f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="89a3f-107">EXAMPLES</span></span>

### <span data-ttu-id="89a3f-108">Exemplo 1: Listar todos os consultores do servidor</span><span class="sxs-lookup"><span data-stu-id="89a3f-108">Example 1: List all the advisors for the server</span></span>
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

<span data-ttu-id="89a3f-109">Esse comando obtém uma lista de todos os consultores do servidor chamado wi-runner-australia-east que pertence ao grupo de recursos chamado WI WifisProd.</span><span class="sxs-lookup"><span data-stu-id="89a3f-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="89a3f-110">Exemplo 2: Obter um único consultor para o servidor</span><span class="sxs-lookup"><span data-stu-id="89a3f-110">Example 2: Get a single advisor for the server</span></span>
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

<span data-ttu-id="89a3f-111">Esse comando obtém o consultor chamado CreateIndex para o servidor chamado wi-runner-australia-east.</span><span class="sxs-lookup"><span data-stu-id="89a3f-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="89a3f-112">Exemplo 3: Listar todos os consultores com suas ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="89a3f-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
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

<span data-ttu-id="89a3f-113">Esse comando obtém todos os consultores do servidor chamados wi-runner-australia-east.</span><span class="sxs-lookup"><span data-stu-id="89a3f-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="89a3f-114">Como o comando usa o parâmetro *ExpandRecom recommendedActions,* o cmdlet obtém as ações recomendadas dos consultores incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="89a3f-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="89a3f-115">Exemplo 4: Obter um único consultor com suas ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="89a3f-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
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

<span data-ttu-id="89a3f-116">Esse comando recebe o advisor chamado CreateIndex do servidor chamado wi-runner-australia-east com suas ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="89a3f-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="89a3f-117">Exemplo 5: Listar todos os consultores do servidor usando filtragem</span><span class="sxs-lookup"><span data-stu-id="89a3f-117">Example 5: List all the advisors for the server using filtering</span></span>
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

<span data-ttu-id="89a3f-118">Este comando obtém uma lista de todos os consultores do servidor chamado wi-runner-australia-east que pertence ao grupo de recursos chamado WI WifisProd que começam com a letra "d".</span><span class="sxs-lookup"><span data-stu-id="89a3f-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="89a3f-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89a3f-119">PARAMETERS</span></span>

### <span data-ttu-id="89a3f-120">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="89a3f-120">-AdvisorName</span></span>
<span data-ttu-id="89a3f-121">Especifica o nome do consultor que este cmdlet recebe.</span><span class="sxs-lookup"><span data-stu-id="89a3f-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="89a3f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a3f-122">-DefaultProfile</span></span>
<span data-ttu-id="89a3f-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="89a3f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89a3f-124">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="89a3f-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="89a3f-125">Indica que o cmdlet inclui as ações recomendadas dos consultores que estão incluídos na resposta.</span><span class="sxs-lookup"><span data-stu-id="89a3f-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="89a3f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89a3f-126">-ResourceGroupName</span></span>
<span data-ttu-id="89a3f-127">Especifica o nome do grupo de recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="89a3f-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="89a3f-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="89a3f-128">-ServerName</span></span>
<span data-ttu-id="89a3f-129">Especifica o nome do servidor para o consultor que este cmdlet solicita.</span><span class="sxs-lookup"><span data-stu-id="89a3f-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="89a3f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a3f-130">CommonParameters</span></span>
<span data-ttu-id="89a3f-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89a3f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a3f-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89a3f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a3f-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="89a3f-133">INPUTS</span></span>

### <span data-ttu-id="89a3f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="89a3f-134">System.String</span></span>

### <span data-ttu-id="89a3f-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89a3f-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89a3f-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="89a3f-136">OUTPUTS</span></span>

### <span data-ttu-id="89a3f-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="89a3f-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="89a3f-138">Notas</span><span class="sxs-lookup"><span data-stu-id="89a3f-138">NOTES</span></span>
* <span data-ttu-id="89a3f-139">Palavras-chave: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="89a3f-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="89a3f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89a3f-140">RELATED LINKS</span></span>

[<span data-ttu-id="89a3f-141">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="89a3f-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="89a3f-142">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="89a3f-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="89a3f-143">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="89a3f-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="89a3f-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="89a3f-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="89a3f-145">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="89a3f-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

