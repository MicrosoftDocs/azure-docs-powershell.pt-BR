---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F619B52A-6BFD-43E4-B313-F4C8D95EA966
online version: ''
schema: 2.0.0
ms.openlocfilehash: 570fdc21d650666e1cededbea597a5ef34023596
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945852"
---
# <span data-ttu-id="7b7af-101">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7b7af-101">Set-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="7b7af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b7af-102">SYNOPSIS</span></span>
<span data-ttu-id="7b7af-103">Atualiza uma política de backup existente.</span><span class="sxs-lookup"><span data-stu-id="7b7af-103">Updates an existing backup policy.</span></span>

## <span data-ttu-id="7b7af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b7af-104">SYNTAX</span></span>

```
Set-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> -BackupPolicyName <String>
 [-BackupSchedulesToAdd <PSObject[]>] [-BackupSchedulesToUpdate <PSObject[]>]
 [-BackupScheduleIdsToDelete <PSObject[]>] [-VolumeIdsToUpdate <PSObject[]>] [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7b7af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b7af-105">DESCRIPTION</span></span>
<span data-ttu-id="7b7af-106">O cmdlet **set-AzureStorSimpleDeviceBackupPolicy** atualiza uma política de backup existente.</span><span class="sxs-lookup"><span data-stu-id="7b7af-106">The **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet updates an existing backup policy.</span></span>
<span data-ttu-id="7b7af-107">Você pode renomear a política, adicionar, atualizar ou excluir agendas e atualizar os volumes associados à política.</span><span class="sxs-lookup"><span data-stu-id="7b7af-107">You can rename the policy, add, update or delete schedules, and update the volumes associated with the policy.</span></span>

## <span data-ttu-id="7b7af-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b7af-108">EXAMPLES</span></span>

### <span data-ttu-id="7b7af-109">Exemplo 1: alterar o nome de uma política de backup</span><span class="sxs-lookup"><span data-stu-id="7b7af-109">Example 1: Change the name of a backup policy</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "e6d9f1b3-a250-4d57-966a-039c8eaef9e9" -BackupPolicyName "UpdatedGeneralPolicy07" -WaitForComplete
VERBOSE: ClientRequestId: f4465b46-26cc-40ff-88da-7a28df88c35c_PS
VERBOSE: ClientRequestId: 5e33a35c-e089-47c1-b760-474635b1ead8_PS
VERBOSE: About to run a task to update your backuppolicy! 
VERBOSE: ClientRequestId: e379ebdb-667f-45a9-aafa-a6cd61e5f6f6_PS


JobId        : 9d621bfd-3faa-4d1c-b28b-45c5f4a96975
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: 4fe965ea-4e12-4869-9d67-e42a24b6c5d8_PS
BackupSchedules          : {58e9cd7c-4c6a-4e33-9109-5ec0b8fcb2cc, b10e1bf4-ef0a-4ad3-8fde-eecfc9971dd2}
Volumes                  : {testvolume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 12/16/2014 2:13:28 PM
NextBackup               : 12/16/2014 3:13:43 PM
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : e6d9f1b3-a250-4d57-966a-039c8eaef9e9
Name                     : UpdatedGeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="7b7af-110">Esse comando altera o nome da política de backup que tem a ID especificada para UpdatedGeneralPolicy07.</span><span class="sxs-lookup"><span data-stu-id="7b7af-110">This command changes the name of the backup policy that has the specified ID to UpdatedGeneralPolicy07.</span></span>
<span data-ttu-id="7b7af-111">Esse comando especifica o parâmetro *WaitForComplete* , portanto, o comando conclui a tarefa e, em seguida, retorna um objeto **TaskStatusInfo** para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="7b7af-111">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="7b7af-112">Exemplo 2: atualizar o cronograma de uma política de backup</span><span class="sxs-lookup"><span data-stu-id="7b7af-112">Example 2: Update the schedule for a backup policy</span></span>
```
PS C:\>$UpdateConfig = New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "3a6c6247-6b4d-42e2-aa87-16f4f21476ea" -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 3 -RetentionCount 2 -Enabled $True
PS C:\> $UpdateArray = @()
PS C:\> $UpdateArray += $UpdateConfig
PS C:\> Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "712605f6-eb03-4db8-8f79-e0ce64b2cce1" -BackupSchedulesToUpdate $UpdateArray
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 7b265417-a5f1-45ad-8fbc-33bad4f63ec9
JobSteps   : {Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep...} 
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : d2e10d44e699b371a84db44d19daf1c3
```

<span data-ttu-id="7b7af-113">O primeiro comando cria um objeto de configuração de atualização usando o cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** e, em seguida, armazena-o na variável $UpdateConfig.</span><span class="sxs-lookup"><span data-stu-id="7b7af-113">The first command creates an update configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet, and then stores it in the $UpdateConfig variable.</span></span>

<span data-ttu-id="7b7af-114">O segundo comando cria uma nova variável de matriz, chamada $UpdateArray.</span><span class="sxs-lookup"><span data-stu-id="7b7af-114">The second command creates a new array variable, named $UpdateArray.</span></span>
<span data-ttu-id="7b7af-115">O próximo comando adiciona a atualização armazenada no $UpdateConfig a essa matriz.</span><span class="sxs-lookup"><span data-stu-id="7b7af-115">The next command adds the update stored in $UpdateConfig to that array.</span></span>
<span data-ttu-id="7b7af-116">Você pode adicionar mais de uma atualização à matriz.</span><span class="sxs-lookup"><span data-stu-id="7b7af-116">You can add more than one update to the array.</span></span>

<span data-ttu-id="7b7af-117">O comando final atualiza a política de backup que tem a ID especificada no dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="7b7af-117">The final command updates the backup policy that has the specified ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="7b7af-118">A política agora tem o cronograma atualizado armazenado em $UpdateArray.</span><span class="sxs-lookup"><span data-stu-id="7b7af-118">The policy now has the updated schedule stored in $UpdateArray.</span></span>

## <span data-ttu-id="7b7af-119">OS</span><span class="sxs-lookup"><span data-stu-id="7b7af-119">PARAMETERS</span></span>

### <span data-ttu-id="7b7af-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="7b7af-120">-BackupPolicyId</span></span>
<span data-ttu-id="7b7af-121">Especifica a ID de instância do objeto **BackupPolicy** a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="7b7af-121">Specifies the instance ID of the **BackupPolicy** object to update.</span></span>

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

### <span data-ttu-id="7b7af-122">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="7b7af-122">-BackupPolicyName</span></span>
<span data-ttu-id="7b7af-123">Especifica um novo nome para a política de backup.</span><span class="sxs-lookup"><span data-stu-id="7b7af-123">Specifies a new name for the backup policy.</span></span>

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

### <span data-ttu-id="7b7af-124">-BackupScheduleIdsToDelete</span><span class="sxs-lookup"><span data-stu-id="7b7af-124">-BackupScheduleIdsToDelete</span></span>
<span data-ttu-id="7b7af-125">Especifica uma matriz de IDs de instância de objetos **BackupSchedule** a serem excluídos.</span><span class="sxs-lookup"><span data-stu-id="7b7af-125">Specifies an array of instance IDs of **BackupSchedule** objects to delete.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b7af-126">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="7b7af-126">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="7b7af-127">Especifica uma matriz de objetos **BackupScheduleBase** para adicionar à política.</span><span class="sxs-lookup"><span data-stu-id="7b7af-127">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="7b7af-128">Para obter um objeto **BackupScheduleBase** , use o cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="7b7af-128">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b7af-129">-BackupSchedulesToUpdate</span><span class="sxs-lookup"><span data-stu-id="7b7af-129">-BackupSchedulesToUpdate</span></span>
<span data-ttu-id="7b7af-130">Especifica uma matriz de objetos **BackupScheduleUpdateRequest** para atualizar.</span><span class="sxs-lookup"><span data-stu-id="7b7af-130">Specifies an array of **BackupScheduleUpdateRequest** objects to update.</span></span>
<span data-ttu-id="7b7af-131">Para obter um objeto **BackupScheduleUpdateRequest** , use o cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** .</span><span class="sxs-lookup"><span data-stu-id="7b7af-131">To obtain a **BackupScheduleUpdateRequest** object, use the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b7af-132">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7b7af-132">-DeviceName</span></span>
<span data-ttu-id="7b7af-133">Especifica o nome do dispositivo StorSimple para o qual atualizar a política de backup.</span><span class="sxs-lookup"><span data-stu-id="7b7af-133">Specifies the name of the StorSimple device for which to update the backup policy.</span></span>

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

### <span data-ttu-id="7b7af-134">-NewName</span><span class="sxs-lookup"><span data-stu-id="7b7af-134">-NewName</span></span>
<span data-ttu-id="7b7af-135">Especifica um nome para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b7af-135">Specifies a name for the device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b7af-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7b7af-136">-Profile</span></span>
<span data-ttu-id="7b7af-137">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b7af-137">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="7b7af-138">-VolumeIdsToUpdate</span><span class="sxs-lookup"><span data-stu-id="7b7af-138">-VolumeIdsToUpdate</span></span>
<span data-ttu-id="7b7af-139">Especifica uma matriz de IDs de volumes cujas políticas de backup você deseja atualizar.</span><span class="sxs-lookup"><span data-stu-id="7b7af-139">Specifies an array of IDs of volumes for which to update backup policies.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b7af-140">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="7b7af-140">-WaitForComplete</span></span>
<span data-ttu-id="7b7af-141">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7b7af-141">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="7b7af-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b7af-142">CommonParameters</span></span>
<span data-ttu-id="7b7af-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b7af-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b7af-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b7af-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b7af-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b7af-145">INPUTS</span></span>

### <span data-ttu-id="7b7af-146">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7b7af-146">None</span></span>

## <span data-ttu-id="7b7af-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b7af-147">OUTPUTS</span></span>

### <span data-ttu-id="7b7af-148">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="7b7af-148">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="7b7af-149">Esse cmdlet retorna um objeto **TaskStatusInfo** se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="7b7af-149">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="7b7af-150">Se você não especificar esse parâmetro, ele retornará um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="7b7af-150">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="7b7af-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b7af-151">NOTES</span></span>

## <span data-ttu-id="7b7af-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b7af-152">RELATED LINKS</span></span>

[<span data-ttu-id="7b7af-153">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7b7af-153">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="7b7af-154">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7b7af-154">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="7b7af-155">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7b7af-155">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="7b7af-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="7b7af-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)


