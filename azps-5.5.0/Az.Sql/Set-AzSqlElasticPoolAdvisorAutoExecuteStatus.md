---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5e26be318f439556a7083dc4d2bcde154083f5e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110905"
---
# <span data-ttu-id="7533e-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="7533e-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="7533e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7533e-102">SYNOPSIS</span></span>
<span data-ttu-id="7533e-103">Atualiza o status de execução automática de um Azure SQL Elastic Pool Advisor.</span><span class="sxs-lookup"><span data-stu-id="7533e-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="7533e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7533e-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7533e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7533e-105">DESCRIPTION</span></span>
<span data-ttu-id="7533e-106">O cmdlet **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** define a propriedade de execução automática para um Azure SQL Elastic Pool Advisor.</span><span class="sxs-lookup"><span data-stu-id="7533e-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="7533e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7533e-107">EXAMPLES</span></span>

### <span data-ttu-id="7533e-108">Exemplo 1: Habilitar a execução automática para um consultor</span><span class="sxs-lookup"><span data-stu-id="7533e-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="7533e-109">Esse comando define o status de execução automática de um consultor chamado CreateIndex para habilitado.</span><span class="sxs-lookup"><span data-stu-id="7533e-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="7533e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7533e-110">PARAMETERS</span></span>

### <span data-ttu-id="7533e-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="7533e-111">-AdvisorName</span></span>
<span data-ttu-id="7533e-112">Especifica o nome do consultor para o qual este cmdlet atualiza o status de execução automática.</span><span class="sxs-lookup"><span data-stu-id="7533e-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="7533e-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="7533e-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="7533e-114">Especifica um novo valor ao qual este cmdlet atualiza o status de execução automática.</span><span class="sxs-lookup"><span data-stu-id="7533e-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="7533e-115">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7533e-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7533e-116">Habilitado</span><span class="sxs-lookup"><span data-stu-id="7533e-116">Enabled</span></span>
- <span data-ttu-id="7533e-117">Desativado</span><span class="sxs-lookup"><span data-stu-id="7533e-117">Disabled</span></span>
- <span data-ttu-id="7533e-118">Padrão</span><span class="sxs-lookup"><span data-stu-id="7533e-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7533e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7533e-119">-DefaultProfile</span></span>
<span data-ttu-id="7533e-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7533e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7533e-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7533e-121">-ElasticPoolName</span></span>
<span data-ttu-id="7533e-122">Especifica o nome do pool elástica.</span><span class="sxs-lookup"><span data-stu-id="7533e-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="7533e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7533e-123">-ResourceGroupName</span></span>
<span data-ttu-id="7533e-124">Especifica o nome do grupo de recursos do servidor que contém esse pool elástica.</span><span class="sxs-lookup"><span data-stu-id="7533e-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="7533e-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7533e-125">-ServerName</span></span>
<span data-ttu-id="7533e-126">Especifica o nome do servidor em que o pool elástica está.</span><span class="sxs-lookup"><span data-stu-id="7533e-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="7533e-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7533e-127">-Confirm</span></span>
<span data-ttu-id="7533e-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7533e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7533e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7533e-129">-WhatIf</span></span>
<span data-ttu-id="7533e-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7533e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7533e-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7533e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7533e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7533e-132">CommonParameters</span></span>
<span data-ttu-id="7533e-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7533e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7533e-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7533e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7533e-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="7533e-135">INPUTS</span></span>

### <span data-ttu-id="7533e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7533e-136">System.String</span></span>

### <span data-ttu-id="7533e-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="7533e-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="7533e-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="7533e-138">OUTPUTS</span></span>

### <span data-ttu-id="7533e-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="7533e-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="7533e-140">Notas</span><span class="sxs-lookup"><span data-stu-id="7533e-140">NOTES</span></span>
* <span data-ttu-id="7533e-141">Palavras-chave: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="7533e-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="7533e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7533e-142">RELATED LINKS</span></span>

[<span data-ttu-id="7533e-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="7533e-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="7533e-144">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="7533e-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
