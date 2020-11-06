---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: f3554aa2e7f4970b3fa1752077a25e02d631abbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441368"
---
# <span data-ttu-id="dd26a-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dd26a-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="dd26a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd26a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd26a-103">Retoma um banco de dados de data warehouse do SQL.</span><span class="sxs-lookup"><span data-stu-id="dd26a-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd26a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd26a-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd26a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd26a-105">DESCRIPTION</span></span>
<span data-ttu-id="dd26a-106">O cmdlet **resume-AzureRmSqlDatabase** retoma um banco de dados de SQL data warehouse do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd26a-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="dd26a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd26a-107">EXAMPLES</span></span>

### <span data-ttu-id="dd26a-108">Exemplo 1: retoma um banco de dados de SQL data warehouse do Azure</span><span class="sxs-lookup"><span data-stu-id="dd26a-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="dd26a-109">Esse comando retoma um banco de dados suspenso do Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="dd26a-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="dd26a-110">OS</span><span class="sxs-lookup"><span data-stu-id="dd26a-110">PARAMETERS</span></span>

### <span data-ttu-id="dd26a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd26a-111">-DatabaseName</span></span>
<span data-ttu-id="dd26a-112">Especifica o nome do banco de dados que este cmdlet reinicia.</span><span class="sxs-lookup"><span data-stu-id="dd26a-112">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="dd26a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd26a-113">-ResourceGroupName</span></span>
<span data-ttu-id="dd26a-114">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="dd26a-114">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="dd26a-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="dd26a-115">-ServerName</span></span>
<span data-ttu-id="dd26a-116">Especifica o nome do servidor que hospeda o banco de dados que este cmdlet reinicia.</span><span class="sxs-lookup"><span data-stu-id="dd26a-116">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="dd26a-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dd26a-117">-Confirm</span></span>
<span data-ttu-id="dd26a-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd26a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd26a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd26a-119">-WhatIf</span></span>
<span data-ttu-id="dd26a-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd26a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd26a-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd26a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd26a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd26a-122">-DefaultProfile</span></span>
<span data-ttu-id="dd26a-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd26a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd26a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd26a-124">CommonParameters</span></span>
<span data-ttu-id="dd26a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd26a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd26a-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd26a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd26a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd26a-127">INPUTS</span></span>

### <span data-ttu-id="dd26a-128">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="dd26a-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="dd26a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd26a-129">OUTPUTS</span></span>

### <span data-ttu-id="dd26a-130">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="dd26a-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="dd26a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd26a-131">NOTES</span></span>
* <span data-ttu-id="dd26a-132">O cmdlet **resume-AzureRmSqlDatabase** funciona apenas em bancos de dados de data warehouse do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd26a-132">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="dd26a-133">Não há suporte para essa operação nas edições Basic, Standard e Premium do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd26a-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="dd26a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd26a-134">RELATED LINKS</span></span>

[<span data-ttu-id="dd26a-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dd26a-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="dd26a-136">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dd26a-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="dd26a-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dd26a-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="dd26a-138">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dd26a-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="dd26a-139">Suspender-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dd26a-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="dd26a-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="dd26a-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


