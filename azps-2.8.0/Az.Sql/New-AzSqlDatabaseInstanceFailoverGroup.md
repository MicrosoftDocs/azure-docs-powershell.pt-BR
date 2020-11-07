---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 04ed033559abe6fe6a60922f7b11a498ff4026bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773844"
---
# <span data-ttu-id="c2b0e-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c2b0e-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="c2b0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b0e-103">Esse comando cria um novo grupo de failover de instância de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="c2b0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2b0e-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup -Name <String> [-PartnerResourceGroupName <String>] [-PartnerSubscriptionId <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2b0e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2b0e-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b0e-106">Cria um novo grupo de failover de instância de banco de dados SQL do Azure entre as regiões especificadas com o par de instâncias gerenciadas observada.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="c2b0e-107">Dois pontos de extremidade TDS do banco de dados SQL do Azure são criados em Name. SqlDatabaseDnsSuffix (por exemplo, Name.database.windows.net) e Name. Secondary. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="c2b0e-108">Esses pontos de extremidade podem ser usados para conectar-se às regiões primárias e secundárias do grupo de failover, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="c2b0e-109">Se a região primária for afetada por uma interrupção, o failover automático dos pontos de extremidade e bancos de dados será disparado conforme determinado pela política de failover do grupo de failover de instância e do período de cortesia.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="c2b0e-110">Durante a visualização do recurso de grupos de failover de instância, somente os valores maiores que ou iguais a 1 hora têm suporte para o parâmetro '-GracePeriodWithDataLossHours '.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="c2b0e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2b0e-111">EXAMPLES</span></span>

### <span data-ttu-id="c2b0e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c2b0e-112">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="c2b0e-113">Esse comando cria um novo grupo de failover de instância com a política de failover ' automático ' para o par de instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="c2b0e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c2b0e-114">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Manual
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="c2b0e-115">Esse comando cria um novo grupo de failover de instância com a política de failover ' manual ' para o par de instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

## <span data-ttu-id="c2b0e-116">OS</span><span class="sxs-lookup"><span data-stu-id="c2b0e-116">PARAMETERS</span></span>

### <span data-ttu-id="c2b0e-117">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="c2b0e-117">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="c2b0e-118">Se uma interrupção no servidor secundário deve disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-118">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="c2b0e-119">Este recurso ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-119">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b0e-120">-DefaultProfile</span></span>
<span data-ttu-id="c2b0e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="c2b0e-122">-FailoverPolicy</span></span>
<span data-ttu-id="c2b0e-123">A política de failover do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-123">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="c2b0e-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="c2b0e-125">Intervalo antes do failover automático será iniciado se ocorrer uma falha no servidor primário e o failover não puder ser concluído sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-125">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-126">-Local</span><span class="sxs-lookup"><span data-stu-id="c2b0e-126">-Location</span></span>
<span data-ttu-id="c2b0e-127">O nome da região local a partir da qual recuperar o grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2b0e-128">-Name</span></span>
<span data-ttu-id="c2b0e-129">O nome do grupo de failover de banco de dados SQL do Azure a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-129">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-130">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="c2b0e-130">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="c2b0e-131">O nome da instância gerenciada na região de parceiro a ser adicionada ao grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-131">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-132">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="c2b0e-132">-PartnerRegion</span></span>
<span data-ttu-id="c2b0e-133">O nome da região parceira do grupo failover de instância.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-133">The name of the partner region of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-134">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b0e-134">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c2b0e-135">O nome do grupo de recursos secundário do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-135">The name of the secondary resource group of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-136">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2b0e-136">-PartnerSubscriptionId</span></span>
<span data-ttu-id="c2b0e-137">A ID da assinatura da instância gerenciada secundária do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-137">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="c2b0e-138">Este parâmetro só é necessário para a configuração de assinatura cruzada</span><span class="sxs-lookup"><span data-stu-id="c2b0e-138">This parameter is only needed for cross-subscription setup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-139">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="c2b0e-139">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="c2b0e-140">O nome da instância gerenciada na região local a ser adicionada ao grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-140">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b0e-141">-ResourceGroupName</span></span>
<span data-ttu-id="c2b0e-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-142">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c2b0e-143">-Confirm</span></span>
<span data-ttu-id="c2b0e-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b0e-145">-WhatIf</span></span>
<span data-ttu-id="c2b0e-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2b0e-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b0e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b0e-148">CommonParameters</span></span>
<span data-ttu-id="c2b0e-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b0e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b0e-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b0e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b0e-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2b0e-151">INPUTS</span></span>

### <span data-ttu-id="c2b0e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c2b0e-152">System.String</span></span>

## <span data-ttu-id="c2b0e-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2b0e-153">OUTPUTS</span></span>

### <span data-ttu-id="c2b0e-154">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c2b0e-154">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="c2b0e-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2b0e-155">NOTES</span></span>

## <span data-ttu-id="c2b0e-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2b0e-156">RELATED LINKS</span></span>