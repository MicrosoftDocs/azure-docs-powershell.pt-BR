---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 43723efe8e04a7913ca84f08927afd4757102801
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773850"
---
# <span data-ttu-id="f25cd-101">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f25cd-101">New-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="f25cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f25cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f25cd-103">Esse comando cria um novo grupo de failover de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f25cd-103">This command creates a new Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="f25cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f25cd-104">SYNTAX</span></span>

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f25cd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f25cd-105">DESCRIPTION</span></span>
<span data-ttu-id="f25cd-106">Cria um novo grupo de failover de banco de dados SQL do Azure para os servidores especificados.</span><span class="sxs-lookup"><span data-stu-id="f25cd-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="f25cd-107">Dois pontos de extremidade TDS do banco de dados SQL do Azure são criados em FailoverGroupName. SqlDatabaseDnsSuffix (por exemplo, FailoverGroupName.database.windows.net) e FailoverGroupName. secundário. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="f25cd-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="f25cd-108">Esses pontos de extremidade podem ser usados para conexão com os servidores primários e secundários do grupo de failover, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f25cd-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="f25cd-109">Se o servidor primário for afetado por uma interrupção, o failover automático dos pontos de extremidade e dos bancos de dados será disparado conforme determinado pela política de failover do grupo de failover e pelo período de carência.</span><span class="sxs-lookup"><span data-stu-id="f25cd-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="f25cd-110">Os grupos de failover recém criados não contêm bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="f25cd-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="f25cd-111">Para controlar o conjunto de bancos de dados em um grupo de failover, use os cmdlets ' Add-AzSqlDatabaseToFailoverGroup ' e ' remove-AzSqlDatabaseFromFailoverGroup '.</span><span class="sxs-lookup"><span data-stu-id="f25cd-111">To control the set of databases in a Failover Group, use the 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="f25cd-112">Apenas valores maiores que ou iguais a 1 hora têm suporte para o parâmetro '-GracePeriodWithDataLossHours '.</span><span class="sxs-lookup"><span data-stu-id="f25cd-112">Only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="f25cd-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f25cd-113">EXAMPLES</span></span>

### <span data-ttu-id="f25cd-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f25cd-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="f25cd-115">Esse comando cria um novo grupo de failover com a política de failover ' automático ' para dois servidores no mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f25cd-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="f25cd-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f25cd-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="f25cd-117">Esse comando cria um novo grupo de failover com a política de failover ' manual ' para dois servidores em diferentes grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="f25cd-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="f25cd-118">OS</span><span class="sxs-lookup"><span data-stu-id="f25cd-118">PARAMETERS</span></span>

### <span data-ttu-id="f25cd-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="f25cd-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="f25cd-120">Se uma interrupção no servidor secundário deve disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f25cd-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="f25cd-121">Este recurso ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="f25cd-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="f25cd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f25cd-122">-DefaultProfile</span></span>
<span data-ttu-id="f25cd-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f25cd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f25cd-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="f25cd-124">-FailoverGroupName</span></span>
<span data-ttu-id="f25cd-125">O nome do grupo de failover de banco de dados SQL do Azure a ser criado.</span><span class="sxs-lookup"><span data-stu-id="f25cd-125">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="f25cd-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="f25cd-126">-FailoverPolicy</span></span>
<span data-ttu-id="f25cd-127">A política de failover do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f25cd-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="f25cd-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="f25cd-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="f25cd-129">Intervalo antes do failover automático será iniciado se ocorrer uma falha no servidor primário e o failover não puder ser concluído sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="f25cd-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="f25cd-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f25cd-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="f25cd-131">O nome do grupo de recursos secundário do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f25cd-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="f25cd-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="f25cd-132">-PartnerServerName</span></span>
<span data-ttu-id="f25cd-133">O nome do servidor secundário do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f25cd-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="f25cd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f25cd-134">-ResourceGroupName</span></span>
<span data-ttu-id="f25cd-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f25cd-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="f25cd-136">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f25cd-136">-ServerName</span></span>
<span data-ttu-id="f25cd-137">O nome do servidor de banco de dados SQL do Azure principal do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="f25cd-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="f25cd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f25cd-138">CommonParameters</span></span>
<span data-ttu-id="f25cd-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f25cd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f25cd-140">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f25cd-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f25cd-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f25cd-141">INPUTS</span></span>

### <span data-ttu-id="f25cd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f25cd-142">System.String</span></span>

## <span data-ttu-id="f25cd-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f25cd-143">OUTPUTS</span></span>

### <span data-ttu-id="f25cd-144">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f25cd-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="f25cd-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f25cd-145">NOTES</span></span>

## <span data-ttu-id="f25cd-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f25cd-146">RELATED LINKS</span></span>

[<span data-ttu-id="f25cd-147">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f25cd-147">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f25cd-148">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f25cd-148">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f25cd-149">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f25cd-149">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="f25cd-150">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f25cd-150">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="f25cd-151">Botão de AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f25cd-151">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f25cd-152">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f25cd-152">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f25cd-153">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f25cd-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
