---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112976"
---
# <span data-ttu-id="1de3f-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="1de3f-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="1de3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1de3f-102">SYNOPSIS</span></span>
<span data-ttu-id="1de3f-103">Inicia a migração de teste para o servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="1de3f-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="1de3f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1de3f-104">SYNTAX</span></span>

### <span data-ttu-id="1de3f-105">ByIDVCbt (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1de3f-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1de3f-106">ByInputObjectVCbt</span><span class="sxs-lookup"><span data-stu-id="1de3f-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1de3f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1de3f-107">DESCRIPTION</span></span>
<span data-ttu-id="1de3f-108">O Start-AzMigrateTestMigration cmdlet inicia a migração de teste para o servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="1de3f-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="1de3f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1de3f-109">EXAMPLES</span></span>

### <span data-ttu-id="1de3f-110">Exemplo 1: por ID de máquina.</span><span class="sxs-lookup"><span data-stu-id="1de3f-110">Example 1: By machine id.</span></span>
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

<span data-ttu-id="1de3f-111">Por ID de máquina.</span><span class="sxs-lookup"><span data-stu-id="1de3f-111">By machine id.</span></span>

### <span data-ttu-id="1de3f-112">Exemplo 2: Por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="1de3f-112">Example 2: By input object</span></span>
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

<span data-ttu-id="1de3f-113">Por objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="1de3f-113">By input object.</span></span>

## <span data-ttu-id="1de3f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1de3f-114">PARAMETERS</span></span>

### <span data-ttu-id="1de3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de3f-115">-DefaultProfile</span></span>
<span data-ttu-id="1de3f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1de3f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1de3f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1de3f-117">-InputObject</span></span>
<span data-ttu-id="1de3f-118">Especifica o servidor de replicação para o qual a migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="1de3f-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="1de3f-119">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication servidor.</span><span class="sxs-lookup"><span data-stu-id="1de3f-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="1de3f-120">Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="1de3f-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1de3f-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1de3f-121">-SubscriptionId</span></span>
<span data-ttu-id="1de3f-122">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="1de3f-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1de3f-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="1de3f-123">-TargetObjectID</span></span>
<span data-ttu-id="1de3f-124">Especifica o servidor de replicação para o qual a migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="1de3f-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="1de3f-125">A ID deve ser recuperada usando o cmdlet Get-AzMigrateServerReplication dados.</span><span class="sxs-lookup"><span data-stu-id="1de3f-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="1de3f-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="1de3f-126">-TestNetworkID</span></span>
<span data-ttu-id="1de3f-127">Atualiza a ID da Rede Virtual dentro da assinatura do Azure de destino a ser usada para a migração de teste.</span><span class="sxs-lookup"><span data-stu-id="1de3f-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

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

### <span data-ttu-id="1de3f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de3f-128">CommonParameters</span></span>
<span data-ttu-id="1de3f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1de3f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de3f-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1de3f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de3f-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="1de3f-131">INPUTS</span></span>

## <span data-ttu-id="1de3f-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="1de3f-132">OUTPUTS</span></span>

### <span data-ttu-id="1de3f-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="1de3f-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="1de3f-134">Notas</span><span class="sxs-lookup"><span data-stu-id="1de3f-134">NOTES</span></span>

<span data-ttu-id="1de3f-135">Aliases</span><span class="sxs-lookup"><span data-stu-id="1de3f-135">ALIASES</span></span>

<span data-ttu-id="1de3f-136">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="1de3f-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1de3f-137">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="1de3f-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1de3f-138">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1de3f-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1de3f-139">INPUTOBJECT: especifica o servidor de replicação para o qual a <IMigrationItem> migração de teste precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="1de3f-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="1de3f-140">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication servidor.</span><span class="sxs-lookup"><span data-stu-id="1de3f-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="1de3f-141">`[Location <String>]`: Localização do Recurso</span><span class="sxs-lookup"><span data-stu-id="1de3f-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="1de3f-142">`[CurrentJobId <String>]`: A ID arm do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="1de3f-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="1de3f-143">`[CurrentJobName <String>]`: o nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="1de3f-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="1de3f-144">`[CurrentJobStartTime <DateTime?>]`: a hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="1de3f-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="1de3f-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="1de3f-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="1de3f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1de3f-146">RELATED LINKS</span></span>

