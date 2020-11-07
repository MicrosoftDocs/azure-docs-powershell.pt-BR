---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 02a4348511afabe7f398eafeb6d0849525f0abac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778003"
---
# <span data-ttu-id="c0bd4-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c0bd4-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="c0bd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="c0bd4-103">Atualiza o status de execução automática de um supervisor do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0bd4-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="c0bd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0bd4-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0bd4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0bd4-105">DESCRIPTION</span></span>
<span data-ttu-id="c0bd4-106">O cmdlet **set-AzSqlServerAdvisorAutoExecuteStatus** define a propriedade auto execute para um SQL Server Advisor do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0bd4-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="c0bd4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0bd4-107">EXAMPLES</span></span>

### <span data-ttu-id="c0bd4-108">Exemplo 1: habilitar a execução automática para um conselheiro</span><span class="sxs-lookup"><span data-stu-id="c0bd4-108">Example 1: Enable auto execute for an Advisor</span></span>
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

<span data-ttu-id="c0bd4-109">Esse comando habilita o status de execução automática de um supervisor chamado CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="c0bd4-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="c0bd4-110">OS</span><span class="sxs-lookup"><span data-stu-id="c0bd4-110">PARAMETERS</span></span>

### <span data-ttu-id="c0bd4-111">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="c0bd4-111">-AdvisorName</span></span>
<span data-ttu-id="c0bd4-112">Especifica o nome do supervisor para o qual esse cmdlet atualiza o status de execução automática.</span><span class="sxs-lookup"><span data-stu-id="c0bd4-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="c0bd4-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c0bd4-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="c0bd4-114">Especifica o valor para o qual esse cmdlet atualiza o status de execução automática.</span><span class="sxs-lookup"><span data-stu-id="c0bd4-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="c0bd4-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c0bd4-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c0bd4-116">Possibilita</span><span class="sxs-lookup"><span data-stu-id="c0bd4-116">Enabled</span></span>
- <span data-ttu-id="c0bd4-117">Ativo</span><span class="sxs-lookup"><span data-stu-id="c0bd4-117">Disabled</span></span>
- <span data-ttu-id="c0bd4-118">Assume</span><span class="sxs-lookup"><span data-stu-id="c0bd4-118">Default</span></span>

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

### <span data-ttu-id="c0bd4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0bd4-119">-DefaultProfile</span></span>
<span data-ttu-id="c0bd4-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c0bd4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0bd4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0bd4-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0bd4-122">Especifica o nome do grupo de recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="c0bd4-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="c0bd4-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c0bd4-123">-ServerName</span></span>
<span data-ttu-id="c0bd4-124">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c0bd4-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c0bd4-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c0bd4-125">-Confirm</span></span>
<span data-ttu-id="c0bd4-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0bd4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0bd4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0bd4-127">-WhatIf</span></span>
<span data-ttu-id="c0bd4-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0bd4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0bd4-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0bd4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0bd4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0bd4-130">CommonParameters</span></span>
<span data-ttu-id="c0bd4-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0bd4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0bd4-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0bd4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0bd4-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0bd4-133">INPUTS</span></span>

### <span data-ttu-id="c0bd4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c0bd4-134">System.String</span></span>

### <span data-ttu-id="c0bd4-135">Microsoft. Azure. Commands. Sql. Advisor. cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c0bd4-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="c0bd4-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0bd4-136">OUTPUTS</span></span>

### <span data-ttu-id="c0bd4-137">Microsoft. Azure. Commands. Sql. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="c0bd4-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="c0bd4-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0bd4-138">NOTES</span></span>
* <span data-ttu-id="c0bd4-139">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Server, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="c0bd4-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="c0bd4-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0bd4-140">RELATED LINKS</span></span>

[<span data-ttu-id="c0bd4-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="c0bd4-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="c0bd4-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="c0bd4-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
