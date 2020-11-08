---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 62f9a2d77ce3a5b34b25c98d681bcfba55ae62e4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115516"
---
# <span data-ttu-id="45dbd-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="45dbd-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="45dbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="45dbd-103">Listar todos ou mostrar detalhes de hubs IoT vinculados em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="45dbd-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="45dbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45dbd-104">SYNTAX</span></span>

### <span data-ttu-id="45dbd-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="45dbd-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45dbd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="45dbd-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45dbd-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="45dbd-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45dbd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45dbd-108">DESCRIPTION</span></span>
<span data-ttu-id="45dbd-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="45dbd-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="45dbd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45dbd-110">EXAMPLES</span></span>

### <span data-ttu-id="45dbd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45dbd-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="45dbd-112">Listar todos os hubs IoT vinculados em "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="45dbd-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="45dbd-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="45dbd-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="45dbd-114">Mostrar detalhes do Hub IoT vinculado "myiothub1" em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="45dbd-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="45dbd-115">OS</span><span class="sxs-lookup"><span data-stu-id="45dbd-115">PARAMETERS</span></span>

### <span data-ttu-id="45dbd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45dbd-116">-DefaultProfile</span></span>
<span data-ttu-id="45dbd-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45dbd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45dbd-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="45dbd-118">-DpsObject</span></span>
<span data-ttu-id="45dbd-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="45dbd-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="45dbd-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="45dbd-120">-LinkedHubName</span></span>
<span data-ttu-id="45dbd-121">Nome do host do Hub IoT vinculado</span><span class="sxs-lookup"><span data-stu-id="45dbd-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="45dbd-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="45dbd-122">-Name</span></span>
<span data-ttu-id="45dbd-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="45dbd-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="45dbd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45dbd-124">-ResourceGroupName</span></span>
<span data-ttu-id="45dbd-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="45dbd-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="45dbd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45dbd-126">-ResourceId</span></span>
<span data-ttu-id="45dbd-127">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="45dbd-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="45dbd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45dbd-128">CommonParameters</span></span>
<span data-ttu-id="45dbd-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45dbd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45dbd-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45dbd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45dbd-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45dbd-131">INPUTS</span></span>

### <span data-ttu-id="45dbd-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="45dbd-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="45dbd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="45dbd-133">System.String</span></span>

## <span data-ttu-id="45dbd-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45dbd-134">OUTPUTS</span></span>

### <span data-ttu-id="45dbd-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="45dbd-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="45dbd-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="45dbd-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="45dbd-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45dbd-137">NOTES</span></span>

## <span data-ttu-id="45dbd-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45dbd-138">RELATED LINKS</span></span>
