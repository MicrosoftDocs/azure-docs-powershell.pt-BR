---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 3031878e30307cd5ff733de6177bc3c65c61a5bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887302"
---
# <span data-ttu-id="0eed5-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0eed5-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="0eed5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eed5-102">SYNOPSIS</span></span>
<span data-ttu-id="0eed5-103">Modifica a configuração de um Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="0eed5-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="0eed5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0eed5-104">SYNTAX</span></span>

### <span data-ttu-id="0eed5-105">SetInstanceFailoverGroupDefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0eed5-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eed5-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0eed5-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eed5-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="0eed5-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eed5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0eed5-108">DESCRIPTION</span></span>
<span data-ttu-id="0eed5-109">Este comando modifica a configuração de um Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="0eed5-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="0eed5-110">A região principal do Grupo de Failover de Instância deve ser usada para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="0eed5-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="0eed5-111">Durante a visualização do recurso Grupos de Failover de Instância, apenas valores maiores ou iguais a 1 hora são suportados para o parâmetro '-GracePeriodWithDataLossHours'.</span><span class="sxs-lookup"><span data-stu-id="0eed5-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="0eed5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0eed5-112">EXAMPLES</span></span>

### <span data-ttu-id="0eed5-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0eed5-113">Example 1</span></span>
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

<span data-ttu-id="0eed5-114">Define a política de failover de um Grupo de Failover de Instância como "Manual" canalização no Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="0eed5-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="0eed5-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0eed5-115">PARAMETERS</span></span>

### <span data-ttu-id="0eed5-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="0eed5-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="0eed5-117">Se as interrupções no servidor secundário devem disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0eed5-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="0eed5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eed5-118">-DefaultProfile</span></span>
<span data-ttu-id="0eed5-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0eed5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eed5-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="0eed5-120">-FailoverPolicy</span></span>
<span data-ttu-id="0eed5-121">A política de failover do Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="0eed5-121">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="0eed5-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="0eed5-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="0eed5-123">Intervalo antes que o failover automático seja iniciado se ocorrer uma paralisação no servidor primário e o failover não puder ser concluído sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="0eed5-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="0eed5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eed5-124">-InputObject</span></span>
<span data-ttu-id="0eed5-125">O objeto Instance Failover Group a ser definido</span><span class="sxs-lookup"><span data-stu-id="0eed5-125">The Instance Failover Group object to set</span></span>

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

### <span data-ttu-id="0eed5-126">-Location</span><span class="sxs-lookup"><span data-stu-id="0eed5-126">-Location</span></span>
<span data-ttu-id="0eed5-127">O nome da Região Local da qual recuperar o Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="0eed5-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="0eed5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0eed5-128">-Name</span></span>
<span data-ttu-id="0eed5-129">O nome do Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="0eed5-129">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="0eed5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eed5-130">-ResourceGroupName</span></span>
<span data-ttu-id="0eed5-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0eed5-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="0eed5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eed5-132">-ResourceId</span></span>
<span data-ttu-id="0eed5-133">A ID de Recurso do Grupo de Failover de Instância a ser definido.</span><span class="sxs-lookup"><span data-stu-id="0eed5-133">The Resource ID of the Instance Failover Group to set.</span></span>

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

### <span data-ttu-id="0eed5-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0eed5-134">-Confirm</span></span>
<span data-ttu-id="0eed5-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eed5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eed5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eed5-136">-WhatIf</span></span>
<span data-ttu-id="0eed5-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0eed5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eed5-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0eed5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eed5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eed5-139">CommonParameters</span></span>
<span data-ttu-id="0eed5-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eed5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eed5-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0eed5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eed5-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0eed5-142">INPUTS</span></span>

### <span data-ttu-id="0eed5-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="0eed5-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="0eed5-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0eed5-144">System.String</span></span>

## <span data-ttu-id="0eed5-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0eed5-145">OUTPUTS</span></span>

### <span data-ttu-id="0eed5-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="0eed5-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="0eed5-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="0eed5-147">NOTES</span></span>

## <span data-ttu-id="0eed5-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0eed5-148">RELATED LINKS</span></span>
