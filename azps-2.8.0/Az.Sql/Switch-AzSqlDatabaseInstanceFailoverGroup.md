---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7d52c80bba03d0e88d6e5302647fd9e6de94675f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773991"
---
# <span data-ttu-id="87b10-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="87b10-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="87b10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87b10-102">SYNOPSIS</span></span>
<span data-ttu-id="87b10-103">Executa um failover de um grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="87b10-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="87b10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87b10-104">SYNTAX</span></span>

### <span data-ttu-id="87b10-105">SwitchIFGDefault (padrão)</span><span class="sxs-lookup"><span data-stu-id="87b10-105">SwitchIFGDefault (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87b10-106">Alternar um grupo de failover de instância da ID do recurso</span><span class="sxs-lookup"><span data-stu-id="87b10-106">Switch a Instance Failover Group from Resource Id</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87b10-107">Alternar um grupo de failover de instância da definição de instância AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="87b10-107">Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87b10-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87b10-108">DESCRIPTION</span></span>
<span data-ttu-id="87b10-109">Esse comando troca as funções das instâncias gerenciadas em um grupo de failover de instância ao fazer failover para a região secundária especificada, tornando-a a nova região primária.</span><span class="sxs-lookup"><span data-stu-id="87b10-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="87b10-110">Todas as novas sessões do TDS conectadas ao ponto de extremidade primário são automaticamente redirecionadas para a nova região primária.</span><span class="sxs-lookup"><span data-stu-id="87b10-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="87b10-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87b10-111">EXAMPLES</span></span>

### <span data-ttu-id="87b10-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="87b10-112">Example 1</span></span>
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

<span data-ttu-id="87b10-113">Emita uma operação de failover que permita a perda de dados por meio do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="87b10-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="87b10-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="87b10-114">Example 2</span></span>
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

<span data-ttu-id="87b10-115">Emita uma melhor operação de failover de esforço que será bem-sucedida sem perder dados ou falhar e reverter.</span><span class="sxs-lookup"><span data-stu-id="87b10-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="87b10-116">OS</span><span class="sxs-lookup"><span data-stu-id="87b10-116">PARAMETERS</span></span>

### <span data-ttu-id="87b10-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="87b10-117">-AllowDataLoss</span></span>
<span data-ttu-id="87b10-118">Conclua o failover mesmo se fizer isso pode resultar em perda de dados.</span><span class="sxs-lookup"><span data-stu-id="87b10-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="87b10-119">Isso permitirá que o failover prossiga mesmo se um banco de dados primário estiver indisponível.</span><span class="sxs-lookup"><span data-stu-id="87b10-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b10-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b10-120">-DefaultProfile</span></span>
<span data-ttu-id="87b10-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87b10-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87b10-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87b10-122">-InputObject</span></span>
<span data-ttu-id="87b10-123">O objeto de grupo de failover de instância para alternar</span><span class="sxs-lookup"><span data-stu-id="87b10-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87b10-124">-Local</span><span class="sxs-lookup"><span data-stu-id="87b10-124">-Location</span></span>
<span data-ttu-id="87b10-125">O nome da região local a partir da qual recuperar o grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="87b10-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault, Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b10-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="87b10-126">-Name</span></span>
<span data-ttu-id="87b10-127">O nome do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="87b10-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b10-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b10-128">-ResourceGroupName</span></span>
<span data-ttu-id="87b10-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="87b10-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b10-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87b10-130">-ResourceId</span></span>
<span data-ttu-id="87b10-131">A ID do recurso do grupo de failover de instância para alternar.</span><span class="sxs-lookup"><span data-stu-id="87b10-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: String
Parameter Sets: Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87b10-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="87b10-132">-Confirm</span></span>
<span data-ttu-id="87b10-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87b10-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87b10-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87b10-134">-WhatIf</span></span>
<span data-ttu-id="87b10-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="87b10-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87b10-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87b10-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87b10-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b10-137">CommonParameters</span></span>
<span data-ttu-id="87b10-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b10-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b10-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87b10-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b10-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87b10-140">INPUTS</span></span>

### <span data-ttu-id="87b10-141">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="87b10-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="87b10-142">System. String</span><span class="sxs-lookup"><span data-stu-id="87b10-142">System.String</span></span>

## <span data-ttu-id="87b10-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87b10-143">OUTPUTS</span></span>

### <span data-ttu-id="87b10-144">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="87b10-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="87b10-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87b10-145">NOTES</span></span>

## <span data-ttu-id="87b10-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87b10-146">RELATED LINKS</span></span>
