---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 39E9BB88-6AD8-4B05-9498-35393E22BA30
online version: ''
schema: 2.0.0
ms.openlocfilehash: 234b1f7fa2719cc1b34e6bcd0b8e8fd340acc4af
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946418"
---
# <span data-ttu-id="50434-101">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="50434-101">Set-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="50434-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50434-102">SYNOPSIS</span></span>
<span data-ttu-id="50434-103">Atualiza as propriedades de um volume existente.</span><span class="sxs-lookup"><span data-stu-id="50434-103">Updates the properties of an existing volume.</span></span>

## <span data-ttu-id="50434-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50434-104">SYNTAX</span></span>

### <span data-ttu-id="50434-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="50434-105">IdentifyByName</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="50434-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="50434-106">IdentifyByObject</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="50434-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50434-107">DESCRIPTION</span></span>
<span data-ttu-id="50434-108">O cmdlet **set-AzureStorSimpleDeviceVolume** atualiza as propriedades de um volume existente.</span><span class="sxs-lookup"><span data-stu-id="50434-108">The **Set-AzureStorSimpleDeviceVolume** cmdlet updates the properties of an existing volume.</span></span>
<span data-ttu-id="50434-109">Este cmdlet associa um volume a um ou mais registros de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="50434-109">This cmdlet associates a volume with one or more access control records.</span></span>
<span data-ttu-id="50434-110">Para obter objetos **AccessControlRecord** , use o cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="50434-110">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="50434-111">Atualize o tamanho ou o tipo do volume.</span><span class="sxs-lookup"><span data-stu-id="50434-111">Update the size or type for the volume.</span></span>
<span data-ttu-id="50434-112">Atualize também se deseja criar o volume online.</span><span class="sxs-lookup"><span data-stu-id="50434-112">Also, update whether to create the volume online.</span></span>

## <span data-ttu-id="50434-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50434-113">EXAMPLES</span></span>

### <span data-ttu-id="50434-114">Exemplo 1: atualizar o valor online para um volume</span><span class="sxs-lookup"><span data-stu-id="50434-114">Example 1: Update online value for a volume</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $False
VERBOSE: ClientRequestId: f2869570-ea47-4be7-801e-9c0f22f2600d_PS
VERBOSE: ClientRequestId: c70bb86a-51d3-4390-be17-4d0847641dc3_PS
VERBOSE: ClientRequestId: d20cb5b2-6b3c-4e06-af99-cada28c5e50a_PS
VERBOSE: ClientRequestId: ab6d533e-b55b-4cfb-9c58-9153295e0547_PS
de7000f1-29c7-4102-a375-b52432f9e67e
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
de7000f1-29c7-4102-a375-b52432f9e67e for tracking the task's status
```

<span data-ttu-id="50434-115">Esse comando atualiza o volume denominado Volume18 para ter um valor online de $False.</span><span class="sxs-lookup"><span data-stu-id="50434-115">This command updates the volume named Volume18 to have an online value of $False.</span></span>
<span data-ttu-id="50434-116">Esse comando inicia a tarefa e, em seguida, retorna um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="50434-116">This command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="50434-117">Para ver o status da tarefa, use o cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="50434-117">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="50434-118">Exemplo 2: modificar o valor e o tipo online</span><span class="sxs-lookup"><span data-stu-id="50434-118">Example 2: Modify online value and type</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $True -VolumeAppType ArchiveVolume 
VERBOSE: ClientRequestId: af42b02a-645e-4801-a2d7-4197511c68cf_PS
VERBOSE: ClientRequestId: 7cb4f3b4-548e-42dc-a38c-0df0911c5206_PS
VERBOSE: ClientRequestId: 7cc706ad-a58f-4939-8e78-cabae8379a51_PS
VERBOSE: ClientRequestId: 6bed21d5-12fc-4a12-a89c-120bdb5636b1_PS
aa977225-af78-4c93-b754-72704afc928f
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
aa977225-af78-4c93-b754-72704afc928f for tracking the task's status
```

<span data-ttu-id="50434-119">Esse comando atualiza o volume chamado Volume18.</span><span class="sxs-lookup"><span data-stu-id="50434-119">This command updates the volume named Volume18.</span></span>
<span data-ttu-id="50434-120">Ele modifica o tipo e altera o valor do parâmetro *online* para $true.</span><span class="sxs-lookup"><span data-stu-id="50434-120">It modifies the type and changes the value of the *Online* parameter to $True.</span></span>

## <span data-ttu-id="50434-121">OS</span><span class="sxs-lookup"><span data-stu-id="50434-121">PARAMETERS</span></span>

### <span data-ttu-id="50434-122">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="50434-122">-AccessControlRecords</span></span>
<span data-ttu-id="50434-123">Especifica uma lista de registros de controle de acesso a serem associados ao volume.</span><span class="sxs-lookup"><span data-stu-id="50434-123">Specifies a list of access control records to associate with the volume.</span></span>

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

### <span data-ttu-id="50434-124">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="50434-124">-DeviceName</span></span>
<span data-ttu-id="50434-125">Especifica o nome do dispositivo StorSimple no qual o volume deve ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="50434-125">Specifies the name of the StorSimple device on which to update the volume exists.</span></span>

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

### <span data-ttu-id="50434-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="50434-126">-InformationAction</span></span>
<span data-ttu-id="50434-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="50434-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="50434-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="50434-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="50434-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="50434-129">Continue</span></span>
- <span data-ttu-id="50434-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="50434-130">Ignore</span></span>
- <span data-ttu-id="50434-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="50434-131">Inquire</span></span>
- <span data-ttu-id="50434-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="50434-132">SilentlyContinue</span></span>
- <span data-ttu-id="50434-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="50434-133">Stop</span></span>
- <span data-ttu-id="50434-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="50434-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50434-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="50434-135">-InformationVariable</span></span>
<span data-ttu-id="50434-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="50434-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50434-137">-NewName</span><span class="sxs-lookup"><span data-stu-id="50434-137">-NewName</span></span>
<span data-ttu-id="50434-138">Especifica um novo nome para o dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="50434-138">Specifies a new name for the StorSimple device.</span></span>

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

### <span data-ttu-id="50434-139">-Online</span><span class="sxs-lookup"><span data-stu-id="50434-139">-Online</span></span>
<span data-ttu-id="50434-140">Especifica se o volume está online.</span><span class="sxs-lookup"><span data-stu-id="50434-140">Specifies whether the volume is online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50434-141">-Perfil</span><span class="sxs-lookup"><span data-stu-id="50434-141">-Profile</span></span>
<span data-ttu-id="50434-142">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="50434-142">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="50434-143">-Volume</span><span class="sxs-lookup"><span data-stu-id="50434-143">-Volume</span></span>
<span data-ttu-id="50434-144">Especifica o nome do volume a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="50434-144">Specifies the name of the volume to update.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50434-145">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="50434-145">-VolumeAppType</span></span>
<span data-ttu-id="50434-146">Especifica se o volume deve ser atualizado para ser um volume principal ou de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="50434-146">Specifies whether to update the volume to be a primary or archive volume.</span></span>
<span data-ttu-id="50434-147">Os valores válidos são: PrimaryVolume e ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="50434-147">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50434-148">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="50434-148">-VolumeName</span></span>
<span data-ttu-id="50434-149">Especifica o nome do volume a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="50434-149">Specifies the name of the volume to update.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50434-150">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="50434-150">-VolumeSizeInBytes</span></span>
<span data-ttu-id="50434-151">Especifica o tamanho atualizado, em bytes, para o volume.</span><span class="sxs-lookup"><span data-stu-id="50434-151">Specifies the updated size, in bytes, for the volume.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50434-152">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="50434-152">-WaitForComplete</span></span>
<span data-ttu-id="50434-153">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="50434-153">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="50434-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50434-154">CommonParameters</span></span>
<span data-ttu-id="50434-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50434-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50434-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50434-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50434-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50434-157">INPUTS</span></span>

### <span data-ttu-id="50434-158">Programação\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="50434-158">List\<AccessControlRecord\></span></span>
<span data-ttu-id="50434-159">Esse cmdlet aceita uma lista de objetos **AccessControlRecord** para associar a um volume.</span><span class="sxs-lookup"><span data-stu-id="50434-159">This cmdlet accepts a list of **AccessControlRecord** objects to associate to a volume.</span></span>

## <span data-ttu-id="50434-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50434-160">OUTPUTS</span></span>

### <span data-ttu-id="50434-161">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="50434-161">TaskStatusInfo</span></span>
<span data-ttu-id="50434-162">Esse cmdlet retorna um objeto **TaskStatusInfo** , se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="50434-162">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="50434-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50434-163">NOTES</span></span>

## <span data-ttu-id="50434-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50434-164">RELATED LINKS</span></span>

[<span data-ttu-id="50434-165">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="50434-165">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="50434-166">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="50434-166">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="50434-167">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="50434-167">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="50434-168">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="50434-168">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="50434-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="50434-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


