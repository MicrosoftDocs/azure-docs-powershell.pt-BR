---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 2e24dc80b93d72722d05a7dced05cbea02751a05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112548"
---
# <span data-ttu-id="80c25-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="80c25-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="80c25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80c25-102">SYNOPSIS</span></span>
<span data-ttu-id="80c25-103">Obtém bancos de dados elásticas em um pool elástica e seus valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="80c25-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="80c25-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80c25-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80c25-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="80c25-105">DESCRIPTION</span></span>
<span data-ttu-id="80c25-106">O cmdlet **Get-AzSqlElasticPoolDatabase** obtém bancos de dados elásticas em um pool elástica e seus valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="80c25-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="80c25-107">Você pode especificar o nome de um banco de dados elástica no Banco de Dados SQL do Azure para ver os valores de propriedade apenas para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="80c25-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="80c25-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="80c25-108">EXAMPLES</span></span>

### <span data-ttu-id="80c25-109">Exemplo 1: Obter todos os bancos de dados em um pool elástica</span><span class="sxs-lookup"><span data-stu-id="80c25-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="80c25-110">Esse comando obtém todos os bancos de dados em um pool elástica chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="80c25-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="80c25-111">Exemplo 2: Obter todos os bancos de dados em um pool elástica usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="80c25-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="80c25-112">Esse comando obtém todos os bancos de dados em um pool elástica chamado ElasticPool01 que começa com "Banco de Dados".</span><span class="sxs-lookup"><span data-stu-id="80c25-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="80c25-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80c25-113">PARAMETERS</span></span>

### <span data-ttu-id="80c25-114">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="80c25-114">-DatabaseName</span></span>
<span data-ttu-id="80c25-115">Especifica o nome do banco de dados SQL que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="80c25-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="80c25-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c25-116">-DefaultProfile</span></span>
<span data-ttu-id="80c25-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="80c25-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80c25-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="80c25-118">-ElasticPoolName</span></span>
<span data-ttu-id="80c25-119">Especifica o nome de um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="80c25-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="80c25-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c25-120">-ResourceGroupName</span></span>
<span data-ttu-id="80c25-121">Especifica o nome de um grupo de recursos ao qual o pool elástica é atribuído.</span><span class="sxs-lookup"><span data-stu-id="80c25-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="80c25-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="80c25-122">-ServerName</span></span>
<span data-ttu-id="80c25-123">Especifica o nome de um servidor que contém um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="80c25-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="80c25-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="80c25-124">-Confirm</span></span>
<span data-ttu-id="80c25-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c25-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c25-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c25-126">-WhatIf</span></span>
<span data-ttu-id="80c25-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="80c25-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c25-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80c25-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c25-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c25-129">CommonParameters</span></span>
<span data-ttu-id="80c25-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80c25-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c25-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80c25-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c25-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="80c25-132">INPUTS</span></span>

### <span data-ttu-id="80c25-133">System.String</span><span class="sxs-lookup"><span data-stu-id="80c25-133">System.String</span></span>

## <span data-ttu-id="80c25-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="80c25-134">OUTPUTS</span></span>

### <span data-ttu-id="80c25-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="80c25-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="80c25-136">Notas</span><span class="sxs-lookup"><span data-stu-id="80c25-136">NOTES</span></span>

## <span data-ttu-id="80c25-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80c25-137">RELATED LINKS</span></span>

[<span data-ttu-id="80c25-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="80c25-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="80c25-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="80c25-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="80c25-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="80c25-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="80c25-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="80c25-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="80c25-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="80c25-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

