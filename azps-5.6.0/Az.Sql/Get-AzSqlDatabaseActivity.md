---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: 12b44d2045574b1d787dd0b2bdb70ec44b616ae5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890699"
---
# <span data-ttu-id="227f3-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="227f3-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="227f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="227f3-102">SYNOPSIS</span></span>
<span data-ttu-id="227f3-103">Obtém o status das operações do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="227f3-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="227f3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="227f3-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="227f3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="227f3-105">DESCRIPTION</span></span>
<span data-ttu-id="227f3-106">O cmdlet **Get-AzSqlDatabaseActivity** obtém o status das operações de banco de dados no Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="227f3-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="227f3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="227f3-107">EXAMPLES</span></span>

### <span data-ttu-id="227f3-108">Exemplo 1: Obter status para todas as SQL banco de dados</span><span class="sxs-lookup"><span data-stu-id="227f3-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="227f3-109">Este comando retorna o status de operação de todas as SQL de banco de dados em um pool elástica chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="227f3-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="227f3-110">Exemplo 2: Obter status para todas as operações SQL Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="227f3-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="227f3-111">Este comando retorna o status de todas as SQL de banco de dados em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="227f3-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="227f3-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="227f3-112">PARAMETERS</span></span>

### <span data-ttu-id="227f3-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="227f3-113">-DatabaseName</span></span>
<span data-ttu-id="227f3-114">Especifica o nome do banco de dados para o qual este cmdlet obtém status.</span><span class="sxs-lookup"><span data-stu-id="227f3-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="227f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="227f3-115">-DefaultProfile</span></span>
<span data-ttu-id="227f3-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="227f3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="227f3-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="227f3-117">-ElasticPoolName</span></span>
<span data-ttu-id="227f3-118">Especifica o nome do pool de banco de dados elástica para o qual este cmdlet obtém status.</span><span class="sxs-lookup"><span data-stu-id="227f3-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="227f3-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="227f3-119">-OperationId</span></span>
<span data-ttu-id="227f3-120">Especifica a ID da operação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="227f3-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="227f3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="227f3-121">-ResourceGroupName</span></span>
<span data-ttu-id="227f3-122">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="227f3-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="227f3-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="227f3-123">-ServerName</span></span>
<span data-ttu-id="227f3-124">Especifica o nome do Microsoft SQL Server que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="227f3-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="227f3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="227f3-125">-Confirm</span></span>
<span data-ttu-id="227f3-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="227f3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="227f3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="227f3-127">-WhatIf</span></span>
<span data-ttu-id="227f3-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="227f3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="227f3-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="227f3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="227f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="227f3-130">CommonParameters</span></span>
<span data-ttu-id="227f3-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="227f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="227f3-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="227f3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="227f3-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="227f3-133">INPUTS</span></span>

### <span data-ttu-id="227f3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="227f3-134">System.String</span></span>

### <span data-ttu-id="227f3-135">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="227f3-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="227f3-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="227f3-136">OUTPUTS</span></span>

### <span data-ttu-id="227f3-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="227f3-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="227f3-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="227f3-138">NOTES</span></span>

## <span data-ttu-id="227f3-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="227f3-139">RELATED LINKS</span></span>
