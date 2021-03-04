---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: 534728e98d913a3de7f7b02628451433b252ded9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892845"
---
# <span data-ttu-id="57573-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="57573-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="57573-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57573-102">SYNOPSIS</span></span>
<span data-ttu-id="57573-103">Limpa a migração de teste para o servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="57573-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="57573-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="57573-104">SYNTAX</span></span>

### <span data-ttu-id="57573-105">ByIDVMwareCbt (Padrão)</span><span class="sxs-lookup"><span data-stu-id="57573-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57573-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="57573-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="57573-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="57573-107">DESCRIPTION</span></span>
<span data-ttu-id="57573-108">O Start-AzMigrateTestMigrationCleanup cmdlet inicia a limpeza da migração de teste para o servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="57573-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="57573-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57573-109">EXAMPLES</span></span>

### <span data-ttu-id="57573-110">Exemplo 1: por ID do computador.</span><span class="sxs-lookup"><span data-stu-id="57573-110">Example 1: By machine id.</span></span>
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

<span data-ttu-id="57573-111">Por ID do computador.</span><span class="sxs-lookup"><span data-stu-id="57573-111">By machine id.</span></span>

### <span data-ttu-id="57573-112">Exemplo 2: Por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="57573-112">Example 2: By input object</span></span>
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

<span data-ttu-id="57573-113">Por objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="57573-113">By input object.</span></span>

## <span data-ttu-id="57573-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="57573-114">PARAMETERS</span></span>

### <span data-ttu-id="57573-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57573-115">-DefaultProfile</span></span>
<span data-ttu-id="57573-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57573-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57573-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57573-117">-InputObject</span></span>
<span data-ttu-id="57573-118">Especifica o servidor de réplica para o qual a limpeza de migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="57573-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="57573-119">O objeto server pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="57573-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57573-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57573-120">-SubscriptionId</span></span>
<span data-ttu-id="57573-121">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="57573-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="57573-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="57573-122">-TargetObjectID</span></span>
<span data-ttu-id="57573-123">Especifica o servidor de réplica para o qual a limpeza de migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="57573-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="57573-124">A ID deve ser recuperada usando Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57573-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="57573-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57573-125">CommonParameters</span></span>
<span data-ttu-id="57573-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57573-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57573-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57573-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57573-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57573-128">INPUTS</span></span>

## <span data-ttu-id="57573-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="57573-129">OUTPUTS</span></span>

### <span data-ttu-id="57573-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="57573-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="57573-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="57573-131">NOTES</span></span>

<span data-ttu-id="57573-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="57573-132">ALIASES</span></span>

<span data-ttu-id="57573-133">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="57573-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57573-134">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="57573-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57573-135">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57573-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57573-136">INPUTOBJECT : Especifica o servidor de réplica para o qual a limpeza de migração de teste <IMigrationItem> precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="57573-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="57573-137">O objeto server pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication servidor</span><span class="sxs-lookup"><span data-stu-id="57573-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="57573-138">`[Location <String>]`: Localização do Recurso</span><span class="sxs-lookup"><span data-stu-id="57573-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="57573-139">`[CurrentJobId <String>]`: A ARM ID do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="57573-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="57573-140">`[CurrentJobName <String>]`: O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="57573-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="57573-141">`[CurrentJobStartTime <DateTime?>]`: A hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="57573-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="57573-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="57573-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="57573-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57573-143">RELATED LINKS</span></span>

