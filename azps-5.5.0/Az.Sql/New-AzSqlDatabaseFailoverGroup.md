---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: c1164f7c4875d6cdd00ca13236c1d8e6d4b07cb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114479"
---
# <span data-ttu-id="a9a7d-101">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a9a7d-101">New-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="a9a7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a7d-103">Esse comando cria um novo Grupo de Failover do Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-103">This command creates a new Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="a9a7d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9a7d-104">SYNTAX</span></span>

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9a7d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9a7d-105">DESCRIPTION</span></span>
<span data-ttu-id="a9a7d-106">Cria um novo Grupo de Failover de Banco de Dados SQL do Azure para os servidores especificados.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="a9a7d-107">Dois pontos de extremidade TDS do banco de dados SQL do Azure são criados em FailoverGroupName.SqlDatabaseDnsSuffix (por exemplo, FailoverGroupName.database.windows.net) e FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="a9a7d-108">Esses pontos de extremidade podem ser usados para se conectar aos servidores primários e secundários no Grupo de Failover, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="a9a7d-109">Se o servidor principal for afetado por uma interrupção, o failover automático dos pontos de extremidade e bancos de dados será disparado conforme determinado pela política de failover e pelo período de carência do Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="a9a7d-110">Os Grupos de Failover recém-criados não contêm bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="a9a7d-111">Para controlar o conjunto de bancos de dados em um Grupo de Failover, use os cmdlets 'Add-AzSqlDatabaseToFailoverGroup' e 'Remove-AzSqlDatabaseFromFailoverGroup'.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-111">To control the set of databases in a Failover Group, use the 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="a9a7d-112">Somente valores maiores ou iguais a 1 hora são suportados para o parâmetro '-GracePeriodWithDataLossHours'.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-112">Only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="a9a7d-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a9a7d-113">EXAMPLES</span></span>

### <span data-ttu-id="a9a7d-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9a7d-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="a9a7d-115">Esse comando cria um novo Grupo de Failover com a política de failover "Automático" para dois servidores no mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="a9a7d-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a9a7d-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="a9a7d-117">Esse comando cria um novo Grupo de Failover com a política de failover "Manual" para dois servidores em grupos de recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="a9a7d-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9a7d-118">PARAMETERS</span></span>

### <span data-ttu-id="a9a7d-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="a9a7d-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="a9a7d-120">Se uma interrupção no servidor secundário deve disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="a9a7d-121">Este recurso ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-121">This feature is not yet supported.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a7d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a7d-122">-DefaultProfile</span></span>
<span data-ttu-id="a9a7d-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a9a7d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9a7d-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a7d-124">-FailoverGroupName</span></span>
<span data-ttu-id="a9a7d-125">O nome do Grupo de Failover de Banco de Dados SQL do Azure a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-125">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a7d-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="a9a7d-126">-FailoverPolicy</span></span>
<span data-ttu-id="a9a7d-127">A política de failover do Grupo failover de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a7d-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="a9a7d-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="a9a7d-129">Intervalo antes de o failover automático ser iniciado se ocorrer uma falha no servidor principal e o failover não puder ser concluído sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a7d-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a7d-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="a9a7d-131">O nome do grupo de recursos secundário do Grupo failover de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a7d-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="a9a7d-132">-PartnerServerName</span></span>
<span data-ttu-id="a9a7d-133">O nome do servidor secundário do Grupo failover de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a7d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a7d-134">-ResourceGroupName</span></span>
<span data-ttu-id="a9a7d-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="a9a7d-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9a7d-136">-ServerName</span></span>
<span data-ttu-id="a9a7d-137">O nome do servidor de banco de dados SQL principal do Azure do Grupo failover.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="a9a7d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a7d-138">CommonParameters</span></span>
<span data-ttu-id="a9a7d-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9a7d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a7d-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9a7d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a7d-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="a9a7d-141">INPUTS</span></span>

### <span data-ttu-id="a9a7d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a9a7d-142">System.String</span></span>

## <span data-ttu-id="a9a7d-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="a9a7d-143">OUTPUTS</span></span>

### <span data-ttu-id="a9a7d-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="a9a7d-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="a9a7d-145">Notas</span><span class="sxs-lookup"><span data-stu-id="a9a7d-145">NOTES</span></span>

## <span data-ttu-id="a9a7d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9a7d-146">RELATED LINKS</span></span>

[<span data-ttu-id="a9a7d-147">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a9a7d-147">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a9a7d-148">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a9a7d-148">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a9a7d-149">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a9a7d-149">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="a9a7d-150">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a9a7d-150">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="a9a7d-151">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a9a7d-151">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a9a7d-152">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a9a7d-152">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a9a7d-153">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="a9a7d-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
