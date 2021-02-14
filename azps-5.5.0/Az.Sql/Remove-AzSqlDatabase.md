---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115735"
---
# <span data-ttu-id="c81ac-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c81ac-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="c81ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c81ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c81ac-103">Remove um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c81ac-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="c81ac-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c81ac-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c81ac-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c81ac-105">DESCRIPTION</span></span>
<span data-ttu-id="c81ac-106">O **cmdlet Remove-AzSqlDatabase** remove um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c81ac-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="c81ac-107">Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="c81ac-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c81ac-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c81ac-108">EXAMPLES</span></span>

### <span data-ttu-id="c81ac-109">Exemplo 1: Remover um banco de dados de um servidor SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="c81ac-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="c81ac-110">Esse comando remove o banco de dados chamado Database01 do servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="c81ac-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="c81ac-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c81ac-111">PARAMETERS</span></span>

### <span data-ttu-id="c81ac-112">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="c81ac-112">-DatabaseName</span></span>
<span data-ttu-id="c81ac-113">Especifica o nome do banco de dados que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="c81ac-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c81ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81ac-114">-DefaultProfile</span></span>
<span data-ttu-id="c81ac-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c81ac-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c81ac-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="c81ac-116">-Force</span></span>
<span data-ttu-id="c81ac-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c81ac-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81ac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c81ac-118">-ResourceGroupName</span></span>
<span data-ttu-id="c81ac-119">Especifica o nome do grupo de recursos do Azure ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="c81ac-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c81ac-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c81ac-120">-ServerName</span></span>
<span data-ttu-id="c81ac-121">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c81ac-121">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c81ac-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c81ac-122">-Confirm</span></span>
<span data-ttu-id="c81ac-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c81ac-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c81ac-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c81ac-124">-WhatIf</span></span>
<span data-ttu-id="c81ac-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c81ac-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c81ac-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c81ac-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c81ac-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81ac-127">CommonParameters</span></span>
<span data-ttu-id="c81ac-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c81ac-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81ac-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c81ac-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81ac-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="c81ac-130">INPUTS</span></span>

### <span data-ttu-id="c81ac-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c81ac-131">System.String</span></span>

## <span data-ttu-id="c81ac-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="c81ac-132">OUTPUTS</span></span>

### <span data-ttu-id="c81ac-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c81ac-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="c81ac-134">Notas</span><span class="sxs-lookup"><span data-stu-id="c81ac-134">NOTES</span></span>

## <span data-ttu-id="c81ac-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c81ac-135">RELATED LINKS</span></span>

[<span data-ttu-id="c81ac-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c81ac-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="c81ac-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c81ac-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="c81ac-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c81ac-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="c81ac-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c81ac-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="c81ac-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c81ac-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="c81ac-141">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="c81ac-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


