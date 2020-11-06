---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: d941e59c3d0681b91cdef9d05617c665dcc83177
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596566"
---
# <span data-ttu-id="5a3ff-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="5a3ff-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="5a3ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a3ff-102">SYNOPSIS</span></span>
<span data-ttu-id="5a3ff-103">Atualizar um hub IoT vinculado em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="5a3ff-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5a3ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a3ff-104">SYNTAX</span></span>

### <span data-ttu-id="5a3ff-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5a3ff-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a3ff-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5a3ff-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a3ff-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="5a3ff-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a3ff-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a3ff-108">DESCRIPTION</span></span>
<span data-ttu-id="5a3ff-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5a3ff-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5a3ff-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a3ff-110">EXAMPLES</span></span>

### <span data-ttu-id="5a3ff-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5a3ff-111">Example 1</span></span>
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

<span data-ttu-id="5a3ff-112">Atualize o Hub IoT vinculado "myiothub.azure-devices.net" em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="5a3ff-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5a3ff-113">OS</span><span class="sxs-lookup"><span data-stu-id="5a3ff-113">PARAMETERS</span></span>

### <span data-ttu-id="5a3ff-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="5a3ff-114">-AllocationWeight</span></span>
<span data-ttu-id="5a3ff-115">Peso de alocação do Hub IoT</span><span class="sxs-lookup"><span data-stu-id="5a3ff-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="5a3ff-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="5a3ff-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="5a3ff-117">Aplicar a política de alocação ao Hub IoT</span><span class="sxs-lookup"><span data-stu-id="5a3ff-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="5a3ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a3ff-118">-DefaultProfile</span></span>
<span data-ttu-id="5a3ff-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a3ff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a3ff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a3ff-120">-InputObject</span></span>
<span data-ttu-id="5a3ff-121">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5a3ff-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5a3ff-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="5a3ff-122">-LinkedHubName</span></span>
<span data-ttu-id="5a3ff-123">Nome do host do Hub IoT vinculado</span><span class="sxs-lookup"><span data-stu-id="5a3ff-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="5a3ff-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a3ff-124">-Name</span></span>
<span data-ttu-id="5a3ff-125">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5a3ff-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5a3ff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a3ff-126">-ResourceGroupName</span></span>
<span data-ttu-id="5a3ff-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5a3ff-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5a3ff-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a3ff-128">-ResourceId</span></span>
<span data-ttu-id="5a3ff-129">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5a3ff-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5a3ff-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5a3ff-130">-Confirm</span></span>
<span data-ttu-id="5a3ff-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a3ff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a3ff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a3ff-132">-WhatIf</span></span>
<span data-ttu-id="5a3ff-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a3ff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a3ff-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a3ff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a3ff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a3ff-135">CommonParameters</span></span>
<span data-ttu-id="5a3ff-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a3ff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a3ff-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a3ff-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a3ff-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a3ff-138">INPUTS</span></span>

### <span data-ttu-id="5a3ff-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="5a3ff-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="5a3ff-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5a3ff-140">System.String</span></span>

## <span data-ttu-id="5a3ff-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a3ff-141">OUTPUTS</span></span>

### <span data-ttu-id="5a3ff-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="5a3ff-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="5a3ff-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a3ff-143">NOTES</span></span>

## <span data-ttu-id="5a3ff-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a3ff-144">RELATED LINKS</span></span>
