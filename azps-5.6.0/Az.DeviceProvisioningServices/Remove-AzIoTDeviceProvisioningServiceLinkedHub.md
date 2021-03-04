---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: fc1b8bbe14fb35e7613ac1ed09ecf87624920081
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889542"
---
# <span data-ttu-id="5113f-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="5113f-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="5113f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5113f-102">SYNOPSIS</span></span>
<span data-ttu-id="5113f-103">Exclua um hub de IoT vinculado em um serviço de provisionamento de dispositivo do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="5113f-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5113f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5113f-104">SYNTAX</span></span>

### <span data-ttu-id="5113f-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5113f-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5113f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5113f-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5113f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5113f-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5113f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5113f-108">DESCRIPTION</span></span>
<span data-ttu-id="5113f-109">Para uma introdução ao Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5113f-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5113f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5113f-110">EXAMPLES</span></span>

### <span data-ttu-id="5113f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5113f-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="5113f-112">Exclua o hub de IoT vinculado "myiothub" em um serviço de provisionamento de dispositivoS do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="5113f-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="5113f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5113f-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="5113f-114">Exclua o hub de IoT vinculado "myiothub" em um serviço de provisionamento de dispositivo do Azure IoT Hub usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="5113f-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="5113f-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5113f-115">PARAMETERS</span></span>

### <span data-ttu-id="5113f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5113f-116">-DefaultProfile</span></span>
<span data-ttu-id="5113f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5113f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5113f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5113f-118">-InputObject</span></span>
<span data-ttu-id="5113f-119">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5113f-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5113f-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="5113f-120">-LinkedHubName</span></span>
<span data-ttu-id="5113f-121">Nome do host do Hub IoT vinculado</span><span class="sxs-lookup"><span data-stu-id="5113f-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="5113f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5113f-122">-Name</span></span>
<span data-ttu-id="5113f-123">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="5113f-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5113f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5113f-124">-PassThru</span></span>
<span data-ttu-id="5113f-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5113f-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5113f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5113f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5113f-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5113f-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5113f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5113f-128">-ResourceId</span></span>
<span data-ttu-id="5113f-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="5113f-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5113f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5113f-130">-Confirm</span></span>
<span data-ttu-id="5113f-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5113f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5113f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5113f-132">-WhatIf</span></span>
<span data-ttu-id="5113f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5113f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5113f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5113f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5113f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5113f-135">CommonParameters</span></span>
<span data-ttu-id="5113f-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5113f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5113f-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5113f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5113f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5113f-138">INPUTS</span></span>

### <span data-ttu-id="5113f-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="5113f-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="5113f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5113f-140">System.String</span></span>

## <span data-ttu-id="5113f-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5113f-141">OUTPUTS</span></span>

### <span data-ttu-id="5113f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5113f-142">System.Boolean</span></span>

## <span data-ttu-id="5113f-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="5113f-143">NOTES</span></span>

## <span data-ttu-id="5113f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5113f-144">RELATED LINKS</span></span>
