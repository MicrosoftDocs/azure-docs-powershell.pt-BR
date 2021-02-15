---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 99be70e225dd607c580c4571f4ae332e7badf33a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114475"
---
# <span data-ttu-id="66483-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="66483-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="66483-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66483-102">SYNOPSIS</span></span>
<span data-ttu-id="66483-103">Esse comando cria um novo Grupo failover de Instância do Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="66483-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="66483-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66483-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66483-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="66483-105">DESCRIPTION</span></span>
<span data-ttu-id="66483-106">Cria um novo Grupo de Failover de Instância do Banco de Dados SQL do Azure entre as regiões especificadas com o par notado instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="66483-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="66483-107">Dois pontos de extremidade TDS do banco de dados SQL do Azure são criados em Name.SqlDatabaseDnsSuffix (por exemplo, Name.database.windows.net) e Name.secondary.SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="66483-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="66483-108">Esses pontos de extremidade podem ser usados para se conectar às regiões primárias e secundárias do Grupo failover, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="66483-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="66483-109">Se a região primária for afetada por uma interrupção, o failover automático dos pontos de extremidade e bancos de dados será disparado conforme determinado pela política de failover e pelo período de graça e política de failover do Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="66483-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="66483-110">Durante a visualização do recurso Grupos de Failover de Instância, somente valores maiores ou iguais a 1 hora são suportados para o parâmetro '-GracePeriodWithDataLossHours'.</span><span class="sxs-lookup"><span data-stu-id="66483-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="66483-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66483-111">EXAMPLES</span></span>

### <span data-ttu-id="66483-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="66483-112">Example 1</span></span>
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

<span data-ttu-id="66483-113">Esse comando cria um novo Grupo de Failover de Instância com a política de failover "Automático" para o par instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="66483-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="66483-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="66483-114">Example 2</span></span>
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

<span data-ttu-id="66483-115">Esse comando cria um novo Grupo de Failover de Instância com a política de failover "Manual" para o par Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="66483-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="66483-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="66483-116">Example 3</span></span>

<span data-ttu-id="66483-117">Esse comando cria um novo Grupo failover de Instância do Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="66483-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="66483-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="66483-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="66483-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66483-119">PARAMETERS</span></span>

### <span data-ttu-id="66483-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="66483-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="66483-121">Se uma interrupção no servidor secundário deve disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="66483-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="66483-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66483-122">-DefaultProfile</span></span>
<span data-ttu-id="66483-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66483-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66483-124">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="66483-124">-FailoverPolicy</span></span>
<span data-ttu-id="66483-125">A política de failover do Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="66483-125">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="66483-126">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="66483-126">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="66483-127">Intervalo antes de o failover automático ser iniciado se ocorrer uma falha no servidor principal e o failover não puder ser concluído sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="66483-127">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="66483-128">-Local</span><span class="sxs-lookup"><span data-stu-id="66483-128">-Location</span></span>
<span data-ttu-id="66483-129">O nome da Região Local a partir da qual recuperar o Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="66483-129">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="66483-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="66483-130">-Name</span></span>
<span data-ttu-id="66483-131">O nome do Grupo de Failover do Banco de Dados SQL do Azure para criar.</span><span class="sxs-lookup"><span data-stu-id="66483-131">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="66483-132">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="66483-132">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="66483-133">O nome da Instância Gerenciada na região do parceiro a ser adicionado ao Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="66483-133">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="66483-134">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="66483-134">-PartnerRegion</span></span>
<span data-ttu-id="66483-135">O nome da região do parceiro do Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="66483-135">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="66483-136">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66483-136">-PartnerResourceGroupName</span></span>
<span data-ttu-id="66483-137">O nome do grupo de recursos secundário do Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="66483-137">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="66483-138">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66483-138">-PartnerSubscriptionId</span></span>
<span data-ttu-id="66483-139">A id da assinatura da Instância Gerenciada secundária do Grupo failover de instância.</span><span class="sxs-lookup"><span data-stu-id="66483-139">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="66483-140">Este parâmetro só é necessário para a configuração entre assinaturas</span><span class="sxs-lookup"><span data-stu-id="66483-140">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="66483-141">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="66483-141">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="66483-142">O nome da Instância Gerenciada na região local a ser adicionado ao Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="66483-142">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="66483-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66483-143">-ResourceGroupName</span></span>
<span data-ttu-id="66483-144">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66483-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="66483-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="66483-145">-Confirm</span></span>
<span data-ttu-id="66483-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66483-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66483-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66483-147">-WhatIf</span></span>
<span data-ttu-id="66483-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="66483-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66483-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66483-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66483-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66483-150">CommonParameters</span></span>
<span data-ttu-id="66483-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66483-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66483-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66483-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66483-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="66483-153">INPUTS</span></span>

### <span data-ttu-id="66483-154">System.String</span><span class="sxs-lookup"><span data-stu-id="66483-154">System.String</span></span>

## <span data-ttu-id="66483-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="66483-155">OUTPUTS</span></span>

### <span data-ttu-id="66483-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="66483-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="66483-157">Notas</span><span class="sxs-lookup"><span data-stu-id="66483-157">NOTES</span></span>

## <span data-ttu-id="66483-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66483-158">RELATED LINKS</span></span>
