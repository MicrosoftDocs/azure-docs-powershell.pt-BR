---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946027"
---
# <span data-ttu-id="458e1-101">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="458e1-101">Start-AzureStorSimpleDeviceBackupJob</span></span>

## <span data-ttu-id="458e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="458e1-102">SYNOPSIS</span></span>
<span data-ttu-id="458e1-103">Inicia um novo trabalho que cria um backup a partir de uma política de backup existente.</span><span class="sxs-lookup"><span data-stu-id="458e1-103">Starts a new job that creates a backup from an existing backup policy.</span></span>

## <span data-ttu-id="458e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="458e1-104">SYNTAX</span></span>

### <span data-ttu-id="458e1-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="458e1-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="458e1-106">BackupTypeGiven</span><span class="sxs-lookup"><span data-stu-id="458e1-106">BackupTypeGiven</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="458e1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="458e1-107">DESCRIPTION</span></span>
<span data-ttu-id="458e1-108">O cmdlet **Start-AzureStorSimpleDeviceBackupJob** inicia um novo trabalho que cria um backup a partir de uma política de backup existente em um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="458e1-108">The **Start-AzureStorSimpleDeviceBackupJob** cmdlet starts a new job that creates a backup from an existing backup policy on a StorSimple device.</span></span>
<span data-ttu-id="458e1-109">Por padrão, esse cmdlet cria um backup de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="458e1-109">By default, this cmdlet creates a local snapshot backup.</span></span>
<span data-ttu-id="458e1-110">Para criar um backup em nuvem, especifique um valor de CloudSnapshot para o parâmetro *backuptype* .</span><span class="sxs-lookup"><span data-stu-id="458e1-110">To create a cloud backup, specify a value of CloudSnapshot for the *BackupType* parameter.</span></span>

## <span data-ttu-id="458e1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="458e1-111">EXAMPLES</span></span>

### <span data-ttu-id="458e1-112">Exemplo 1: criar um backup de instantâneo local</span><span class="sxs-lookup"><span data-stu-id="458e1-112">Example 1: Create a local snapshot backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

<span data-ttu-id="458e1-113">Esse comando cria um backup de instantâneo local para a ID da política especificada.</span><span class="sxs-lookup"><span data-stu-id="458e1-113">This command creates a local snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="458e1-114">Esse comando inicia o trabalho e, em seguida, retorna um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="458e1-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="458e1-115">Para ver o status do trabalho, use o cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="458e1-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="458e1-116">Exemplo 2: criar um backup de instantâneo de nuvem e aguardar para concluir</span><span class="sxs-lookup"><span data-stu-id="458e1-116">Example 2: Create a cloud snapshot backup and wait to finish</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

<span data-ttu-id="458e1-117">Esse comando cria um backup de instantâneo de nuvem para a ID de política especificada.</span><span class="sxs-lookup"><span data-stu-id="458e1-117">This command creates a cloud snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="458e1-118">Esse comando especifica o parâmetro *WaitForComplete* , portanto, o comando conclui a tarefa e, em seguida, retorna um objeto **TaskStatusInfo** para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="458e1-118">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the job.</span></span>

## <span data-ttu-id="458e1-119">OS</span><span class="sxs-lookup"><span data-stu-id="458e1-119">PARAMETERS</span></span>

### <span data-ttu-id="458e1-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="458e1-120">-BackupPolicyId</span></span>
<span data-ttu-id="458e1-121">Especifica a ID da política de backup a ser usada para criar o backup.</span><span class="sxs-lookup"><span data-stu-id="458e1-121">Specifies the ID of the backup policy to use to create the backup.</span></span>

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

### <span data-ttu-id="458e1-122">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="458e1-122">-BackupType</span></span>
<span data-ttu-id="458e1-123">Especifica o tipo de backup.</span><span class="sxs-lookup"><span data-stu-id="458e1-123">Specifies the backup type.</span></span>
<span data-ttu-id="458e1-124">Os valores válidos são: LocalSnapshot e CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="458e1-124">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458e1-125">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="458e1-125">-DeviceName</span></span>
<span data-ttu-id="458e1-126">Especifica o nome do dispositivo StorSimple no qual iniciar o trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="458e1-126">Specifies the name of the StorSimple device on which to start the backup job.</span></span>

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

### <span data-ttu-id="458e1-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="458e1-127">-Profile</span></span>
<span data-ttu-id="458e1-128">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="458e1-128">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="458e1-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="458e1-129">-WaitForComplete</span></span>
<span data-ttu-id="458e1-130">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="458e1-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="458e1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="458e1-131">CommonParameters</span></span>
<span data-ttu-id="458e1-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="458e1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="458e1-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="458e1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="458e1-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="458e1-134">INPUTS</span></span>

### <span data-ttu-id="458e1-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="458e1-135">None</span></span>

## <span data-ttu-id="458e1-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="458e1-136">OUTPUTS</span></span>

### <span data-ttu-id="458e1-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="458e1-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="458e1-138">Esse cmdlet retorna um objeto **TaskStatusInfo** se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="458e1-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="458e1-139">Se você não especificar esse parâmetro, ele retornará um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="458e1-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="458e1-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="458e1-140">NOTES</span></span>

## <span data-ttu-id="458e1-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="458e1-141">RELATED LINKS</span></span>

[<span data-ttu-id="458e1-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="458e1-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="458e1-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="458e1-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


