---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945748"
---
# <span data-ttu-id="bc977-101">Start-AzureStorSimpleBackupCloneJob</span><span class="sxs-lookup"><span data-stu-id="bc977-101">Start-AzureStorSimpleBackupCloneJob</span></span>

## <span data-ttu-id="bc977-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc977-102">SYNOPSIS</span></span>
<span data-ttu-id="bc977-103">Inicia um trabalho que clona um backup em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc977-103">Starts a job that clones a backup on a device.</span></span>

## <span data-ttu-id="bc977-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc977-104">SYNTAX</span></span>

### <span data-ttu-id="bc977-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="bc977-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bc977-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="bc977-106">IdentifyByName</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bc977-107">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="bc977-107">IdentifyById</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bc977-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc977-108">DESCRIPTION</span></span>
<span data-ttu-id="bc977-109">O cmdlet **Start-AzureStorSimpleBackupCloneJob** inicia um trabalho que clona um backup existente em um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="bc977-109">The **Start-AzureStorSimpleBackupCloneJob** cmdlet starts a job that clones an existing backup on a StorSimple device.</span></span>

## <span data-ttu-id="bc977-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc977-110">EXAMPLES</span></span>

### <span data-ttu-id="bc977-111">Exemplo 1: clonar um backup para um volume diferente usando nomes de dispositivos</span><span class="sxs-lookup"><span data-stu-id="bc977-111">Example 1: Clone a backup to a different volume by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="bc977-112">O primeiro comando obtém o primeiro backup para o dispositivo chamado ContosoDev07 usando o cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="bc977-112">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="bc977-113">O comando armazena o backup na variável $Backup.</span><span class="sxs-lookup"><span data-stu-id="bc977-113">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="bc977-114">O segundo comando obtém registros de controle de acesso usando o cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="bc977-114">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="bc977-115">O comando armazena o resultado na variável $Acrs.</span><span class="sxs-lookup"><span data-stu-id="bc977-115">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="bc977-116">O comando final inicia um trabalho que clona um backup especificado de um volume em um dispositivo para um volume diferente no mesmo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc977-116">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="bc977-117">Este exemplo especifica o dispositivo por nome.</span><span class="sxs-lookup"><span data-stu-id="bc977-117">This example specifies the device by name.</span></span>
<span data-ttu-id="bc977-118">O comando usa os valores armazenados em $Backup e $Acrs.</span><span class="sxs-lookup"><span data-stu-id="bc977-118">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="bc977-119">O comando retorna a ID do trabalho.</span><span class="sxs-lookup"><span data-stu-id="bc977-119">The command returns the ID of the job.</span></span>

### <span data-ttu-id="bc977-120">Exemplo 2: clonar um backup para um volume diferente usando IDs de dispositivo</span><span class="sxs-lookup"><span data-stu-id="bc977-120">Example 2: Clone a backup to a different volume by using device IDs</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="bc977-121">O primeiro comando obtém o primeiro backup para o dispositivo chamado ContosoDev07 usando o cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="bc977-121">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="bc977-122">O comando armazena o backup na variável $Backup.</span><span class="sxs-lookup"><span data-stu-id="bc977-122">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="bc977-123">O segundo comando obtém registros de controle de acesso usando o cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="bc977-123">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="bc977-124">O comando armazena o resultado na variável $Acrs.</span><span class="sxs-lookup"><span data-stu-id="bc977-124">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="bc977-125">O comando final inicia um trabalho que clona um backup especificado de um volume em um dispositivo para um volume diferente no mesmo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc977-125">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="bc977-126">Este exemplo especifica o dispositivo por ID do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc977-126">This example specifies the device by device ID.</span></span>
<span data-ttu-id="bc977-127">O comando usa os valores armazenados em $Backup e $Acrs.</span><span class="sxs-lookup"><span data-stu-id="bc977-127">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="bc977-128">O comando retorna a ID do trabalho.</span><span class="sxs-lookup"><span data-stu-id="bc977-128">The command returns the ID of the job.</span></span>

### <span data-ttu-id="bc977-129">Exemplo 3: clonar um backup para um volume em um dispositivo diferente usando nomes de dispositivos</span><span class="sxs-lookup"><span data-stu-id="bc977-129">Example 3: Clone a backup to a volume on a different device by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="bc977-130">O primeiro comando obtém o primeiro backup para o dispositivo chamado ContosoDev07 usando o cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="bc977-130">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="bc977-131">O comando armazena o backup na variável $Backup.</span><span class="sxs-lookup"><span data-stu-id="bc977-131">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="bc977-132">O segundo comando obtém registros de controle de acesso usando o cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="bc977-132">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="bc977-133">O comando armazena o resultado na variável $Acrs.</span><span class="sxs-lookup"><span data-stu-id="bc977-133">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="bc977-134">O comando final inicia um trabalho que clona um backup especificado de um volume em um dispositivo para um volume em um dispositivo diferente.</span><span class="sxs-lookup"><span data-stu-id="bc977-134">The final command begins a job that clones a specified backup of a volume on a device to a volume on a different device.</span></span>
<span data-ttu-id="bc977-135">Este exemplo especifica os dispositivos por nome.</span><span class="sxs-lookup"><span data-stu-id="bc977-135">This example specifies the devices by name.</span></span>
<span data-ttu-id="bc977-136">O comando usa os valores armazenados em $Backup e $Acrs.</span><span class="sxs-lookup"><span data-stu-id="bc977-136">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="bc977-137">O comando retorna a ID do trabalho.</span><span class="sxs-lookup"><span data-stu-id="bc977-137">The command returns the ID of the job.</span></span>

### <span data-ttu-id="bc977-138">Exemplo 4: clonar um backup para um volume diferente usando nomes de dispositivos e o operador de pipeline</span><span class="sxs-lookup"><span data-stu-id="bc977-138">Example 4: Clone a backup to a different volume by using device names and the pipeline operator</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

<span data-ttu-id="bc977-139">O primeiro comando obtém o primeiro backup para o dispositivo chamado ContosoDev07 usando o cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="bc977-139">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="bc977-140">O comando armazena o backup na variável $Backup.</span><span class="sxs-lookup"><span data-stu-id="bc977-140">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="bc977-141">O segundo comando obtém registros de controle de acesso usando o cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="bc977-141">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="bc977-142">O comando passa seus resultados para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="bc977-142">The command passes its results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bc977-143">O cmdlet atual inicia um trabalho que clona um backup especificado de um volume em um dispositivo, em um volume diferente no mesmo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc977-143">The current cmdlet begins a job that clones a specified backup of a volume on a device, to a different volume on the same device.</span></span>
<span data-ttu-id="bc977-144">Este exemplo especifica o dispositivo por nome.</span><span class="sxs-lookup"><span data-stu-id="bc977-144">This example specifies the device by name.</span></span>
<span data-ttu-id="bc977-145">O comando usa o valor armazenado em $Backup.</span><span class="sxs-lookup"><span data-stu-id="bc977-145">The command uses the value stored in $Backup.</span></span>
<span data-ttu-id="bc977-146">O comando assume o valor do parâmetro *TargetAccessControlRecords* do pipeline.</span><span class="sxs-lookup"><span data-stu-id="bc977-146">The command takes the value of the *TargetAccessControlRecords* parameter from the pipeline.</span></span>
<span data-ttu-id="bc977-147">O comando retorna a ID do trabalho.</span><span class="sxs-lookup"><span data-stu-id="bc977-147">The command returns the ID of the job.</span></span>

## <span data-ttu-id="bc977-148">OS</span><span class="sxs-lookup"><span data-stu-id="bc977-148">PARAMETERS</span></span>

### <span data-ttu-id="bc977-149">-BackupId</span><span class="sxs-lookup"><span data-stu-id="bc977-149">-BackupId</span></span>
<span data-ttu-id="bc977-150">Especifica a ID da instância do backup a ser clonado.</span><span class="sxs-lookup"><span data-stu-id="bc977-150">Specifies the instance ID of the backup to clone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc977-151">-CloneVolumeName</span><span class="sxs-lookup"><span data-stu-id="bc977-151">-CloneVolumeName</span></span>
<span data-ttu-id="bc977-152">Especifica o nome do novo volume clonado no dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="bc977-152">Specifies the name for the new cloned volume on the target device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc977-153">-Force</span><span class="sxs-lookup"><span data-stu-id="bc977-153">-Force</span></span>
<span data-ttu-id="bc977-154">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bc977-154">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc977-155">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bc977-155">-Profile</span></span>
<span data-ttu-id="bc977-156">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc977-156">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc977-157">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="bc977-157">-Snapshot</span></span>
<span data-ttu-id="bc977-158">Especifica o objeto de instantâneo em que esse cmdlet é clonado.</span><span class="sxs-lookup"><span data-stu-id="bc977-158">Specifies the snapshot object that this cmdlet clones.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc977-159">-SourceDeviceId</span><span class="sxs-lookup"><span data-stu-id="bc977-159">-SourceDeviceId</span></span>
<span data-ttu-id="bc977-160">Especifica a ID da instância do dispositivo de origem.</span><span class="sxs-lookup"><span data-stu-id="bc977-160">Specifies the instance ID of the source device.</span></span>
<span data-ttu-id="bc977-161">Esse cmdlet clona a parte de trás do dispositivo de origem.</span><span class="sxs-lookup"><span data-stu-id="bc977-161">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc977-162">-SourceDeviceName</span><span class="sxs-lookup"><span data-stu-id="bc977-162">-SourceDeviceName</span></span>
<span data-ttu-id="bc977-163">Especifica o nome do dispositivo de origem.</span><span class="sxs-lookup"><span data-stu-id="bc977-163">Specifies the name of the source device.</span></span>
<span data-ttu-id="bc977-164">Esse cmdlet clona a parte de trás do dispositivo de origem.</span><span class="sxs-lookup"><span data-stu-id="bc977-164">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc977-165">-TargetAccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="bc977-165">-TargetAccessControlRecords</span></span>
<span data-ttu-id="bc977-166">Especifica os registros de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="bc977-166">Specifies the access control records.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc977-167">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="bc977-167">-TargetDeviceId</span></span>
<span data-ttu-id="bc977-168">Especifica a ID da instância do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="bc977-168">Specifies the instance ID of the target device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc977-169">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="bc977-169">-TargetDeviceName</span></span>
<span data-ttu-id="bc977-170">Especifica o nome do dispositivo para o qual esse cmdlet clona o backup.</span><span class="sxs-lookup"><span data-stu-id="bc977-170">Specifies the name of the device to which this cmdlet clones the backup.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc977-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc977-171">CommonParameters</span></span>
<span data-ttu-id="bc977-172">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc977-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc977-173">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc977-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc977-174">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc977-174">INPUTS</span></span>

### <span data-ttu-id="bc977-175">Instantâneo, lista de AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="bc977-175">Snapshot, List of AccessControlRecord</span></span>
<span data-ttu-id="bc977-176">Você pode canalizar objetos de **instantâneo** ou uma lista de objetos **AccessControlRecord** para esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc977-176">You can pipe **Snapshot** objects or a list of **AccessControlRecord** objects to this cmdlet.</span></span>

## <span data-ttu-id="bc977-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc977-177">OUTPUTS</span></span>

## <span data-ttu-id="bc977-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc977-178">NOTES</span></span>

## <span data-ttu-id="bc977-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc977-179">RELATED LINKS</span></span>

[<span data-ttu-id="bc977-180">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="bc977-180">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="bc977-181">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="bc977-181">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


