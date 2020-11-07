---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 049201C9-590F-47EB-9030-25F80CD8DFA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f3337556a9d7bd52e5800af5cdbd65b71ab9818
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945523"
---
# <span data-ttu-id="409b6-101">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="409b6-101">New-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="409b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="409b6-102">SYNOPSIS</span></span>
<span data-ttu-id="409b6-103">Cria um volume em um contêiner de volume especificado.</span><span class="sxs-lookup"><span data-stu-id="409b6-103">Creates a volume in a specified volume container.</span></span>

## <span data-ttu-id="409b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="409b6-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer> -VolumeName <String>
 -VolumeSizeInBytes <Int64>
 -AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>
 -VolumeAppType <AppType> -Online <Boolean> -EnableDefaultBackup <Boolean> -EnableMonitoring <Boolean>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="409b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="409b6-105">DESCRIPTION</span></span>
<span data-ttu-id="409b6-106">O cmdlet **New-AzureStorSimpleDeviceVolume** cria um volume em um contêiner de volume especificado.</span><span class="sxs-lookup"><span data-stu-id="409b6-106">The **New-AzureStorSimpleDeviceVolume** cmdlet creates a volume in a specified volume container.</span></span>
<span data-ttu-id="409b6-107">Este cmdlet associa cada volume a um ou mais registros de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="409b6-107">This cmdlet associates each volume with one or more access control records.</span></span>
<span data-ttu-id="409b6-108">Para obter objetos **AccessControlRecord** , use o cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="409b6-108">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="409b6-109">Especifique um nome, tamanho e AppType para o volume.</span><span class="sxs-lookup"><span data-stu-id="409b6-109">Specify a name, size, and AppType for the volume.</span></span>
<span data-ttu-id="409b6-110">Além disso, especifique se deseja criar o volume online, se deseja habilitar o backup padrão e se deseja habilitar o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="409b6-110">Also, specify whether to create the volume online, whether to enable default backup, and whether to enable monitoring.</span></span>

## <span data-ttu-id="409b6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="409b6-111">EXAMPLES</span></span>

### <span data-ttu-id="409b6-112">Exemplo 1: criar um volume</span><span class="sxs-lookup"><span data-stu-id="409b6-112">Example 1: Create a volume</span></span>
```
PS C:\>$AcrList = Get-AzureStorSimpleAccessControlRecord
PS C:\> Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer07" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Size 2000000000 -AccessControlRecords $AcrList -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False

VERBOSE: ClientRequestId: a29d1a84-1f81-4f20-9130-7adfe45e41fb_PS
VERBOSE: ClientRequestId: 8fa63df1-3f81-4029-a536-b536a70068ad_PS
VERBOSE: ClientRequestId: 964c5744-8bb1-4f70-beda-95ca4c7f3eb6_PS
VERBOSE: ClientRequestId: f09fff3a-54fa-4a0e-93db-b079260ed2dd_PS
VERBOSE: ClientRequestId: 59aa29e3-8044-411a-adae-b64a2681ffed_PS
VERBOSE: ClientRequestId: 0ffd0297-19be-40fe-a64e-6a2947d831b4_PS
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90 for tracking the task's status
VERBOSE: Volume container with name: VolumeContainer07 is found.
```

<span data-ttu-id="409b6-113">O primeiro comando obtém os registros de controle de acesso na configuração do serviço StorSimple Manager usando o cmdlet **Get-AzureStorSimpleAccessControlRecord** e, em seguida, os armazena na variável $AcrList.</span><span class="sxs-lookup"><span data-stu-id="409b6-113">The first command gets the access control records in the StorSimple Manager service configuration by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet, and then stores them in the $AcrList variable.</span></span>

<span data-ttu-id="409b6-114">O segundo comando obtém o contêiner de volume chamado VolumeContainer07 para o dispositivo chamado Contoso63-AppVm usando o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="409b6-114">The second command gets the volume container named VolumeContainer07 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="409b6-115">O comando passa esse contêiner para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="409b6-115">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="409b6-116">Esse cmdlet cria o volume.</span><span class="sxs-lookup"><span data-stu-id="409b6-116">This cmdlet creates the volume.</span></span>
<span data-ttu-id="409b6-117">O comando especifica o nome do volume, do tamanho e dos registros de controle de acesso armazenados em $AcrList.</span><span class="sxs-lookup"><span data-stu-id="409b6-117">The command specifies the name for the volume, the size, and the access control records stored in $AcrList.</span></span>
<span data-ttu-id="409b6-118">Esse comando inicia o trabalho e, em seguida, retorna um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="409b6-118">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="409b6-119">Para ver o status do trabalho, use o cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="409b6-119">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="409b6-120">Exemplo 2: criar um volume sem o Access Controlaccess Control recordsaccess Control</span><span class="sxs-lookup"><span data-stu-id="409b6-120">Example 2: Create a volume without Access Controlaccess control recordsaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer01" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume22" -Size 2000000000 -AccessControlRecords @() -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False -WaitForComplete
VERBOSE: ClientRequestId: 3f359790-7e1f-48e7-acf8-ecabba850966_PS
VERBOSE: ClientRequestId: 2723ebcf-cd72-47bb-99b5-0c099d45641b_PS
VERBOSE: ClientRequestId: e605091f-dd63-42a7-bda2-24753cbc1f9a_PS
VERBOSE: ClientRequestId: b3fd08c3-67c5-4309-9591-15d92c360469_PS
VERBOSE: ClientRequestId: 15a024a3-b0c9-4f83-9c34-0ed8b95d024b_PS
VERBOSE: ClientRequestId: c13f92f9-aea1-40dd-af80-3affe273adbe_PS


TaskId       : ceef657e-390e-4f7a-aab7-669a29c29e7f
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 1d79febf-f752-4255-af2d-230d40773bc6_PS
AccessType             : NoAccess
AcrIdList              : {}
AcrList                : {}
AppType                : PrimaryVolume
DataContainer          : Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainer
DataContainerId        : 68b63d15-6aa5-4e69-9f9d-4a0bc607d6e9
InstanceId             : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd
InternalInstanceId     : 
IsBackupEnabled        : False
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
Name                   : Volume22
Online                 : True
OperationInProgress    : None
SizeInBytes            : 2000000000
VSN                    : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd

VERBOSE: Volume container with name: VolumeContainer01 is found.
```

<span data-ttu-id="409b6-121">Esse comando obtém o contêiner de volume chamado VolumeContainer01 para o dispositivo chamado Contoso63-AppVm usando o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="409b6-121">This command gets the volume container named VolumeContainer01 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="409b6-122">O comando passa esse contêiner para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="409b6-122">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="409b6-123">Esse cmdlet cria o volume.</span><span class="sxs-lookup"><span data-stu-id="409b6-123">This cmdlet creates the volume.</span></span>
<span data-ttu-id="409b6-124">O comando especifica o nome do volume, o tamanho e um valor vazio para os registros de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="409b6-124">The command specifies the name for the volume, the size, and an empty value for access control records.</span></span>
<span data-ttu-id="409b6-125">Esse comando especifica o parâmetro *WaitForComplete* , portanto retorna um **TaskStatusInfo** depois que ele cria o volume.</span><span class="sxs-lookup"><span data-stu-id="409b6-125">This command specifies the *WaitForComplete* parameter, so it returns a **TaskStatusInfo** after it creates the volume.</span></span>

<span data-ttu-id="409b6-126">Como o comando especifica nenhum registro de controle de acesso, esse volume não pode ser acessado.</span><span class="sxs-lookup"><span data-stu-id="409b6-126">Because the command specifies no access control records, this volume cannot be accessed.</span></span>
<span data-ttu-id="409b6-127">Você pode adicionar o Access mais tarde usando o cmdlet **set-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="409b6-127">You can add access, later, by using **Set-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

## <span data-ttu-id="409b6-128">OS</span><span class="sxs-lookup"><span data-stu-id="409b6-128">PARAMETERS</span></span>

### <span data-ttu-id="409b6-129">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="409b6-129">-AccessControlRecords</span></span>
<span data-ttu-id="409b6-130">Especifica uma lista de registros de controle de acesso a serem associados ao volume.</span><span class="sxs-lookup"><span data-stu-id="409b6-130">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="409b6-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="409b6-131">-DeviceName</span></span>
<span data-ttu-id="409b6-132">Especifica o nome do dispositivo StorSimple no qual criar o volume.</span><span class="sxs-lookup"><span data-stu-id="409b6-132">Specifies the name of the StorSimple device on which to create the volume.</span></span>

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

### <span data-ttu-id="409b6-133">-EnableDefaultBackup</span><span class="sxs-lookup"><span data-stu-id="409b6-133">-EnableDefaultBackup</span></span>
<span data-ttu-id="409b6-134">Especifica se o backup padrão deve ser habilitado para o volume.</span><span class="sxs-lookup"><span data-stu-id="409b6-134">Specifies whether to enable default backup for the volume.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409b6-135">-EnableMonitoring</span><span class="sxs-lookup"><span data-stu-id="409b6-135">-EnableMonitoring</span></span>
<span data-ttu-id="409b6-136">Especifica se o monitoramento do volume deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="409b6-136">Specifies whether to enable monitoring for the volume.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409b6-137">-Online</span><span class="sxs-lookup"><span data-stu-id="409b6-137">-Online</span></span>
<span data-ttu-id="409b6-138">Especifica se você deseja criar o volume online.</span><span class="sxs-lookup"><span data-stu-id="409b6-138">Specifies whether to create the volume online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409b6-139">-Perfil</span><span class="sxs-lookup"><span data-stu-id="409b6-139">-Profile</span></span>
<span data-ttu-id="409b6-140">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="409b6-140">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="409b6-141">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="409b6-141">-VolumeAppType</span></span>
<span data-ttu-id="409b6-142">Especifica se um volume principal ou de arquivamento deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="409b6-142">Specifies whether to create a primary or archive volume.</span></span>
<span data-ttu-id="409b6-143">Os valores válidos são: PrimaryVolume e ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="409b6-143">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409b6-144">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="409b6-144">-VolumeContainer</span></span>
<span data-ttu-id="409b6-145">Especifica o contêiner, como um objeto **DataContainer** , no qual criar o volume.</span><span class="sxs-lookup"><span data-stu-id="409b6-145">Specifies the container, as a **DataContainer** object, in which to create the volume.</span></span>
<span data-ttu-id="409b6-146">Para obter um objeto **VirtualDisk** , use o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="409b6-146">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="409b6-147">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="409b6-147">-VolumeName</span></span>
<span data-ttu-id="409b6-148">Especifica um nome para o novo volume.</span><span class="sxs-lookup"><span data-stu-id="409b6-148">Specifies a name for the new volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409b6-149">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="409b6-149">-VolumeSizeInBytes</span></span>
<span data-ttu-id="409b6-150">Especifica o tamanho do volume em bytes.</span><span class="sxs-lookup"><span data-stu-id="409b6-150">Specifies the volume size in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409b6-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="409b6-151">-WaitForComplete</span></span>
<span data-ttu-id="409b6-152">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="409b6-152">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="409b6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="409b6-153">CommonParameters</span></span>
<span data-ttu-id="409b6-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="409b6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="409b6-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="409b6-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="409b6-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="409b6-156">INPUTS</span></span>

### <span data-ttu-id="409b6-157">DataContainer, lista\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="409b6-157">DataContainer, List\<AccessControlRecord\></span></span>
<span data-ttu-id="409b6-158">Esse cmdlet aceita um objeto **DataContainer** e uma lista de objetos **AccessControlRecord** para o novo volume.</span><span class="sxs-lookup"><span data-stu-id="409b6-158">This cmdlet accepts a **DataContainer** object and a list of **AccessControlRecord** objects for the new volume.</span></span>

## <span data-ttu-id="409b6-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="409b6-159">OUTPUTS</span></span>

### <span data-ttu-id="409b6-160">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="409b6-160">TaskStatusInfo</span></span>
<span data-ttu-id="409b6-161">Esse cmdlet retorna um objeto **TaskStatusInfo** , se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="409b6-161">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="409b6-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="409b6-162">NOTES</span></span>

## <span data-ttu-id="409b6-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="409b6-163">RELATED LINKS</span></span>

[<span data-ttu-id="409b6-164">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="409b6-164">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="409b6-165">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="409b6-165">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="409b6-166">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="409b6-166">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="409b6-167">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="409b6-167">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="409b6-168">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="409b6-168">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="409b6-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="409b6-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


