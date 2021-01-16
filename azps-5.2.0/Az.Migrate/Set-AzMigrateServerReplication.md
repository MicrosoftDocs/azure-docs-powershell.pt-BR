---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263136"
---
# <span data-ttu-id="328fb-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="328fb-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="328fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="328fb-102">SYNOPSIS</span></span>
<span data-ttu-id="328fb-103">Atualiza as propriedades de destino para o servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="328fb-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="328fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="328fb-104">SYNTAX</span></span>

### <span data-ttu-id="328fb-105">ByIDVMwareCbt (padrão)</span><span class="sxs-lookup"><span data-stu-id="328fb-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="328fb-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="328fb-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="328fb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="328fb-107">DESCRIPTION</span></span>
<span data-ttu-id="328fb-108">O cmdlet Set-AzMigrateServerReplication atualiza as propriedades de destino para o servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="328fb-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="328fb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="328fb-109">EXAMPLES</span></span>

### <span data-ttu-id="328fb-110">Exemplo 1: atualizar por ID</span><span class="sxs-lookup"><span data-stu-id="328fb-110">Example 1: Update by id</span></span>
```powershell
PS C:\> Set-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629' -TargetVMName 'rb-w2k12r2-1'

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Update
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Update
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="328fb-111">Por ID.</span><span class="sxs-lookup"><span data-stu-id="328fb-111">By id.</span></span>

## <span data-ttu-id="328fb-112">OS</span><span class="sxs-lookup"><span data-stu-id="328fb-112">PARAMETERS</span></span>

### <span data-ttu-id="328fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="328fb-113">-DefaultProfile</span></span>
<span data-ttu-id="328fb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="328fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="328fb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="328fb-115">-InputObject</span></span>
<span data-ttu-id="328fb-116">Especifica o servidor de replicação para o qual as propriedades precisam ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="328fb-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="328fb-117">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="328fb-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="328fb-118">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="328fb-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="328fb-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="328fb-119">-NicToUpdate</span></span>
<span data-ttu-id="328fb-120">Atualiza a NIC da máquina virtual do Azure a ser criada.</span><span class="sxs-lookup"><span data-stu-id="328fb-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="328fb-121">Para construir, consulte a seção notas para propriedades NICTOUPDATE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="328fb-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="328fb-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="328fb-122">-SubscriptionId</span></span>
<span data-ttu-id="328fb-123">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="328fb-123">The subscription Id.</span></span>

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

### <span data-ttu-id="328fb-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="328fb-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="328fb-125">Especifica o conjunto de disponibilidade a ser usado para a criação de VM.</span><span class="sxs-lookup"><span data-stu-id="328fb-125">Specifies the Availability Set to be used for VM creation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="328fb-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="328fb-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="328fb-127">Especifica a zona de disponibilidade a ser usada para a criação de VM.</span><span class="sxs-lookup"><span data-stu-id="328fb-127">Specifies the Availability Zone to be used for VM creation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="328fb-128">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="328fb-128">-TargetNetworkId</span></span>
<span data-ttu-id="328fb-129">Atualiza a ID de rede virtual na assinatura de destino do Azure à qual o servidor precisa ser migrado.</span><span class="sxs-lookup"><span data-stu-id="328fb-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="328fb-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="328fb-130">-TargetObjectID</span></span>
<span data-ttu-id="328fb-131">Especifica o servidor replcating para o qual as propriedades precisam ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="328fb-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="328fb-132">A ID deve ser recuperada usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="328fb-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="328fb-133">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="328fb-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="328fb-134">Atualiza a ID do grupo de recursos na assinatura de destino do Azure à qual o servidor precisa ser migrado.</span><span class="sxs-lookup"><span data-stu-id="328fb-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="328fb-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="328fb-135">-TargetVMName</span></span>
<span data-ttu-id="328fb-136">Especifica o servidor replcating para o qual as propriedades precisam ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="328fb-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="328fb-137">A ID deve ser recuperada usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="328fb-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="328fb-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="328fb-138">-TargetVMSize</span></span>
<span data-ttu-id="328fb-139">Atualiza a SKU da VM do Azure a ser criada.</span><span class="sxs-lookup"><span data-stu-id="328fb-139">Updates the SKU of the Azure VM to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="328fb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="328fb-140">CommonParameters</span></span>
<span data-ttu-id="328fb-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="328fb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="328fb-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="328fb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="328fb-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="328fb-143">INPUTS</span></span>

## <span data-ttu-id="328fb-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="328fb-144">OUTPUTS</span></span>

### <span data-ttu-id="328fb-145">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="328fb-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="328fb-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="328fb-146">NOTES</span></span>

<span data-ttu-id="328fb-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="328fb-147">ALIASES</span></span>

<span data-ttu-id="328fb-148">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="328fb-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="328fb-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="328fb-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="328fb-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="328fb-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="328fb-151">INPUTobject <IMigrationItem> : especifica o servidor de replicação para o qual as propriedades precisam ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="328fb-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="328fb-152">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="328fb-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="328fb-153">`[Location <String>]`: Local do recurso</span><span class="sxs-lookup"><span data-stu-id="328fb-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="328fb-154">`[CurrentJobId <String>]`: A ID do braço do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="328fb-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="328fb-155">`[CurrentJobName <String>]`: O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="328fb-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="328fb-156">`[CurrentJobStartTime <DateTime?>]`: A hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="328fb-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="328fb-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="328fb-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="328fb-158">NICTOUPDATE <IVMwareCbtNicInput [] >: atualiza a NIC da máquina virtual do Azure a ser criada.</span><span class="sxs-lookup"><span data-stu-id="328fb-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="328fb-159">`IsPrimaryNic <String>`: Um valor que indica se esta é a NIC primária.</span><span class="sxs-lookup"><span data-stu-id="328fb-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="328fb-160">`NicId <String>`: A ID da NIC.</span><span class="sxs-lookup"><span data-stu-id="328fb-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="328fb-161">`[IsSelectedForMigration <String>]`: Um valor que indica se essa NIC está selecionada para migração.</span><span class="sxs-lookup"><span data-stu-id="328fb-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="328fb-162">`[TargetStaticIPAddress <String>]`: O endereço IP estático.</span><span class="sxs-lookup"><span data-stu-id="328fb-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="328fb-163">`[TargetSubnetName <String>]`: Nome da sub-rede de destino.</span><span class="sxs-lookup"><span data-stu-id="328fb-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="328fb-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="328fb-164">RELATED LINKS</span></span>

