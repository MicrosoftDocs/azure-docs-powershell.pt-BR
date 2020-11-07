---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A62D1A9D-C0EF-4305-B1F9-3AE68A79222D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a5023abffae6bbc2b70b7400e604ffabb1d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946460"
---
# <span data-ttu-id="3797e-101">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="3797e-101">Remove-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="3797e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3797e-102">SYNOPSIS</span></span>
<span data-ttu-id="3797e-103">Remove um volume de um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="3797e-103">Removes a volume from a StorSimple device.</span></span>

## <span data-ttu-id="3797e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3797e-104">SYNTAX</span></span>

### <span data-ttu-id="3797e-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="3797e-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3797e-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="3797e-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3797e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3797e-107">DESCRIPTION</span></span>
<span data-ttu-id="3797e-108">O cmdlet **Remove-AzureStorSimpleDeviceVolume** remove um volume de um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="3797e-108">The **Remove-AzureStorSimpleDeviceVolume** cmdlet removes a volume from a StorSimple device.</span></span>
<span data-ttu-id="3797e-109">Esse cmdlet solicita confirmação, a menos que você especifique o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="3797e-109">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="3797e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3797e-110">EXAMPLES</span></span>

### <span data-ttu-id="3797e-111">Exemplo 1: remover um volume usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="3797e-111">Example 1: Remove a volume by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" | Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: 2933e24d-9564-42b5-9053-5f0bc4f59ea8_PS
VERBOSE: ClientRequestId: 7c2d854b-537a-4253-bb0c-c15bc8aa2b49_PS
VERBOSE: ClientRequestId: 4bf749ac-517c-49e7-8027-a8f62e272014_PS
VERBOSE: ClientRequestId: 7d9ec87a-616d-4ca9-bfb8-158859174d59_PS

Confirm
Are you sure you want to remove the volume? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 67a38e28-a015-44b1-8159-c1a6604f4d81_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: 56101c10-07ca-40f4-8f19-c6fdd895e3a5_PS
32925451-4451-4478-89f7-d8930505d3fb
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
32925451-4451-4478-89f7-d8930505d3fb for tracking the task's status
VERBOSE: Volume with name: Volume18 is found.
```

<span data-ttu-id="3797e-112">Esse comando obtém o volume chamado Volume18 no dispositivo chamado Contoso63-AppVm e, em seguida, passa esse volume para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="3797e-112">This command gets the volume named Volume18 on the device named Contoso63-AppVm, and then passes that volume to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3797e-113">O cmdlet atual inicia a tarefa que remove o volume e, em seguida, retorna um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="3797e-113">The current cmdlet starts the task that removes the volume, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="3797e-114">Para ver o status da tarefa, use o cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="3797e-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="3797e-115">O comando não especifica o parâmetro *Force* , portanto, o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="3797e-115">The command does not specify the *Force* parameter, so the cmdlet prompts you for confirmation.</span></span>

### <span data-ttu-id="3797e-116">Exemplo 2: remover um volume sem confirmação</span><span class="sxs-lookup"><span data-stu-id="3797e-116">Example 2: Remove a volume without confirmation</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Force
VERBOSE: ClientRequestId: 72f13290-41eb-4ac4-9535-da1a42d0fa0b_PS
VERBOSE: ClientRequestId: ae0c1d99-1a66-4a69-9260-f2c8c12546bd_PS
VERBOSE: ClientRequestId: 9610744f-d031-488f-87e6-3ecddb305e13_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: d33525d8-7276-4d2a-942d-d10f8078f1f7_PS
483f8cb4-ebc3-46a9-a9e6-0989e25738a0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
483f8cb4-ebc3-46a9-a9e6-0989e25738a0 for tracking the task's status
```

<span data-ttu-id="3797e-117">Esse comando Remove o volume denominado Volume18 do dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="3797e-117">This command removes the volume named Volume18 from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="3797e-118">O comando especifica o parâmetro *Force* , portanto, o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="3797e-118">The command specifies the *Force* parameter, so the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3797e-119">OS</span><span class="sxs-lookup"><span data-stu-id="3797e-119">PARAMETERS</span></span>

### <span data-ttu-id="3797e-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3797e-120">-DeviceName</span></span>
<span data-ttu-id="3797e-121">Especifica o nome do dispositivo StorSimple em que existe o volume a ser removido.</span><span class="sxs-lookup"><span data-stu-id="3797e-121">Specifies the name of the StorSimple device on which to the volume to remove exists.</span></span>

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

### <span data-ttu-id="3797e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3797e-122">-Force</span></span>
<span data-ttu-id="3797e-123">Indica que esse cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="3797e-123">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="3797e-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3797e-124">-Profile</span></span>
<span data-ttu-id="3797e-125">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="3797e-125">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="3797e-126">-Volume</span><span class="sxs-lookup"><span data-stu-id="3797e-126">-Volume</span></span>
<span data-ttu-id="3797e-127">Especifica o volume a ser removido, como um objeto **VirtualDisk** .</span><span class="sxs-lookup"><span data-stu-id="3797e-127">Specifies the volume to remove, as a **VirtualDisk** object.</span></span>
<span data-ttu-id="3797e-128">Para obter um objeto **VirtualDisk** , use o cmdlet **Get-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="3797e-128">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

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

### <span data-ttu-id="3797e-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="3797e-129">-VolumeName</span></span>
<span data-ttu-id="3797e-130">Especifica o nome do volume a ser removido.</span><span class="sxs-lookup"><span data-stu-id="3797e-130">Specifies the name of the volume to remove.</span></span>

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

### <span data-ttu-id="3797e-131">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="3797e-131">-WaitForComplete</span></span>
<span data-ttu-id="3797e-132">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3797e-132">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="3797e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3797e-133">CommonParameters</span></span>
<span data-ttu-id="3797e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3797e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3797e-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3797e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3797e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3797e-136">INPUTS</span></span>

### <span data-ttu-id="3797e-137">VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="3797e-137">VirtualDisk</span></span>
<span data-ttu-id="3797e-138">Esse cmdlet aceita o objeto **VirtualDisk** para excluir ou o nome do volume do **VirtualDisk** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="3797e-138">This cmdlet accepts either the **VirtualDisk** object to delete or the volume name of the **VirtualDisk** to delete.</span></span>

## <span data-ttu-id="3797e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3797e-139">OUTPUTS</span></span>

### <span data-ttu-id="3797e-140">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="3797e-140">TaskStatusInfo</span></span>
<span data-ttu-id="3797e-141">Esse cmdlet retorna um objeto **TaskStatusInfo** , se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="3797e-141">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="3797e-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3797e-142">NOTES</span></span>

## <span data-ttu-id="3797e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3797e-143">RELATED LINKS</span></span>

[<span data-ttu-id="3797e-144">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="3797e-144">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="3797e-145">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="3797e-145">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="3797e-146">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="3797e-146">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="3797e-147">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="3797e-147">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


