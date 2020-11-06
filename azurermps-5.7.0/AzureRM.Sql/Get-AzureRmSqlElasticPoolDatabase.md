---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: 3068b3a406414eb7302d76d5d053658dcf0e6245
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602831"
---
# <span data-ttu-id="6b493-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="6b493-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="6b493-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b493-102">SYNOPSIS</span></span>
<span data-ttu-id="6b493-103">Obtém bancos de dados elásticos em um pool elástico e seus valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6b493-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b493-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b493-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b493-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b493-105">DESCRIPTION</span></span>
<span data-ttu-id="6b493-106">O cmdlet **Get-AzureRmSqlElasticPoolDatabase** Obtém bancos de dados elásticos em um pool elástico e seus valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6b493-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="6b493-107">Você pode especificar o nome de um banco de dados elástico no banco de dados SQL do Azure para ver os valores de propriedade somente para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6b493-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="6b493-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b493-108">EXAMPLES</span></span>

### <span data-ttu-id="6b493-109">Exemplo 1: obter todos os bancos de dados em um pool elástico</span><span class="sxs-lookup"><span data-stu-id="6b493-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="6b493-110">Esse comando obtém todos os bancos de dados em um pool elástico chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="6b493-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="6b493-111">OS</span><span class="sxs-lookup"><span data-stu-id="6b493-111">PARAMETERS</span></span>

### <span data-ttu-id="6b493-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6b493-112">-DatabaseName</span></span>
<span data-ttu-id="6b493-113">Especifica o nome do banco de dados SQL que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6b493-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6b493-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b493-114">-DefaultProfile</span></span>
<span data-ttu-id="6b493-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6b493-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b493-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6b493-116">-ElasticPoolName</span></span>
<span data-ttu-id="6b493-117">Especifica o nome de um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="6b493-117">Specifies the name of an elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b493-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b493-118">-ResourceGroupName</span></span>
<span data-ttu-id="6b493-119">Especifica o nome de um grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="6b493-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="6b493-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="6b493-120">-ServerName</span></span>
<span data-ttu-id="6b493-121">Especifica o nome de um servidor que contém um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="6b493-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="6b493-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6b493-122">-Confirm</span></span>
<span data-ttu-id="6b493-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b493-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b493-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b493-124">-WhatIf</span></span>
<span data-ttu-id="6b493-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b493-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b493-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b493-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b493-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b493-127">CommonParameters</span></span>
<span data-ttu-id="6b493-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b493-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b493-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b493-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b493-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b493-130">INPUTS</span></span>

### <span data-ttu-id="6b493-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6b493-131">None</span></span>
<span data-ttu-id="6b493-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6b493-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b493-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b493-133">OUTPUTS</span></span>

### <span data-ttu-id="6b493-134">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6b493-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="6b493-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b493-135">NOTES</span></span>

## <span data-ttu-id="6b493-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b493-136">RELATED LINKS</span></span>

[<span data-ttu-id="6b493-137">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6b493-137">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="6b493-138">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="6b493-138">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="6b493-139">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6b493-139">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="6b493-140">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6b493-140">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="6b493-141">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6b493-141">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

