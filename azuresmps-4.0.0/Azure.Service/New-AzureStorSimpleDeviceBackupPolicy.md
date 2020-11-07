---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946208"
---
# <span data-ttu-id="9309d-101">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9309d-101">New-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="9309d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9309d-102">SYNOPSIS</span></span>
<span data-ttu-id="9309d-103">Cria uma política de backup.</span><span class="sxs-lookup"><span data-stu-id="9309d-103">Creates a backup policy.</span></span>

## <span data-ttu-id="9309d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9309d-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9309d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9309d-105">DESCRIPTION</span></span>
<span data-ttu-id="9309d-106">O cmdlet **New-AzureStorSimpleDeviceBackupPolicy** cria uma política de backup.</span><span class="sxs-lookup"><span data-stu-id="9309d-106">The **New-AzureStorSimpleDeviceBackupPolicy** cmdlet creates a backup policy.</span></span>
<span data-ttu-id="9309d-107">Uma política de backup contém uma ou mais agendas de backup que podem ser executadas em um ou mais volumes.</span><span class="sxs-lookup"><span data-stu-id="9309d-107">A backup policy contains one or more backup schedules that can run on one or more volumes.</span></span>
<span data-ttu-id="9309d-108">Para criar um agendamento de backup, use o cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="9309d-108">To create a backup schedule, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

## <span data-ttu-id="9309d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9309d-109">EXAMPLES</span></span>

### <span data-ttu-id="9309d-110">Exemplo 1: criar uma política de backup</span><span class="sxs-lookup"><span data-stu-id="9309d-110">Example 1: Create a backup policy</span></span>
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="9309d-111">O primeiro comando cria um objeto de configuração de agendamento de backup usando o cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** e, em seguida, armazena esse objeto na variável $Schedule 01.</span><span class="sxs-lookup"><span data-stu-id="9309d-111">The first command creates a backup schedule configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet, and then stores that object in the $Schedule01 variable.</span></span>

<span data-ttu-id="9309d-112">O segundo comando cria outro objeto de configuração de backup usando **New-AzureStorSimpleDeviceBackupScheduleAddConfig** e, em seguida, armazena esse objeto na variável $Schedule 02.</span><span class="sxs-lookup"><span data-stu-id="9309d-112">The second command creates another backup configuration object by using **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , and then stores that object in the $Schedule02 variable.</span></span>

<span data-ttu-id="9309d-113">O terceiro comando cria uma variável de matriz vazia, chamada $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="9309d-113">The third command creates an empty array variable, named $ScheduleArray.</span></span>
<span data-ttu-id="9309d-114">Os próximos dois comandos adicionam os objetos criados nos dois primeiros comandos para $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="9309d-114">The next two commands add the objects created in the first two commands to $ScheduleArray.</span></span>

<span data-ttu-id="9309d-115">O sexto comando obtém um contêiner de volume para o dispositivo chamado Contoso63-AppVm usando o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** e armazena esse objeto de contêiner na variável $DeviceContainer.</span><span class="sxs-lookup"><span data-stu-id="9309d-115">The sixth command gets a volume container for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet, and then stores that container object in the $DeviceContainer variable.</span></span>

<span data-ttu-id="9309d-116">O sétimo comando obtém um volume do contêiner de volume armazenado no primeiro membro de $DeviceContainer usando o cmdlet **Get-AzureStorSimpleDeviceVolume** e, em seguida, armazena esse volume na variável $volume.</span><span class="sxs-lookup"><span data-stu-id="9309d-116">The seventh command gets a volume for the volume container stored in the first member of $DeviceContainer by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then stores that volume in the $Volume variable.</span></span>

<span data-ttu-id="9309d-117">O oitavo comando cria uma variável de matriz vazia, chamada $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="9309d-117">The eighth command creates an empty array variable, named $VolumeArray.</span></span>
<span data-ttu-id="9309d-118">O próximo comando adiciona uma ID de volume a $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="9309d-118">The next command adds a volume ID to $VolumeArray.</span></span>
<span data-ttu-id="9309d-119">Esse valor identifica o volume, armazenado em $Volume, no qual a política de backup é executada.</span><span class="sxs-lookup"><span data-stu-id="9309d-119">This value identifies the volume, stored in $Volume, on which the backup policy runs.</span></span>
<span data-ttu-id="9309d-120">Você pode adicionar IDs de volume adicionais a $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="9309d-120">You can add additional volume IDs to $VolumeArray.</span></span>

<span data-ttu-id="9309d-121">O comando final cria a política de backup chamada GeneralPolicy07 para o dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="9309d-121">The final command creates the backup policy named GeneralPolicy07 for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="9309d-122">O comando especifica os objetos de configuração de agendamento armazenados em $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="9309d-122">The command specifies the schedule configuration objects stored in $ScheduleArray.</span></span>
<span data-ttu-id="9309d-123">O comando especifica o volume ou os volumes aos quais aplicar a política em $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="9309d-123">The command specifies the volume or volumes to which to apply the policy in $VolumeArray.</span></span>
<span data-ttu-id="9309d-124">Você pode verificar a política de backup usando o cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="9309d-124">You can verify the backup policy by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="9309d-125">OS</span><span class="sxs-lookup"><span data-stu-id="9309d-125">PARAMETERS</span></span>

### <span data-ttu-id="9309d-126">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="9309d-126">-BackupPolicyName</span></span>
<span data-ttu-id="9309d-127">Especifica o nome da política de backup.</span><span class="sxs-lookup"><span data-stu-id="9309d-127">Specifies the name of the backup policy.</span></span>

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

### <span data-ttu-id="9309d-128">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="9309d-128">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="9309d-129">Especifica uma matriz de objetos **BackupScheduleBase** para adicionar à política.</span><span class="sxs-lookup"><span data-stu-id="9309d-129">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="9309d-130">Cada objeto representa um cronograma.</span><span class="sxs-lookup"><span data-stu-id="9309d-130">Each object represents a schedule.</span></span>
<span data-ttu-id="9309d-131">Uma política de backup contém um ou mais cronogramas.</span><span class="sxs-lookup"><span data-stu-id="9309d-131">A backup policy contains one or more schedules.</span></span>
<span data-ttu-id="9309d-132">Para obter um objeto **BackupScheduleBase** , use o cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="9309d-132">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9309d-133">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9309d-133">-DeviceName</span></span>
<span data-ttu-id="9309d-134">Especifica o nome do dispositivo StorSimple no qual criar a política de backup.</span><span class="sxs-lookup"><span data-stu-id="9309d-134">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

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

### <span data-ttu-id="9309d-135">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9309d-135">-Profile</span></span>
<span data-ttu-id="9309d-136">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="9309d-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9309d-137">-VolumeIdsToAdd</span><span class="sxs-lookup"><span data-stu-id="9309d-137">-VolumeIdsToAdd</span></span>
<span data-ttu-id="9309d-138">Especifica uma matriz das IDs dos volumes a serem adicionados à política de backup.</span><span class="sxs-lookup"><span data-stu-id="9309d-138">Specifies an array of the IDs of volumes to add to the backup policy.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9309d-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="9309d-139">-WaitForComplete</span></span>
<span data-ttu-id="9309d-140">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9309d-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="9309d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9309d-141">CommonParameters</span></span>
<span data-ttu-id="9309d-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9309d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9309d-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9309d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9309d-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9309d-144">INPUTS</span></span>

### <span data-ttu-id="9309d-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9309d-145">None</span></span>

## <span data-ttu-id="9309d-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9309d-146">OUTPUTS</span></span>

### <span data-ttu-id="9309d-147">BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9309d-147">BackupPolicy</span></span>
<span data-ttu-id="9309d-148">Esse cmdlet retorna um objeto **BackupPolicy** que contém os novos cronogramas e volumes.</span><span class="sxs-lookup"><span data-stu-id="9309d-148">This cmdlet returns a **BackupPolicy** object that contains the new schedules and volumes.</span></span>

## <span data-ttu-id="9309d-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9309d-149">NOTES</span></span>

## <span data-ttu-id="9309d-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9309d-150">RELATED LINKS</span></span>

[<span data-ttu-id="9309d-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9309d-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="9309d-152">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="9309d-152">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="9309d-153">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="9309d-153">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="9309d-154">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9309d-154">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="9309d-155">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9309d-155">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="9309d-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="9309d-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


