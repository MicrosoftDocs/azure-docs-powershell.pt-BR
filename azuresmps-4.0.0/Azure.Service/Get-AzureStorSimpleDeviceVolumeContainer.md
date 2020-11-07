---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945563"
---
# <span data-ttu-id="09a67-101">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="09a67-101">Get-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="09a67-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09a67-102">SYNOPSIS</span></span>
<span data-ttu-id="09a67-103">Obtém contêineres de volume em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09a67-103">Gets volume containers on a device.</span></span>

## <span data-ttu-id="09a67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09a67-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="09a67-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09a67-105">DESCRIPTION</span></span>
<span data-ttu-id="09a67-106">O cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** Obtém uma lista de contêineres de volume em um dispositivo ou contêiner de volume que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="09a67-106">The **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet gets a list of volume containers on a device, or volume container that has the specified name.</span></span>
<span data-ttu-id="09a67-107">O objeto retornado contém as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="09a67-107">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="09a67-108">**BandwidthRate**</span><span class="sxs-lookup"><span data-stu-id="09a67-108">**BandwidthRate**</span></span>
- <span data-ttu-id="09a67-109">**EncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="09a67-109">**EncryptionKey**</span></span>
- <span data-ttu-id="09a67-110">**Instância**</span><span class="sxs-lookup"><span data-stu-id="09a67-110">**InstanceId**</span></span>
- <span data-ttu-id="09a67-111">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="09a67-111">**IsDefault**</span></span>
- <span data-ttu-id="09a67-112">**IsEncryptionEnabled**</span><span class="sxs-lookup"><span data-stu-id="09a67-112">**IsEncryptionEnabled**</span></span>
- <span data-ttu-id="09a67-113">**Sobrenome**</span><span class="sxs-lookup"><span data-stu-id="09a67-113">**Name**</span></span>
- <span data-ttu-id="09a67-114">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="09a67-114">**OperationInProgress**</span></span>
- <span data-ttu-id="09a67-115">**Sua**</span><span class="sxs-lookup"><span data-stu-id="09a67-115">**Owned**</span></span>
- <span data-ttu-id="09a67-116">**PrimaryStorageAccountCredential**</span><span class="sxs-lookup"><span data-stu-id="09a67-116">**PrimaryStorageAccountCredential**</span></span>
- <span data-ttu-id="09a67-117">**SecretsEncryptionThumbprint**</span><span class="sxs-lookup"><span data-stu-id="09a67-117">**SecretsEncryptionThumbprint**</span></span>
- <span data-ttu-id="09a67-118">**VolumeCount**</span><span class="sxs-lookup"><span data-stu-id="09a67-118">**VolumeCount**</span></span>

## <span data-ttu-id="09a67-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09a67-119">EXAMPLES</span></span>

### <span data-ttu-id="09a67-120">Exemplo 1: obter todos os contêineres em um dispositivo</span><span class="sxs-lookup"><span data-stu-id="09a67-120">Example 1: Get all the containers on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

<span data-ttu-id="09a67-121">Esse comando obtém uma lista dos contêineres de volume no dispositivo chamado 8600-bravo 001.</span><span class="sxs-lookup"><span data-stu-id="09a67-121">This command gets a list of the volume containers on the device named 8600-Bravo 001.</span></span>

### <span data-ttu-id="09a67-122">Exemplo 2: obter um contêiner usando seu nome</span><span class="sxs-lookup"><span data-stu-id="09a67-122">Example 2: Get a container by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

<span data-ttu-id="09a67-123">Esse comando obtém o contêiner de volume chamado Container08 no dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="09a67-123">This command gets the volume container named Container08 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="09a67-124">OS</span><span class="sxs-lookup"><span data-stu-id="09a67-124">PARAMETERS</span></span>

### <span data-ttu-id="09a67-125">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="09a67-125">-DeviceName</span></span>
<span data-ttu-id="09a67-126">Especifica o nome de um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="09a67-126">Specifies the name of a StorSimple device.</span></span>
<span data-ttu-id="09a67-127">Esse cmdlet obtém contêineres de volume do dispositivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="09a67-127">This cmdlet gets volume containers from the device that this parameter specifies.</span></span>

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

### <span data-ttu-id="09a67-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="09a67-128">-Profile</span></span>
<span data-ttu-id="09a67-129">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="09a67-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="09a67-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="09a67-130">-VolumeContainerName</span></span>
<span data-ttu-id="09a67-131">Especifica o nome do contêiner de volume a obter.</span><span class="sxs-lookup"><span data-stu-id="09a67-131">Specifies the name of the volume container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a67-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a67-132">CommonParameters</span></span>
<span data-ttu-id="09a67-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09a67-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a67-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09a67-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a67-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09a67-135">INPUTS</span></span>

### <span data-ttu-id="09a67-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="09a67-136">None</span></span>

## <span data-ttu-id="09a67-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09a67-137">OUTPUTS</span></span>

### <span data-ttu-id="09a67-138">DataContainer, IList\<DataContainer\></span><span class="sxs-lookup"><span data-stu-id="09a67-138">DataContainer, IList\<DataContainer\></span></span>
<span data-ttu-id="09a67-139">Esse cmdlet retorna um objeto **DataContainer** , se você especificar o parâmetro *VolumeContainerName* .</span><span class="sxs-lookup"><span data-stu-id="09a67-139">This cmdlet returns a **DataContainer** object, if you specify the *VolumeContainerName* parameter.</span></span>
<span data-ttu-id="09a67-140">Se você não especificar esse parâmetro, esse cmdlet retornará um objeto **IList \<DataContainer\>** .</span><span class="sxs-lookup"><span data-stu-id="09a67-140">If you do not specify that parameter, this cmdlet returns an **IList\<DataContainer\>** object.</span></span>

## <span data-ttu-id="09a67-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09a67-141">NOTES</span></span>

## <span data-ttu-id="09a67-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09a67-142">RELATED LINKS</span></span>

[<span data-ttu-id="09a67-143">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="09a67-143">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="09a67-144">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="09a67-144">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


