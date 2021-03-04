---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a8ad9a3925ccf1c0f56ce9be6a962d667f122307
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890566"
---
# <span data-ttu-id="f0940-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f0940-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="f0940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0940-102">SYNOPSIS</span></span>
<span data-ttu-id="f0940-103">Executa um failover de um Grupo de Failover de Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f0940-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="f0940-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f0940-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0940-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f0940-105">DESCRIPTION</span></span>
<span data-ttu-id="f0940-106">Esse comando troca as funções dos servidores em um Grupo de Failover e alterna todos os bancos de dados secundários para a função primária.</span><span class="sxs-lookup"><span data-stu-id="f0940-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="f0940-107">Todas as novas sessões TDS são automaticamente roteadas para o servidor secundário depois que o cache do cliente DNS é atualizado.</span><span class="sxs-lookup"><span data-stu-id="f0940-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="f0940-108">Quando o servidor primário original estiver novamente online, todos os bancos de dados primários anteriormente nele mudarão para a função secundária.</span><span class="sxs-lookup"><span data-stu-id="f0940-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="f0940-109">O servidor secundário do Grupo de Failover deve ser usado para executar esse comando.</span><span class="sxs-lookup"><span data-stu-id="f0940-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="f0940-110">Se o parâmetro AllowDataLoss não for especificado, esse comando aguardará até que ambas as funções sejam comutada.</span><span class="sxs-lookup"><span data-stu-id="f0940-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="f0940-111">Se o parâmetro AllowDataLoss for especificado, o comando aguardará apenas até que o novo primário assuma sua função.</span><span class="sxs-lookup"><span data-stu-id="f0940-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="f0940-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0940-112">EXAMPLES</span></span>

### <span data-ttu-id="f0940-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0940-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="f0940-114">Emitir uma operação de failover permitindo a perda de dados canalização no Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="f0940-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="f0940-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f0940-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="f0940-116">Emito uma melhor operação de failover de esforço que será bem-sucedida sem perder dados ou falhar e reverter.</span><span class="sxs-lookup"><span data-stu-id="f0940-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="f0940-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f0940-117">PARAMETERS</span></span>

### <span data-ttu-id="f0940-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="f0940-118">-AllowDataLoss</span></span>
<span data-ttu-id="f0940-119">Conclua o failover mesmo que isso possa resultar em perda de dados.</span><span class="sxs-lookup"><span data-stu-id="f0940-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="f0940-120">Isso permitirá que o failover prossiga mesmo se um banco de dados principal não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="f0940-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="f0940-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0940-121">-AsJob</span></span>
<span data-ttu-id="f0940-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f0940-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0940-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0940-123">-DefaultProfile</span></span>
<span data-ttu-id="f0940-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f0940-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0940-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="f0940-125">-FailoverGroupName</span></span>
<span data-ttu-id="f0940-126">O nome do Grupo de Failover SQL Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0940-126">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="f0940-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0940-127">-ResourceGroupName</span></span>
<span data-ttu-id="f0940-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f0940-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="f0940-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f0940-129">-ServerName</span></span>
<span data-ttu-id="f0940-130">O nome do Servidor de Banco de Dados do Azure SQL secundário do Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="f0940-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="f0940-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0940-131">-Confirm</span></span>
<span data-ttu-id="f0940-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0940-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0940-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0940-133">-WhatIf</span></span>
<span data-ttu-id="f0940-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f0940-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0940-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f0940-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0940-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0940-136">CommonParameters</span></span>
<span data-ttu-id="f0940-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0940-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0940-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0940-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0940-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0940-139">INPUTS</span></span>

### <span data-ttu-id="f0940-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f0940-140">System.String</span></span>

## <span data-ttu-id="f0940-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f0940-141">OUTPUTS</span></span>

### <span data-ttu-id="f0940-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f0940-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="f0940-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="f0940-143">NOTES</span></span>

## <span data-ttu-id="f0940-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0940-144">RELATED LINKS</span></span>

[<span data-ttu-id="f0940-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f0940-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f0940-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f0940-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f0940-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f0940-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f0940-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f0940-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="f0940-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f0940-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="f0940-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f0940-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f0940-151">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="f0940-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
