---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: 1d487c4397d1a7c29f0b415ee973d01e4dc6f1a1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944255"
---
# <span data-ttu-id="58fc6-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="58fc6-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="58fc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="58fc6-103">Obtém um ou mais conselheiros para um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="58fc6-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="58fc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58fc6-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58fc6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="58fc6-106">O cmdlet **Get-AzSqlServerAdvisor** Obtém um ou mais conselheiros do SQL Server do Azure para um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="58fc6-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="58fc6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58fc6-107">EXAMPLES</span></span>

### <span data-ttu-id="58fc6-108">Exemplo 1: listar todos os conselheiros do servidor</span><span class="sxs-lookup"><span data-stu-id="58fc6-108">Example 1: List all the advisors for the server</span></span>
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

<span data-ttu-id="58fc6-109">Esse comando obtém uma lista de todos os consultores do servidor chamado Wi-Runner-Austrália-leste que pertence ao grupo de recursos chamado WIRunnersProd.</span><span class="sxs-lookup"><span data-stu-id="58fc6-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="58fc6-110">Exemplo 2: obter um único supervisor para o servidor</span><span class="sxs-lookup"><span data-stu-id="58fc6-110">Example 2: Get a single advisor for the server</span></span>
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

<span data-ttu-id="58fc6-111">Esse comando obtém o supervisor chamado CreateIndex para o servidor chamado Wi-Runner-Austrália-leste.</span><span class="sxs-lookup"><span data-stu-id="58fc6-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="58fc6-112">Exemplo 3: listar todos os conselheiros com as ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="58fc6-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
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

<span data-ttu-id="58fc6-113">Esse comando obtém todos os conselheiros do servidor chamado Wi-Runner-Austrália-leste.</span><span class="sxs-lookup"><span data-stu-id="58fc6-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="58fc6-114">Como o comando usa o parâmetro *ExpandRecommendedActions* , o cmdlet obtém as ações recomendadas dos conselheiros incluídos na resposta.</span><span class="sxs-lookup"><span data-stu-id="58fc6-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="58fc6-115">Exemplo 4: obter um único conselheiro com as ações recomendadas incluídas na resposta</span><span class="sxs-lookup"><span data-stu-id="58fc6-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
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

<span data-ttu-id="58fc6-116">Este comando obtém o supervisor chamado CreateIndex do servidor chamado Wi-Runner-Austrália-leste com as ações recomendadas incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="58fc6-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="58fc6-117">Exemplo 5: listar todos os conselheiros do servidor usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="58fc6-117">Example 5: List all the advisors for the server using filtering</span></span>
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

<span data-ttu-id="58fc6-118">Esse comando obtém uma lista de todos os conselheiros do servidor chamado de Wi-Runner-Austrália-leste que pertence ao grupo de recursos chamado WIRunnersProd, que começa com a letra "d".</span><span class="sxs-lookup"><span data-stu-id="58fc6-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="58fc6-119">OS</span><span class="sxs-lookup"><span data-stu-id="58fc6-119">PARAMETERS</span></span>

### <span data-ttu-id="58fc6-120">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="58fc6-120">-AdvisorName</span></span>
<span data-ttu-id="58fc6-121">Especifica o nome do supervisor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="58fc6-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="58fc6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58fc6-122">-DefaultProfile</span></span>
<span data-ttu-id="58fc6-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="58fc6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58fc6-124">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="58fc6-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="58fc6-125">Indica que o cmdlet inclui as ações recomendadas dos consultores que estão incluídos na resposta.</span><span class="sxs-lookup"><span data-stu-id="58fc6-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="58fc6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58fc6-126">-ResourceGroupName</span></span>
<span data-ttu-id="58fc6-127">Especifica o nome do grupo de recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="58fc6-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="58fc6-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="58fc6-128">-ServerName</span></span>
<span data-ttu-id="58fc6-129">Especifica o nome do servidor para o supervisor que este cmdlet solicita.</span><span class="sxs-lookup"><span data-stu-id="58fc6-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="58fc6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58fc6-130">CommonParameters</span></span>
<span data-ttu-id="58fc6-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58fc6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58fc6-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58fc6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58fc6-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58fc6-133">INPUTS</span></span>

### <span data-ttu-id="58fc6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="58fc6-134">System.String</span></span>

### <span data-ttu-id="58fc6-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="58fc6-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="58fc6-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58fc6-136">OUTPUTS</span></span>

### <span data-ttu-id="58fc6-137">Microsoft. Azure. Commands. Sql. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="58fc6-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="58fc6-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58fc6-138">NOTES</span></span>
* <span data-ttu-id="58fc6-139">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Server, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="58fc6-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="58fc6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58fc6-140">RELATED LINKS</span></span>

[<span data-ttu-id="58fc6-141">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="58fc6-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="58fc6-142">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="58fc6-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="58fc6-143">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="58fc6-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="58fc6-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="58fc6-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="58fc6-145">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="58fc6-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

