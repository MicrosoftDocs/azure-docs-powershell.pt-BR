---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: 57f5f656f3c85e9d1c0d29c07a602a303208e7f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431767"
---
# <span data-ttu-id="02e7b-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="02e7b-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="02e7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="02e7b-103">Exclui um pool de banco de dados elástico.</span><span class="sxs-lookup"><span data-stu-id="02e7b-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02e7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02e7b-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02e7b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02e7b-105">DESCRIPTION</span></span>
<span data-ttu-id="02e7b-106">O cmdlet **Remove-AzureRmSqlElasticPool** exclui um pool elástico do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="02e7b-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="02e7b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02e7b-107">EXAMPLES</span></span>

### <span data-ttu-id="02e7b-108">Exemplo 1: excluir um pool elástico</span><span class="sxs-lookup"><span data-stu-id="02e7b-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="02e7b-109">Esse comando exclui um pool elástico chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="02e7b-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="02e7b-110">OS</span><span class="sxs-lookup"><span data-stu-id="02e7b-110">PARAMETERS</span></span>

### <span data-ttu-id="02e7b-111">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="02e7b-111">-ElasticPoolName</span></span>
<span data-ttu-id="02e7b-112">Especifica o nome do pool elástico que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="02e7b-112">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02e7b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="02e7b-113">-Force</span></span>
<span data-ttu-id="02e7b-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="02e7b-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e7b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02e7b-115">-ResourceGroupName</span></span>
<span data-ttu-id="02e7b-116">Especifica o nome do grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="02e7b-116">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="02e7b-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="02e7b-117">-ServerName</span></span>
<span data-ttu-id="02e7b-118">Especifica o nome do servidor que hospeda o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="02e7b-118">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="02e7b-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="02e7b-119">-Confirm</span></span>
<span data-ttu-id="02e7b-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02e7b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02e7b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02e7b-121">-WhatIf</span></span>
<span data-ttu-id="02e7b-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02e7b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02e7b-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02e7b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02e7b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e7b-124">-DefaultProfile</span></span>
<span data-ttu-id="02e7b-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02e7b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02e7b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e7b-126">CommonParameters</span></span>
<span data-ttu-id="02e7b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02e7b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e7b-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02e7b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e7b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02e7b-129">INPUTS</span></span>

### <span data-ttu-id="02e7b-130">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="02e7b-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="02e7b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02e7b-131">OUTPUTS</span></span>

### <span data-ttu-id="02e7b-132">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="02e7b-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="02e7b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02e7b-133">NOTES</span></span>

## <span data-ttu-id="02e7b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02e7b-134">RELATED LINKS</span></span>

[<span data-ttu-id="02e7b-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="02e7b-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="02e7b-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="02e7b-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="02e7b-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="02e7b-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="02e7b-138">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="02e7b-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="02e7b-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="02e7b-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="02e7b-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="02e7b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


