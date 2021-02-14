---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: d8eff694378f6145931a18a622f29bf88d99e1ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115690"
---
# <span data-ttu-id="40e9f-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="40e9f-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="40e9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="40e9f-103">Executa um failover de um Grupo failover de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="40e9f-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="40e9f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40e9f-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40e9f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="40e9f-105">DESCRIPTION</span></span>
<span data-ttu-id="40e9f-106">Esse comando troca as funções dos servidores em um Grupo de Failover e alterna todos os bancos de dados secundários para a função principal.</span><span class="sxs-lookup"><span data-stu-id="40e9f-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="40e9f-107">Todas as novas sessões TDS são automaticamente roteadas para o servidor secundário depois que o cache do cliente DNS é atualizado.</span><span class="sxs-lookup"><span data-stu-id="40e9f-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="40e9f-108">Quando o servidor principal original estiver novamente online, todos os bancos de dados primários anteriormente nele mudarão para a função secundária.</span><span class="sxs-lookup"><span data-stu-id="40e9f-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="40e9f-109">O servidor secundário do Grupo de Failover deve ser usado para executar esse comando.</span><span class="sxs-lookup"><span data-stu-id="40e9f-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="40e9f-110">Se o parâmetro AllowDataLoss não for especificado, esse comando aguardará até que ambas as funções sejam trocadas.</span><span class="sxs-lookup"><span data-stu-id="40e9f-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="40e9f-111">Se o parâmetro AllowDataLoss for especificado, o comando só aguardará até que o novo principal assuma sua função.</span><span class="sxs-lookup"><span data-stu-id="40e9f-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="40e9f-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="40e9f-112">EXAMPLES</span></span>

### <span data-ttu-id="40e9f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40e9f-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="40e9f-114">Emissão de uma operação de failover permitindo a perda de dados por meio de uma piping no Grupo failover.</span><span class="sxs-lookup"><span data-stu-id="40e9f-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="40e9f-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="40e9f-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="40e9f-116">Eme uma melhor operação de failover de esforço que seja bem-sucedida sem perder dados ou falhar e reverter.</span><span class="sxs-lookup"><span data-stu-id="40e9f-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="40e9f-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40e9f-117">PARAMETERS</span></span>

### <span data-ttu-id="40e9f-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="40e9f-118">-AllowDataLoss</span></span>
<span data-ttu-id="40e9f-119">Conclua o failover mesmo que isso possa resultar em perda de dados.</span><span class="sxs-lookup"><span data-stu-id="40e9f-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="40e9f-120">Isso permitirá que o failover prossiga mesmo se um banco de dados principal não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="40e9f-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="40e9f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40e9f-121">-AsJob</span></span>
<span data-ttu-id="40e9f-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="40e9f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40e9f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e9f-123">-DefaultProfile</span></span>
<span data-ttu-id="40e9f-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="40e9f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40e9f-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="40e9f-125">-FailoverGroupName</span></span>
<span data-ttu-id="40e9f-126">O nome do Grupo failover de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="40e9f-126">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="40e9f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e9f-127">-ResourceGroupName</span></span>
<span data-ttu-id="40e9f-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40e9f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="40e9f-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="40e9f-129">-ServerName</span></span>
<span data-ttu-id="40e9f-130">O nome do Servidor de Banco de Dados SQL secundário do Azure do Grupo failover.</span><span class="sxs-lookup"><span data-stu-id="40e9f-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="40e9f-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="40e9f-131">-Confirm</span></span>
<span data-ttu-id="40e9f-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40e9f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40e9f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e9f-133">-WhatIf</span></span>
<span data-ttu-id="40e9f-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="40e9f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40e9f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40e9f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40e9f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e9f-136">CommonParameters</span></span>
<span data-ttu-id="40e9f-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e9f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e9f-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40e9f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e9f-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="40e9f-139">INPUTS</span></span>

### <span data-ttu-id="40e9f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="40e9f-140">System.String</span></span>

## <span data-ttu-id="40e9f-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="40e9f-141">OUTPUTS</span></span>

### <span data-ttu-id="40e9f-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="40e9f-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="40e9f-143">Notas</span><span class="sxs-lookup"><span data-stu-id="40e9f-143">NOTES</span></span>

## <span data-ttu-id="40e9f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40e9f-144">RELATED LINKS</span></span>

[<span data-ttu-id="40e9f-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="40e9f-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="40e9f-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="40e9f-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="40e9f-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="40e9f-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="40e9f-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="40e9f-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="40e9f-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="40e9f-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="40e9f-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="40e9f-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="40e9f-151">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="40e9f-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
