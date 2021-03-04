---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 8b5a42110c99a4572b411d082879f4f2853bac0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889330"
---
# <span data-ttu-id="1de9c-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="1de9c-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="1de9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1de9c-102">SYNOPSIS</span></span>
<span data-ttu-id="1de9c-103">Hub IoT vinculado a um serviço de provisionamento de dispositivo do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="1de9c-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="1de9c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1de9c-104">SYNTAX</span></span>

### <span data-ttu-id="1de9c-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1de9c-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1de9c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1de9c-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1de9c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1de9c-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1de9c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1de9c-108">DESCRIPTION</span></span>
<span data-ttu-id="1de9c-109">Para uma introdução ao Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="1de9c-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="1de9c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1de9c-110">EXAMPLES</span></span>

### <span data-ttu-id="1de9c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1de9c-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="1de9c-112">Hub IoT vinculado a um serviço de provisionamento de dispositivo do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="1de9c-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="1de9c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1de9c-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="1de9c-114">Hub IoT vinculado a um serviço de provisionamento de dispositivo do Azure IoT Hub com AllocationWeight e ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="1de9c-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="1de9c-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1de9c-115">PARAMETERS</span></span>

### <span data-ttu-id="1de9c-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="1de9c-116">-AllocationWeight</span></span>
<span data-ttu-id="1de9c-117">Peso da alocação do Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="1de9c-117">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="1de9c-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="1de9c-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="1de9c-119">Um booleano indicando se a política de alocação deve ser aplicada ao Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="1de9c-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="1de9c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de9c-120">-DefaultProfile</span></span>
<span data-ttu-id="1de9c-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1de9c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1de9c-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="1de9c-122">-DpsObject</span></span>
<span data-ttu-id="1de9c-123">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="1de9c-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="1de9c-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="1de9c-124">-IotHubConnectionString</span></span>
<span data-ttu-id="1de9c-125">Cadeia de conexão do recurso hub de Iot.</span><span class="sxs-lookup"><span data-stu-id="1de9c-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="1de9c-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="1de9c-126">-IotHubLocation</span></span>
<span data-ttu-id="1de9c-127">Local do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="1de9c-127">Location of the Iot Hub</span></span>

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

### <span data-ttu-id="1de9c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1de9c-128">-Name</span></span>
<span data-ttu-id="1de9c-129">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="1de9c-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1de9c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1de9c-130">-ResourceGroupName</span></span>
<span data-ttu-id="1de9c-131">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1de9c-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1de9c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1de9c-132">-ResourceId</span></span>
<span data-ttu-id="1de9c-133">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="1de9c-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1de9c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1de9c-134">-Confirm</span></span>
<span data-ttu-id="1de9c-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1de9c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1de9c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1de9c-136">-WhatIf</span></span>
<span data-ttu-id="1de9c-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1de9c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1de9c-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1de9c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1de9c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de9c-139">CommonParameters</span></span>
<span data-ttu-id="1de9c-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1de9c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de9c-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1de9c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de9c-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1de9c-142">INPUTS</span></span>

### <span data-ttu-id="1de9c-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1de9c-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="1de9c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="1de9c-144">System.String</span></span>

## <span data-ttu-id="1de9c-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1de9c-145">OUTPUTS</span></span>

### <span data-ttu-id="1de9c-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="1de9c-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="1de9c-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="1de9c-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="1de9c-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="1de9c-148">NOTES</span></span>

## <span data-ttu-id="1de9c-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1de9c-149">RELATED LINKS</span></span>
