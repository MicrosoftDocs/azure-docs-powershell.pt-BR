---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 02a4348511afabe7f398eafeb6d0849525f0abac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115696"
---
# <span data-ttu-id="0009d-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="0009d-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="0009d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0009d-102">SYNOPSIS</span></span>
<span data-ttu-id="0009d-103">Atualiza o status de execução automática de um Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="0009d-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="0009d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0009d-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0009d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0009d-105">DESCRIPTION</span></span>
<span data-ttu-id="0009d-106">O cmdlet **Set-AzSqlServerAdvisorAutoExecuteStatus** define a propriedade de execução automática para um Supervisor do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="0009d-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="0009d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0009d-107">EXAMPLES</span></span>

### <span data-ttu-id="0009d-108">Exemplo 1: Habilitar a execução automática para um Consultor</span><span class="sxs-lookup"><span data-stu-id="0009d-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="0009d-109">Esse comando habilita o status de execução automática de um Consultor chamado CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="0009d-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="0009d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0009d-110">PARAMETERS</span></span>

### <span data-ttu-id="0009d-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="0009d-111">-AdvisorName</span></span>
<span data-ttu-id="0009d-112">Especifica o nome do consultor para o qual este cmdlet atualiza o status de execução automática.</span><span class="sxs-lookup"><span data-stu-id="0009d-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="0009d-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="0009d-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="0009d-114">Especifica o valor ao qual este cmdlet atualiza o status de execução automática.</span><span class="sxs-lookup"><span data-stu-id="0009d-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="0009d-115">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0009d-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0009d-116">Habilitado</span><span class="sxs-lookup"><span data-stu-id="0009d-116">Enabled</span></span>
- <span data-ttu-id="0009d-117">Desativado</span><span class="sxs-lookup"><span data-stu-id="0009d-117">Disabled</span></span>
- <span data-ttu-id="0009d-118">Padrão</span><span class="sxs-lookup"><span data-stu-id="0009d-118">Default</span></span>

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

### <span data-ttu-id="0009d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0009d-119">-DefaultProfile</span></span>
<span data-ttu-id="0009d-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0009d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0009d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0009d-121">-ResourceGroupName</span></span>
<span data-ttu-id="0009d-122">Especifica o nome do grupo de recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="0009d-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="0009d-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0009d-123">-ServerName</span></span>
<span data-ttu-id="0009d-124">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0009d-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="0009d-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0009d-125">-Confirm</span></span>
<span data-ttu-id="0009d-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0009d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0009d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0009d-127">-WhatIf</span></span>
<span data-ttu-id="0009d-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0009d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0009d-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0009d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0009d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0009d-130">CommonParameters</span></span>
<span data-ttu-id="0009d-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0009d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0009d-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0009d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0009d-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="0009d-133">INPUTS</span></span>

### <span data-ttu-id="0009d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0009d-134">System.String</span></span>

### <span data-ttu-id="0009d-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="0009d-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="0009d-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="0009d-136">OUTPUTS</span></span>

### <span data-ttu-id="0009d-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="0009d-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="0009d-138">Notas</span><span class="sxs-lookup"><span data-stu-id="0009d-138">NOTES</span></span>
* <span data-ttu-id="0009d-139">Palavras-chave: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="0009d-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="0009d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0009d-140">RELATED LINKS</span></span>

[<span data-ttu-id="0009d-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="0009d-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="0009d-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="0009d-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
