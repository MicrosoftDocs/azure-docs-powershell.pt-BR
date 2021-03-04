---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: 65f9527005b849b9ffbcc8c343b57515b2d437c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892472"
---
# <span data-ttu-id="7a67a-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="7a67a-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="7a67a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a67a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a67a-103">Interrompe a replicação para o servidor migrado.</span><span class="sxs-lookup"><span data-stu-id="7a67a-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="7a67a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7a67a-104">SYNTAX</span></span>

### <span data-ttu-id="7a67a-105">ByIDVMwareCbt (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7a67a-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7a67a-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="7a67a-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7a67a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7a67a-107">DESCRIPTION</span></span>
<span data-ttu-id="7a67a-108">O Remove-AzMigrateServerReplication cmdlet interrompe a replicação de um servidor migrado.</span><span class="sxs-lookup"><span data-stu-id="7a67a-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="7a67a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a67a-109">EXAMPLES</span></span>

### <span data-ttu-id="7a67a-110">Exemplo 1: Remover por id.</span><span class="sxs-lookup"><span data-stu-id="7a67a-110">Example 1: Remove by id.</span></span>
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

<span data-ttu-id="7a67a-111">Resync por id.</span><span class="sxs-lookup"><span data-stu-id="7a67a-111">Resync by id.</span></span>

### <span data-ttu-id="7a67a-112">Exemplo 2: Remover por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="7a67a-112">Example 2: Remove by Input Object</span></span>
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

<span data-ttu-id="7a67a-113">Por nome.</span><span class="sxs-lookup"><span data-stu-id="7a67a-113">By name.</span></span>

## <span data-ttu-id="7a67a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7a67a-114">PARAMETERS</span></span>

### <span data-ttu-id="7a67a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a67a-115">-DefaultProfile</span></span>
<span data-ttu-id="7a67a-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a67a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a67a-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="7a67a-117">-ForceRemove</span></span>
<span data-ttu-id="7a67a-118">Especifica se a replicação precisa ser removida com força.</span><span class="sxs-lookup"><span data-stu-id="7a67a-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="7a67a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a67a-119">-InputObject</span></span>
<span data-ttu-id="7a67a-120">Especifica o objeto machine do servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="7a67a-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="7a67a-121">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7a67a-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7a67a-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a67a-122">-SubscriptionId</span></span>
<span data-ttu-id="7a67a-123">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a67a-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="7a67a-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="7a67a-124">-TargetObjectID</span></span>
<span data-ttu-id="7a67a-125">Especifica o servidor de replcating para o qual a réplica precisa ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7a67a-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="7a67a-126">A ID deve ser recuperada usando Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a67a-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="7a67a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a67a-127">CommonParameters</span></span>
<span data-ttu-id="7a67a-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a67a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a67a-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a67a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a67a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a67a-130">INPUTS</span></span>

## <span data-ttu-id="7a67a-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7a67a-131">OUTPUTS</span></span>

### <span data-ttu-id="7a67a-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="7a67a-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="7a67a-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="7a67a-133">NOTES</span></span>

<span data-ttu-id="7a67a-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7a67a-134">ALIASES</span></span>

<span data-ttu-id="7a67a-135">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="7a67a-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a67a-136">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="7a67a-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a67a-137">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7a67a-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a67a-138">INPUTOBJECT <IMigrationItem> : Especifica o objeto do computador do servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="7a67a-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="7a67a-139">`[Location <String>]`: Localização do Recurso</span><span class="sxs-lookup"><span data-stu-id="7a67a-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="7a67a-140">`[CurrentJobId <String>]`: A ARM ID do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="7a67a-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="7a67a-141">`[CurrentJobName <String>]`: O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="7a67a-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="7a67a-142">`[CurrentJobStartTime <DateTime?>]`: A hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="7a67a-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="7a67a-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="7a67a-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="7a67a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a67a-144">RELATED LINKS</span></span>

