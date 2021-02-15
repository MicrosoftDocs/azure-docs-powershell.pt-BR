---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: df4eac2c6380c36dcd07c906ccbbee4d2a93f27b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112975"
---
# <span data-ttu-id="e5e83-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="e5e83-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="e5e83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5e83-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e83-103">Limpa a migração de teste para o servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="e5e83-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="e5e83-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5e83-104">SYNTAX</span></span>

### <span data-ttu-id="e5e83-105">ByIDVCbt (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e5e83-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e5e83-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="e5e83-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e5e83-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5e83-107">DESCRIPTION</span></span>
<span data-ttu-id="e5e83-108">O Start-AzMigrateTestMigrationCleanup cmdlet inicia a limpeza da migração de teste para o servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="e5e83-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="e5e83-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e5e83-109">EXAMPLES</span></span>

### <span data-ttu-id="e5e83-110">Exemplo 1: por ID de máquina.</span><span class="sxs-lookup"><span data-stu-id="e5e83-110">Example 1: By machine id.</span></span>
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

<span data-ttu-id="e5e83-111">Por ID de máquina.</span><span class="sxs-lookup"><span data-stu-id="e5e83-111">By machine id.</span></span>

### <span data-ttu-id="e5e83-112">Exemplo 2: Por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="e5e83-112">Example 2: By input object</span></span>
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

<span data-ttu-id="e5e83-113">Por objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="e5e83-113">By input object.</span></span>

## <span data-ttu-id="e5e83-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5e83-114">PARAMETERS</span></span>

### <span data-ttu-id="e5e83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e83-115">-DefaultProfile</span></span>
<span data-ttu-id="e5e83-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e83-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5e83-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5e83-117">-InputObject</span></span>
<span data-ttu-id="e5e83-118">Especifica o servidor de replicação para o qual a limpeza de migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="e5e83-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="e5e83-119">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="e5e83-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e5e83-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5e83-120">-SubscriptionId</span></span>
<span data-ttu-id="e5e83-121">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e83-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="e5e83-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="e5e83-122">-TargetObjectID</span></span>
<span data-ttu-id="e5e83-123">Especifica o servidor de replicação para o qual a limpeza de migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="e5e83-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="e5e83-124">A ID deve ser recuperada usando o cmdlet Get-AzMigrateServerReplication dados.</span><span class="sxs-lookup"><span data-stu-id="e5e83-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="e5e83-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e83-125">CommonParameters</span></span>
<span data-ttu-id="e5e83-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e83-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e83-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5e83-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e83-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="e5e83-128">INPUTS</span></span>

## <span data-ttu-id="e5e83-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="e5e83-129">OUTPUTS</span></span>

### <span data-ttu-id="e5e83-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="e5e83-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="e5e83-131">Notas</span><span class="sxs-lookup"><span data-stu-id="e5e83-131">NOTES</span></span>

<span data-ttu-id="e5e83-132">Aliases</span><span class="sxs-lookup"><span data-stu-id="e5e83-132">ALIASES</span></span>

<span data-ttu-id="e5e83-133">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="e5e83-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e5e83-134">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e5e83-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e5e83-135">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e5e83-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e5e83-136">INPUTOBJECT: especifica o servidor de replicação para o qual a limpeza de migração de teste <IMigrationItem> precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="e5e83-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="e5e83-137">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication servidor</span><span class="sxs-lookup"><span data-stu-id="e5e83-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="e5e83-138">`[Location <String>]`: Localização do Recurso</span><span class="sxs-lookup"><span data-stu-id="e5e83-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="e5e83-139">`[CurrentJobId <String>]`: A ID arm do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="e5e83-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="e5e83-140">`[CurrentJobName <String>]`: o nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e5e83-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="e5e83-141">`[CurrentJobStartTime <DateTime?>]`: a hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e5e83-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="e5e83-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="e5e83-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="e5e83-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5e83-143">RELATED LINKS</span></span>

