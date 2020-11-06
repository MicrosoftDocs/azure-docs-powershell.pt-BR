---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ca32f2d0436ea16d8897f279239ce4de079d1550
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602949"
---
# <span data-ttu-id="439c3-101">Add-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="439c3-101">Add-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="439c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="439c3-102">SYNOPSIS</span></span>
<span data-ttu-id="439c3-103">Hub IoT vinculado a um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="439c3-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="439c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="439c3-104">SYNTAX</span></span>

### <span data-ttu-id="439c3-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="439c3-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="439c3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="439c3-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="439c3-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="439c3-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="439c3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="439c3-108">DESCRIPTION</span></span>
<span data-ttu-id="439c3-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="439c3-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="439c3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="439c3-110">EXAMPLES</span></span>

### <span data-ttu-id="439c3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="439c3-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="439c3-112">Hub IoT vinculado a um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="439c3-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="439c3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="439c3-113">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="439c3-114">Hub IoT vinculado a um serviço de provisionamento de dispositivo Hub IoT do Azure com o AllocationWeight e o ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="439c3-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="439c3-115">OS</span><span class="sxs-lookup"><span data-stu-id="439c3-115">PARAMETERS</span></span>

### <span data-ttu-id="439c3-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="439c3-116">-AllocationWeight</span></span>
<span data-ttu-id="439c3-117">Peso de alocação do Hub IoT</span><span class="sxs-lookup"><span data-stu-id="439c3-117">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439c3-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="439c3-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="439c3-119">Um booliano que indica se a política de alocação deve ser aplicada ao Hub IoT</span><span class="sxs-lookup"><span data-stu-id="439c3-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="439c3-120">-DefaultProfile</span></span>
<span data-ttu-id="439c3-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="439c3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="439c3-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="439c3-122">-DpsObject</span></span>
<span data-ttu-id="439c3-123">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="439c3-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="439c3-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="439c3-124">-IotHubConnectionString</span></span>
<span data-ttu-id="439c3-125">Cadeia de conexão do recurso de Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="439c3-125">Connection String of the Iot Hub resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439c3-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="439c3-126">-IotHubLocation</span></span>
<span data-ttu-id="439c3-127">Localização do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="439c3-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439c3-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="439c3-128">-Name</span></span>
<span data-ttu-id="439c3-129">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="439c3-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="439c3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="439c3-130">-ResourceGroupName</span></span>
<span data-ttu-id="439c3-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="439c3-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="439c3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="439c3-132">-ResourceId</span></span>
<span data-ttu-id="439c3-133">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="439c3-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="439c3-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="439c3-134">-Confirm</span></span>
<span data-ttu-id="439c3-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="439c3-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439c3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="439c3-136">-WhatIf</span></span>
<span data-ttu-id="439c3-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="439c3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="439c3-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="439c3-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439c3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439c3-139">CommonParameters</span></span>
<span data-ttu-id="439c3-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="439c3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439c3-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="439c3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439c3-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="439c3-142">INPUTS</span></span>

### <span data-ttu-id="439c3-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="439c3-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="439c3-144">Parâmetros: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="439c3-144">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="439c3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="439c3-145">System.String</span></span>

## <span data-ttu-id="439c3-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="439c3-146">OUTPUTS</span></span>

### <span data-ttu-id="439c3-147">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="439c3-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="439c3-148">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="439c3-148">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="439c3-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="439c3-149">NOTES</span></span>

## <span data-ttu-id="439c3-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="439c3-150">RELATED LINKS</span></span>
