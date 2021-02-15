---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: df4ad0ea9f0e1990fa3c71915b1882baf1d3a762
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112559"
---
# <span data-ttu-id="fb035-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="fb035-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="fb035-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb035-102">SYNOPSIS</span></span>
<span data-ttu-id="fb035-103">Obtém o status das operações de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fb035-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="fb035-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb035-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb035-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb035-105">DESCRIPTION</span></span>
<span data-ttu-id="fb035-106">O cmdlet **Get-AzSqlDatabaseActivity** obtém o status das operações de banco de dados no Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb035-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="fb035-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fb035-107">EXAMPLES</span></span>

### <span data-ttu-id="fb035-108">Exemplo 1: Obter status para todas as instâncias do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="fb035-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="fb035-109">Esse comando retorna o status da operação de todas as instâncias do banco de dados SQL em um pool elástica chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="fb035-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="fb035-110">Exemplo 2: Obter status para todas as operações de banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="fb035-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="fb035-111">Esse comando retorna o status de todas as operações de banco de dados SQL em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fb035-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="fb035-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb035-112">PARAMETERS</span></span>

### <span data-ttu-id="fb035-113">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="fb035-113">-DatabaseName</span></span>
<span data-ttu-id="fb035-114">Especifica o nome do banco de dados para o qual este cmdlet obtém status.</span><span class="sxs-lookup"><span data-stu-id="fb035-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="fb035-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb035-115">-DefaultProfile</span></span>
<span data-ttu-id="fb035-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fb035-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb035-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fb035-117">-ElasticPoolName</span></span>
<span data-ttu-id="fb035-118">Especifica o nome do pool de banco de dados elástica para o qual este cmdlet obtém status.</span><span class="sxs-lookup"><span data-stu-id="fb035-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="fb035-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="fb035-119">-OperationId</span></span>
<span data-ttu-id="fb035-120">Especifica a ID da operação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="fb035-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fb035-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb035-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb035-122">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="fb035-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="fb035-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fb035-123">-ServerName</span></span>
<span data-ttu-id="fb035-124">Especifica o nome do Microsoft SQL Server que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fb035-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="fb035-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fb035-125">-Confirm</span></span>
<span data-ttu-id="fb035-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb035-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb035-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb035-127">-WhatIf</span></span>
<span data-ttu-id="fb035-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fb035-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb035-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb035-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb035-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb035-130">CommonParameters</span></span>
<span data-ttu-id="fb035-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb035-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb035-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb035-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb035-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="fb035-133">INPUTS</span></span>

### <span data-ttu-id="fb035-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fb035-134">System.String</span></span>

### <span data-ttu-id="fb035-135">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb035-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fb035-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="fb035-136">OUTPUTS</span></span>

### <span data-ttu-id="fb035-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="fb035-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="fb035-138">Notas</span><span class="sxs-lookup"><span data-stu-id="fb035-138">NOTES</span></span>

## <span data-ttu-id="fb035-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb035-139">RELATED LINKS</span></span>
