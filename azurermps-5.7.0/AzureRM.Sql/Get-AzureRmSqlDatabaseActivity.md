---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: 64d8dae1b12630c6ef0086ab2648fcd424c0389d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432888"
---
# <span data-ttu-id="66e53-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="66e53-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="66e53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66e53-102">SYNOPSIS</span></span>
<span data-ttu-id="66e53-103">Obtém o status das operações de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="66e53-103">Gets the status of database operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66e53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66e53-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66e53-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66e53-105">DESCRIPTION</span></span>
<span data-ttu-id="66e53-106">O cmdlet **Get-AzureRmSqlDatabaseActivity** Obtém o status das operações de banco de dados no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="66e53-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="66e53-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66e53-107">EXAMPLES</span></span>

### <span data-ttu-id="66e53-108">Exemplo 1: obter o status de todas as instâncias de banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="66e53-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="66e53-109">Esse comando retorna o status da operação de todas as instâncias do banco de dados SQL em um pool elástico chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="66e53-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="66e53-110">Exemplo 2: obter o status de todas as operações de banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="66e53-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="66e53-111">Esse comando retorna o status de todas as operações de banco de dados SQL em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="66e53-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="66e53-112">OS</span><span class="sxs-lookup"><span data-stu-id="66e53-112">PARAMETERS</span></span>

### <span data-ttu-id="66e53-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66e53-113">-DatabaseName</span></span>
<span data-ttu-id="66e53-114">Especifica o nome do banco de dados para o qual esse cmdlet obtém o status.</span><span class="sxs-lookup"><span data-stu-id="66e53-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e53-115">-DefaultProfile</span></span>
<span data-ttu-id="66e53-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66e53-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e53-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="66e53-117">-ElasticPoolName</span></span>
<span data-ttu-id="66e53-118">Especifica o nome do pool de banco de dados elástico para o qual esse cmdlet obtém o status.</span><span class="sxs-lookup"><span data-stu-id="66e53-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e53-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="66e53-119">-OperationId</span></span>
<span data-ttu-id="66e53-120">Especifica a ID da operação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="66e53-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e53-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66e53-121">-ResourceGroupName</span></span>
<span data-ttu-id="66e53-122">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="66e53-122">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e53-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="66e53-123">-ServerName</span></span>
<span data-ttu-id="66e53-124">Especifica o nome do Microsoft SQL Server que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="66e53-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e53-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="66e53-125">-Confirm</span></span>
<span data-ttu-id="66e53-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66e53-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e53-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66e53-127">-WhatIf</span></span>
<span data-ttu-id="66e53-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66e53-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66e53-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66e53-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e53-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e53-130">CommonParameters</span></span>
<span data-ttu-id="66e53-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66e53-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e53-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66e53-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e53-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66e53-133">INPUTS</span></span>

### <span data-ttu-id="66e53-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="66e53-134">None</span></span>
<span data-ttu-id="66e53-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="66e53-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66e53-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66e53-136">OUTPUTS</span></span>

### <span data-ttu-id="66e53-137">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="66e53-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="66e53-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66e53-138">NOTES</span></span>

## <span data-ttu-id="66e53-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66e53-139">RELATED LINKS</span></span>
