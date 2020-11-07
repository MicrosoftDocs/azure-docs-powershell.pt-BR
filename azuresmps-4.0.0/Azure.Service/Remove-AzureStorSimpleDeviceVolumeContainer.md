---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C50959BB-7481-4898-BF4B-C5ABF8758473
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2c06455004afbd15235f59164034abc2147964b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946453"
---
# <span data-ttu-id="bc3e1-101">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="bc3e1-101">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="bc3e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc3e1-102">SYNOPSIS</span></span>
<span data-ttu-id="bc3e1-103">Remove um contêiner de volume de um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-103">Removes a volume container from a StorSimple device.</span></span>

## <span data-ttu-id="bc3e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc3e1-104">SYNTAX</span></span>

```
Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainer <DataContainer>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bc3e1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc3e1-105">DESCRIPTION</span></span>
<span data-ttu-id="bc3e1-106">O cmdlet **Remove-AzureStorSimpleDeviceVolumeContainer** remove um objeto de contêiner de volume de um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-106">The **Remove-AzureStorSimpleDeviceVolumeContainer** cmdlet removes a volume container object from a StorSimple device.</span></span>
<span data-ttu-id="bc3e1-107">Esse cmdlet solicita confirmação, a menos que você especifique o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="bc3e1-107">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="bc3e1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc3e1-108">EXAMPLES</span></span>

### <span data-ttu-id="bc3e1-109">Exemplo 1: remover um contêiner usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="bc3e1-109">Example 1: Remove a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" | Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -Force
VERBOSE: ClientRequestId: 0efbb4fc-ceb0-4311-bc49-0e08161d0a37_PS
VERBOSE: ClientRequestId: bf5b615f-47e3-4868-91b6-f2d12217a302_PS
VERBOSE: ClientRequestId: 5590c87e-0602-4197-b6c3-cf58b0e7a7b3_PS
VERBOSE: ClientRequestId: b33c71ac-c345-44ff-8213-d7fdf9f8480a_PS
VERBOSE: ClientRequestId: 903d42ef-58f4-4e89-ba7f-5f234262356d_PS
VERBOSE: About to create a job to remove your Volume container! 
VERBOSE: ClientRequestId: 2279575f-5115-4344-9c6f-9ef599bd203e_PS
e9ddec89-67ac-4e2e-a2ed-820de3547bb0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
e9ddec89-67ac-4e2e-a2ed-820de3547bb0 for tracking the task's status
VERBOSE: Volume container with name: Container08 is found.
```

<span data-ttu-id="bc3e1-110">Esse comando obtém o contêiner de volume chamado Container08 no dispositivo chamado Contoso63-AppVm usando o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="bc3e1-110">This command gets the volume container named Container08 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="bc3e1-111">O comando passa o contêiner de volume para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-111">The command passes the volume container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bc3e1-112">Esse comando inicia a tarefa para remover o contêiner e, em seguida, retorna um objeto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="bc3e1-112">This command starts the task to remove the container, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="bc3e1-113">Para ver o status da tarefa, use o cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="bc3e1-113">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="bc3e1-114">Esse comando especifica o parâmetro *Force* , portanto, não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-114">This command specifies the *Force* parameter, so it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="bc3e1-115">OS</span><span class="sxs-lookup"><span data-stu-id="bc3e1-115">PARAMETERS</span></span>

### <span data-ttu-id="bc3e1-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bc3e1-116">-DeviceName</span></span>
<span data-ttu-id="bc3e1-117">Especifica o nome do dispositivo StorSimple em que existe o contêiner de volume a ser removido.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-117">Specifies the name of the StorSimple device on which to the volume container to remove exists.</span></span>

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

### <span data-ttu-id="bc3e1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bc3e1-118">-Force</span></span>
<span data-ttu-id="bc3e1-119">Indica que esse cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-119">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="bc3e1-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bc3e1-120">-Profile</span></span>
<span data-ttu-id="bc3e1-121">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="bc3e1-122">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="bc3e1-122">-VolumeContainer</span></span>
<span data-ttu-id="bc3e1-123">Especifica o contêiner de volume a ser removido, como um objeto **DataContainer** .</span><span class="sxs-lookup"><span data-stu-id="bc3e1-123">Specifies the volume container to remove, as a **DataContainer** object.</span></span>
<span data-ttu-id="bc3e1-124">Para obter um objeto **DataContainer** , use o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="bc3e1-124">To obtain a **DataContainer** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc3e1-125">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="bc3e1-125">-WaitForComplete</span></span>
<span data-ttu-id="bc3e1-126">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-126">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="bc3e1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc3e1-127">CommonParameters</span></span>
<span data-ttu-id="bc3e1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc3e1-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc3e1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc3e1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc3e1-130">INPUTS</span></span>

### <span data-ttu-id="bc3e1-131">DataContainer</span><span class="sxs-lookup"><span data-stu-id="bc3e1-131">DataContainer</span></span>
<span data-ttu-id="bc3e1-132">Esse cmdlet aceita um objeto **DataContainer** a ser removido.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-132">This cmdlet accepts a **DataContainer** object to remove.</span></span>

## <span data-ttu-id="bc3e1-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc3e1-133">OUTPUTS</span></span>

### <span data-ttu-id="bc3e1-134">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="bc3e1-134">TaskStatusInfo</span></span>
<span data-ttu-id="bc3e1-135">Esse cmdlet retorna um objeto **TaskStatusInfo** , se você especificar o parâmetro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="bc3e1-135">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="bc3e1-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc3e1-136">NOTES</span></span>

## <span data-ttu-id="bc3e1-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc3e1-137">RELATED LINKS</span></span>

[<span data-ttu-id="bc3e1-138">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="bc3e1-138">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="bc3e1-139">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="bc3e1-139">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


