---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: 0ef21777f5a7f22fff5d9352f667d8968ff843f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271964"
---
# <span data-ttu-id="6ebe0-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="6ebe0-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="6ebe0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ebe0-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebe0-103">Inicia a replicação para o servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="6ebe0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ebe0-104">SYNTAX</span></span>

### <span data-ttu-id="6ebe0-105">ByIdDefaultUser (padrão)</span><span class="sxs-lookup"><span data-stu-id="6ebe0-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -LicenseType <LicenseType> -MachineId <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6ebe0-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="6ebe0-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <LicenseType>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6ebe0-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="6ebe0-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-DiskEncryptionSetID <String>]
 [-PerformAutoResync <String>] [-SubscriptionId <String>] [-TargetAvailabilitySet <String>]
 [-TargetAvailabilityZone <String>] [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>]
 [-VMWarerunasaccountID <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6ebe0-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="6ebe0-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6ebe0-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ebe0-109">DESCRIPTION</span></span>
<span data-ttu-id="6ebe0-110">O cmdlet New-AzMigrateServerReplication inicia a replicação de um servidor descoberto específico no projeto de migração do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="6ebe0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ebe0-111">EXAMPLES</span></span>

### <span data-ttu-id="6ebe0-112">Exemplo 1: quando há apenas o disco do so</span><span class="sxs-lookup"><span data-stu-id="6ebe0-112">Example 1: When there is only OS disk</span></span>
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

<span data-ttu-id="6ebe0-113">Isso se destina ao cenário, quando há apenas um único disco que está protegido.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="6ebe0-114">Exemplo 2: quando há vários discos</span><span class="sxs-lookup"><span data-stu-id="6ebe0-114">Example 2: When there are multiple disks</span></span>
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

<span data-ttu-id="6ebe0-115">Isso se destina ao cenário, quando há vários discos que devem ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="6ebe0-116">OS</span><span class="sxs-lookup"><span data-stu-id="6ebe0-116">PARAMETERS</span></span>

### <span data-ttu-id="6ebe0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebe0-117">-DefaultProfile</span></span>
<span data-ttu-id="6ebe0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ebe0-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="6ebe0-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="6ebe0-120">Especifica o conjunto de encyption de disco a ser usado.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-120">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="6ebe0-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="6ebe0-121">-DiskToInclude</span></span>
<span data-ttu-id="6ebe0-122">Especifica os discos no servidor de origem a serem incluídos para replicação.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="6ebe0-123">Para construir, consulte a seção notas para propriedades DISKTOINCLUDE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="6ebe0-124">-Disktype</span><span class="sxs-lookup"><span data-stu-id="6ebe0-124">-DiskType</span></span>
<span data-ttu-id="6ebe0-125">Especifica o tipo de disco a ser usado para a VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebe0-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ebe0-126">-InputObject</span></span>
<span data-ttu-id="6ebe0-127">Especifica o servidor descoberto a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="6ebe0-128">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServer.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="6ebe0-129">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6ebe0-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6ebe0-130">-LicenseType</span></span>
<span data-ttu-id="6ebe0-131">Especifica se o benefício híbrido do Azure é aplicável para o servidor de origem ser migrado.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.LicenseType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebe0-132">-MachineID</span><span class="sxs-lookup"><span data-stu-id="6ebe0-132">-MachineId</span></span>
<span data-ttu-id="6ebe0-133">Especifica a ID da máquina do servidor descoberto a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="6ebe0-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="6ebe0-134">-OSDiskID</span></span>
<span data-ttu-id="6ebe0-135">Especifica o disco do sistema operacional para o qual o servidor de origem será migrado.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

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

### <span data-ttu-id="6ebe0-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="6ebe0-136">-PerformAutoResync</span></span>
<span data-ttu-id="6ebe0-137">Especifica se a replicação será reparada automaticamente para o controle de alterações de maiúsculas e minúsculas ser perdida para o servidor de origem em replicação.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="6ebe0-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ebe0-138">-SubscriptionId</span></span>
<span data-ttu-id="6ebe0-139">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6ebe0-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6ebe0-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="6ebe0-141">Especifica o conjunto de disponibilidade a ser usado para a VM creationSpecifies o conjunto de disponibilidade a ser usado para a criação de VM.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="6ebe0-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="6ebe0-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="6ebe0-143">Especifica a zona de disponibilidade a ser usada para a criação de VM.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="6ebe0-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ebe0-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="6ebe0-145">Especifica a conta de armazenamento a ser usada para o diagnóstico de inicialização.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="6ebe0-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="6ebe0-146">-TargetNetworkId</span></span>
<span data-ttu-id="6ebe0-147">Especifica a ID de rede virtual na assinatura de destino do Azure à qual o servidor precisa ser migrado.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="6ebe0-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="6ebe0-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="6ebe0-149">Especifica a ID do grupo de recursos na assinatura de destino do Azure à qual o servidor precisa ser migrado.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="6ebe0-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="6ebe0-150">-TargetSubnetName</span></span>
<span data-ttu-id="6ebe0-151">Especifica o nome da sub-rede dentro do Netowk virtual de destino para o qual o servidor precisa ser migrado.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="6ebe0-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="6ebe0-152">-TargetVMName</span></span>
<span data-ttu-id="6ebe0-153">Especifica o nome da VM do Azure a ser criada.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="6ebe0-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="6ebe0-154">-TargetVMSize</span></span>
<span data-ttu-id="6ebe0-155">Especifica a SKU da máquina virtual do Azure a ser criada.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="6ebe0-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="6ebe0-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="6ebe0-157">ID da conta.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-157">Account id.</span></span>

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

### <span data-ttu-id="6ebe0-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebe0-158">CommonParameters</span></span>
<span data-ttu-id="6ebe0-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebe0-160">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ebe0-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ebe0-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ebe0-161">INPUTS</span></span>

## <span data-ttu-id="6ebe0-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ebe0-162">OUTPUTS</span></span>

### <span data-ttu-id="6ebe0-163">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="6ebe0-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="6ebe0-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ebe0-164">NOTES</span></span>

<span data-ttu-id="6ebe0-165">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6ebe0-165">ALIASES</span></span>

<span data-ttu-id="6ebe0-166">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="6ebe0-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6ebe0-167">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6ebe0-168">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6ebe0-169">DISKTOINCLUDE <IVMwareCbtDiskInput [] >: especifica os discos no servidor de origem a serem incluídos para replicação.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="6ebe0-170">`DiskId <String>`: A ID de disco.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="6ebe0-171">`IsOSDisk <String>`: Um valor que indica se o disco é o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="6ebe0-172">`LogStorageAccountId <String>`: A ID do braço da conta de armazenamento de log.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="6ebe0-173">`LogStorageAccountSasSecretName <String>`: O nome do segredo do cofre de chaves da conta de armazenamento de log.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="6ebe0-174">`[DiskEncryptionSetId <String>]`: A ID do braço DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="6ebe0-175">`[DiskType <DiskAccountType?>]`: O tipo de disco.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="6ebe0-176">INPUTobject <IVMwareMachine> : especifica o servidor descoberto a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="6ebe0-177">O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServer.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="6ebe0-178">`[GuestOSDetailOstype <String>]`: Tipo do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6ebe0-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="6ebe0-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ebe0-179">RELATED LINKS</span></span>

