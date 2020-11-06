---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/resume-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: 5681b046afb6682809d9b2dc744784514c2aefa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430822"
---
# <span data-ttu-id="21401-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="21401-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="21401-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21401-102">SYNOPSIS</span></span>
<span data-ttu-id="21401-103">Retoma um banco de dados de data warehouse do SQL.</span><span class="sxs-lookup"><span data-stu-id="21401-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21401-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21401-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21401-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21401-105">DESCRIPTION</span></span>
<span data-ttu-id="21401-106">O cmdlet **resume-AzureRmSqlDatabase** retoma um banco de dados de SQL data warehouse do Azure.</span><span class="sxs-lookup"><span data-stu-id="21401-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="21401-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21401-107">EXAMPLES</span></span>

### <span data-ttu-id="21401-108">Exemplo 1: retoma um banco de dados de SQL data warehouse do Azure</span><span class="sxs-lookup"><span data-stu-id="21401-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="21401-109">Esse comando retoma um banco de dados suspenso do Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="21401-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="21401-110">OS</span><span class="sxs-lookup"><span data-stu-id="21401-110">PARAMETERS</span></span>

### <span data-ttu-id="21401-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21401-111">-AsJob</span></span>
<span data-ttu-id="21401-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="21401-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21401-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="21401-113">-DatabaseName</span></span>
<span data-ttu-id="21401-114">Especifica o nome do banco de dados que este cmdlet reinicia.</span><span class="sxs-lookup"><span data-stu-id="21401-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="21401-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21401-115">-DefaultProfile</span></span>
<span data-ttu-id="21401-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="21401-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21401-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21401-117">-ResourceGroupName</span></span>
<span data-ttu-id="21401-118">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="21401-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="21401-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="21401-119">-ServerName</span></span>
<span data-ttu-id="21401-120">Especifica o nome do servidor que hospeda o banco de dados que este cmdlet reinicia.</span><span class="sxs-lookup"><span data-stu-id="21401-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="21401-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21401-121">-Confirm</span></span>
<span data-ttu-id="21401-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21401-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21401-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21401-123">-WhatIf</span></span>
<span data-ttu-id="21401-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21401-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21401-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21401-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21401-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21401-126">CommonParameters</span></span>
<span data-ttu-id="21401-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21401-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21401-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21401-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21401-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21401-129">INPUTS</span></span>

### <span data-ttu-id="21401-130">System. String</span><span class="sxs-lookup"><span data-stu-id="21401-130">System.String</span></span>

## <span data-ttu-id="21401-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21401-131">OUTPUTS</span></span>

### <span data-ttu-id="21401-132">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="21401-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="21401-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21401-133">NOTES</span></span>
* <span data-ttu-id="21401-134">O cmdlet **resume-AzureRmSqlDatabase** funciona apenas em bancos de dados de data warehouse do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="21401-134">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="21401-135">Não há suporte para essa operação nas edições Basic, Standard e Premium do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="21401-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="21401-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21401-136">RELATED LINKS</span></span>

[<span data-ttu-id="21401-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="21401-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="21401-138">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="21401-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="21401-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="21401-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="21401-140">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="21401-140">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="21401-141">Suspender-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="21401-141">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="21401-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="21401-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


