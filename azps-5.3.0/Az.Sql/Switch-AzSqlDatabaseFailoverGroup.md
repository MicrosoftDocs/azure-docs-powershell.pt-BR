---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: d8eff694378f6145931a18a622f29bf88d99e1ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428463"
---
# <span data-ttu-id="ff753-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ff753-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="ff753-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff753-102">SYNOPSIS</span></span>
<span data-ttu-id="ff753-103">Executa um failover de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff753-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="ff753-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff753-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff753-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff753-105">DESCRIPTION</span></span>
<span data-ttu-id="ff753-106">Esse comando troca as funções dos servidores em um grupo de failover e alterna todos os bancos de dados secundários para a função primária.</span><span class="sxs-lookup"><span data-stu-id="ff753-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="ff753-107">Todas as novas sessões TDS são automaticamente redirecionadas para o servidor secundário após a atualização do cache do cliente DNS.</span><span class="sxs-lookup"><span data-stu-id="ff753-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="ff753-108">Quando o servidor primário original estiver novamente online, todos os bancos de dados primários anteriormente serão alternados para a função secundária.</span><span class="sxs-lookup"><span data-stu-id="ff753-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="ff753-109">O servidor secundário do grupo de failover deve ser usado para executar este comando.</span><span class="sxs-lookup"><span data-stu-id="ff753-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="ff753-110">Se o parâmetro AllowDataLoss não for especificado, esse comando aguardará até ambas as funções serem trocadas.</span><span class="sxs-lookup"><span data-stu-id="ff753-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="ff753-111">Se o parâmetro AllowDataLoss for especificado, o comando só aguardará até que a nova primária assuma sua função.</span><span class="sxs-lookup"><span data-stu-id="ff753-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="ff753-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff753-112">EXAMPLES</span></span>

### <span data-ttu-id="ff753-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ff753-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="ff753-114">Emita uma operação de failover que permita a perda de dados por meio do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="ff753-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="ff753-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ff753-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="ff753-116">Emita uma melhor operação de failover de esforço que será bem-sucedida sem perder dados ou falhar e reverter.</span><span class="sxs-lookup"><span data-stu-id="ff753-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="ff753-117">OS</span><span class="sxs-lookup"><span data-stu-id="ff753-117">PARAMETERS</span></span>

### <span data-ttu-id="ff753-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="ff753-118">-AllowDataLoss</span></span>
<span data-ttu-id="ff753-119">Conclua o failover mesmo se fizer isso pode resultar em perda de dados.</span><span class="sxs-lookup"><span data-stu-id="ff753-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="ff753-120">Isso permitirá que o failover prossiga mesmo se um banco de dados primário estiver indisponível.</span><span class="sxs-lookup"><span data-stu-id="ff753-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="ff753-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff753-121">-AsJob</span></span>
<span data-ttu-id="ff753-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ff753-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff753-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff753-123">-DefaultProfile</span></span>
<span data-ttu-id="ff753-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ff753-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff753-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="ff753-125">-FailoverGroupName</span></span>
<span data-ttu-id="ff753-126">O nome do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff753-126">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="ff753-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff753-127">-ResourceGroupName</span></span>
<span data-ttu-id="ff753-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff753-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="ff753-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ff753-129">-ServerName</span></span>
<span data-ttu-id="ff753-130">O nome do servidor de banco de dados SQL do Azure secundário do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="ff753-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="ff753-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ff753-131">-Confirm</span></span>
<span data-ttu-id="ff753-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff753-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff753-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff753-133">-WhatIf</span></span>
<span data-ttu-id="ff753-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff753-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff753-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff753-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff753-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff753-136">CommonParameters</span></span>
<span data-ttu-id="ff753-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff753-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff753-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff753-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff753-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff753-139">INPUTS</span></span>

### <span data-ttu-id="ff753-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ff753-140">System.String</span></span>

## <span data-ttu-id="ff753-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff753-141">OUTPUTS</span></span>

### <span data-ttu-id="ff753-142">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ff753-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="ff753-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff753-143">NOTES</span></span>

## <span data-ttu-id="ff753-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff753-144">RELATED LINKS</span></span>

[<span data-ttu-id="ff753-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ff753-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ff753-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ff753-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ff753-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ff753-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ff753-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ff753-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="ff753-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ff753-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="ff753-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ff753-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ff753-151">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ff753-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
