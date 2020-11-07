---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945747"
---
# <span data-ttu-id="d44a8-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="d44a8-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>

## <span data-ttu-id="d44a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d44a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d44a8-103">Inicia um trabalho que restaura um backup em um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="d44a8-103">Starts a job that restores a backup on a StorSimple device.</span></span>

## <span data-ttu-id="d44a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d44a8-104">SYNTAX</span></span>

### <span data-ttu-id="d44a8-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="d44a8-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d44a8-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="d44a8-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d44a8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d44a8-107">DESCRIPTION</span></span>
<span data-ttu-id="d44a8-108">O cmdlet **Start-AzureStorSimpleDeviceBackupRestoreJob** inicia um trabalho que restaura um backup em um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="d44a8-108">The **Start-AzureStorSimpleDeviceBackupRestoreJob** cmdlet starts a job that restores a backup on a StorSimple device.</span></span>
<span data-ttu-id="d44a8-109">Especifique uma ID de backup e uma ID de instantâneo opcional.</span><span class="sxs-lookup"><span data-stu-id="d44a8-109">Specify a backup ID and an optional snapshot ID.</span></span>

## <span data-ttu-id="d44a8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d44a8-110">EXAMPLES</span></span>

### <span data-ttu-id="d44a8-111">Exemplo 1: iniciar um trabalho para restaurar um backup</span><span class="sxs-lookup"><span data-stu-id="d44a8-111">Example 1: Start a job to restore a backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

<span data-ttu-id="d44a8-112">Esse comando inicia um trabalho que restaura o objeto de backup que tem a ID especificada e seus instantâneos associados, no dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="d44a8-112">This command starts a job that restores the backup object that has the specified ID, and its associated snapshots, on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="d44a8-113">O comando especifica o parâmetro *WaitForComplete* , portanto, o trabalho termina antes de o cmdlet retornar o controle ao console.</span><span class="sxs-lookup"><span data-stu-id="d44a8-113">The command specifies the *WaitForComplete* parameter, so the job finishes before the cmdlet returns control to the console.</span></span>

### <span data-ttu-id="d44a8-114">Exemplo 2: iniciar um trabalho para restaurar um instantâneo específico</span><span class="sxs-lookup"><span data-stu-id="d44a8-114">Example 2: Start a job to restore a specific snapshot</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

<span data-ttu-id="d44a8-115">Esse comando inicia um trabalho que restaura o instantâneo de backup com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="d44a8-115">This command starts a job that restores the backup snapshot that has the specified ID.</span></span>
<span data-ttu-id="d44a8-116">O comando especifica o objeto backup por ID no dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="d44a8-116">The command specifies the backup object by ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="d44a8-117">O comando especifica o parâmetro *Force* , portanto, ele inicia o trabalho sem solicitar que você confirme.</span><span class="sxs-lookup"><span data-stu-id="d44a8-117">The command specifies the *Force* parameter, so it starts the job without prompting you to confirm.</span></span>

## <span data-ttu-id="d44a8-118">OS</span><span class="sxs-lookup"><span data-stu-id="d44a8-118">PARAMETERS</span></span>

### <span data-ttu-id="d44a8-119">-BackupId</span><span class="sxs-lookup"><span data-stu-id="d44a8-119">-BackupId</span></span>
<span data-ttu-id="d44a8-120">Especifica a ID da instância do backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="d44a8-120">Specifies the instance ID of the backup to restore.</span></span>

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

### <span data-ttu-id="d44a8-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d44a8-121">-DeviceName</span></span>
<span data-ttu-id="d44a8-122">Especifica o nome do dispositivo StorSimple no qual o backup existe.</span><span class="sxs-lookup"><span data-stu-id="d44a8-122">Specifies the name of the StorSimple device on which the backup exists.</span></span>

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

### <span data-ttu-id="d44a8-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d44a8-123">-Force</span></span>
<span data-ttu-id="d44a8-124">Indica que esse cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="d44a8-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="d44a8-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d44a8-125">-Profile</span></span>
<span data-ttu-id="d44a8-126">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="d44a8-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="d44a8-127">-Captura de imagem</span><span class="sxs-lookup"><span data-stu-id="d44a8-127">-SnapshotId</span></span>
<span data-ttu-id="d44a8-128">Especifica a ID da instância do instantâneo a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="d44a8-128">Specifies the instance ID of the snapshot to restore.</span></span>

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

### <span data-ttu-id="d44a8-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="d44a8-129">-WaitForComplete</span></span>
<span data-ttu-id="d44a8-130">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d44a8-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="d44a8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d44a8-131">CommonParameters</span></span>
<span data-ttu-id="d44a8-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d44a8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d44a8-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d44a8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d44a8-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d44a8-134">INPUTS</span></span>

### <span data-ttu-id="d44a8-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d44a8-135">None</span></span>

## <span data-ttu-id="d44a8-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d44a8-136">OUTPUTS</span></span>

### <span data-ttu-id="d44a8-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="d44a8-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="d44a8-138">Esse cmdlet retorna um objeto **TaskStatusInfo** se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="d44a8-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="d44a8-139">Se você não especificar esse parâmetro, ele retornará um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="d44a8-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="d44a8-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d44a8-140">NOTES</span></span>

## <span data-ttu-id="d44a8-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d44a8-141">RELATED LINKS</span></span>

[<span data-ttu-id="d44a8-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="d44a8-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="d44a8-143">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="d44a8-143">Start-AzureStorSimpleDeviceBackupJob</span></span>](./Start-AzureStorSimpleDeviceBackupJob.md)


