---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: ee12c80843433200d6bf48818665156830cf2941
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429953"
---
# <span data-ttu-id="4af9d-101">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4af9d-101">New-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="4af9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4af9d-102">SYNOPSIS</span></span>
<span data-ttu-id="4af9d-103">Esse comando cria um novo grupo de failover de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4af9d-103">This command creates a new Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4af9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4af9d-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4af9d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4af9d-105">DESCRIPTION</span></span>
<span data-ttu-id="4af9d-106">Cria um novo grupo de failover de banco de dados SQL do Azure para os servidores especificados.</span><span class="sxs-lookup"><span data-stu-id="4af9d-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>

<span data-ttu-id="4af9d-107">Dois pontos de extremidade TDS do banco de dados SQL do Azure são criados em FailoverGroupName. SqlDatabaseDnsSuffix (por exemplo, FailoverGroupName.database.windows.net) e FailoverGroupName. secundário. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="4af9d-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="4af9d-108">Esses pontos de extremidade podem ser usados para conexão com os servidores primários e secundários do grupo de failover, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4af9d-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="4af9d-109">Se o servidor primário for afetado por uma interrupção, o failover automático dos pontos de extremidade e dos bancos de dados será disparado conforme determinado pela política de failover do grupo de failover e pelo período de carência.</span><span class="sxs-lookup"><span data-stu-id="4af9d-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="4af9d-110">Os grupos de failover recém criados não contêm bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="4af9d-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="4af9d-111">Para controlar o conjunto de bancos de dados em um grupo de failover, use os cmdlets ' Add-AzureRmSqlDatabaseToFailoverGroup ' e ' remove-AzureRmSqlDatabaseFromFailoverGroup '.</span><span class="sxs-lookup"><span data-stu-id="4af9d-111">To control the set of databases in a Failover Group, use the 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' cmdlets.</span></span>

<span data-ttu-id="4af9d-112">Durante a visualização do recurso de grupos de failover, somente os valores maiores que ou iguais a 1 hora são compatíveis com o parâmetro '-GracePeriodWithDataLossHours '.</span><span class="sxs-lookup"><span data-stu-id="4af9d-112">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="4af9d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4af9d-113">EXAMPLES</span></span>

### <span data-ttu-id="4af9d-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4af9d-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="4af9d-115">Esse comando cria um novo grupo de failover com a política de failover ' automático ' para dois servidores no mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4af9d-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="4af9d-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4af9d-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="4af9d-117">Esse comando cria um novo grupo de failover com a política de failover ' manual ' para dois servidores em diferentes grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="4af9d-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="4af9d-118">OS</span><span class="sxs-lookup"><span data-stu-id="4af9d-118">PARAMETERS</span></span>

### <span data-ttu-id="4af9d-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="4af9d-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="4af9d-120">Se uma interrupção no servidor secundário deve disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4af9d-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="4af9d-121">Este recurso ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="4af9d-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="4af9d-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="4af9d-122">-FailoverGroupName</span></span>
<span data-ttu-id="4af9d-123">O nome do grupo de failover de banco de dados SQL do Azure a ser criado.</span><span class="sxs-lookup"><span data-stu-id="4af9d-123">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="4af9d-124">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="4af9d-124">-FailoverPolicy</span></span>
<span data-ttu-id="4af9d-125">A política de failover do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4af9d-125">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="4af9d-126">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="4af9d-126">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="4af9d-127">Intervalo antes do failover automático será iniciado se ocorrer uma falha no servidor primário e o failover não puder ser concluído sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="4af9d-127">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="4af9d-128">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4af9d-128">-PartnerResourceGroupName</span></span>
<span data-ttu-id="4af9d-129">O nome do grupo de recursos secundário do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4af9d-129">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="4af9d-130">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="4af9d-130">-PartnerServerName</span></span>
<span data-ttu-id="4af9d-131">O nome do servidor secundário do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4af9d-131">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="4af9d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4af9d-132">-ResourceGroupName</span></span>
<span data-ttu-id="4af9d-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4af9d-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="4af9d-134">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4af9d-134">-ServerName</span></span>
<span data-ttu-id="4af9d-135">O nome do servidor de banco de dados SQL do Azure principal do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="4af9d-135">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="4af9d-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af9d-136">-DefaultProfile</span></span>
<span data-ttu-id="4af9d-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4af9d-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4af9d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af9d-138">CommonParameters</span></span>
<span data-ttu-id="4af9d-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4af9d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af9d-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4af9d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af9d-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4af9d-141">INPUTS</span></span>

### <span data-ttu-id="4af9d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4af9d-142">System.String</span></span>

## <span data-ttu-id="4af9d-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4af9d-143">OUTPUTS</span></span>

### <span data-ttu-id="4af9d-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="4af9d-144">System.Object</span></span>

## <span data-ttu-id="4af9d-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4af9d-145">NOTES</span></span>

## <span data-ttu-id="4af9d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4af9d-146">RELATED LINKS</span></span>

[<span data-ttu-id="4af9d-147">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4af9d-147">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4af9d-148">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4af9d-148">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4af9d-149">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4af9d-149">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="4af9d-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4af9d-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="4af9d-151">Botão de AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4af9d-151">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4af9d-152">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4af9d-152">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4af9d-153">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4af9d-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)