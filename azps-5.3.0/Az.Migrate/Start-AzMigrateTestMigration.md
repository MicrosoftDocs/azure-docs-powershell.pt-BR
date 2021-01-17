---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427114"
---
# <span data-ttu-id="d8919-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="d8919-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="d8919-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8919-102">SYNOPSIS</span></span>
<span data-ttu-id="d8919-103">Inicia a migração de teste para o servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="d8919-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="d8919-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8919-104">SYNTAX</span></span>

### <span data-ttu-id="d8919-105">ByIDVMwareCbt (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8919-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8919-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="d8919-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d8919-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8919-107">DESCRIPTION</span></span>
<span data-ttu-id="d8919-108">O cmdlet Start-AzMigrateTestMigration inicia a migração de teste para o servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="d8919-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="d8919-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8919-109">EXAMPLES</span></span>

### <span data-ttu-id="d8919-110">Exemplo 1: por ID da máquina.</span><span class="sxs-lookup"><span data-stu-id="d8919-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigration -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f' -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxxresourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="d8919-111">Por ID da máquina.</span><span class="sxs-lookup"><span data-stu-id="d8919-111">By machine id.</span></span>

### <span data-ttu-id="d8919-112">Exemplo 2: por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="d8919-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigration -InputObject $obj -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="d8919-113">Por objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="d8919-113">By input object.</span></span>

## <span data-ttu-id="d8919-114">OS</span><span class="sxs-lookup"><span data-stu-id="d8919-114">PARAMETERS</span></span>

### <span data-ttu-id="d8919-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8919-115">-DefaultProfile</span></span>
<span data-ttu-id="d8919-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8919-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8919-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8919-117">-InputObject</span></span>
<span data-ttu-id="d8919-118">Especifica o servidor de replicação para o qual a migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="d8919-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="d8919-119">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="d8919-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="d8919-120">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d8919-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8919-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8919-121">-SubscriptionId</span></span>
<span data-ttu-id="d8919-122">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="d8919-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d8919-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="d8919-123">-TargetObjectID</span></span>
<span data-ttu-id="d8919-124">Especifica o servidor de replicação para o qual a migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="d8919-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="d8919-125">A ID deve ser recuperada usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="d8919-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="d8919-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="d8919-126">-TestNetworkID</span></span>
<span data-ttu-id="d8919-127">Atualiza a ID de rede virtual na assinatura de destino do Azure para ser usada para a migração de teste.</span><span class="sxs-lookup"><span data-stu-id="d8919-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8919-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8919-128">CommonParameters</span></span>
<span data-ttu-id="d8919-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8919-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8919-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8919-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8919-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8919-131">INPUTS</span></span>

## <span data-ttu-id="d8919-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8919-132">OUTPUTS</span></span>

### <span data-ttu-id="d8919-133">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="d8919-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="d8919-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8919-134">NOTES</span></span>

<span data-ttu-id="d8919-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d8919-135">ALIASES</span></span>

<span data-ttu-id="d8919-136">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="d8919-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8919-137">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d8919-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8919-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8919-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8919-139">INPUTobject <IMigrationItem> : especifica o servidor de replicação para o qual a migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="d8919-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="d8919-140">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="d8919-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="d8919-141">`[Location <String>]`: Local do recurso</span><span class="sxs-lookup"><span data-stu-id="d8919-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="d8919-142">`[CurrentJobId <String>]`: A ID do braço do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="d8919-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="d8919-143">`[CurrentJobName <String>]`: O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="d8919-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="d8919-144">`[CurrentJobStartTime <DateTime?>]`: A hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="d8919-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="d8919-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="d8919-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="d8919-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8919-146">RELATED LINKS</span></span>

