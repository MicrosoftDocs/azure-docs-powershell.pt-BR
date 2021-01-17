---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427118"
---
# <span data-ttu-id="2bd07-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="2bd07-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="2bd07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bd07-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd07-103">Interrompe a replicação para o servidor migrado.</span><span class="sxs-lookup"><span data-stu-id="2bd07-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="2bd07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bd07-104">SYNTAX</span></span>

### <span data-ttu-id="2bd07-105">ByIDVMwareCbt (padrão)</span><span class="sxs-lookup"><span data-stu-id="2bd07-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2bd07-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="2bd07-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2bd07-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bd07-107">DESCRIPTION</span></span>
<span data-ttu-id="2bd07-108">O cmdlet Remove-AzMigrateServerReplication interrompe a replicação de um servidor migrado.</span><span class="sxs-lookup"><span data-stu-id="2bd07-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="2bd07-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bd07-109">EXAMPLES</span></span>

### <span data-ttu-id="2bd07-110">Exemplo 1: remover por ID.</span><span class="sxs-lookup"><span data-stu-id="2bd07-110">Example 1: Remove by id.</span></span>
```powershell
PS C:\> Remove-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="2bd07-111">Ressincronize por ID.</span><span class="sxs-lookup"><span data-stu-id="2bd07-111">Resync by id.</span></span>

### <span data-ttu-id="2bd07-112">Exemplo 2: remover por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="2bd07-112">Example 2: Remove by Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> Remove-AzMigrateServerReplication -InputObject $obj


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="2bd07-113">Por nome.</span><span class="sxs-lookup"><span data-stu-id="2bd07-113">By name.</span></span>

## <span data-ttu-id="2bd07-114">OS</span><span class="sxs-lookup"><span data-stu-id="2bd07-114">PARAMETERS</span></span>

### <span data-ttu-id="2bd07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd07-115">-DefaultProfile</span></span>
<span data-ttu-id="2bd07-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd07-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd07-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="2bd07-117">-ForceRemove</span></span>
<span data-ttu-id="2bd07-118">Especifica se a replicação precisa ser reforçada.</span><span class="sxs-lookup"><span data-stu-id="2bd07-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="2bd07-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bd07-119">-InputObject</span></span>
<span data-ttu-id="2bd07-120">Especifica o objeto de máquina do servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="2bd07-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="2bd07-121">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2bd07-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: ByInputObjectVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd07-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2bd07-122">-SubscriptionId</span></span>
<span data-ttu-id="2bd07-123">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd07-123">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd07-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="2bd07-124">-TargetObjectID</span></span>
<span data-ttu-id="2bd07-125">Especifica o servidor replcating para o qual o Replicatio precisa ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="2bd07-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="2bd07-126">A ID deve ser recuperada usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="2bd07-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIDVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd07-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd07-127">CommonParameters</span></span>
<span data-ttu-id="2bd07-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd07-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd07-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bd07-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd07-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bd07-130">INPUTS</span></span>

## <span data-ttu-id="2bd07-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bd07-131">OUTPUTS</span></span>

### <span data-ttu-id="2bd07-132">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="2bd07-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="2bd07-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bd07-133">NOTES</span></span>

<span data-ttu-id="2bd07-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2bd07-134">ALIASES</span></span>

<span data-ttu-id="2bd07-135">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="2bd07-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2bd07-136">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="2bd07-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2bd07-137">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2bd07-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2bd07-138">INPUTobject <IMigrationItem> : especifica o objeto de máquina do servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="2bd07-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="2bd07-139">`[Location <String>]`: Local do recurso</span><span class="sxs-lookup"><span data-stu-id="2bd07-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="2bd07-140">`[CurrentJobId <String>]`: A ID do braço do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="2bd07-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="2bd07-141">`[CurrentJobName <String>]`: O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="2bd07-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="2bd07-142">`[CurrentJobStartTime <DateTime?>]`: A hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="2bd07-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="2bd07-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="2bd07-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="2bd07-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bd07-144">RELATED LINKS</span></span>

