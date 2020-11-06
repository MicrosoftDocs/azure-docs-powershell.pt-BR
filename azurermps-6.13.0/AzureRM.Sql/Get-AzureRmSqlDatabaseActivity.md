---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: 08c5778002a80bb4fb2effdd977f134079f3aa0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431894"
---
# <span data-ttu-id="a7d0c-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="a7d0c-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="a7d0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d0c-103">Obtém o status das operações de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-103">Gets the status of database operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7d0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7d0c-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7d0c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7d0c-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d0c-106">O cmdlet **Get-AzureRmSqlDatabaseActivity** Obtém o status das operações de banco de dados no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="a7d0c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7d0c-107">EXAMPLES</span></span>

### <span data-ttu-id="a7d0c-108">Exemplo 1: obter o status de todas as instâncias de banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="a7d0c-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="a7d0c-109">Esse comando retorna o status da operação de todas as instâncias do banco de dados SQL em um pool elástico chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="a7d0c-110">Exemplo 2: obter o status de todas as operações de banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="a7d0c-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a7d0c-111">Esse comando retorna o status de todas as operações de banco de dados SQL em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="a7d0c-112">OS</span><span class="sxs-lookup"><span data-stu-id="a7d0c-112">PARAMETERS</span></span>

### <span data-ttu-id="a7d0c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7d0c-113">-DatabaseName</span></span>
<span data-ttu-id="a7d0c-114">Especifica o nome do banco de dados para o qual esse cmdlet obtém o status.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="a7d0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d0c-115">-DefaultProfile</span></span>
<span data-ttu-id="a7d0c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7d0c-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a7d0c-117">-ElasticPoolName</span></span>
<span data-ttu-id="a7d0c-118">Especifica o nome do pool de banco de dados elástico para o qual esse cmdlet obtém o status.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="a7d0c-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a7d0c-119">-OperationId</span></span>
<span data-ttu-id="a7d0c-120">Especifica a ID da operação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a7d0c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d0c-121">-ResourceGroupName</span></span>
<span data-ttu-id="a7d0c-122">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a7d0c-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="a7d0c-123">-ServerName</span></span>
<span data-ttu-id="a7d0c-124">Especifica o nome do Microsoft SQL Server que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="a7d0c-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a7d0c-125">-Confirm</span></span>
<span data-ttu-id="a7d0c-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7d0c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7d0c-127">-WhatIf</span></span>
<span data-ttu-id="a7d0c-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7d0c-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7d0c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d0c-130">CommonParameters</span></span>
<span data-ttu-id="a7d0c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d0c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d0c-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d0c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d0c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7d0c-133">INPUTS</span></span>

### <span data-ttu-id="a7d0c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a7d0c-134">System.String</span></span>

### <span data-ttu-id="a7d0c-135">System. Nullable ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a7d0c-135">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a7d0c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7d0c-136">OUTPUTS</span></span>

### <span data-ttu-id="a7d0c-137">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="a7d0c-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="a7d0c-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7d0c-138">NOTES</span></span>

## <span data-ttu-id="a7d0c-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7d0c-139">RELATED LINKS</span></span>
