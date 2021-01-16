---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: df4eac2c6380c36dcd07c906ccbbee4d2a93f27b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263133"
---
# <span data-ttu-id="9131a-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="9131a-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="9131a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9131a-102">SYNOPSIS</span></span>
<span data-ttu-id="9131a-103">Limpa a migração de teste para o servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="9131a-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="9131a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9131a-104">SYNTAX</span></span>

### <span data-ttu-id="9131a-105">ByIDVMwareCbt (padrão)</span><span class="sxs-lookup"><span data-stu-id="9131a-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9131a-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="9131a-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9131a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9131a-107">DESCRIPTION</span></span>
<span data-ttu-id="9131a-108">O cmdlet Start-AzMigrateTestMigrationCleanup inicia a limpeza da migração de teste para o servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="9131a-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="9131a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9131a-109">EXAMPLES</span></span>

### <span data-ttu-id="9131a-110">Exemplo 1: por ID da máquina.</span><span class="sxs-lookup"><span data-stu-id="9131a-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigrationCleanup -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="9131a-111">Por ID da máquina.</span><span class="sxs-lookup"><span data-stu-id="9131a-111">By machine id.</span></span>

### <span data-ttu-id="9131a-112">Exemplo 2: por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="9131a-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigrationCleanup -InputObject $ob


AllowedOperation            : {DisableMigration, TestMigrate, Migrate}

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="9131a-113">Por objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="9131a-113">By input object.</span></span>

## <span data-ttu-id="9131a-114">OS</span><span class="sxs-lookup"><span data-stu-id="9131a-114">PARAMETERS</span></span>

### <span data-ttu-id="9131a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9131a-115">-DefaultProfile</span></span>
<span data-ttu-id="9131a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9131a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9131a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9131a-117">-InputObject</span></span>
<span data-ttu-id="9131a-118">Especifica o servidor de replicação para o qual a limpeza de migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="9131a-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="9131a-119">O objeto de servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication para construir, consulte a seção de anotações para obter as propriedades INPUTobject e criar uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9131a-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9131a-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9131a-120">-SubscriptionId</span></span>
<span data-ttu-id="9131a-121">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="9131a-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="9131a-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="9131a-122">-TargetObjectID</span></span>
<span data-ttu-id="9131a-123">Especifica o servidor de replicação para o qual a limpeza de migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="9131a-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="9131a-124">A ID deve ser recuperada usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="9131a-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="9131a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9131a-125">CommonParameters</span></span>
<span data-ttu-id="9131a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9131a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9131a-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9131a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9131a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9131a-128">INPUTS</span></span>

## <span data-ttu-id="9131a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9131a-129">OUTPUTS</span></span>

### <span data-ttu-id="9131a-130">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="9131a-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="9131a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9131a-131">NOTES</span></span>

<span data-ttu-id="9131a-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9131a-132">ALIASES</span></span>

<span data-ttu-id="9131a-133">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="9131a-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9131a-134">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="9131a-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9131a-135">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9131a-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9131a-136">INPUTobject <IMigrationItem> : especifica o servidor de replicação para o qual a limpeza de migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="9131a-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="9131a-137">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="9131a-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="9131a-138">`[Location <String>]`: Local do recurso</span><span class="sxs-lookup"><span data-stu-id="9131a-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="9131a-139">`[CurrentJobId <String>]`: A ID do braço do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="9131a-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="9131a-140">`[CurrentJobName <String>]`: O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="9131a-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="9131a-141">`[CurrentJobStartTime <DateTime?>]`: A hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="9131a-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="9131a-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="9131a-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="9131a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9131a-143">RELATED LINKS</span></span>

