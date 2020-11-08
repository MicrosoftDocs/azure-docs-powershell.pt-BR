---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7a893099a81225f165fc6fc56c6ba3fd6cfaec3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116984"
---
# <span data-ttu-id="cb9d3-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cb9d3-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="cb9d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9d3-103">Esse comando cria um novo grupo de failover de instância de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="cb9d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb9d3-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb9d3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb9d3-105">DESCRIPTION</span></span>
<span data-ttu-id="cb9d3-106">Cria um novo grupo de failover de instância de banco de dados SQL do Azure entre as regiões especificadas com o par de instâncias gerenciadas observada.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="cb9d3-107">Dois pontos de extremidade TDS do banco de dados SQL do Azure são criados em Name. SqlDatabaseDnsSuffix (por exemplo, Name.database.windows.net) e Name. Secondary. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="cb9d3-108">Esses pontos de extremidade podem ser usados para conectar-se às regiões primárias e secundárias do grupo de failover, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="cb9d3-109">Se a região primária for afetada por uma interrupção, o failover automático dos pontos de extremidade e bancos de dados será disparado conforme determinado pela política de failover do grupo de failover de instância e do período de cortesia.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="cb9d3-110">Durante a visualização do recurso de grupos de failover de instância, somente os valores maiores que ou iguais a 1 hora têm suporte para o parâmetro '-GracePeriodWithDataLossHours '.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="cb9d3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb9d3-111">EXAMPLES</span></span>

### <span data-ttu-id="cb9d3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cb9d3-112">Example 1</span></span>
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

<span data-ttu-id="cb9d3-113">Esse comando cria um novo grupo de failover de instância com a política de failover ' automático ' para o par de instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="cb9d3-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cb9d3-114">Example 2</span></span>
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

<span data-ttu-id="cb9d3-115">Esse comando cria um novo grupo de failover de instância com a política de failover ' manual ' para o par de instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="cb9d3-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="cb9d3-116">Example 3</span></span>

<span data-ttu-id="cb9d3-117">Esse comando cria um novo grupo de failover de instância de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="cb9d3-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="cb9d3-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="cb9d3-119">OS</span><span class="sxs-lookup"><span data-stu-id="cb9d3-119">PARAMETERS</span></span>

### <span data-ttu-id="cb9d3-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="cb9d3-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="cb9d3-121">Se uma interrupção no servidor secundário deve disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="cb9d3-122">Este recurso ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-122">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="cb9d3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9d3-123">-DefaultProfile</span></span>
<span data-ttu-id="cb9d3-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb9d3-125">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="cb9d3-125">-FailoverPolicy</span></span>
<span data-ttu-id="cb9d3-126">A política de failover do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-126">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="cb9d3-127">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="cb9d3-127">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="cb9d3-128">Intervalo antes do failover automático será iniciado se ocorrer uma falha no servidor primário e o failover não puder ser concluído sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-128">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="cb9d3-129">-Local</span><span class="sxs-lookup"><span data-stu-id="cb9d3-129">-Location</span></span>
<span data-ttu-id="cb9d3-130">O nome da região local a partir da qual recuperar o grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-130">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="cb9d3-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb9d3-131">-Name</span></span>
<span data-ttu-id="cb9d3-132">O nome do grupo de failover de banco de dados SQL do Azure a ser criado.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-132">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="cb9d3-133">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="cb9d3-133">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="cb9d3-134">O nome da instância gerenciada na região de parceiro a ser adicionada ao grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-134">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="cb9d3-135">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="cb9d3-135">-PartnerRegion</span></span>
<span data-ttu-id="cb9d3-136">O nome da região parceira do grupo failover de instância.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-136">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="cb9d3-137">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb9d3-137">-PartnerResourceGroupName</span></span>
<span data-ttu-id="cb9d3-138">O nome do grupo de recursos secundário do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-138">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="cb9d3-139">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb9d3-139">-PartnerSubscriptionId</span></span>
<span data-ttu-id="cb9d3-140">A ID da assinatura da instância gerenciada secundária do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-140">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="cb9d3-141">Este parâmetro só é necessário para a configuração de assinatura cruzada</span><span class="sxs-lookup"><span data-stu-id="cb9d3-141">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="cb9d3-142">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="cb9d3-142">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="cb9d3-143">O nome da instância gerenciada na região local a ser adicionada ao grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-143">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="cb9d3-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb9d3-144">-ResourceGroupName</span></span>
<span data-ttu-id="cb9d3-145">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-145">The name of the resource group.</span></span>

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

### <span data-ttu-id="cb9d3-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb9d3-146">-Confirm</span></span>
<span data-ttu-id="cb9d3-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb9d3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb9d3-148">-WhatIf</span></span>
<span data-ttu-id="cb9d3-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb9d3-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb9d3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9d3-151">CommonParameters</span></span>
<span data-ttu-id="cb9d3-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb9d3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9d3-153">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb9d3-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9d3-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb9d3-154">INPUTS</span></span>

### <span data-ttu-id="cb9d3-155">System. String</span><span class="sxs-lookup"><span data-stu-id="cb9d3-155">System.String</span></span>

## <span data-ttu-id="cb9d3-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb9d3-156">OUTPUTS</span></span>

### <span data-ttu-id="cb9d3-157">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="cb9d3-157">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="cb9d3-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb9d3-158">NOTES</span></span>

## <span data-ttu-id="cb9d3-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb9d3-159">RELATED LINKS</span></span>
