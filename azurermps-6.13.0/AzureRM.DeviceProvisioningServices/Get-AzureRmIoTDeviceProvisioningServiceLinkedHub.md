---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: bae363b984f148ff55f34eaa04b1ba85eaad4449
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426355"
---
# <span data-ttu-id="fec54-101">Get-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="fec54-101">Get-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="fec54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fec54-102">SYNOPSIS</span></span>
<span data-ttu-id="fec54-103">Listar todos ou mostrar detalhes de hubs IoT vinculados em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="fec54-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fec54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fec54-104">SYNTAX</span></span>

### <span data-ttu-id="fec54-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fec54-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fec54-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fec54-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fec54-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="fec54-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fec54-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fec54-108">DESCRIPTION</span></span>
<span data-ttu-id="fec54-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="fec54-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="fec54-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fec54-110">EXAMPLES</span></span>

### <span data-ttu-id="fec54-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fec54-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="fec54-112">Listar todos os hubs IoT vinculados em "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="fec54-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="fec54-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fec54-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="fec54-114">Mostrar detalhes do Hub IoT vinculado "myiothub1" em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="fec54-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="fec54-115">OS</span><span class="sxs-lookup"><span data-stu-id="fec54-115">PARAMETERS</span></span>

### <span data-ttu-id="fec54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec54-116">-DefaultProfile</span></span>
<span data-ttu-id="fec54-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fec54-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec54-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="fec54-118">-DpsObject</span></span>
<span data-ttu-id="fec54-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="fec54-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fec54-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="fec54-120">-LinkedHubName</span></span>
<span data-ttu-id="fec54-121">Nome do host do Hub IoT vinculado</span><span class="sxs-lookup"><span data-stu-id="fec54-121">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec54-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fec54-122">-Name</span></span>
<span data-ttu-id="fec54-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="fec54-123">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec54-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fec54-124">-ResourceGroupName</span></span>
<span data-ttu-id="fec54-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fec54-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec54-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fec54-126">-ResourceId</span></span>
<span data-ttu-id="fec54-127">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="fec54-127">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fec54-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec54-128">CommonParameters</span></span>
<span data-ttu-id="fec54-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec54-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec54-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fec54-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec54-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fec54-131">INPUTS</span></span>

### <span data-ttu-id="fec54-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="fec54-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="fec54-133">Parâmetros: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fec54-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="fec54-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fec54-134">System.String</span></span>

## <span data-ttu-id="fec54-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fec54-135">OUTPUTS</span></span>

### <span data-ttu-id="fec54-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="fec54-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="fec54-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="fec54-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="fec54-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fec54-138">NOTES</span></span>

## <span data-ttu-id="fec54-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fec54-139">RELATED LINKS</span></span>
