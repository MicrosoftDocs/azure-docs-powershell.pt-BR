---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: 7a5ecbb21af23b31b321ef1568c2eb953a548cf1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598726"
---
# <span data-ttu-id="7bace-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7bace-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="7bace-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bace-102">SYNOPSIS</span></span>
<span data-ttu-id="7bace-103">Suspende um banco de dados de data warehouse do SQL.</span><span class="sxs-lookup"><span data-stu-id="7bace-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="7bace-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bace-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bace-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bace-105">DESCRIPTION</span></span>
<span data-ttu-id="7bace-106">O cmdlet **Suspend-AzSqlDatabase** suspende um banco de dados de SQL data warehouse do Azure.</span><span class="sxs-lookup"><span data-stu-id="7bace-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="7bace-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bace-107">EXAMPLES</span></span>

### <span data-ttu-id="7bace-108">Exemplo 1: suspende um banco de dados de SQL data warehouse do Azure</span><span class="sxs-lookup"><span data-stu-id="7bace-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="7bace-109">Esse comando suspende um banco de dados ativo do Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="7bace-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="7bace-110">OS</span><span class="sxs-lookup"><span data-stu-id="7bace-110">PARAMETERS</span></span>

### <span data-ttu-id="7bace-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bace-111">-AsJob</span></span>
<span data-ttu-id="7bace-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7bace-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bace-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7bace-113">-DatabaseName</span></span>
<span data-ttu-id="7bace-114">Especifica o nome do banco de dados que este cmdlet suspende.</span><span class="sxs-lookup"><span data-stu-id="7bace-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="7bace-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bace-115">-DefaultProfile</span></span>
<span data-ttu-id="7bace-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7bace-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bace-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bace-117">-ResourceGroupName</span></span>
<span data-ttu-id="7bace-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7bace-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7bace-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="7bace-119">-ServerName</span></span>
<span data-ttu-id="7bace-120">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7bace-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="7bace-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7bace-121">-Confirm</span></span>
<span data-ttu-id="7bace-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bace-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bace-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bace-123">-WhatIf</span></span>
<span data-ttu-id="7bace-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7bace-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bace-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7bace-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bace-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bace-126">CommonParameters</span></span>
<span data-ttu-id="7bace-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bace-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bace-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bace-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bace-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bace-129">INPUTS</span></span>

### <span data-ttu-id="7bace-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7bace-130">System.String</span></span>

## <span data-ttu-id="7bace-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bace-131">OUTPUTS</span></span>

### <span data-ttu-id="7bace-132">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7bace-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="7bace-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bace-133">NOTES</span></span>
* <span data-ttu-id="7bace-134">O cmdlet **Suspend-AzSqlDatabase** funciona apenas em bancos de dados de data warehouse do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7bace-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="7bace-135">Não há suporte para essa operação nas edições Basic, Standard e Premium do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7bace-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="7bace-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bace-136">RELATED LINKS</span></span>

[<span data-ttu-id="7bace-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7bace-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="7bace-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7bace-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="7bace-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7bace-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="7bace-140">Currículo-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7bace-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="7bace-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7bace-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="7bace-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="7bace-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


