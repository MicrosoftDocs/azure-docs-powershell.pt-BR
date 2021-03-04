---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: cf6b87b8d03855ae79fc0cea62a3bd126f8342a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888352"
---
# <span data-ttu-id="2a4f7-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="2a4f7-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="2a4f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="2a4f7-103">Inicia a replicação para o servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="2a4f7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2a4f7-104">SYNTAX</span></span>

### <span data-ttu-id="2a4f7-105">ByIdDefaultUser (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2a4f7-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <String> -LicenseType <String> -MachineId <String> -OSDiskID <String>
 -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String> -TargetVMName <String>
 [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2a4f7-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="2a4f7-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <String>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2a4f7-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="2a4f7-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <String> -InputObject <IVMwareMachine> -LicenseType <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2a4f7-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="2a4f7-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2a4f7-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2a4f7-109">DESCRIPTION</span></span>
<span data-ttu-id="2a4f7-110">O New-AzMigrateServerReplication cmdlet inicia a replicação de um determinado servidor descoberto no projeto migrar do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="2a4f7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a4f7-111">EXAMPLES</span></span>

### <span data-ttu-id="2a4f7-112">Exemplo 1: quando há apenas disco do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="2a4f7-112">Example 1: When there is only OS disk</span></span>
```powershell
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx4/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskType "Standard_LRS" -OSDiskID "6000C299-343d-7bcd-c05e-a94bd63316dd"

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="2a4f7-113">Isso é para o cenário, quando há apenas um único disco que precisa ser protegido.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="2a4f7-114">Exemplo 2: quando há vários discos</span><span class="sxs-lookup"><span data-stu-id="2a4f7-114">Example 2: When there are multiple disks</span></span>
```powershell
PS C:\> $OSDisk = New-AzMigrateDiskMapping -DiskID '6000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'true'
PS C:\> $DataDisk = New-AzMigrateDiskMapping -DiskID '7000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'false'
PS C:\> $DisksToInclude += $OSDisk
PS C:\> $DisksToInclude += $DataDisk
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskToInclude $DisksToInclude -PerformAutoResync true

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="2a4f7-115">Isso é para o cenário, quando há vários discos que devem ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="2a4f7-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2a4f7-116">PARAMETERS</span></span>

### <span data-ttu-id="2a4f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a4f7-117">-DefaultProfile</span></span>
<span data-ttu-id="2a4f7-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a4f7-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="2a4f7-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="2a4f7-120">Especifica o conjunto dencyption de disco a ser usado.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-120">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4f7-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="2a4f7-121">-DiskToInclude</span></span>
<span data-ttu-id="2a4f7-122">Especifica os discos no servidor de origem a serem incluídos para replicação.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="2a4f7-123">Para construir, consulte a seção NOTES para propriedades DISKTOINCLUDE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput[]
Parameter Sets: ByIdPowerUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4f7-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="2a4f7-124">-DiskType</span></span>
<span data-ttu-id="2a4f7-125">Especifica o tipo de disco a ser usado para a VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4f7-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a4f7-126">-InputObject</span></span>
<span data-ttu-id="2a4f7-127">Especifica o servidor descoberto a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="2a4f7-128">O objeto server pode ser recuperado usando o cmdlet Get-AzMigrateServer servidor.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="2a4f7-129">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine
Parameter Sets: ByInputObjectDefaultUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4f7-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2a4f7-130">-LicenseType</span></span>
<span data-ttu-id="2a4f7-131">Especifica se o benefício híbrido do Azure é aplicável para o servidor de origem a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

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

### <span data-ttu-id="2a4f7-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="2a4f7-132">-MachineId</span></span>
<span data-ttu-id="2a4f7-133">Especifica a ID do computador do servidor descoberto a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByIdPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4f7-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="2a4f7-134">-OSDiskID</span></span>
<span data-ttu-id="2a4f7-135">Especifica o disco do Sistema Operacional para o servidor de origem a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4f7-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="2a4f7-136">-PerformAutoResync</span></span>
<span data-ttu-id="2a4f7-137">Especifica se a replicação será reparada automaticamente caso o controle de alterações seja perdido para o servidor de origem em replicação.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="2a4f7-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a4f7-138">-SubscriptionId</span></span>
<span data-ttu-id="2a4f7-139">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="2a4f7-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2a4f7-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="2a4f7-141">Especifica o Conjunto de Disponibilidade a ser usado para criação de VM Especifica o Conjunto de Disponibilidade a ser usado para criação de VM.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="2a4f7-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="2a4f7-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="2a4f7-143">Especifica a Zona de Disponibilidade a ser usada para criação de VM.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="2a4f7-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2a4f7-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="2a4f7-145">Especifica a conta de armazenamento a ser usada para diagnósticos de inicialização.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="2a4f7-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="2a4f7-146">-TargetNetworkId</span></span>
<span data-ttu-id="2a4f7-147">Especifica a ID da Rede Virtual dentro da assinatura do Azure de destino para a qual o servidor precisa ser migrado.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="2a4f7-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="2a4f7-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="2a4f7-149">Especifica a ID do Grupo de Recursos dentro da assinatura do Azure de destino para a qual o servidor precisa ser migrado.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="2a4f7-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="2a4f7-150">-TargetSubnetName</span></span>
<span data-ttu-id="2a4f7-151">Especifica o nome da Sub-rede no destino Virtual Netowk para o qual o servidor precisa ser migrado.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="2a4f7-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="2a4f7-152">-TargetVMName</span></span>
<span data-ttu-id="2a4f7-153">Especifica o nome da VM do Azure a ser criada.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="2a4f7-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="2a4f7-154">-TargetVMSize</span></span>
<span data-ttu-id="2a4f7-155">Especifica a SKU da VM do Azure a ser criada.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="2a4f7-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="2a4f7-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="2a4f7-157">ID da conta.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-157">Account id.</span></span>

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

### <span data-ttu-id="2a4f7-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a4f7-158">CommonParameters</span></span>
<span data-ttu-id="2a4f7-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a4f7-160">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a4f7-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a4f7-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a4f7-161">INPUTS</span></span>

## <span data-ttu-id="2a4f7-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2a4f7-162">OUTPUTS</span></span>

### <span data-ttu-id="2a4f7-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="2a4f7-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="2a4f7-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="2a4f7-164">NOTES</span></span>

<span data-ttu-id="2a4f7-165">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2a4f7-165">ALIASES</span></span>

<span data-ttu-id="2a4f7-166">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="2a4f7-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a4f7-167">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a4f7-168">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a4f7-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: especifica os discos no servidor de origem a serem incluídos para replicação.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="2a4f7-170">`DiskId <String>`: A ID do disco.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="2a4f7-171">`IsOSDisk <String>`: Um valor que indica se o disco é o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="2a4f7-172">`LogStorageAccountId <String>`: A conta de armazenamento de log ARM Id.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="2a4f7-173">`LogStorageAccountSasSecretName <String>`: O nome secreto do cofre de chaves da conta de armazenamento de log.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="2a4f7-174">`[DiskEncryptionSetId <String>]`: A ID DiskEncryptionSet ARM.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="2a4f7-175">`[DiskType <DiskAccountType?>]`: O tipo de disco.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="2a4f7-176">INPUTOBJECT <IVMwareMachine> : Especifica o servidor descoberto a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="2a4f7-177">O objeto server pode ser recuperado usando o cmdlet Get-AzMigrateServer servidor.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="2a4f7-178">`[GuestOSDetailOstype <String>]`: Tipo do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="2a4f7-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a4f7-179">RELATED LINKS</span></span>

