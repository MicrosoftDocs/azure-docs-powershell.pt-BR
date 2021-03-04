---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 1f63238fede4c3a280cd4eb631c33e97db8f73ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890245"
---
# <span data-ttu-id="94845-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="94845-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="94845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94845-102">SYNOPSIS</span></span>
<span data-ttu-id="94845-103">Reinicia a replicação para o servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="94845-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="94845-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="94845-104">SYNTAX</span></span>

### <span data-ttu-id="94845-105">ByIDVMwareCbt (Padrão)</span><span class="sxs-lookup"><span data-stu-id="94845-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="94845-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="94845-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="94845-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="94845-107">DESCRIPTION</span></span>
<span data-ttu-id="94845-108">O Restart-AzMigrateServerReplication cmdlet repara a replicação do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="94845-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="94845-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94845-109">EXAMPLES</span></span>

### <span data-ttu-id="94845-110">Exemplo 1: Por id.</span><span class="sxs-lookup"><span data-stu-id="94845-110">Example 1: By id.</span></span>
```powershell
PS C:\> Restart-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="94845-111">Por id.</span><span class="sxs-lookup"><span data-stu-id="94845-111">By id.</span></span>

### <span data-ttu-id="94845-112">Exemplo 2: Por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="94845-112">Example 2: By Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> $output = Restart-AzMigrateServerReplication -InputObject $obj
ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="94845-113">Por Objeto Input.</span><span class="sxs-lookup"><span data-stu-id="94845-113">By Input Object.</span></span>

## <span data-ttu-id="94845-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="94845-114">PARAMETERS</span></span>

### <span data-ttu-id="94845-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94845-115">-DefaultProfile</span></span>
<span data-ttu-id="94845-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94845-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94845-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94845-117">-InputObject</span></span>
<span data-ttu-id="94845-118">Especifica o objeto machine do servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="94845-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="94845-119">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="94845-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94845-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94845-120">-SubscriptionId</span></span>
<span data-ttu-id="94845-121">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="94845-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="94845-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="94845-122">-TargetObjectID</span></span>
<span data-ttu-id="94845-123">Especifica o servidor de replcating para o qual o resync precisa ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="94845-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="94845-124">A ID deve ser recuperada usando Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94845-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="94845-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94845-125">CommonParameters</span></span>
<span data-ttu-id="94845-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94845-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94845-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94845-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94845-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94845-128">INPUTS</span></span>

## <span data-ttu-id="94845-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="94845-129">OUTPUTS</span></span>

### <span data-ttu-id="94845-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="94845-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="94845-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="94845-131">NOTES</span></span>

<span data-ttu-id="94845-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="94845-132">ALIASES</span></span>

<span data-ttu-id="94845-133">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="94845-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94845-134">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="94845-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94845-135">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="94845-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94845-136">INPUTOBJECT <IMigrationItem> : Especifica o objeto do computador do servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="94845-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="94845-137">`[Location <String>]`: Localização do Recurso</span><span class="sxs-lookup"><span data-stu-id="94845-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="94845-138">`[CurrentJobId <String>]`: A ARM ID do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="94845-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="94845-139">`[CurrentJobName <String>]`: O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="94845-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="94845-140">`[CurrentJobStartTime <DateTime?>]`: A hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="94845-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="94845-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="94845-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="94845-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94845-142">RELATED LINKS</span></span>

