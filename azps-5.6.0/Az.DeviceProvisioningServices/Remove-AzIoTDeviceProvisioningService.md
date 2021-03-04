---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 99df3feae227aff03d49bfd029f34be4bc32d250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887775"
---
# <span data-ttu-id="2fa81-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="2fa81-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="2fa81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fa81-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa81-103">Exclua um serviço de provisionamento de dispositivo do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="2fa81-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="2fa81-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2fa81-104">SYNTAX</span></span>

### <span data-ttu-id="2fa81-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2fa81-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fa81-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2fa81-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fa81-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2fa81-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fa81-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2fa81-108">DESCRIPTION</span></span>
<span data-ttu-id="2fa81-109">Para uma introdução ao Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="2fa81-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="2fa81-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2fa81-110">EXAMPLES</span></span>

### <span data-ttu-id="2fa81-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2fa81-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="2fa81-112">Exclua um serviço de provisionamento de dispositivo do Azure IoT Hub 'myiotdps'.</span><span class="sxs-lookup"><span data-stu-id="2fa81-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="2fa81-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2fa81-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="2fa81-114">Exclua um serviço de provisionamento de dispositivo do Azure IoT Hub 'myiotdps' usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="2fa81-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="2fa81-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2fa81-115">PARAMETERS</span></span>

### <span data-ttu-id="2fa81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa81-116">-DefaultProfile</span></span>
<span data-ttu-id="2fa81-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa81-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fa81-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fa81-118">-InputObject</span></span>
<span data-ttu-id="2fa81-119">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="2fa81-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2fa81-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2fa81-120">-Name</span></span>
<span data-ttu-id="2fa81-121">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="2fa81-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2fa81-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fa81-122">-PassThru</span></span>
<span data-ttu-id="2fa81-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2fa81-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2fa81-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fa81-124">-ResourceGroupName</span></span>
<span data-ttu-id="2fa81-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2fa81-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2fa81-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fa81-126">-ResourceId</span></span>
<span data-ttu-id="2fa81-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="2fa81-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2fa81-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fa81-128">-Confirm</span></span>
<span data-ttu-id="2fa81-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fa81-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fa81-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa81-130">-WhatIf</span></span>
<span data-ttu-id="2fa81-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2fa81-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fa81-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2fa81-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fa81-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa81-133">CommonParameters</span></span>
<span data-ttu-id="2fa81-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fa81-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa81-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa81-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa81-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2fa81-136">INPUTS</span></span>

### <span data-ttu-id="2fa81-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2fa81-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2fa81-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2fa81-138">System.String</span></span>

## <span data-ttu-id="2fa81-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2fa81-139">OUTPUTS</span></span>

### <span data-ttu-id="2fa81-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2fa81-140">System.Boolean</span></span>

## <span data-ttu-id="2fa81-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="2fa81-141">NOTES</span></span>

## <span data-ttu-id="2fa81-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2fa81-142">RELATED LINKS</span></span>
