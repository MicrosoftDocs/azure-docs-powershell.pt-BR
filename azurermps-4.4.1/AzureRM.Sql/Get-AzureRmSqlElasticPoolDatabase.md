---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: f2229fa904144b0dd95a054da95db99600963406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429043"
---
# <span data-ttu-id="1bda4-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="1bda4-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="1bda4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1bda4-102">SYNOPSIS</span></span>
<span data-ttu-id="1bda4-103">Obtém bancos de dados elásticos em um pool elástico e seus valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1bda4-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bda4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bda4-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1bda4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1bda4-105">DESCRIPTION</span></span>
<span data-ttu-id="1bda4-106">O cmdlet **Get-AzureRmSqlElasticPoolDatabase** Obtém bancos de dados elásticos em um pool elástico e seus valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1bda4-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="1bda4-107">Você pode especificar o nome de um banco de dados elástico no banco de dados SQL do Azure para ver os valores de propriedade somente para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1bda4-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="1bda4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1bda4-108">EXAMPLES</span></span>

### <span data-ttu-id="1bda4-109">Exemplo 1: obter todos os bancos de dados em um pool elástico</span><span class="sxs-lookup"><span data-stu-id="1bda4-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="1bda4-110">Esse comando obtém todos os bancos de dados em um pool elástico chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="1bda4-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="1bda4-111">OS</span><span class="sxs-lookup"><span data-stu-id="1bda4-111">PARAMETERS</span></span>

### <span data-ttu-id="1bda4-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1bda4-112">-DatabaseName</span></span>
<span data-ttu-id="1bda4-113">Especifica o nome do banco de dados SQL que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="1bda4-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1bda4-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1bda4-114">-ElasticPoolName</span></span>
<span data-ttu-id="1bda4-115">Especifica o nome de um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="1bda4-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="1bda4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bda4-116">-ResourceGroupName</span></span>
<span data-ttu-id="1bda4-117">Especifica o nome de um grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="1bda4-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="1bda4-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="1bda4-118">-ServerName</span></span>
<span data-ttu-id="1bda4-119">Especifica o nome de um servidor que contém um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="1bda4-119">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="1bda4-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1bda4-120">-Confirm</span></span>
<span data-ttu-id="1bda4-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bda4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bda4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bda4-122">-WhatIf</span></span>
<span data-ttu-id="1bda4-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1bda4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bda4-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1bda4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bda4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bda4-125">-DefaultProfile</span></span>
<span data-ttu-id="1bda4-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1bda4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bda4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bda4-127">CommonParameters</span></span>
<span data-ttu-id="1bda4-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bda4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bda4-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bda4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bda4-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1bda4-130">INPUTS</span></span>

## <span data-ttu-id="1bda4-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1bda4-131">OUTPUTS</span></span>

### <span data-ttu-id="1bda4-132">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1bda4-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="1bda4-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1bda4-133">NOTES</span></span>

## <span data-ttu-id="1bda4-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bda4-134">RELATED LINKS</span></span>

[<span data-ttu-id="1bda4-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1bda4-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="1bda4-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="1bda4-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="1bda4-137">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1bda4-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="1bda4-138">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1bda4-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="1bda4-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1bda4-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

