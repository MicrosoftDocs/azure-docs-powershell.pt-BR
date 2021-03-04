---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 4065e44d9ec0ed2512438356231176a1de10e7aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889530"
---
# <span data-ttu-id="a3862-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="a3862-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="a3862-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3862-102">SYNOPSIS</span></span>
<span data-ttu-id="a3862-103">Atualize um hub de IoT vinculado em um serviço de provisionamento de dispositivo do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="a3862-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="a3862-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a3862-104">SYNTAX</span></span>

### <span data-ttu-id="a3862-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a3862-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3862-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a3862-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3862-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a3862-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3862-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a3862-108">DESCRIPTION</span></span>
<span data-ttu-id="a3862-109">Para uma introdução ao Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="a3862-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="a3862-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3862-110">EXAMPLES</span></span>

### <span data-ttu-id="a3862-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3862-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="a3862-112">Atualize o hub de IoT vinculado "myiothub.azure-devices.net" em um serviço de provisionamento de dispositivoS do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="a3862-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="a3862-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a3862-113">PARAMETERS</span></span>

### <span data-ttu-id="a3862-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="a3862-114">-AllocationWeight</span></span>
<span data-ttu-id="a3862-115">Peso da alocação do Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="a3862-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="a3862-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="a3862-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="a3862-117">Aplicar política de alocação ao Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="a3862-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="a3862-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3862-118">-DefaultProfile</span></span>
<span data-ttu-id="a3862-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3862-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3862-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3862-120">-InputObject</span></span>
<span data-ttu-id="a3862-121">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="a3862-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3862-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="a3862-122">-LinkedHubName</span></span>
<span data-ttu-id="a3862-123">Nome do host do Hub IoT vinculado</span><span class="sxs-lookup"><span data-stu-id="a3862-123">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3862-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a3862-124">-Name</span></span>
<span data-ttu-id="a3862-125">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="a3862-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a3862-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3862-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3862-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="a3862-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a3862-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3862-128">-ResourceId</span></span>
<span data-ttu-id="a3862-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="a3862-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a3862-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3862-130">-Confirm</span></span>
<span data-ttu-id="a3862-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3862-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3862-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3862-132">-WhatIf</span></span>
<span data-ttu-id="a3862-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3862-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3862-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3862-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3862-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3862-135">CommonParameters</span></span>
<span data-ttu-id="a3862-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3862-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3862-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3862-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3862-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3862-138">INPUTS</span></span>

### <span data-ttu-id="a3862-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="a3862-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="a3862-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a3862-140">System.String</span></span>

## <span data-ttu-id="a3862-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a3862-141">OUTPUTS</span></span>

### <span data-ttu-id="a3862-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="a3862-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="a3862-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="a3862-143">NOTES</span></span>

## <span data-ttu-id="a3862-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3862-144">RELATED LINKS</span></span>
