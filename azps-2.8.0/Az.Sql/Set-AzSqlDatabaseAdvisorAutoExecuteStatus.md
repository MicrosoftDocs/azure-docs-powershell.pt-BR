---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 11f0d2429397578c622bb894db292d0c58a74122
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773514"
---
# <span data-ttu-id="0657a-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="0657a-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="0657a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0657a-102">SYNOPSIS</span></span>
<span data-ttu-id="0657a-103">Modifica o status de execução automática de um supervisor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0657a-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="0657a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0657a-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0657a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0657a-105">DESCRIPTION</span></span>
<span data-ttu-id="0657a-106">O cmdlet **set-AzSqlDatabaseAdvisorAutoExecuteStatus** modifica a propriedade de execução automática para um supervisor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0657a-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="0657a-107">Atualmente, esse cmdlet dá suporte a valores habilitados, desabilitados e padrão.</span><span class="sxs-lookup"><span data-stu-id="0657a-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="0657a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0657a-108">EXAMPLES</span></span>

### <span data-ttu-id="0657a-109">Exemplo 1: habilitar a execução automática para um conselheiro</span><span class="sxs-lookup"><span data-stu-id="0657a-109">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="0657a-110">Esse comando altera o status de execução automática de um supervisor chamado CreateIndex para Enabled.</span><span class="sxs-lookup"><span data-stu-id="0657a-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="0657a-111">OS</span><span class="sxs-lookup"><span data-stu-id="0657a-111">PARAMETERS</span></span>

### <span data-ttu-id="0657a-112">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="0657a-112">-AdvisorName</span></span>
<span data-ttu-id="0657a-113">Especifica o nome do supervisor para o qual esse cmdlet modifica o status.</span><span class="sxs-lookup"><span data-stu-id="0657a-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="0657a-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="0657a-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="0657a-115">Especifica o valor do status.</span><span class="sxs-lookup"><span data-stu-id="0657a-115">Specifies the value for the status.</span></span>
<span data-ttu-id="0657a-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0657a-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0657a-117">Possibilita</span><span class="sxs-lookup"><span data-stu-id="0657a-117">Enabled</span></span> 
- <span data-ttu-id="0657a-118">Ativo</span><span class="sxs-lookup"><span data-stu-id="0657a-118">Disabled</span></span> 
- <span data-ttu-id="0657a-119">Assume</span><span class="sxs-lookup"><span data-stu-id="0657a-119">Default</span></span>

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

### <span data-ttu-id="0657a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0657a-120">-DatabaseName</span></span>
<span data-ttu-id="0657a-121">Especifica o nome do banco de dados para o qual esse cmdlet modifica o status.</span><span class="sxs-lookup"><span data-stu-id="0657a-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="0657a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0657a-122">-DefaultProfile</span></span>
<span data-ttu-id="0657a-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0657a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0657a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0657a-124">-ResourceGroupName</span></span>
<span data-ttu-id="0657a-125">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0657a-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="0657a-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0657a-126">-ServerName</span></span>
<span data-ttu-id="0657a-127">Especifica o nome do servidor do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0657a-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="0657a-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0657a-128">-Confirm</span></span>
<span data-ttu-id="0657a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0657a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0657a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0657a-130">-WhatIf</span></span>
<span data-ttu-id="0657a-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0657a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0657a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0657a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0657a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0657a-133">CommonParameters</span></span>
<span data-ttu-id="0657a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0657a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0657a-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0657a-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0657a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0657a-136">INPUTS</span></span>

### <span data-ttu-id="0657a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0657a-137">System.String</span></span>

### <span data-ttu-id="0657a-138">Microsoft. Azure. Commands. Sql. Advisor. cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="0657a-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="0657a-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0657a-139">OUTPUTS</span></span>

### <span data-ttu-id="0657a-140">Microsoft. Azure. Commands. Sql. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="0657a-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="0657a-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0657a-141">NOTES</span></span>

## <span data-ttu-id="0657a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0657a-142">RELATED LINKS</span></span>

[<span data-ttu-id="0657a-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="0657a-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="0657a-144">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="0657a-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

