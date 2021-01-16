---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 9f82c8a50cba86fed394d55692d03eeec2ef97ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426777"
---
# <span data-ttu-id="5162d-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5162d-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="5162d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5162d-102">SYNOPSIS</span></span>
<span data-ttu-id="5162d-103">Executa um failover de um grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="5162d-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="5162d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5162d-104">SYNTAX</span></span>

### <span data-ttu-id="5162d-105">SwitchInstanceFailoverGroupDefaultSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5162d-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5162d-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5162d-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5162d-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5162d-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5162d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5162d-108">DESCRIPTION</span></span>
<span data-ttu-id="5162d-109">Esse comando troca as funções das instâncias gerenciadas em um grupo de failover de instância ao fazer failover para a região secundária especificada, tornando-a a nova região primária.</span><span class="sxs-lookup"><span data-stu-id="5162d-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="5162d-110">Todas as novas sessões do TDS conectadas ao ponto de extremidade primário são automaticamente redirecionadas para a nova região primária.</span><span class="sxs-lookup"><span data-stu-id="5162d-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="5162d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5162d-111">EXAMPLES</span></span>

### <span data-ttu-id="5162d-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5162d-112">Example 1</span></span>
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

<span data-ttu-id="5162d-113">Emita uma operação de failover que permita a perda de dados por meio do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="5162d-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="5162d-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5162d-114">Example 2</span></span>
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

<span data-ttu-id="5162d-115">Emita uma melhor operação de failover de esforço que será bem-sucedida sem perder dados ou falhar e reverter.</span><span class="sxs-lookup"><span data-stu-id="5162d-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="5162d-116">OS</span><span class="sxs-lookup"><span data-stu-id="5162d-116">PARAMETERS</span></span>

### <span data-ttu-id="5162d-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="5162d-117">-AllowDataLoss</span></span>
<span data-ttu-id="5162d-118">Conclua o failover mesmo se fizer isso pode resultar em perda de dados.</span><span class="sxs-lookup"><span data-stu-id="5162d-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="5162d-119">Isso permitirá que o failover prossiga mesmo se um banco de dados primário estiver indisponível.</span><span class="sxs-lookup"><span data-stu-id="5162d-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="5162d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5162d-120">-DefaultProfile</span></span>
<span data-ttu-id="5162d-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5162d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5162d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5162d-122">-InputObject</span></span>
<span data-ttu-id="5162d-123">O objeto de grupo de failover de instância para alternar</span><span class="sxs-lookup"><span data-stu-id="5162d-123">The Instance Failover Group object to switch</span></span>

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

### <span data-ttu-id="5162d-124">-Local</span><span class="sxs-lookup"><span data-stu-id="5162d-124">-Location</span></span>
<span data-ttu-id="5162d-125">O nome da região local a partir da qual recuperar o grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="5162d-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="5162d-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="5162d-126">-Name</span></span>
<span data-ttu-id="5162d-127">O nome do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="5162d-127">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="5162d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5162d-128">-ResourceGroupName</span></span>
<span data-ttu-id="5162d-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5162d-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="5162d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5162d-130">-ResourceId</span></span>
<span data-ttu-id="5162d-131">A ID do recurso do grupo de failover de instância para alternar.</span><span class="sxs-lookup"><span data-stu-id="5162d-131">The Resource ID of the Instance Failover Group to switch.</span></span>

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

### <span data-ttu-id="5162d-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5162d-132">-Confirm</span></span>
<span data-ttu-id="5162d-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5162d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5162d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5162d-134">-WhatIf</span></span>
<span data-ttu-id="5162d-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5162d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5162d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5162d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5162d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5162d-137">CommonParameters</span></span>
<span data-ttu-id="5162d-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5162d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5162d-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5162d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5162d-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5162d-140">INPUTS</span></span>

### <span data-ttu-id="5162d-141">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5162d-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="5162d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5162d-142">System.String</span></span>

## <span data-ttu-id="5162d-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5162d-143">OUTPUTS</span></span>

### <span data-ttu-id="5162d-144">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5162d-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="5162d-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5162d-145">NOTES</span></span>

## <span data-ttu-id="5162d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5162d-146">RELATED LINKS</span></span>
