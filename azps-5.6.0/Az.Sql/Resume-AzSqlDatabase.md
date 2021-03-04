---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: 3ba3703882371975ee9b0d2f87bd03b75b58e6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890956"
---
# <span data-ttu-id="2cdc1-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2cdc1-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="2cdc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cdc1-102">SYNOPSIS</span></span>
<span data-ttu-id="2cdc1-103">Retoma um banco de dados SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="2cdc1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2cdc1-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cdc1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2cdc1-105">DESCRIPTION</span></span>
<span data-ttu-id="2cdc1-106">O cmdlet **Resume-AzSqlDatabase** retoma um banco de dados do Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="2cdc1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2cdc1-107">EXAMPLES</span></span>

### <span data-ttu-id="2cdc1-108">Exemplo 1: retoma um banco de dados do Azure SQL Data Warehouse</span><span class="sxs-lookup"><span data-stu-id="2cdc1-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="2cdc1-109">Este comando retoma um banco de dados suspenso do Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="2cdc1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2cdc1-110">PARAMETERS</span></span>

### <span data-ttu-id="2cdc1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cdc1-111">-AsJob</span></span>
<span data-ttu-id="2cdc1-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2cdc1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cdc1-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2cdc1-113">-DatabaseName</span></span>
<span data-ttu-id="2cdc1-114">Especifica o nome do banco de dados que este cmdlet retoma.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="2cdc1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cdc1-115">-DefaultProfile</span></span>
<span data-ttu-id="2cdc1-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2cdc1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2cdc1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cdc1-117">-ResourceGroupName</span></span>
<span data-ttu-id="2cdc1-118">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="2cdc1-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2cdc1-119">-ServerName</span></span>
<span data-ttu-id="2cdc1-120">Especifica o nome do servidor que hospeda o banco de dados que este cmdlet retoma.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="2cdc1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cdc1-121">-Confirm</span></span>
<span data-ttu-id="2cdc1-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cdc1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cdc1-123">-WhatIf</span></span>
<span data-ttu-id="2cdc1-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cdc1-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cdc1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cdc1-126">CommonParameters</span></span>
<span data-ttu-id="2cdc1-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cdc1-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cdc1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cdc1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cdc1-129">INPUTS</span></span>

### <span data-ttu-id="2cdc1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2cdc1-130">System.String</span></span>

## <span data-ttu-id="2cdc1-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2cdc1-131">OUTPUTS</span></span>

### <span data-ttu-id="2cdc1-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2cdc1-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2cdc1-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="2cdc1-133">NOTES</span></span>
* <span data-ttu-id="2cdc1-134">O cmdlet **Resume-AzSqlDatabase** funciona somente em bancos de dados do Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="2cdc1-135">Essa operação não é suportada nas edições Azure SQL Database Basic, Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="2cdc1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cdc1-136">RELATED LINKS</span></span>

[<span data-ttu-id="2cdc1-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2cdc1-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="2cdc1-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2cdc1-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="2cdc1-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2cdc1-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="2cdc1-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2cdc1-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="2cdc1-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2cdc1-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="2cdc1-142">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="2cdc1-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


