---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 99be70e225dd607c580c4571f4ae332e7badf33a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433811"
---
# <span data-ttu-id="e2e14-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e2e14-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="e2e14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2e14-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e14-103">Esse comando cria um novo grupo de failover de instância de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e14-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="e2e14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2e14-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2e14-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2e14-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e14-106">Cria um novo grupo de failover de instância de banco de dados SQL do Azure entre as regiões especificadas com o par de instâncias gerenciadas observada.</span><span class="sxs-lookup"><span data-stu-id="e2e14-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="e2e14-107">Dois pontos de extremidade TDS do banco de dados SQL do Azure são criados em Name. SqlDatabaseDnsSuffix (por exemplo, Name.database.windows.net) e Name. Secondary. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="e2e14-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="e2e14-108">Esses pontos de extremidade podem ser usados para conectar-se às regiões primárias e secundárias do grupo de failover, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e2e14-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="e2e14-109">Se a região primária for afetada por uma interrupção, o failover automático dos pontos de extremidade e bancos de dados será disparado conforme determinado pela política de failover do grupo de failover de instância e do período de cortesia.</span><span class="sxs-lookup"><span data-stu-id="e2e14-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="e2e14-110">Durante a visualização do recurso de grupos de failover de instância, somente os valores maiores que ou iguais a 1 hora têm suporte para o parâmetro '-GracePeriodWithDataLossHours '.</span><span class="sxs-lookup"><span data-stu-id="e2e14-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="e2e14-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2e14-111">EXAMPLES</span></span>

### <span data-ttu-id="e2e14-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e2e14-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="e2e14-113">Esse comando cria um novo grupo de failover de instância com a política de failover ' automático ' para o par de instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="e2e14-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="e2e14-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e2e14-114">Example 2</span></span>
```powershell
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

<span data-ttu-id="e2e14-115">Esse comando cria um novo grupo de failover de instância com a política de failover ' manual ' para o par de instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="e2e14-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="e2e14-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e2e14-116">Example 3</span></span>

<span data-ttu-id="e2e14-117">Esse comando cria um novo grupo de failover de instância de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e14-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="e2e14-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e2e14-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="e2e14-119">OS</span><span class="sxs-lookup"><span data-stu-id="e2e14-119">PARAMETERS</span></span>

### <span data-ttu-id="e2e14-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="e2e14-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="e2e14-121">Se uma interrupção no servidor secundário deve disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e2e14-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="e2e14-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e14-122">-DefaultProfile</span></span>
<span data-ttu-id="e2e14-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e14-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2e14-124">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="e2e14-124">-FailoverPolicy</span></span>
<span data-ttu-id="e2e14-125">A política de failover do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="e2e14-125">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="e2e14-126">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="e2e14-126">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="e2e14-127">Intervalo antes do failover automático será iniciado se ocorrer uma falha no servidor primário e o failover não puder ser concluído sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="e2e14-127">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e14-128">-Local</span><span class="sxs-lookup"><span data-stu-id="e2e14-128">-Location</span></span>
<span data-ttu-id="e2e14-129">O nome da região local a partir da qual recuperar o grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="e2e14-129">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e14-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2e14-130">-Name</span></span>
<span data-ttu-id="e2e14-131">O nome do grupo de failover de banco de dados SQL do Azure a ser criado.</span><span class="sxs-lookup"><span data-stu-id="e2e14-131">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e14-132">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="e2e14-132">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="e2e14-133">O nome da instância gerenciada na região de parceiro a ser adicionada ao grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="e2e14-133">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="e2e14-134">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="e2e14-134">-PartnerRegion</span></span>
<span data-ttu-id="e2e14-135">O nome da região parceira do grupo failover de instância.</span><span class="sxs-lookup"><span data-stu-id="e2e14-135">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="e2e14-136">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e14-136">-PartnerResourceGroupName</span></span>
<span data-ttu-id="e2e14-137">O nome do grupo de recursos secundário do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="e2e14-137">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="e2e14-138">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2e14-138">-PartnerSubscriptionId</span></span>
<span data-ttu-id="e2e14-139">A ID da assinatura da instância gerenciada secundária do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="e2e14-139">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="e2e14-140">Este parâmetro só é necessário para a configuração de assinatura cruzada</span><span class="sxs-lookup"><span data-stu-id="e2e14-140">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="e2e14-141">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="e2e14-141">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="e2e14-142">O nome da instância gerenciada na região local a ser adicionada ao grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="e2e14-142">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="e2e14-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e14-143">-ResourceGroupName</span></span>
<span data-ttu-id="e2e14-144">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2e14-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e14-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2e14-145">-Confirm</span></span>
<span data-ttu-id="e2e14-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2e14-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e14-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e14-147">-WhatIf</span></span>
<span data-ttu-id="e2e14-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2e14-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2e14-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2e14-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e14-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e14-150">CommonParameters</span></span>
<span data-ttu-id="e2e14-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e14-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e14-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2e14-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e14-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2e14-153">INPUTS</span></span>

### <span data-ttu-id="e2e14-154">System. String</span><span class="sxs-lookup"><span data-stu-id="e2e14-154">System.String</span></span>

## <span data-ttu-id="e2e14-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2e14-155">OUTPUTS</span></span>

### <span data-ttu-id="e2e14-156">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e2e14-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="e2e14-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2e14-157">NOTES</span></span>

## <span data-ttu-id="e2e14-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2e14-158">RELATED LINKS</span></span>
