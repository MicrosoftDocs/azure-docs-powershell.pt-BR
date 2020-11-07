---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946467"
---
# <span data-ttu-id="c2fc5-101">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="c2fc5-101">Remove-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="c2fc5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fc5-103">Exclui um objeto de backup.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-103">Deletes a backup object.</span></span>

## <span data-ttu-id="c2fc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2fc5-104">SYNTAX</span></span>

### <span data-ttu-id="c2fc5-105">IdentifyById (padrão)</span><span class="sxs-lookup"><span data-stu-id="c2fc5-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c2fc5-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="c2fc5-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c2fc5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2fc5-107">DESCRIPTION</span></span>
<span data-ttu-id="c2fc5-108">O cmdlet **Remove-AzureStorSimpleDeviceBackup** exclui um único objeto de backup.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-108">The **Remove-AzureStorSimpleDeviceBackup** cmdlet deletes a single backup object.</span></span>
<span data-ttu-id="c2fc5-109">Se você tentar excluir um backup que já foi excluído, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-109">If you attempt to delete a backup that has already been deleted, this cmdlet returns an error.</span></span>

## <span data-ttu-id="c2fc5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2fc5-110">EXAMPLES</span></span>

### <span data-ttu-id="c2fc5-111">Exemplo 1: remover um backup de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2fc5-111">Example 1: Remove a backup for a device</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

<span data-ttu-id="c2fc5-112">Esse comando Remove o backup com a ID especificada para o dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-112">This command removes the backup that has the specified ID for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="c2fc5-113">O comando inicia a operação que remove o objeto **backup** e, em seguida, retorna um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="c2fc5-113">The command starts the operation that removes the **Backup** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="c2fc5-114">Para ver o status da tarefa, use o cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="c2fc5-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="c2fc5-115">Exemplo 2: remover o primeiro backup de um dispositivo usando sua ID</span><span class="sxs-lookup"><span data-stu-id="c2fc5-115">Example 2: Remove the first backup for a device by using its ID</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

<span data-ttu-id="c2fc5-116">O primeiro comando obtém os backups do dispositivo chamado Contoso63-AppVm e, em seguida, os armazena na variável $Backup.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-116">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="c2fc5-117">O segundo comando exclui um backup do dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-117">The second command deletes a backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="c2fc5-118">O comando usa a notação de ponto padrão para se referir à propriedade **InstanceId** do primeiro elemento da matriz de $backup.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-118">The command uses standard dot notation to refer to the **InstanceId** property of the first element of the $Backup array.</span></span>
<span data-ttu-id="c2fc5-119">Esse comando especifica o parâmetro *WaitForComplete* e, portanto, o comando aguarda até que a operação seja concluída e, em seguida, retorna um objeto **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="c2fc5-119">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="c2fc5-120">Exemplo 3: remover o primeiro backup de um dispositivo usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="c2fc5-120">Example 3: Remove the first backup for a device by using the pipeline</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

<span data-ttu-id="c2fc5-121">O primeiro comando obtém os backups do dispositivo chamado Contoso63-AppVm e, em seguida, os armazena na variável $Backup.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-121">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="c2fc5-122">O segundo comando passa o primeiro objeto armazenado na matriz $Backup para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-122">The second command passes the first object stored in the $Backup array to the current cmdlet.</span></span>
<span data-ttu-id="c2fc5-123">Esse cmdlet exclui o backup do dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-123">That cmdlet deletes that backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="c2fc5-124">Esse comando especifica o parâmetro *WaitForComplete* e, portanto, o comando aguarda até que a operação seja concluída e, em seguida, retorna um objeto **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="c2fc5-124">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="c2fc5-125">OS</span><span class="sxs-lookup"><span data-stu-id="c2fc5-125">PARAMETERS</span></span>

### <span data-ttu-id="c2fc5-126">-Backup</span><span class="sxs-lookup"><span data-stu-id="c2fc5-126">-Backup</span></span>
<span data-ttu-id="c2fc5-127">Especifica o objeto de **backup** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-127">Specifies the **Backup** object to delete.</span></span>
<span data-ttu-id="c2fc5-128">Para obter um objeto de **backup** , use o cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="c2fc5-128">To obtain a **Backup** object, use the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2fc5-129">-BackupId</span><span class="sxs-lookup"><span data-stu-id="c2fc5-129">-BackupId</span></span>
<span data-ttu-id="c2fc5-130">Especifica a ID de instância de um backup a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-130">Specifies the instance ID of a backup to delete.</span></span>

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

### <span data-ttu-id="c2fc5-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c2fc5-131">-DeviceName</span></span>
<span data-ttu-id="c2fc5-132">Especifica o nome do dispositivo StorSimple no qual excluir um backup.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-132">Specifies the name of the StorSimple device on which to delete a backup.</span></span>

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

### <span data-ttu-id="c2fc5-133">-Force</span><span class="sxs-lookup"><span data-stu-id="c2fc5-133">-Force</span></span>
<span data-ttu-id="c2fc5-134">Indica que esse cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="c2fc5-135">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c2fc5-135">-Profile</span></span>
<span data-ttu-id="c2fc5-136">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="c2fc5-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="c2fc5-137">-WaitForComplete</span></span>
<span data-ttu-id="c2fc5-138">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="c2fc5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fc5-139">CommonParameters</span></span>
<span data-ttu-id="c2fc5-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fc5-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2fc5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fc5-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2fc5-142">INPUTS</span></span>

### <span data-ttu-id="c2fc5-143">Fazer</span><span class="sxs-lookup"><span data-stu-id="c2fc5-143">Backup</span></span>

## <span data-ttu-id="c2fc5-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2fc5-144">OUTPUTS</span></span>

### <span data-ttu-id="c2fc5-145">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="c2fc5-145">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="c2fc5-146">Esse cmdlet retorna um objeto **TaskStatusInfo** se você especificar o parâmetro *WaitForComplete* se você não especificar esse parâmetro, ele retornará um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="c2fc5-146">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="c2fc5-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2fc5-147">NOTES</span></span>

## <span data-ttu-id="c2fc5-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2fc5-148">RELATED LINKS</span></span>

[<span data-ttu-id="c2fc5-149">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="c2fc5-149">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)


