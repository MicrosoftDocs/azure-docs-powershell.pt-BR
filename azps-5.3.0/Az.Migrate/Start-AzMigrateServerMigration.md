---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427116"
---
# <span data-ttu-id="80501-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="80501-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="80501-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80501-102">SYNOPSIS</span></span>
<span data-ttu-id="80501-103">Inicia a migração para o servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="80501-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="80501-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80501-104">SYNTAX</span></span>

### <span data-ttu-id="80501-105">ByIDVMwareCbt (padrão)</span><span class="sxs-lookup"><span data-stu-id="80501-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="80501-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="80501-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="80501-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80501-107">DESCRIPTION</span></span>
<span data-ttu-id="80501-108">Inicia a migração para o servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="80501-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="80501-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80501-109">EXAMPLES</span></span>

### <span data-ttu-id="80501-110">Exemplo 1: por ID</span><span class="sxs-lookup"><span data-stu-id="80501-110">Example 1: By id</span></span>
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

<span data-ttu-id="80501-111">Por ID</span><span class="sxs-lookup"><span data-stu-id="80501-111">By id</span></span>

## <span data-ttu-id="80501-112">OS</span><span class="sxs-lookup"><span data-stu-id="80501-112">PARAMETERS</span></span>

### <span data-ttu-id="80501-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80501-113">-DefaultProfile</span></span>
<span data-ttu-id="80501-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80501-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80501-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80501-115">-InputObject</span></span>
<span data-ttu-id="80501-116">Especifica o servidor de replicação para o qual a migração precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="80501-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="80501-117">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="80501-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="80501-118">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="80501-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="80501-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80501-119">-SubscriptionId</span></span>
<span data-ttu-id="80501-120">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="80501-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="80501-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="80501-121">-TargetObjectID</span></span>
<span data-ttu-id="80501-122">Especifica o servidor replcating para o qual a migração precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="80501-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="80501-123">A ID deve ser recuperada usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="80501-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="80501-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="80501-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="80501-125">Especifica se o servidor de origem deve ser desativado após a migração.</span><span class="sxs-lookup"><span data-stu-id="80501-125">Specifies whether the source server should be turned off post migration.</span></span>

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

### <span data-ttu-id="80501-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80501-126">CommonParameters</span></span>
<span data-ttu-id="80501-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80501-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80501-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80501-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80501-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80501-129">INPUTS</span></span>

## <span data-ttu-id="80501-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80501-130">OUTPUTS</span></span>

### <span data-ttu-id="80501-131">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="80501-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="80501-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80501-132">NOTES</span></span>

<span data-ttu-id="80501-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="80501-133">ALIASES</span></span>

<span data-ttu-id="80501-134">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="80501-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80501-135">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="80501-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80501-136">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80501-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80501-137">INPUTobject <IMigrationItem> : especifica o servidor de replicação para o qual a migração precisa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="80501-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="80501-138">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="80501-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="80501-139">`[Location <String>]`: Local do recurso</span><span class="sxs-lookup"><span data-stu-id="80501-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="80501-140">`[CurrentJobId <String>]`: A ID do braço do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="80501-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="80501-141">`[CurrentJobName <String>]`: O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="80501-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="80501-142">`[CurrentJobStartTime <DateTime?>]`: A hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="80501-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="80501-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="80501-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="80501-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80501-144">RELATED LINKS</span></span>

