---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 4a9e128fb8c67c44329dd2b99da8ce4722835323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891593"
---
# <span data-ttu-id="d143c-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="d143c-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="d143c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d143c-102">SYNOPSIS</span></span>
<span data-ttu-id="d143c-103">Obtém bancos de dados elásticas em um pool elástica e seus valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d143c-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="d143c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d143c-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d143c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d143c-105">DESCRIPTION</span></span>
<span data-ttu-id="d143c-106">O cmdlet **Get-AzSqlElasticPoolDatabase** obtém bancos de dados elásticas em um pool elástica e seus valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d143c-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="d143c-107">Você pode especificar o nome de um banco de dados elástica no Banco de Dados do Azure SQL para ver os valores de propriedade apenas para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d143c-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="d143c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d143c-108">EXAMPLES</span></span>

### <span data-ttu-id="d143c-109">Exemplo 1: Obter todos os bancos de dados em um pool elástica</span><span class="sxs-lookup"><span data-stu-id="d143c-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="d143c-110">Este comando obtém todos os bancos de dados em um pool elástica chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="d143c-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="d143c-111">Exemplo 2: Obter todos os bancos de dados em um pool elástica usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="d143c-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="d143c-112">Esse comando obtém todos os bancos de dados em um pool elástica chamado ElasticPool01 que começa com "Database".</span><span class="sxs-lookup"><span data-stu-id="d143c-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="d143c-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d143c-113">PARAMETERS</span></span>

### <span data-ttu-id="d143c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d143c-114">-DatabaseName</span></span>
<span data-ttu-id="d143c-115">Especifica o nome do banco de dados SQL que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="d143c-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d143c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d143c-116">-DefaultProfile</span></span>
<span data-ttu-id="d143c-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d143c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d143c-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d143c-118">-ElasticPoolName</span></span>
<span data-ttu-id="d143c-119">Especifica o nome de um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="d143c-119">Specifies the name of an elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d143c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d143c-120">-ResourceGroupName</span></span>
<span data-ttu-id="d143c-121">Especifica o nome de um grupo de recursos ao qual o pool elástica é atribuído.</span><span class="sxs-lookup"><span data-stu-id="d143c-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="d143c-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d143c-122">-ServerName</span></span>
<span data-ttu-id="d143c-123">Especifica o nome de um servidor que contém um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="d143c-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="d143c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d143c-124">-Confirm</span></span>
<span data-ttu-id="d143c-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d143c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d143c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d143c-126">-WhatIf</span></span>
<span data-ttu-id="d143c-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d143c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d143c-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d143c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d143c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d143c-129">CommonParameters</span></span>
<span data-ttu-id="d143c-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d143c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d143c-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d143c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d143c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d143c-132">INPUTS</span></span>

### <span data-ttu-id="d143c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d143c-133">System.String</span></span>

## <span data-ttu-id="d143c-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d143c-134">OUTPUTS</span></span>

### <span data-ttu-id="d143c-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d143c-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d143c-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="d143c-136">NOTES</span></span>

## <span data-ttu-id="d143c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d143c-137">RELATED LINKS</span></span>

[<span data-ttu-id="d143c-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d143c-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="d143c-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="d143c-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="d143c-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d143c-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="d143c-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d143c-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="d143c-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d143c-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

