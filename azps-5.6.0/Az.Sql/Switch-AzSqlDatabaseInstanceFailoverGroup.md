---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: a20f2196b6052befb74cd74366c96bf262cdd325
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890563"
---
# <span data-ttu-id="6f6be-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6f6be-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="6f6be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f6be-102">SYNOPSIS</span></span>
<span data-ttu-id="6f6be-103">Executa um failover de um Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="6f6be-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="6f6be-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6f6be-104">SYNTAX</span></span>

### <span data-ttu-id="6f6be-105">SwitchInstanceFailoverGroupDefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6f6be-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f6be-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6f6be-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f6be-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6f6be-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f6be-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6f6be-108">DESCRIPTION</span></span>
<span data-ttu-id="6f6be-109">Esse comando troca as funções das instâncias gerenciadas em um Grupo de Failover de Instância falhando na região secundária especificada, tornando-a a nova região primária.</span><span class="sxs-lookup"><span data-stu-id="6f6be-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="6f6be-110">Todas as novas sessões TDS que se conectam ao ponto de extremidade principal são automaticamente roteada para a nova região primária.</span><span class="sxs-lookup"><span data-stu-id="6f6be-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="6f6be-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f6be-111">EXAMPLES</span></span>

### <span data-ttu-id="6f6be-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f6be-112">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup -AllowDataLoss
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

<span data-ttu-id="6f6be-113">Emitir uma operação de failover permitindo a perda de dados canalização no Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="6f6be-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="6f6be-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6f6be-114">Example 2</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup
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

<span data-ttu-id="6f6be-115">Emito uma melhor operação de failover de esforço que será bem-sucedida sem perder dados ou falhar e reverter.</span><span class="sxs-lookup"><span data-stu-id="6f6be-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="6f6be-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6f6be-116">PARAMETERS</span></span>

### <span data-ttu-id="6f6be-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="6f6be-117">-AllowDataLoss</span></span>
<span data-ttu-id="6f6be-118">Conclua o failover mesmo que isso possa resultar em perda de dados.</span><span class="sxs-lookup"><span data-stu-id="6f6be-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="6f6be-119">Isso permitirá que o failover prossiga mesmo se um banco de dados principal não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="6f6be-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f6be-120">-DefaultProfile</span></span>
<span data-ttu-id="6f6be-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f6be-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f6be-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f6be-122">-InputObject</span></span>
<span data-ttu-id="6f6be-123">O objeto Grupo de Failover de Instância a ser alternado</span><span class="sxs-lookup"><span data-stu-id="6f6be-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SwitchInstanceFailoverGroupByInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f6be-124">-Location</span><span class="sxs-lookup"><span data-stu-id="6f6be-124">-Location</span></span>
<span data-ttu-id="6f6be-125">O nome da Região Local da qual recuperar o Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="6f6be-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet, SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6be-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6f6be-126">-Name</span></span>
<span data-ttu-id="6f6be-127">O nome do Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="6f6be-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6be-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f6be-128">-ResourceGroupName</span></span>
<span data-ttu-id="6f6be-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6f6be-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6be-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f6be-130">-ResourceId</span></span>
<span data-ttu-id="6f6be-131">A ID de Recurso do Grupo de Failover de Instância a ser alternado.</span><span class="sxs-lookup"><span data-stu-id="6f6be-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f6be-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f6be-132">-Confirm</span></span>
<span data-ttu-id="6f6be-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f6be-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f6be-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f6be-134">-WhatIf</span></span>
<span data-ttu-id="6f6be-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6f6be-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f6be-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6f6be-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f6be-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f6be-137">CommonParameters</span></span>
<span data-ttu-id="6f6be-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f6be-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f6be-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f6be-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f6be-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f6be-140">INPUTS</span></span>

### <span data-ttu-id="6f6be-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="6f6be-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="6f6be-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6f6be-142">System.String</span></span>

## <span data-ttu-id="6f6be-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6f6be-143">OUTPUTS</span></span>

### <span data-ttu-id="6f6be-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="6f6be-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="6f6be-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="6f6be-145">NOTES</span></span>

## <span data-ttu-id="6f6be-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f6be-146">RELATED LINKS</span></span>
