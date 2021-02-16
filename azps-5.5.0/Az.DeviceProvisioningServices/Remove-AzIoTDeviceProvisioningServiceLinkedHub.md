---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117678"
---
# <span data-ttu-id="18204-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="18204-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="18204-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18204-102">SYNOPSIS</span></span>
<span data-ttu-id="18204-103">Exclua um hub de IoT vinculado em um serviço de provisionamento de dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="18204-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="18204-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18204-104">SYNTAX</span></span>

### <span data-ttu-id="18204-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="18204-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18204-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="18204-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18204-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="18204-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18204-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="18204-108">DESCRIPTION</span></span>
<span data-ttu-id="18204-109">Para uma introdução ao Serviço de Provisionamento de Dispositivo do Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="18204-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="18204-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="18204-110">EXAMPLES</span></span>

### <span data-ttu-id="18204-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18204-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="18204-112">Exclua o hub de IoT vinculado "myiothub" em um serviço de provisionamento de dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="18204-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="18204-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="18204-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="18204-114">Exclua o hub de IoT vinculado "myiothub" em um serviço de provisionamento de dispositivo do Hub do Azure IoT usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="18204-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="18204-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18204-115">PARAMETERS</span></span>

### <span data-ttu-id="18204-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18204-116">-DefaultProfile</span></span>
<span data-ttu-id="18204-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18204-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18204-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18204-118">-InputObject</span></span>
<span data-ttu-id="18204-119">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="18204-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="18204-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="18204-120">-LinkedHubName</span></span>
<span data-ttu-id="18204-121">Nome do host do Hub de IoT vinculado</span><span class="sxs-lookup"><span data-stu-id="18204-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="18204-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="18204-122">-Name</span></span>
<span data-ttu-id="18204-123">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="18204-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="18204-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18204-124">-PassThru</span></span>
<span data-ttu-id="18204-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="18204-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="18204-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18204-126">-ResourceGroupName</span></span>
<span data-ttu-id="18204-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="18204-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="18204-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18204-128">-ResourceId</span></span>
<span data-ttu-id="18204-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="18204-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="18204-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="18204-130">-Confirm</span></span>
<span data-ttu-id="18204-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18204-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18204-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18204-132">-WhatIf</span></span>
<span data-ttu-id="18204-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="18204-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18204-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18204-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18204-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18204-135">CommonParameters</span></span>
<span data-ttu-id="18204-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18204-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18204-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18204-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18204-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="18204-138">INPUTS</span></span>

### <span data-ttu-id="18204-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="18204-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="18204-140">System.String</span><span class="sxs-lookup"><span data-stu-id="18204-140">System.String</span></span>

## <span data-ttu-id="18204-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="18204-141">OUTPUTS</span></span>

### <span data-ttu-id="18204-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="18204-142">System.Boolean</span></span>

## <span data-ttu-id="18204-143">Notas</span><span class="sxs-lookup"><span data-stu-id="18204-143">NOTES</span></span>

## <span data-ttu-id="18204-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18204-144">RELATED LINKS</span></span>
