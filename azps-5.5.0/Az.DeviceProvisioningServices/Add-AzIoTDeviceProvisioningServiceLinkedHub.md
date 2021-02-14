---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 30bcf61f309a400270e9cca378fce6d1149cf66a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116825"
---
# <span data-ttu-id="5e1ae-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="5e1ae-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="5e1ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1ae-103">Hub de IoT vinculado a um serviço de provisionamento de dispositivos do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5e1ae-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e1ae-104">SYNTAX</span></span>

### <span data-ttu-id="5e1ae-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5e1ae-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e1ae-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5e1ae-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e1ae-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5e1ae-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e1ae-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e1ae-108">DESCRIPTION</span></span>
<span data-ttu-id="5e1ae-109">Para uma introdução ao Serviço de Provisionamento de Dispositivo do Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5e1ae-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5e1ae-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5e1ae-110">EXAMPLES</span></span>

### <span data-ttu-id="5e1ae-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5e1ae-111">Example 1</span></span>
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

<span data-ttu-id="5e1ae-112">Hub de IoT vinculado a um serviço de provisionamento de dispositivos do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="5e1ae-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5e1ae-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="5e1ae-114">Hub de IoT vinculado a um serviço de provisionamento de dispositivos do Hub IoT do Azure com AllocationWeight e ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="5e1ae-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e1ae-115">PARAMETERS</span></span>

### <span data-ttu-id="5e1ae-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="5e1ae-116">-AllocationWeight</span></span>
<span data-ttu-id="5e1ae-117">Peso da alocação do Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="5e1ae-117">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="5e1ae-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="5e1ae-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="5e1ae-119">Um boolano indicando se você deve aplicar a política de alocação ao Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="5e1ae-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="5e1ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1ae-120">-DefaultProfile</span></span>
<span data-ttu-id="5e1ae-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e1ae-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5e1ae-122">-DpsObject</span></span>
<span data-ttu-id="5e1ae-123">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5e1ae-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5e1ae-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="5e1ae-124">-IotHubConnectionString</span></span>
<span data-ttu-id="5e1ae-125">Cadeia de conexão do recurso Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="5e1ae-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="5e1ae-126">-IotHubLocation</span></span>
<span data-ttu-id="5e1ae-127">Local do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="5e1ae-127">Location of the Iot Hub</span></span>

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

### <span data-ttu-id="5e1ae-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e1ae-128">-Name</span></span>
<span data-ttu-id="5e1ae-129">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5e1ae-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5e1ae-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e1ae-130">-ResourceGroupName</span></span>
<span data-ttu-id="5e1ae-131">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5e1ae-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5e1ae-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e1ae-132">-ResourceId</span></span>
<span data-ttu-id="5e1ae-133">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="5e1ae-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5e1ae-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5e1ae-134">-Confirm</span></span>
<span data-ttu-id="5e1ae-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e1ae-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e1ae-136">-WhatIf</span></span>
<span data-ttu-id="5e1ae-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e1ae-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e1ae-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1ae-139">CommonParameters</span></span>
<span data-ttu-id="5e1ae-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e1ae-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1ae-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e1ae-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1ae-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="5e1ae-142">INPUTS</span></span>

### <span data-ttu-id="5e1ae-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5e1ae-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5e1ae-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5e1ae-144">System.String</span></span>

## <span data-ttu-id="5e1ae-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="5e1ae-145">OUTPUTS</span></span>

### <span data-ttu-id="5e1ae-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="5e1ae-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="5e1ae-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="5e1ae-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="5e1ae-148">Notas</span><span class="sxs-lookup"><span data-stu-id="5e1ae-148">NOTES</span></span>

## <span data-ttu-id="5e1ae-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e1ae-149">RELATED LINKS</span></span>
