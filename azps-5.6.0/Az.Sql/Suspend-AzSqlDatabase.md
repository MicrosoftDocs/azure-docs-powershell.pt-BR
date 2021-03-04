---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: 43284eb2f3d0cc39e5fcf5869ad26ebf0e52bd5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890569"
---
# <span data-ttu-id="cabff-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cabff-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="cabff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cabff-102">SYNOPSIS</span></span>
<span data-ttu-id="cabff-103">Suspende um banco de dados SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="cabff-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="cabff-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cabff-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cabff-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cabff-105">DESCRIPTION</span></span>
<span data-ttu-id="cabff-106">O cmdlet **Suspend-AzSqlDatabase** suspende um banco de dados do Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="cabff-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="cabff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cabff-107">EXAMPLES</span></span>

### <span data-ttu-id="cabff-108">Exemplo 1: suspende um banco de dados do Azure SQL Data Warehouse</span><span class="sxs-lookup"><span data-stu-id="cabff-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="cabff-109">Este comando suspende um banco de dados ativo do Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="cabff-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="cabff-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cabff-110">PARAMETERS</span></span>

### <span data-ttu-id="cabff-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cabff-111">-AsJob</span></span>
<span data-ttu-id="cabff-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cabff-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cabff-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cabff-113">-DatabaseName</span></span>
<span data-ttu-id="cabff-114">Especifica o nome do banco de dados que esse cmdlet suspende.</span><span class="sxs-lookup"><span data-stu-id="cabff-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="cabff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cabff-115">-DefaultProfile</span></span>
<span data-ttu-id="cabff-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="cabff-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cabff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cabff-117">-ResourceGroupName</span></span>
<span data-ttu-id="cabff-118">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="cabff-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="cabff-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cabff-119">-ServerName</span></span>
<span data-ttu-id="cabff-120">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cabff-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="cabff-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cabff-121">-Confirm</span></span>
<span data-ttu-id="cabff-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cabff-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cabff-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cabff-123">-WhatIf</span></span>
<span data-ttu-id="cabff-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cabff-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cabff-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cabff-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cabff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabff-126">CommonParameters</span></span>
<span data-ttu-id="cabff-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cabff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabff-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cabff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabff-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cabff-129">INPUTS</span></span>

### <span data-ttu-id="cabff-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cabff-130">System.String</span></span>

## <span data-ttu-id="cabff-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cabff-131">OUTPUTS</span></span>

### <span data-ttu-id="cabff-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cabff-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="cabff-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="cabff-133">NOTES</span></span>
* <span data-ttu-id="cabff-134">O cmdlet **Suspend-AzSqlDatabase** funciona somente em bancos de dados do Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="cabff-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="cabff-135">Essa operação não é suportada nas edições Azure SQL Database Basic, Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="cabff-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="cabff-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cabff-136">RELATED LINKS</span></span>

[<span data-ttu-id="cabff-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cabff-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="cabff-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cabff-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="cabff-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cabff-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="cabff-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cabff-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="cabff-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cabff-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="cabff-142">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="cabff-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


