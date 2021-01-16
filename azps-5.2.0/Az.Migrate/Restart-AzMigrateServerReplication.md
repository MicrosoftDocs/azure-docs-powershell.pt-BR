---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 35bf416249f24d7158720e2a9c28230da3f4f291
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263137"
---
# <span data-ttu-id="299ac-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="299ac-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="299ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="299ac-102">SYNOPSIS</span></span>
<span data-ttu-id="299ac-103">Reinicia a replicação do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="299ac-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="299ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="299ac-104">SYNTAX</span></span>

### <span data-ttu-id="299ac-105">ByIDVMwareCbt (padrão)</span><span class="sxs-lookup"><span data-stu-id="299ac-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="299ac-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="299ac-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="299ac-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="299ac-107">DESCRIPTION</span></span>
<span data-ttu-id="299ac-108">O cmdlet Restart-AzMigrateServerReplication repara a replicação do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="299ac-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="299ac-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="299ac-109">EXAMPLES</span></span>

### <span data-ttu-id="299ac-110">Exemplo 1: por ID.</span><span class="sxs-lookup"><span data-stu-id="299ac-110">Example 1: By id.</span></span>
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

<span data-ttu-id="299ac-111">Por ID.</span><span class="sxs-lookup"><span data-stu-id="299ac-111">By id.</span></span>

### <span data-ttu-id="299ac-112">Exemplo 2: por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="299ac-112">Example 2: By Input Object</span></span>
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

<span data-ttu-id="299ac-113">Por objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="299ac-113">By Input Object.</span></span>

## <span data-ttu-id="299ac-114">OS</span><span class="sxs-lookup"><span data-stu-id="299ac-114">PARAMETERS</span></span>

### <span data-ttu-id="299ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299ac-115">-DefaultProfile</span></span>
<span data-ttu-id="299ac-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="299ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="299ac-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="299ac-117">-InputObject</span></span>
<span data-ttu-id="299ac-118">Especifica o objeto de máquina do servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="299ac-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="299ac-119">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="299ac-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="299ac-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="299ac-120">-SubscriptionId</span></span>
<span data-ttu-id="299ac-121">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="299ac-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="299ac-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="299ac-122">-TargetObjectID</span></span>
<span data-ttu-id="299ac-123">Especifica o servidor replcating para o qual a resincronização precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="299ac-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="299ac-124">A ID deve ser recuperada usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="299ac-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="299ac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299ac-125">CommonParameters</span></span>
<span data-ttu-id="299ac-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="299ac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299ac-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="299ac-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299ac-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="299ac-128">INPUTS</span></span>

## <span data-ttu-id="299ac-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="299ac-129">OUTPUTS</span></span>

### <span data-ttu-id="299ac-130">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="299ac-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="299ac-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="299ac-131">NOTES</span></span>

<span data-ttu-id="299ac-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="299ac-132">ALIASES</span></span>

<span data-ttu-id="299ac-133">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="299ac-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="299ac-134">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="299ac-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="299ac-135">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="299ac-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="299ac-136">INPUTobject <IMigrationItem> : especifica o objeto de máquina do servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="299ac-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="299ac-137">`[Location <String>]`: Local do recurso</span><span class="sxs-lookup"><span data-stu-id="299ac-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="299ac-138">`[CurrentJobId <String>]`: A ID do braço do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="299ac-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="299ac-139">`[CurrentJobName <String>]`: O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="299ac-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="299ac-140">`[CurrentJobStartTime <DateTime?>]`: A hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="299ac-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="299ac-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="299ac-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="299ac-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="299ac-142">RELATED LINKS</span></span>

