---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: 23affeb81159da5a9f1212f5190f927dc1689e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440159"
---
# <span data-ttu-id="a8456-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8456-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="a8456-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8456-102">SYNOPSIS</span></span>
<span data-ttu-id="a8456-103">Suspende um banco de dados de data warehouse do SQL.</span><span class="sxs-lookup"><span data-stu-id="a8456-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8456-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8456-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8456-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8456-105">DESCRIPTION</span></span>
<span data-ttu-id="a8456-106">O cmdlet **Suspend-AzureRmSqlDatabase** suspende um banco de dados de SQL data warehouse do Azure.</span><span class="sxs-lookup"><span data-stu-id="a8456-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a8456-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8456-107">EXAMPLES</span></span>

### <span data-ttu-id="a8456-108">Exemplo 1: suspende um banco de dados de SQL data warehouse do Azure</span><span class="sxs-lookup"><span data-stu-id="a8456-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a8456-109">Esse comando suspende um banco de dados ativo do Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="a8456-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a8456-110">OS</span><span class="sxs-lookup"><span data-stu-id="a8456-110">PARAMETERS</span></span>

### <span data-ttu-id="a8456-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a8456-111">-DatabaseName</span></span>
<span data-ttu-id="a8456-112">Especifica o nome do banco de dados que este cmdlet suspende.</span><span class="sxs-lookup"><span data-stu-id="a8456-112">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="a8456-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8456-113">-ResourceGroupName</span></span>
<span data-ttu-id="a8456-114">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a8456-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a8456-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="a8456-115">-ServerName</span></span>
<span data-ttu-id="a8456-116">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a8456-116">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="a8456-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a8456-117">-Confirm</span></span>
<span data-ttu-id="a8456-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8456-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8456-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8456-119">-WhatIf</span></span>
<span data-ttu-id="a8456-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8456-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8456-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8456-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8456-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8456-122">-DefaultProfile</span></span>
<span data-ttu-id="a8456-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8456-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8456-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8456-124">CommonParameters</span></span>
<span data-ttu-id="a8456-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8456-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8456-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8456-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8456-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8456-127">INPUTS</span></span>

### <span data-ttu-id="a8456-128">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a8456-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a8456-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8456-129">OUTPUTS</span></span>

### <span data-ttu-id="a8456-130">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a8456-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a8456-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8456-131">NOTES</span></span>
* <span data-ttu-id="a8456-132">O cmdlet **Suspend-AzureRmSqlDatabase** funciona apenas em bancos de dados de data warehouse do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a8456-132">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="a8456-133">Não há suporte para essa operação nas edições Basic, Standard e Premium do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a8456-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="a8456-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8456-134">RELATED LINKS</span></span>

[<span data-ttu-id="a8456-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8456-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="a8456-136">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8456-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="a8456-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8456-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="a8456-138">Currículo-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8456-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="a8456-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a8456-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="a8456-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="a8456-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


