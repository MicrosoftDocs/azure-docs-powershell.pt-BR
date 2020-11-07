---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941910"
---
# <span data-ttu-id="80246-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="80246-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="80246-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80246-102">SYNOPSIS</span></span>
<span data-ttu-id="80246-103">Excluir um hub IoT vinculado em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="80246-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="80246-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80246-104">SYNTAX</span></span>

### <span data-ttu-id="80246-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="80246-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80246-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="80246-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80246-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="80246-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80246-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80246-108">DESCRIPTION</span></span>
<span data-ttu-id="80246-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="80246-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="80246-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80246-110">EXAMPLES</span></span>

### <span data-ttu-id="80246-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="80246-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="80246-112">Excluir o Hub IoT vinculado "myiothub" em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="80246-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="80246-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="80246-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="80246-114">Exclua o Hub IoT vinculado "myiothub" em um serviço de provisionamento de dispositivo Hub do Azure IoT usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="80246-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="80246-115">OS</span><span class="sxs-lookup"><span data-stu-id="80246-115">PARAMETERS</span></span>

### <span data-ttu-id="80246-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80246-116">-DefaultProfile</span></span>
<span data-ttu-id="80246-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80246-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80246-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80246-118">-InputObject</span></span>
<span data-ttu-id="80246-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="80246-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="80246-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="80246-120">-LinkedHubName</span></span>
<span data-ttu-id="80246-121">Nome do host do Hub IoT vinculado</span><span class="sxs-lookup"><span data-stu-id="80246-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="80246-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="80246-122">-Name</span></span>
<span data-ttu-id="80246-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="80246-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="80246-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80246-124">-PassThru</span></span>
<span data-ttu-id="80246-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="80246-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="80246-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80246-126">-ResourceGroupName</span></span>
<span data-ttu-id="80246-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="80246-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="80246-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80246-128">-ResourceId</span></span>
<span data-ttu-id="80246-129">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="80246-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="80246-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="80246-130">-Confirm</span></span>
<span data-ttu-id="80246-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80246-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80246-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80246-132">-WhatIf</span></span>
<span data-ttu-id="80246-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80246-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80246-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80246-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80246-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80246-135">CommonParameters</span></span>
<span data-ttu-id="80246-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80246-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80246-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80246-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80246-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80246-138">INPUTS</span></span>

### <span data-ttu-id="80246-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="80246-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="80246-140">System. String</span><span class="sxs-lookup"><span data-stu-id="80246-140">System.String</span></span>

## <span data-ttu-id="80246-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80246-141">OUTPUTS</span></span>

### <span data-ttu-id="80246-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80246-142">System.Boolean</span></span>

## <span data-ttu-id="80246-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80246-143">NOTES</span></span>

## <span data-ttu-id="80246-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80246-144">RELATED LINKS</span></span>
