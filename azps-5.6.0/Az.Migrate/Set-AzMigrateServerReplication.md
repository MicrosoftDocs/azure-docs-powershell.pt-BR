---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: b87e541266c3ce555c0fc11910c9541914b14738
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892850"
---
# <span data-ttu-id="dc543-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="dc543-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="dc543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc543-102">SYNOPSIS</span></span>
<span data-ttu-id="dc543-103">Atualiza as propriedades de destino para o servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="dc543-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="dc543-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dc543-104">SYNTAX</span></span>

### <span data-ttu-id="dc543-105">ByIDVMwareCbt (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dc543-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc543-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="dc543-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dc543-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dc543-107">DESCRIPTION</span></span>
<span data-ttu-id="dc543-108">O Set-AzMigrateServerReplication cmdlet atualiza as propriedades de destino para o servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="dc543-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="dc543-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc543-109">EXAMPLES</span></span>

### <span data-ttu-id="dc543-110">Exemplo 1: Atualização por id</span><span class="sxs-lookup"><span data-stu-id="dc543-110">Example 1: Update by id</span></span>
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

<span data-ttu-id="dc543-111">Por id.</span><span class="sxs-lookup"><span data-stu-id="dc543-111">By id.</span></span>

## <span data-ttu-id="dc543-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dc543-112">PARAMETERS</span></span>

### <span data-ttu-id="dc543-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc543-113">-DefaultProfile</span></span>
<span data-ttu-id="dc543-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc543-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc543-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc543-115">-InputObject</span></span>
<span data-ttu-id="dc543-116">Especifica o servidor de réplica para o qual as propriedades precisam ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="dc543-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="dc543-117">O objeto server pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication servidor.</span><span class="sxs-lookup"><span data-stu-id="dc543-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="dc543-118">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="dc543-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc543-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="dc543-119">-NicToUpdate</span></span>
<span data-ttu-id="dc543-120">Atualiza a NIC para a VM do Azure a ser criada.</span><span class="sxs-lookup"><span data-stu-id="dc543-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="dc543-121">Para construir, consulte a seção NOTES para propriedades NICTOUPDATE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="dc543-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc543-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc543-122">-SubscriptionId</span></span>
<span data-ttu-id="dc543-123">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="dc543-123">The subscription Id.</span></span>

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

### <span data-ttu-id="dc543-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="dc543-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="dc543-125">Especifica o Conjunto de Disponibilidade a ser usado para criação de VM.</span><span class="sxs-lookup"><span data-stu-id="dc543-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="dc543-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="dc543-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="dc543-127">Especifica a Zona de Disponibilidade a ser usada para criação de VM.</span><span class="sxs-lookup"><span data-stu-id="dc543-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="dc543-128">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc543-128">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="dc543-129">Especifica a conta de armazenamento a ser usada para diagnósticos de inicialização.</span><span class="sxs-lookup"><span data-stu-id="dc543-129">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="dc543-130">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="dc543-130">-TargetNetworkId</span></span>
<span data-ttu-id="dc543-131">Atualiza a ID da Rede Virtual dentro da assinatura do Azure de destino para a qual o servidor precisa ser migrado.</span><span class="sxs-lookup"><span data-stu-id="dc543-131">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="dc543-132">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="dc543-132">-TargetObjectID</span></span>
<span data-ttu-id="dc543-133">Especifica o servidor de respostas para o qual as propriedades precisam ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="dc543-133">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="dc543-134">A ID deve ser recuperada usando Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc543-134">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="dc543-135">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="dc543-135">-TargetResourceGroupID</span></span>
<span data-ttu-id="dc543-136">Atualiza a ID do Grupo de Recursos na assinatura do Azure de destino para a qual o servidor precisa ser migrado.</span><span class="sxs-lookup"><span data-stu-id="dc543-136">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="dc543-137">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="dc543-137">-TargetVMName</span></span>
<span data-ttu-id="dc543-138">Especifica o servidor de respostas para o qual as propriedades precisam ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="dc543-138">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="dc543-139">A ID deve ser recuperada usando Get-AzMigrateServerReplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc543-139">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="dc543-140">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="dc543-140">-TargetVMSize</span></span>
<span data-ttu-id="dc543-141">Atualiza a SKU da VM do Azure a ser criada.</span><span class="sxs-lookup"><span data-stu-id="dc543-141">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="dc543-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc543-142">CommonParameters</span></span>
<span data-ttu-id="dc543-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc543-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc543-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc543-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc543-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc543-145">INPUTS</span></span>

## <span data-ttu-id="dc543-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dc543-146">OUTPUTS</span></span>

### <span data-ttu-id="dc543-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="dc543-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="dc543-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="dc543-148">NOTES</span></span>

<span data-ttu-id="dc543-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dc543-149">ALIASES</span></span>

<span data-ttu-id="dc543-150">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="dc543-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc543-151">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="dc543-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc543-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dc543-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc543-153">INPUTOBJECT <IMigrationItem> : Especifica o servidor de réplica para o qual as propriedades precisam ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="dc543-153">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="dc543-154">O objeto server pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication servidor.</span><span class="sxs-lookup"><span data-stu-id="dc543-154">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="dc543-155">`[Location <String>]`: Localização do Recurso</span><span class="sxs-lookup"><span data-stu-id="dc543-155">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="dc543-156">`[CurrentJobId <String>]`: A ARM ID do trabalho que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="dc543-156">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="dc543-157">`[CurrentJobName <String>]`: O nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="dc543-157">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="dc543-158">`[CurrentJobStartTime <DateTime?>]`: A hora de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="dc543-158">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="dc543-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.</span><span class="sxs-lookup"><span data-stu-id="dc543-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="dc543-160">NICTOUPDATE <IVMwareCbtNicInput[]>: atualiza a NIC para a VM do Azure a ser criada.</span><span class="sxs-lookup"><span data-stu-id="dc543-160">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="dc543-161">`IsPrimaryNic <String>`: Um valor que indica se esse é o NIC principal.</span><span class="sxs-lookup"><span data-stu-id="dc543-161">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="dc543-162">`NicId <String>`: A ID da NIC.</span><span class="sxs-lookup"><span data-stu-id="dc543-162">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="dc543-163">`[IsSelectedForMigration <String>]`: Um valor que indica se essa NIC está selecionada para migração.</span><span class="sxs-lookup"><span data-stu-id="dc543-163">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="dc543-164">`[TargetStaticIPAddress <String>]`: O endereço IP estático.</span><span class="sxs-lookup"><span data-stu-id="dc543-164">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="dc543-165">`[TargetSubnetName <String>]`: Nome da sub-rede de destino.</span><span class="sxs-lookup"><span data-stu-id="dc543-165">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="dc543-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc543-166">RELATED LINKS</span></span>

