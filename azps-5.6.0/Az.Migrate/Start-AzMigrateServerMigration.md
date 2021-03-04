---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 47f87fc2f1f1d4e6186e9caaf4921990122c07fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888627"
---
# <span data-ttu-id="8804e-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="8804e-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="8804e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8804e-102">SYNOPSIS</span></span>
<span data-ttu-id="8804e-103">Inicia a migração para o servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="8804e-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="8804e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8804e-104">SYNTAX</span></span>

### <span data-ttu-id="8804e-105">ByIDVMwareCbt (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8804e-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8804e-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="8804e-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8804e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8804e-107">DESCRIPTION</span></span>
<span data-ttu-id="8804e-108">Inicia a migração para o servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="8804e-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="8804e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8804e-109">EXAMPLES</span></span>

### <span data-ttu-id="8804e-110">Exemplo 1: Por id</span><span class="sxs-lookup"><span data-stu-id="8804e-110">Example 1: By id</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Start-AzMigrateServerMigration -TargetObjectID "/Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_52f42ee7-8eb3-1aa4-e2d5-1ae83f86b085"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Migrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="8804e-111">Por id</span><span class="sxs-lookup"><span data-stu-id="8804e-111">By id</span></span>

## <span data-ttu-id="8804e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8804e-112">PARAMETERS</span></span>

### <span data-ttu-id="8804e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8804e-113">-DefaultProfile</span></span>
<span data-ttu-id="8804e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8804e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8804e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8804e-115">-InputObject</span></span>
<span data-ttu-id="8804e-116">Especifica o servidor de réplica para o qual a migração precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="8804e-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="8804e-117">O objeto server pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication servidor.</span><span class="sxs-lookup"><span data-stu-id="8804e-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="8804e-118">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8804e-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8804e-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8804e-119">-SubscriptionId</span></span>
<span data-ttu-id="8804e-120">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8804e-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8804e-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="8804e-121">-TargetObjectID</span></span>
<span data-ttu-id="8804e-122">Especifica o servidor de respostas para o qual a migração precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="8804e-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="8804e-123">A ID deve ser recuperada usando Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8804e-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="8804e-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="8804e-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="8804e-125">Especifica se o servidor de origem deve ser desligado após a migração.</span><span class="sxs-lookup"><span data-stu-id="8804e-125">Specifies whether the source server should be turned off post migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8804e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8804e-126">CommonParameters</span></span>
<span data-ttu-id="8804e-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8804e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8804e-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8804e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8804e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8804e-129">INPUTS</span></span>

## <span data-ttu-id="8804e-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8804e-130">OUTPUTS</span></span>

### <span data-ttu-id="8804e-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="8804e-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="8804e-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="8804e-132">NOTES</span></span>

<span data-ttu-id="8804e-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8804e-133">ALIASES</span></span>

<span data-ttu-id="8804e-134">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="8804e-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8804e-135">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8804e-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8804e-136">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8804e-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8804e-137">INPUTOBJECT : Especifica o servidor de réplica para o qual a migração <IMigrationItem> precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="8804e-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="8804e-138">O objeto server pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication servidor.</span><span class="sxs-lookup"><span data-stu-id="8804e-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="8804e-139">`[Location <String>]`: Localização do Recurso</span><span class="sxs-lookup"><span data-stu-id="8804e-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="8804e-140">`[CurrentJobId <String>]`: A ARM ID do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="8804e-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="8804e-141">`[CurrentJobName <String>]`: O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8804e-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="8804e-142">`[CurrentJobStartTime <DateTime?>]`: A hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8804e-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="8804e-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="8804e-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="8804e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8804e-144">RELATED LINKS</span></span>

