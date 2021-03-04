---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: be1f2fc5c0aa2abda5f036580e377f05b26c2eb2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888424"
---
# <span data-ttu-id="f557b-101">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f557b-101">New-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="f557b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f557b-102">SYNOPSIS</span></span>
<span data-ttu-id="f557b-103">Este comando cria um novo Grupo de Failover SQL Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="f557b-103">This command creates a new Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="f557b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f557b-104">SYNTAX</span></span>

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f557b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f557b-105">DESCRIPTION</span></span>
<span data-ttu-id="f557b-106">Cria um novo Grupo SQL Failover de Banco de Dados do Azure para os servidores especificados.</span><span class="sxs-lookup"><span data-stu-id="f557b-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="f557b-107">Dois pontos de extremidade do Azure SQL Database TDS são criados em FailoverGroupName.SqlDatabaseDnsSuffix (por exemplo, FailoverGroupName.database.windows.net) e FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="f557b-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="f557b-108">Esses pontos de extremidade podem ser usados para se conectar aos servidores primários e secundários no Grupo de Failover, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f557b-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="f557b-109">Se o servidor principal for afetado por uma interrupção, o failover automático dos pontos de extremidade e bancos de dados será acionado conforme ditado pela política de failover e o período de carência do Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="f557b-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="f557b-110">Os Grupos de Failover recém-criados não contêm bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="f557b-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="f557b-111">Para controlar o conjunto de bancos de dados em um Grupo de Failover, use os cmdlets 'Add-AzSqlDatabaseToFailoverGroup' e 'Remove-AzSqlDatabaseFromFailoverGroup'.</span><span class="sxs-lookup"><span data-stu-id="f557b-111">To control the set of databases in a Failover Group, use the 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="f557b-112">Somente valores maiores ou iguais a 1 hora são suportados para o parâmetro '-GracePeriodWithDataLossHours'.</span><span class="sxs-lookup"><span data-stu-id="f557b-112">Only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="f557b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f557b-113">EXAMPLES</span></span>

### <span data-ttu-id="f557b-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f557b-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="f557b-115">Este comando cria um novo Grupo de Failover com a política de failover 'Automatic' para dois servidores no mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f557b-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="f557b-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f557b-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="f557b-117">Este comando cria um novo Grupo de Failover com a política de failover 'Manual' para dois servidores em grupos de recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="f557b-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="f557b-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f557b-118">PARAMETERS</span></span>

### <span data-ttu-id="f557b-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="f557b-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="f557b-120">Se uma interrupção no servidor secundário deve disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f557b-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="f557b-121">Esse recurso ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="f557b-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="f557b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f557b-122">-DefaultProfile</span></span>
<span data-ttu-id="f557b-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f557b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f557b-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="f557b-124">-FailoverGroupName</span></span>
<span data-ttu-id="f557b-125">O nome do Grupo de Failover do Banco de Dados do Azure SQL a ser criado.</span><span class="sxs-lookup"><span data-stu-id="f557b-125">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="f557b-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="f557b-126">-FailoverPolicy</span></span>
<span data-ttu-id="f557b-127">A política de failover do Grupo de Failover SQL Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="f557b-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="f557b-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="f557b-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="f557b-129">Intervalo antes que o failover automático seja iniciado se ocorrer uma paralisação no servidor primário e o failover não puder ser concluído sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="f557b-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="f557b-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f557b-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="f557b-131">O nome do grupo de recursos secundário do Grupo de Failover de Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f557b-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="f557b-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="f557b-132">-PartnerServerName</span></span>
<span data-ttu-id="f557b-133">O nome do servidor secundário do Grupo de Failover de Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f557b-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="f557b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f557b-134">-ResourceGroupName</span></span>
<span data-ttu-id="f557b-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f557b-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="f557b-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f557b-136">-ServerName</span></span>
<span data-ttu-id="f557b-137">O nome do Servidor de Banco de Dados do Azure SQL principal do Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="f557b-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="f557b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f557b-138">CommonParameters</span></span>
<span data-ttu-id="f557b-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f557b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f557b-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f557b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f557b-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f557b-141">INPUTS</span></span>

### <span data-ttu-id="f557b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f557b-142">System.String</span></span>

## <span data-ttu-id="f557b-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f557b-143">OUTPUTS</span></span>

### <span data-ttu-id="f557b-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f557b-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="f557b-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="f557b-145">NOTES</span></span>

## <span data-ttu-id="f557b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f557b-146">RELATED LINKS</span></span>

[<span data-ttu-id="f557b-147">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f557b-147">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f557b-148">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f557b-148">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f557b-149">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f557b-149">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="f557b-150">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f557b-150">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="f557b-151">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f557b-151">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f557b-152">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f557b-152">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f557b-153">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="f557b-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
