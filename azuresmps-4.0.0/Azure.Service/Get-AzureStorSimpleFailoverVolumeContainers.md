---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945561"
---
# <span data-ttu-id="9082e-101">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="9082e-101">Get-AzureStorSimpleFailoverVolumeContainers</span></span>

## <span data-ttu-id="9082e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9082e-102">SYNOPSIS</span></span>
<span data-ttu-id="9082e-103">Obtém os grupos de contêineres de volume para failover de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9082e-103">Gets the volume container groups for device failover.</span></span>

## <span data-ttu-id="9082e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9082e-104">SYNTAX</span></span>

### <span data-ttu-id="9082e-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="9082e-105">IdentifyById</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9082e-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="9082e-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9082e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9082e-107">DESCRIPTION</span></span>
<span data-ttu-id="9082e-108">O cmdlet **Get-AzureStorSimpleFailoverVolumeContainers** Obtém os grupos de contêineres de volume para failover de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9082e-108">The **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet gets the volume container groups for device failover.</span></span>
<span data-ttu-id="9082e-109">Passe um único grupo **VolumeContainer** ou uma matriz de grupos **VolumeContainer** para o cmdlet **Start-AzureStorSimpleDeviceFailover** .</span><span class="sxs-lookup"><span data-stu-id="9082e-109">Pass a single **VolumeContainer** group or an array of **VolumeContainer** groups to the **Start-AzureStorSimpleDeviceFailover** cmdlet.</span></span>
<span data-ttu-id="9082e-110">Somente os grupos que têm um valor de $True para a propriedade **IsDCGroupEligibleForDR** são elegíveis para failover.</span><span class="sxs-lookup"><span data-stu-id="9082e-110">Only groups that have a value of $True for the **IsDCGroupEligibleForDR** property are eligible for failover.</span></span>

## <span data-ttu-id="9082e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9082e-111">EXAMPLES</span></span>

### <span data-ttu-id="9082e-112">Exemplo 1: obter contêineres de volume de failover</span><span class="sxs-lookup"><span data-stu-id="9082e-112">Example 1: Get failover volume containers</span></span>
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

<span data-ttu-id="9082e-113">Esse comando obtém contêineres de volume de failover.</span><span class="sxs-lookup"><span data-stu-id="9082e-113">This command gets failover volume containers.</span></span>
<span data-ttu-id="9082e-114">Somente os DCGroups que têm um valor de $True para a propriedade **IsDCGroupEligibleForDR** podem ser usados para failover de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9082e-114">Only the DCGroups that have a value of $True for the **IsDCGroupEligibleForDR** property can be used for device failover.</span></span>

## <span data-ttu-id="9082e-115">OS</span><span class="sxs-lookup"><span data-stu-id="9082e-115">PARAMETERS</span></span>

### <span data-ttu-id="9082e-116">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="9082e-116">-DeviceId</span></span>
<span data-ttu-id="9082e-117">Especifica a ID de instância do dispositivo StorSimple no qual executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9082e-117">Specifies the instance ID of the StorSimple device on which to run the cmdlet.</span></span>

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

### <span data-ttu-id="9082e-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9082e-118">-DeviceName</span></span>
<span data-ttu-id="9082e-119">Especifica o nome do dispositivo StorSimple no qual executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9082e-119">Specifies the name of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9082e-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9082e-120">-Profile</span></span>
<span data-ttu-id="9082e-121">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="9082e-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9082e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9082e-122">CommonParameters</span></span>
<span data-ttu-id="9082e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9082e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9082e-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9082e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9082e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9082e-125">INPUTS</span></span>

## <span data-ttu-id="9082e-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9082e-126">OUTPUTS</span></span>

### <span data-ttu-id="9082e-127">IList\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="9082e-127">IList\<DataContainerGroup\></span></span>
<span data-ttu-id="9082e-128">Esse cmdlet retorna uma lista de grupos de **VolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="9082e-128">This cmdlet returns a list of **VolumeContainer** groups.</span></span>

## <span data-ttu-id="9082e-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9082e-129">NOTES</span></span>

## <span data-ttu-id="9082e-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9082e-130">RELATED LINKS</span></span>

[<span data-ttu-id="9082e-131">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="9082e-131">Start-AzureStorSimpleDeviceFailoverJob</span></span>](./Start-AzureStorSimpleDeviceFailoverJob.md)

[<span data-ttu-id="9082e-132">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="9082e-132">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


