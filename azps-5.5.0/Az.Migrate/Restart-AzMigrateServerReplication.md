---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 35bf416249f24d7158720e2a9c28230da3f4f291
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112979"
---
# <span data-ttu-id="8a421-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="8a421-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="8a421-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a421-102">SYNOPSIS</span></span>
<span data-ttu-id="8a421-103">Reinicia a replicação do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="8a421-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="8a421-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a421-104">SYNTAX</span></span>

### <span data-ttu-id="8a421-105">ByIDVCbt (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8a421-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a421-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="8a421-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8a421-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a421-107">DESCRIPTION</span></span>
<span data-ttu-id="8a421-108">O Restart-AzMigrateServerReplication cmdlet repara a replicação do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="8a421-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="8a421-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8a421-109">EXAMPLES</span></span>

### <span data-ttu-id="8a421-110">Exemplo 1: por id.</span><span class="sxs-lookup"><span data-stu-id="8a421-110">Example 1: By id.</span></span>
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

<span data-ttu-id="8a421-111">Por id.</span><span class="sxs-lookup"><span data-stu-id="8a421-111">By id.</span></span>

### <span data-ttu-id="8a421-112">Exemplo 2: Por Objeto de Entrada</span><span class="sxs-lookup"><span data-stu-id="8a421-112">Example 2: By Input Object</span></span>
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

<span data-ttu-id="8a421-113">Por Objeto de Entrada.</span><span class="sxs-lookup"><span data-stu-id="8a421-113">By Input Object.</span></span>

## <span data-ttu-id="8a421-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a421-114">PARAMETERS</span></span>

### <span data-ttu-id="8a421-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a421-115">-DefaultProfile</span></span>
<span data-ttu-id="8a421-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a421-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a421-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a421-117">-InputObject</span></span>
<span data-ttu-id="8a421-118">Especifica o objeto de máquina do servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="8a421-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="8a421-119">Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="8a421-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8a421-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a421-120">-SubscriptionId</span></span>
<span data-ttu-id="8a421-121">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a421-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8a421-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="8a421-122">-TargetObjectID</span></span>
<span data-ttu-id="8a421-123">Especifica o servidor de resposta para o qual o resync precisa ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="8a421-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="8a421-124">A ID deve ser recuperada usando o cmdlet Get-AzMigrateServerReplication dados.</span><span class="sxs-lookup"><span data-stu-id="8a421-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="8a421-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a421-125">CommonParameters</span></span>
<span data-ttu-id="8a421-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a421-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a421-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a421-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a421-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="8a421-128">INPUTS</span></span>

## <span data-ttu-id="8a421-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="8a421-129">OUTPUTS</span></span>

### <span data-ttu-id="8a421-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="8a421-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="8a421-131">Notas</span><span class="sxs-lookup"><span data-stu-id="8a421-131">NOTES</span></span>

<span data-ttu-id="8a421-132">Aliases</span><span class="sxs-lookup"><span data-stu-id="8a421-132">ALIASES</span></span>

<span data-ttu-id="8a421-133">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="8a421-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a421-134">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8a421-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a421-135">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a421-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a421-136">INPUTOBJECT: <IMigrationItem> especifica o objeto de máquina do servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="8a421-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="8a421-137">`[Location <String>]`: Localização do Recurso</span><span class="sxs-lookup"><span data-stu-id="8a421-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="8a421-138">`[CurrentJobId <String>]`: A ID arm do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="8a421-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="8a421-139">`[CurrentJobName <String>]`: o nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8a421-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="8a421-140">`[CurrentJobStartTime <DateTime?>]`: a hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8a421-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="8a421-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="8a421-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="8a421-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a421-142">RELATED LINKS</span></span>

