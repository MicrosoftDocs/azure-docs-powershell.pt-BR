---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: b37ae31c1f0dc6360743a863f0305fd5823cbb3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440545"
---
# <span data-ttu-id="5a015-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="5a015-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="5a015-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a015-102">SYNOPSIS</span></span>
<span data-ttu-id="5a015-103">Obtém o status da movimentação de bancos de dados elásticos.</span><span class="sxs-lookup"><span data-stu-id="5a015-103">Gets the status of moving elastic databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a015-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a015-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> -ElasticPoolName <String> -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a015-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a015-105">DESCRIPTION</span></span>
<span data-ttu-id="5a015-106">O cmdlet **Get-AzureRmSqlDatabaseActivity** Obtém o status de bancos de dados elásticos que se movem para dentro ou para fora de um pool de banco de dados elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5a015-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of elastic databases moving into or out of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="5a015-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a015-107">EXAMPLES</span></span>

### <span data-ttu-id="5a015-108">Exemplo 1: obter o status de todas as instâncias de banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="5a015-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="5a015-109">Esse comando retorna o status da operação de todas as instâncias do banco de dados SQL em um pool elástico chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="5a015-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="5a015-110">OS</span><span class="sxs-lookup"><span data-stu-id="5a015-110">PARAMETERS</span></span>

### <span data-ttu-id="5a015-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a015-111">-DatabaseName</span></span>
<span data-ttu-id="5a015-112">Especifica o nome do banco de dados para o qual esse cmdlet obtém o status.</span><span class="sxs-lookup"><span data-stu-id="5a015-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="5a015-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5a015-113">-ElasticPoolName</span></span>
<span data-ttu-id="5a015-114">Especifica o nome do pool de banco de dados elástico para o qual esse cmdlet obtém o status.</span><span class="sxs-lookup"><span data-stu-id="5a015-114">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="5a015-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5a015-115">-OperationId</span></span>
<span data-ttu-id="5a015-116">Especifica a ID da operação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="5a015-116">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5a015-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a015-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a015-118">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="5a015-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5a015-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5a015-119">-ServerName</span></span>
<span data-ttu-id="5a015-120">Especifica o nome do Microsoft SQL Server que hospeda o pool de banco de dados elástico.</span><span class="sxs-lookup"><span data-stu-id="5a015-120">Specifies the name of the Microsoft SQL Server that hosts the elastic database pool.</span></span>

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

### <span data-ttu-id="5a015-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5a015-121">-Confirm</span></span>
<span data-ttu-id="5a015-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a015-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a015-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a015-123">-WhatIf</span></span>
<span data-ttu-id="5a015-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a015-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a015-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a015-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a015-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a015-126">-DefaultProfile</span></span>
<span data-ttu-id="5a015-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a015-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a015-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a015-128">CommonParameters</span></span>
<span data-ttu-id="5a015-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a015-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a015-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a015-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a015-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a015-131">INPUTS</span></span>

## <span data-ttu-id="5a015-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a015-132">OUTPUTS</span></span>

### <span data-ttu-id="5a015-133">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="5a015-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="5a015-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a015-134">NOTES</span></span>

## <span data-ttu-id="5a015-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a015-135">RELATED LINKS</span></span>

