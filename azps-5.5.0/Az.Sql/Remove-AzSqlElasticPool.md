---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: d751954a5c66d9220513017aa62b6797f8f1ea6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116137"
---
# <span data-ttu-id="cceb5-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="cceb5-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="cceb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cceb5-102">SYNOPSIS</span></span>
<span data-ttu-id="cceb5-103">Exclui um pool de banco de dados elástica.</span><span class="sxs-lookup"><span data-stu-id="cceb5-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="cceb5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cceb5-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cceb5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="cceb5-105">DESCRIPTION</span></span>
<span data-ttu-id="cceb5-106">O cmdlet **Remove-AzSqlElasticPool** exclui um pool elástica do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cceb5-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="cceb5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cceb5-107">EXAMPLES</span></span>

### <span data-ttu-id="cceb5-108">Exemplo 1: Excluir um pool elástica</span><span class="sxs-lookup"><span data-stu-id="cceb5-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="cceb5-109">Esse comando exclui um pool elástica chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="cceb5-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="cceb5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cceb5-110">PARAMETERS</span></span>

### <span data-ttu-id="cceb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cceb5-111">-DefaultProfile</span></span>
<span data-ttu-id="cceb5-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="cceb5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cceb5-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="cceb5-113">-ElasticPoolName</span></span>
<span data-ttu-id="cceb5-114">Especifica o nome do pool elástica que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="cceb5-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="cceb5-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="cceb5-115">-Force</span></span>
<span data-ttu-id="cceb5-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="cceb5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cceb5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cceb5-117">-ResourceGroupName</span></span>
<span data-ttu-id="cceb5-118">Especifica o nome do grupo de recursos ao qual o pool elástica é atribuído.</span><span class="sxs-lookup"><span data-stu-id="cceb5-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="cceb5-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cceb5-119">-ServerName</span></span>
<span data-ttu-id="cceb5-120">Especifica o nome do servidor que hospeda o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="cceb5-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="cceb5-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cceb5-121">-Confirm</span></span>
<span data-ttu-id="cceb5-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cceb5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cceb5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cceb5-123">-WhatIf</span></span>
<span data-ttu-id="cceb5-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cceb5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cceb5-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cceb5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cceb5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cceb5-126">CommonParameters</span></span>
<span data-ttu-id="cceb5-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cceb5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cceb5-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cceb5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cceb5-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="cceb5-129">INPUTS</span></span>

### <span data-ttu-id="cceb5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cceb5-130">System.String</span></span>

## <span data-ttu-id="cceb5-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="cceb5-131">OUTPUTS</span></span>

### <span data-ttu-id="cceb5-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="cceb5-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="cceb5-133">Notas</span><span class="sxs-lookup"><span data-stu-id="cceb5-133">NOTES</span></span>

## <span data-ttu-id="cceb5-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cceb5-134">RELATED LINKS</span></span>

[<span data-ttu-id="cceb5-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="cceb5-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="cceb5-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="cceb5-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="cceb5-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="cceb5-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="cceb5-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="cceb5-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="cceb5-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="cceb5-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="cceb5-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="cceb5-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


