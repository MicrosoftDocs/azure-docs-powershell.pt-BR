---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: f8ac83b684718a6a2698fd1b304b85ffa1ae5d45
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426796"
---
# <span data-ttu-id="15226-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="15226-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="15226-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15226-102">SYNOPSIS</span></span>
<span data-ttu-id="15226-103">Modifica a configuração de um grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="15226-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="15226-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15226-104">SYNTAX</span></span>

### <span data-ttu-id="15226-105">SetInstanceFailoverGroupDefaultSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="15226-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15226-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="15226-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15226-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="15226-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15226-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15226-108">DESCRIPTION</span></span>
<span data-ttu-id="15226-109">Esse comando modifica a configuração de um grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="15226-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="15226-110">A região primária do grupo de failover de instância deve ser usada para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="15226-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="15226-111">Durante a visualização do recurso de grupos de failover de instância, somente os valores maiores que ou iguais a 1 hora têm suporte para o parâmetro '-GracePeriodWithDataLossHours '.</span><span class="sxs-lookup"><span data-stu-id="15226-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="15226-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15226-112">EXAMPLES</span></span>

### <span data-ttu-id="15226-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="15226-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Manual
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

<span data-ttu-id="15226-114">Define a política de failover do grupo de failover de instância como ' manual ' por tubulação no grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="15226-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="15226-115">OS</span><span class="sxs-lookup"><span data-stu-id="15226-115">PARAMETERS</span></span>

### <span data-ttu-id="15226-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="15226-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="15226-117">Se as paralisações no servidor secundário devem disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="15226-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="15226-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15226-118">-DefaultProfile</span></span>
<span data-ttu-id="15226-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15226-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15226-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="15226-120">-FailoverPolicy</span></span>
<span data-ttu-id="15226-121">A política de failover do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="15226-121">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="15226-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="15226-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="15226-123">Intervalo antes do failover automático será iniciado se ocorrer uma falha no servidor primário e o failover não puder ser concluído sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="15226-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="15226-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15226-124">-InputObject</span></span>
<span data-ttu-id="15226-125">O objeto de grupo de failover de instância a ser definido</span><span class="sxs-lookup"><span data-stu-id="15226-125">The Instance Failover Group object to set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15226-126">-Local</span><span class="sxs-lookup"><span data-stu-id="15226-126">-Location</span></span>
<span data-ttu-id="15226-127">O nome da região local a partir da qual recuperar o grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="15226-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet, SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15226-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="15226-128">-Name</span></span>
<span data-ttu-id="15226-129">O nome do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="15226-129">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15226-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15226-130">-ResourceGroupName</span></span>
<span data-ttu-id="15226-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15226-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15226-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15226-132">-ResourceId</span></span>
<span data-ttu-id="15226-133">A ID do recurso do grupo de failover de instância a ser definido.</span><span class="sxs-lookup"><span data-stu-id="15226-133">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15226-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="15226-134">-Confirm</span></span>
<span data-ttu-id="15226-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15226-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15226-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15226-136">-WhatIf</span></span>
<span data-ttu-id="15226-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15226-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15226-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15226-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15226-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15226-139">CommonParameters</span></span>
<span data-ttu-id="15226-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15226-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15226-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15226-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15226-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15226-142">INPUTS</span></span>

### <span data-ttu-id="15226-143">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="15226-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="15226-144">System. String</span><span class="sxs-lookup"><span data-stu-id="15226-144">System.String</span></span>

## <span data-ttu-id="15226-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15226-145">OUTPUTS</span></span>

### <span data-ttu-id="15226-146">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="15226-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="15226-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15226-147">NOTES</span></span>

## <span data-ttu-id="15226-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15226-148">RELATED LINKS</span></span>
