---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: f50c0955d56b42c341b6a1a6b64b1993ee66175e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610601"
---
# <span data-ttu-id="1ad05-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="1ad05-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="1ad05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ad05-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad05-103">Excluir um hub IoT vinculado em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ad05-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ad05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ad05-104">SYNTAX</span></span>

### <span data-ttu-id="1ad05-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ad05-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ad05-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1ad05-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ad05-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="1ad05-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ad05-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ad05-108">DESCRIPTION</span></span>
<span data-ttu-id="1ad05-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="1ad05-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="1ad05-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ad05-110">EXAMPLES</span></span>

### <span data-ttu-id="1ad05-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ad05-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="1ad05-112">Excluir o Hub IoT vinculado "myiothub" em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ad05-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="1ad05-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1ad05-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzureRmIoTDpsHub
```

<span data-ttu-id="1ad05-114">Exclua o Hub IoT vinculado "myiothub" em um serviço de provisionamento de dispositivo Hub do Azure IoT usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="1ad05-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="1ad05-115">OS</span><span class="sxs-lookup"><span data-stu-id="1ad05-115">PARAMETERS</span></span>

### <span data-ttu-id="1ad05-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad05-116">-DefaultProfile</span></span>
<span data-ttu-id="1ad05-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ad05-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ad05-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ad05-118">-InputObject</span></span>
<span data-ttu-id="1ad05-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="1ad05-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="1ad05-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="1ad05-120">-LinkedHubName</span></span>
<span data-ttu-id="1ad05-121">Nome do host do Hub IoT vinculado</span><span class="sxs-lookup"><span data-stu-id="1ad05-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="1ad05-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ad05-122">-Name</span></span>
<span data-ttu-id="1ad05-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="1ad05-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1ad05-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ad05-124">-PassThru</span></span>
<span data-ttu-id="1ad05-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="1ad05-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1ad05-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ad05-126">-ResourceGroupName</span></span>
<span data-ttu-id="1ad05-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1ad05-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1ad05-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ad05-128">-ResourceId</span></span>
<span data-ttu-id="1ad05-129">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="1ad05-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1ad05-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1ad05-130">-Confirm</span></span>
<span data-ttu-id="1ad05-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ad05-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ad05-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad05-132">-WhatIf</span></span>
<span data-ttu-id="1ad05-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ad05-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ad05-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ad05-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ad05-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad05-135">CommonParameters</span></span>
<span data-ttu-id="1ad05-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ad05-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad05-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ad05-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad05-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ad05-138">INPUTS</span></span>

### <span data-ttu-id="1ad05-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="1ad05-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>
<span data-ttu-id="1ad05-140">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ad05-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1ad05-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1ad05-141">System.String</span></span>

## <span data-ttu-id="1ad05-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ad05-142">OUTPUTS</span></span>

### <span data-ttu-id="1ad05-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ad05-143">System.Boolean</span></span>

## <span data-ttu-id="1ad05-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ad05-144">NOTES</span></span>

## <span data-ttu-id="1ad05-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ad05-145">RELATED LINKS</span></span>
