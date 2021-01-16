---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: d751954a5c66d9220513017aa62b6797f8f1ea6f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98264702"
---
# <span data-ttu-id="c33b1-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c33b1-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="c33b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c33b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c33b1-103">Exclui um pool de banco de dados elástico.</span><span class="sxs-lookup"><span data-stu-id="c33b1-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="c33b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c33b1-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c33b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c33b1-105">DESCRIPTION</span></span>
<span data-ttu-id="c33b1-106">O cmdlet **Remove-AzSqlElasticPool** exclui um pool elástico do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c33b1-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="c33b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c33b1-107">EXAMPLES</span></span>

### <span data-ttu-id="c33b1-108">Exemplo 1: excluir um pool elástico</span><span class="sxs-lookup"><span data-stu-id="c33b1-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="c33b1-109">Esse comando exclui um pool elástico chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="c33b1-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="c33b1-110">OS</span><span class="sxs-lookup"><span data-stu-id="c33b1-110">PARAMETERS</span></span>

### <span data-ttu-id="c33b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c33b1-111">-DefaultProfile</span></span>
<span data-ttu-id="c33b1-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c33b1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c33b1-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c33b1-113">-ElasticPoolName</span></span>
<span data-ttu-id="c33b1-114">Especifica o nome do pool elástico que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="c33b1-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c33b1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c33b1-115">-Force</span></span>
<span data-ttu-id="c33b1-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c33b1-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c33b1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c33b1-117">-ResourceGroupName</span></span>
<span data-ttu-id="c33b1-118">Especifica o nome do grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="c33b1-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="c33b1-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c33b1-119">-ServerName</span></span>
<span data-ttu-id="c33b1-120">Especifica o nome do servidor que hospeda o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="c33b1-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="c33b1-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c33b1-121">-Confirm</span></span>
<span data-ttu-id="c33b1-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c33b1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c33b1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c33b1-123">-WhatIf</span></span>
<span data-ttu-id="c33b1-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c33b1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c33b1-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c33b1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c33b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33b1-126">CommonParameters</span></span>
<span data-ttu-id="c33b1-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c33b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33b1-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c33b1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33b1-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c33b1-129">INPUTS</span></span>

### <span data-ttu-id="c33b1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c33b1-130">System.String</span></span>

## <span data-ttu-id="c33b1-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c33b1-131">OUTPUTS</span></span>

### <span data-ttu-id="c33b1-132">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="c33b1-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="c33b1-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c33b1-133">NOTES</span></span>

## <span data-ttu-id="c33b1-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c33b1-134">RELATED LINKS</span></span>

[<span data-ttu-id="c33b1-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c33b1-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="c33b1-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="c33b1-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="c33b1-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="c33b1-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="c33b1-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c33b1-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="c33b1-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c33b1-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="c33b1-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="c33b1-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


