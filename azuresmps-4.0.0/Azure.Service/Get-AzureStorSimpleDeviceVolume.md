---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945566"
---
# <span data-ttu-id="1d080-101">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="1d080-101">Get-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="1d080-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d080-102">SYNOPSIS</span></span>
<span data-ttu-id="1d080-103">Obtém volumes em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d080-103">Gets volumes on a device.</span></span>

## <span data-ttu-id="1d080-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d080-104">SYNTAX</span></span>

### <span data-ttu-id="1d080-105">IdentifyByParentObject</span><span class="sxs-lookup"><span data-stu-id="1d080-105">IdentifyByParentObject</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1d080-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="1d080-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d080-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d080-107">DESCRIPTION</span></span>
<span data-ttu-id="1d080-108">O cmdlet **Get-AzureStorSimpleDeviceVolume** Obtém uma lista de volumes para um contêiner de volume especificado ou um volume que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="1d080-108">The **Get-AzureStorSimpleDeviceVolume** cmdlet gets a list of volumes for a specified volume container, or volume that has the specified name.</span></span>
<span data-ttu-id="1d080-109">O objeto retornado contém as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="1d080-109">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="1d080-110">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="1d080-110">**AccessType**</span></span>
- <span data-ttu-id="1d080-111">**AcrList**</span><span class="sxs-lookup"><span data-stu-id="1d080-111">**AcrList**</span></span>
- <span data-ttu-id="1d080-112">**AppType**</span><span class="sxs-lookup"><span data-stu-id="1d080-112">**AppType**</span></span>
- <span data-ttu-id="1d080-113">**DataContainer**</span><span class="sxs-lookup"><span data-stu-id="1d080-113">**DataContainer**</span></span>
- <span data-ttu-id="1d080-114">**Datacontainerid**</span><span class="sxs-lookup"><span data-stu-id="1d080-114">**DataContainerId**</span></span>
- <span data-ttu-id="1d080-115">**Instância**</span><span class="sxs-lookup"><span data-stu-id="1d080-115">**InstanceId**</span></span>
- <span data-ttu-id="1d080-116">**IsBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="1d080-116">**IsBackupEnabled**</span></span>
- <span data-ttu-id="1d080-117">**IsDefaultBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="1d080-117">**IsDefaultBackupEnabled**</span></span>
- <span data-ttu-id="1d080-118">**IsMonitoringEnabled**</span><span class="sxs-lookup"><span data-stu-id="1d080-118">**IsMonitoringEnabled**</span></span>
- <span data-ttu-id="1d080-119">**Sobrenome**</span><span class="sxs-lookup"><span data-stu-id="1d080-119">**Name**</span></span>
- <span data-ttu-id="1d080-120">**Internet**</span><span class="sxs-lookup"><span data-stu-id="1d080-120">**Online**</span></span>
- <span data-ttu-id="1d080-121">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="1d080-121">**OperationInProgress**</span></span>
- <span data-ttu-id="1d080-122">**SizeInBytes**</span><span class="sxs-lookup"><span data-stu-id="1d080-122">**SizeInBytes**</span></span>
- <span data-ttu-id="1d080-123">**VSN**</span><span class="sxs-lookup"><span data-stu-id="1d080-123">**VSN**</span></span>

## <span data-ttu-id="1d080-124">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d080-124">EXAMPLES</span></span>

### <span data-ttu-id="1d080-125">Exemplo 1: obter volumes em um contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="1d080-125">Example 1: Get volumes in a specified container</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

<span data-ttu-id="1d080-126">Esse comando obtém o contêiner de volume chamado Container03 no dispositivo chamado Contoso63-AppVm usando o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="1d080-126">This command gets the volume container named Container03 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="1d080-127">O comando usa o operador pipeline para passar esse contêiner para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="1d080-127">The command uses the pipeline operator to pass that container to the current cmdlet.</span></span>
<span data-ttu-id="1d080-128">Esse cmdlet obtém todos os volumes nesse contêiner para o dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="1d080-128">That cmdlet gets all the volumes in that container for the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="1d080-129">Exemplo 2: obter um volume usando seu nome</span><span class="sxs-lookup"><span data-stu-id="1d080-129">Example 2: Get a volume by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

<span data-ttu-id="1d080-130">Esse comando obtém o volume chamado Volume18 no dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="1d080-130">This command gets the volume named Volume18 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="1d080-131">OS</span><span class="sxs-lookup"><span data-stu-id="1d080-131">PARAMETERS</span></span>

### <span data-ttu-id="1d080-132">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1d080-132">-DeviceName</span></span>
<span data-ttu-id="1d080-133">Especifica o nome do dispositivo StorSimple do qual obter volumes.</span><span class="sxs-lookup"><span data-stu-id="1d080-133">Specifies the name of the StorSimple device from which to get volumes.</span></span>

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

### <span data-ttu-id="1d080-134">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1d080-134">-Profile</span></span>
<span data-ttu-id="1d080-135">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="1d080-135">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="1d080-136">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="1d080-136">-VolumeContainer</span></span>
<span data-ttu-id="1d080-137">Especifica o contêiner de volume, como um objeto **DataContainer** , que inclui os volumes a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="1d080-137">Specifies the volume container, as a **DataContainer** object, that includes the volumes to get.</span></span>
<span data-ttu-id="1d080-138">Para obter um **DataContainer** , use o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="1d080-138">To obtain a **DataContainer** , use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d080-139">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="1d080-139">-VolumeName</span></span>
<span data-ttu-id="1d080-140">Especifica o nome do volume a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="1d080-140">Specifies the name of the volume to get.</span></span>

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

### <span data-ttu-id="1d080-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d080-141">CommonParameters</span></span>
<span data-ttu-id="1d080-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d080-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d080-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d080-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d080-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d080-144">INPUTS</span></span>

### <span data-ttu-id="1d080-145">DataContainer</span><span class="sxs-lookup"><span data-stu-id="1d080-145">DataContainer</span></span>
<span data-ttu-id="1d080-146">Esse cmdlet aceita um objeto **DataContainer** que contém o volume a obter.</span><span class="sxs-lookup"><span data-stu-id="1d080-146">This cmdlet accepts a **DataContainer** object that contains the volume to get.</span></span>

## <span data-ttu-id="1d080-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d080-147">OUTPUTS</span></span>

### <span data-ttu-id="1d080-148">VirtualDisk, IList\<VirtualDisk\></span><span class="sxs-lookup"><span data-stu-id="1d080-148">VirtualDisk, IList\<VirtualDisk\></span></span>
<span data-ttu-id="1d080-149">Esse cmdlet retorna um objeto **VirtualDisk** se você especificar o parâmetro *VolumeName* .</span><span class="sxs-lookup"><span data-stu-id="1d080-149">This cmdlet returns a **VirtualDisk** object if you specify the *VolumeName* parameter.</span></span>
<span data-ttu-id="1d080-150">Se você especificar o *VolumeContainer* , este cmdlet retornará um **objeto \<VirtualDisk\> IList** .</span><span class="sxs-lookup"><span data-stu-id="1d080-150">If you specify the *VolumeContainer* , this cmdlet returns an **IList\<VirtualDisk\>** object.</span></span>

## <span data-ttu-id="1d080-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d080-151">NOTES</span></span>

## <span data-ttu-id="1d080-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d080-152">RELATED LINKS</span></span>

[<span data-ttu-id="1d080-153">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="1d080-153">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="1d080-154">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="1d080-154">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="1d080-155">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="1d080-155">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="1d080-156">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="1d080-156">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


