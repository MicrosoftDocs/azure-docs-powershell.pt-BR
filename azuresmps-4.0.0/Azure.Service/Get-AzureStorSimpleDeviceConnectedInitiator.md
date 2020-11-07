---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946291"
---
# <span data-ttu-id="c1c73-101">Get-AzureStorSimpleDeviceConnectedInitiator</span><span class="sxs-lookup"><span data-stu-id="c1c73-101">Get-AzureStorSimpleDeviceConnectedInitiator</span></span>

## <span data-ttu-id="c1c73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1c73-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c73-103">Obtém as conexões iSCSI disponíveis para um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="c1c73-103">Gets the iSCSI connections available for a StorSimple device.</span></span>

## <span data-ttu-id="c1c73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1c73-104">SYNTAX</span></span>

### <span data-ttu-id="c1c73-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="c1c73-105">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c1c73-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="c1c73-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1c73-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1c73-107">DESCRIPTION</span></span>
<span data-ttu-id="c1c73-108">O cmdlet **Get-AzureStorSimpleDeviceConnectedInitiator** Obtém uma lista das conexões iSCSI disponíveis para um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="c1c73-108">The **Get-AzureStorSimpleDeviceConnectedInitiator** cmdlet gets a list of the iSCSI connections available for a StorSimple device.</span></span>
<span data-ttu-id="c1c73-109">Os objetos de conexão iSCSI que este cmdlet retorna contêm as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="c1c73-109">The iSCSI connection objects that this cmdlet returns contain the following properties:</span></span>

- <span data-ttu-id="c1c73-110">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="c1c73-110">**AcrInstanceId**</span></span>
- <span data-ttu-id="c1c73-111">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="c1c73-111">**AcrName**</span></span>
- <span data-ttu-id="c1c73-112">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="c1c73-112">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="c1c73-113">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="c1c73-113">**InitiatorAddress**</span></span>
- <span data-ttu-id="c1c73-114">**Classes**</span><span class="sxs-lookup"><span data-stu-id="c1c73-114">**Interfaces**</span></span>
- <span data-ttu-id="c1c73-115">**Iqn**</span><span class="sxs-lookup"><span data-stu-id="c1c73-115">**Iqn**</span></span>
- <span data-ttu-id="c1c73-116">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="c1c73-116">**IscsiConnectionId**</span></span>

<span data-ttu-id="c1c73-117">Este cmdlet obtém o objeto Connection apenas se as conexões iSCSI estiverem ativadas para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1c73-117">This cmdlet gets connection object only if iSCSI connections are turned on for the device.</span></span>
<span data-ttu-id="c1c73-118">Por padrão, as conexões estão desativadas.</span><span class="sxs-lookup"><span data-stu-id="c1c73-118">By default, connections are turned off.</span></span>

## <span data-ttu-id="c1c73-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1c73-119">EXAMPLES</span></span>

### <span data-ttu-id="c1c73-120">Exemplo 1: obter todas as conexões de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="c1c73-120">Example 1: Get all connections for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

<span data-ttu-id="c1c73-121">Esse comando obtém todas as conexões iSCSI para o dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="c1c73-121">This command gets all iSCSI connections for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="c1c73-122">Esse comando retornará as conexões somente se as conexões estiverem ativadas para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1c73-122">This command returns connections only if connections are turned on for the device.</span></span>

## <span data-ttu-id="c1c73-123">OS</span><span class="sxs-lookup"><span data-stu-id="c1c73-123">PARAMETERS</span></span>

### <span data-ttu-id="c1c73-124">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="c1c73-124">-DeviceId</span></span>
<span data-ttu-id="c1c73-125">Especifica a ID de instância do dispositivo StorSimple do qual obter iniciadores iSCSI.</span><span class="sxs-lookup"><span data-stu-id="c1c73-125">Specifies the instance ID of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c73-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c1c73-126">-DeviceName</span></span>
<span data-ttu-id="c1c73-127">Especifica o nome do dispositivo StorSimple do qual obter iniciadores iSCSI.</span><span class="sxs-lookup"><span data-stu-id="c1c73-127">Specifies the name of the StorSimple device from which to get iSCSI initiators.</span></span>

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

### <span data-ttu-id="c1c73-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c1c73-128">-Profile</span></span>
<span data-ttu-id="c1c73-129">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="c1c73-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="c1c73-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c73-130">CommonParameters</span></span>
<span data-ttu-id="c1c73-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1c73-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c73-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c73-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c73-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1c73-133">INPUTS</span></span>

### <span data-ttu-id="c1c73-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c1c73-134">None</span></span>

## <span data-ttu-id="c1c73-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1c73-135">OUTPUTS</span></span>

### <span data-ttu-id="c1c73-136">Programação\<IscsiConnection\></span><span class="sxs-lookup"><span data-stu-id="c1c73-136">List\<IscsiConnection\></span></span>
<span data-ttu-id="c1c73-137">Esse cmdlet retorna um objeto de conexão iSCSI que contém as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="c1c73-137">This cmdlet returns an iSCSI connection object that contains the following properties:</span></span> 

- <span data-ttu-id="c1c73-138">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="c1c73-138">**AcrInstanceId**</span></span>
- <span data-ttu-id="c1c73-139">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="c1c73-139">**AcrName**</span></span>
- <span data-ttu-id="c1c73-140">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="c1c73-140">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="c1c73-141">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="c1c73-141">**InitiatorAddress**</span></span>
- <span data-ttu-id="c1c73-142">**Classes**</span><span class="sxs-lookup"><span data-stu-id="c1c73-142">**Interfaces**</span></span>
- <span data-ttu-id="c1c73-143">**Iqn**</span><span class="sxs-lookup"><span data-stu-id="c1c73-143">**Iqn**</span></span>
- <span data-ttu-id="c1c73-144">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="c1c73-144">**IscsiConnectionId**</span></span>

## <span data-ttu-id="c1c73-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1c73-145">NOTES</span></span>

## <span data-ttu-id="c1c73-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1c73-146">RELATED LINKS</span></span>

[<span data-ttu-id="c1c73-147">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="c1c73-147">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


