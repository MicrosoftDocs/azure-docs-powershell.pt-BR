---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271362"
---
# <span data-ttu-id="16d59-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="16d59-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="16d59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16d59-102">SYNOPSIS</span></span>
<span data-ttu-id="16d59-103">Retoma um banco de dados de data warehouse do SQL.</span><span class="sxs-lookup"><span data-stu-id="16d59-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="16d59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16d59-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16d59-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16d59-105">DESCRIPTION</span></span>
<span data-ttu-id="16d59-106">O cmdlet **resume-AzSqlDatabase** retoma um banco de dados de SQL data warehouse do Azure.</span><span class="sxs-lookup"><span data-stu-id="16d59-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="16d59-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16d59-107">EXAMPLES</span></span>

### <span data-ttu-id="16d59-108">Exemplo 1: retoma um banco de dados de SQL data warehouse do Azure</span><span class="sxs-lookup"><span data-stu-id="16d59-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="16d59-109">Esse comando retoma um banco de dados suspenso do Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="16d59-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="16d59-110">OS</span><span class="sxs-lookup"><span data-stu-id="16d59-110">PARAMETERS</span></span>

### <span data-ttu-id="16d59-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16d59-111">-AsJob</span></span>
<span data-ttu-id="16d59-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="16d59-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16d59-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16d59-113">-DatabaseName</span></span>
<span data-ttu-id="16d59-114">Especifica o nome do banco de dados que este cmdlet reinicia.</span><span class="sxs-lookup"><span data-stu-id="16d59-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="16d59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d59-115">-DefaultProfile</span></span>
<span data-ttu-id="16d59-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="16d59-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16d59-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16d59-117">-ResourceGroupName</span></span>
<span data-ttu-id="16d59-118">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="16d59-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="16d59-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="16d59-119">-ServerName</span></span>
<span data-ttu-id="16d59-120">Especifica o nome do servidor que hospeda o banco de dados que este cmdlet reinicia.</span><span class="sxs-lookup"><span data-stu-id="16d59-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="16d59-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="16d59-121">-Confirm</span></span>
<span data-ttu-id="16d59-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16d59-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16d59-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16d59-123">-WhatIf</span></span>
<span data-ttu-id="16d59-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16d59-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16d59-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16d59-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16d59-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d59-126">CommonParameters</span></span>
<span data-ttu-id="16d59-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d59-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d59-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16d59-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d59-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16d59-129">INPUTS</span></span>

### <span data-ttu-id="16d59-130">System. String</span><span class="sxs-lookup"><span data-stu-id="16d59-130">System.String</span></span>

## <span data-ttu-id="16d59-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16d59-131">OUTPUTS</span></span>

### <span data-ttu-id="16d59-132">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="16d59-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="16d59-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16d59-133">NOTES</span></span>
* <span data-ttu-id="16d59-134">O cmdlet **resume-AzSqlDatabase** funciona apenas em bancos de dados de data warehouse do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="16d59-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="16d59-135">Não há suporte para essa operação nas edições Basic, Standard e Premium do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="16d59-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="16d59-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16d59-136">RELATED LINKS</span></span>

[<span data-ttu-id="16d59-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="16d59-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="16d59-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="16d59-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="16d59-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="16d59-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="16d59-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="16d59-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="16d59-141">Suspender-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="16d59-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="16d59-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="16d59-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


