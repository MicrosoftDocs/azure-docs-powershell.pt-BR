---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: 2a4142c7d8bb0f48bf75613b214dccd1876c5264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886130"
---
# <span data-ttu-id="21620-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="21620-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="21620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21620-102">SYNOPSIS</span></span>
<span data-ttu-id="21620-103">Remove um banco de dados SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="21620-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="21620-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="21620-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21620-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="21620-105">DESCRIPTION</span></span>
<span data-ttu-id="21620-106">O cmdlet **Remove-AzSqlDatabase** remove um banco de dados SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="21620-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="21620-107">Esse cmdlet também é suportado pelo serviço SQL Server Banco de Dados de Extensão no Azure.</span><span class="sxs-lookup"><span data-stu-id="21620-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="21620-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21620-108">EXAMPLES</span></span>

### <span data-ttu-id="21620-109">Exemplo 1: Remover um banco de dados de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="21620-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="21620-110">Este comando remove o banco de dados chamado Database01 do servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="21620-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="21620-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="21620-111">PARAMETERS</span></span>

### <span data-ttu-id="21620-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="21620-112">-DatabaseName</span></span>
<span data-ttu-id="21620-113">Especifica o nome do banco de dados que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="21620-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="21620-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21620-114">-DefaultProfile</span></span>
<span data-ttu-id="21620-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="21620-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21620-116">-Force</span><span class="sxs-lookup"><span data-stu-id="21620-116">-Force</span></span>
<span data-ttu-id="21620-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="21620-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="21620-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21620-118">-ResourceGroupName</span></span>
<span data-ttu-id="21620-119">Especifica o nome do grupo de recursos do Azure ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="21620-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="21620-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="21620-120">-ServerName</span></span>
<span data-ttu-id="21620-121">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="21620-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="21620-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21620-122">-Confirm</span></span>
<span data-ttu-id="21620-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21620-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21620-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21620-124">-WhatIf</span></span>
<span data-ttu-id="21620-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21620-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21620-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21620-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21620-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21620-127">CommonParameters</span></span>
<span data-ttu-id="21620-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21620-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21620-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21620-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21620-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21620-130">INPUTS</span></span>

### <span data-ttu-id="21620-131">System.String</span><span class="sxs-lookup"><span data-stu-id="21620-131">System.String</span></span>

## <span data-ttu-id="21620-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="21620-132">OUTPUTS</span></span>

### <span data-ttu-id="21620-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="21620-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="21620-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="21620-134">NOTES</span></span>

## <span data-ttu-id="21620-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21620-135">RELATED LINKS</span></span>

[<span data-ttu-id="21620-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="21620-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="21620-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="21620-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="21620-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="21620-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="21620-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="21620-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="21620-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="21620-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="21620-141">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="21620-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


