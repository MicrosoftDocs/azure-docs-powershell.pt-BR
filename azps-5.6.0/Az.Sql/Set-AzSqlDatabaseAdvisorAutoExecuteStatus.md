---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 214fe4c32ed49433aa57752508604d0179334401
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890953"
---
# <span data-ttu-id="ff8a6-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="ff8a6-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="ff8a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="ff8a6-103">Modifica o status de execução automática de um Azure SQL Database Advisor.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="ff8a6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ff8a6-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff8a6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ff8a6-105">DESCRIPTION</span></span>
<span data-ttu-id="ff8a6-106">O cmdlet **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** modifica a propriedade de execução automática para um Supervisor de Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="ff8a6-107">Atualmente, esse cmdlet dá suporte aos valores Enabled, Disabled e Default.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="ff8a6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff8a6-108">EXAMPLES</span></span>

### <span data-ttu-id="ff8a6-109">Exemplo 1: Habilitar a execução automática para um consultor</span><span class="sxs-lookup"><span data-stu-id="ff8a6-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="ff8a6-110">Este comando altera o status de execução automática de um consultor chamado CreateIndex como Habilitado.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="ff8a6-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ff8a6-111">PARAMETERS</span></span>

### <span data-ttu-id="ff8a6-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="ff8a6-112">-AdvisorName</span></span>
<span data-ttu-id="ff8a6-113">Especifica o nome do consultor para o qual este cmdlet modifica o status.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="ff8a6-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="ff8a6-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="ff8a6-115">Especifica o valor do status.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-115">Specifies the value for the status.</span></span>
<span data-ttu-id="ff8a6-116">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ff8a6-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff8a6-117">Habilitado</span><span class="sxs-lookup"><span data-stu-id="ff8a6-117">Enabled</span></span> 
- <span data-ttu-id="ff8a6-118">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="ff8a6-118">Disabled</span></span> 
- <span data-ttu-id="ff8a6-119">Padrão</span><span class="sxs-lookup"><span data-stu-id="ff8a6-119">Default</span></span>

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

### <span data-ttu-id="ff8a6-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ff8a6-120">-DatabaseName</span></span>
<span data-ttu-id="ff8a6-121">Especifica o nome do banco de dados para o qual este cmdlet modifica o status.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="ff8a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff8a6-122">-DefaultProfile</span></span>
<span data-ttu-id="ff8a6-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ff8a6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff8a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff8a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="ff8a6-125">Especifica o nome do grupo de recursos do servidor que contém esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="ff8a6-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ff8a6-126">-ServerName</span></span>
<span data-ttu-id="ff8a6-127">Especifica o nome do servidor para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="ff8a6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff8a6-128">-Confirm</span></span>
<span data-ttu-id="ff8a6-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff8a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff8a6-130">-WhatIf</span></span>
<span data-ttu-id="ff8a6-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff8a6-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff8a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff8a6-133">CommonParameters</span></span>
<span data-ttu-id="ff8a6-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff8a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff8a6-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff8a6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff8a6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff8a6-136">INPUTS</span></span>

### <span data-ttu-id="ff8a6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ff8a6-137">System.String</span></span>

### <span data-ttu-id="ff8a6-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="ff8a6-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="ff8a6-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ff8a6-139">OUTPUTS</span></span>

### <span data-ttu-id="ff8a6-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="ff8a6-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="ff8a6-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="ff8a6-141">NOTES</span></span>

## <span data-ttu-id="ff8a6-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff8a6-142">RELATED LINKS</span></span>

[<span data-ttu-id="ff8a6-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="ff8a6-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="ff8a6-144">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="ff8a6-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

