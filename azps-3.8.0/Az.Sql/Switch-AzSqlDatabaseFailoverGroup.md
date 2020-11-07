---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 40488a196afb35cbce4bda323b52a17c105ab649
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777971"
---
# <span data-ttu-id="3f02d-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f02d-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="3f02d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f02d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f02d-103">Executa um failover de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f02d-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="3f02d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f02d-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f02d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f02d-105">DESCRIPTION</span></span>
<span data-ttu-id="3f02d-106">Esse comando troca as funções dos servidores em um grupo de failover e alterna todos os bancos de dados secundários para a função primária.</span><span class="sxs-lookup"><span data-stu-id="3f02d-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="3f02d-107">Todas as novas sessões TDS são automaticamente redirecionadas para o servidor secundário após a atualização do cache do cliente DNS.</span><span class="sxs-lookup"><span data-stu-id="3f02d-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="3f02d-108">Quando o servidor primário original estiver novamente online, todos os bancos de dados primários anteriormente serão alternados para a função secundária.</span><span class="sxs-lookup"><span data-stu-id="3f02d-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="3f02d-109">O servidor secundário do grupo de failover deve ser usado para executar este comando.</span><span class="sxs-lookup"><span data-stu-id="3f02d-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="3f02d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f02d-110">EXAMPLES</span></span>

### <span data-ttu-id="3f02d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f02d-111">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="3f02d-112">Emita uma operação de failover que permita a perda de dados por meio do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="3f02d-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="3f02d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3f02d-113">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="3f02d-114">Emita uma melhor operação de failover de esforço que será bem-sucedida sem perder dados ou falhar e reverter.</span><span class="sxs-lookup"><span data-stu-id="3f02d-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="3f02d-115">OS</span><span class="sxs-lookup"><span data-stu-id="3f02d-115">PARAMETERS</span></span>

### <span data-ttu-id="3f02d-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="3f02d-116">-AllowDataLoss</span></span>
<span data-ttu-id="3f02d-117">Conclua o failover mesmo se fizer isso pode resultar em perda de dados.</span><span class="sxs-lookup"><span data-stu-id="3f02d-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="3f02d-118">Isso permitirá que o failover prossiga mesmo se um banco de dados primário estiver indisponível.</span><span class="sxs-lookup"><span data-stu-id="3f02d-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f02d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f02d-119">-AsJob</span></span>
<span data-ttu-id="3f02d-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3f02d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f02d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f02d-121">-DefaultProfile</span></span>
<span data-ttu-id="3f02d-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3f02d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f02d-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="3f02d-123">-FailoverGroupName</span></span>
<span data-ttu-id="3f02d-124">O nome do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f02d-124">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f02d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f02d-125">-ResourceGroupName</span></span>
<span data-ttu-id="3f02d-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f02d-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f02d-127">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="3f02d-127">-ServerName</span></span>
<span data-ttu-id="3f02d-128">O nome do servidor de banco de dados SQL do Azure secundário do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="3f02d-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="3f02d-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3f02d-129">-Confirm</span></span>
<span data-ttu-id="3f02d-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f02d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f02d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f02d-131">-WhatIf</span></span>
<span data-ttu-id="3f02d-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3f02d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f02d-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f02d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f02d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f02d-134">CommonParameters</span></span>
<span data-ttu-id="3f02d-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f02d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f02d-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f02d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f02d-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f02d-137">INPUTS</span></span>

### <span data-ttu-id="3f02d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3f02d-138">System.String</span></span>

## <span data-ttu-id="3f02d-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f02d-139">OUTPUTS</span></span>

### <span data-ttu-id="3f02d-140">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="3f02d-140">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="3f02d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f02d-141">NOTES</span></span>

## <span data-ttu-id="3f02d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f02d-142">RELATED LINKS</span></span>

[<span data-ttu-id="3f02d-143">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f02d-143">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3f02d-144">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f02d-144">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3f02d-145">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f02d-145">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3f02d-146">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f02d-146">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="3f02d-147">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f02d-147">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="3f02d-148">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3f02d-148">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3f02d-149">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="3f02d-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
