---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: ecc91bb19b3d5d40f8c5aa3e4f25812a9999e45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429547"
---
# <span data-ttu-id="ac800-101">Remove-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="ac800-101">Remove-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="ac800-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac800-102">SYNOPSIS</span></span>
<span data-ttu-id="ac800-103">Excluir um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="ac800-103">Delete an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac800-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac800-104">SYNTAX</span></span>

### <span data-ttu-id="ac800-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ac800-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac800-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ac800-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac800-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="ac800-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac800-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac800-108">DESCRIPTION</span></span>
<span data-ttu-id="ac800-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="ac800-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="ac800-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac800-110">EXAMPLES</span></span>

### <span data-ttu-id="ac800-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ac800-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="ac800-112">Excluir um serviço de provisionamento de dispositivo Hub IoT do Azure ' myiotdps '.</span><span class="sxs-lookup"><span data-stu-id="ac800-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="ac800-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ac800-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzureRmIotDps
```

<span data-ttu-id="ac800-114">Excluir um serviço de provisionamento de dispositivo Hub IoT do Azure ' myiotdps ' usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="ac800-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="ac800-115">OS</span><span class="sxs-lookup"><span data-stu-id="ac800-115">PARAMETERS</span></span>

### <span data-ttu-id="ac800-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac800-116">-DefaultProfile</span></span>
<span data-ttu-id="ac800-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac800-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac800-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac800-118">-InputObject</span></span>
<span data-ttu-id="ac800-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="ac800-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ac800-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac800-120">-Name</span></span>
<span data-ttu-id="ac800-121">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="ac800-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ac800-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac800-122">-PassThru</span></span>
<span data-ttu-id="ac800-123">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="ac800-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ac800-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac800-124">-ResourceGroupName</span></span>
<span data-ttu-id="ac800-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ac800-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ac800-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac800-126">-ResourceId</span></span>
<span data-ttu-id="ac800-127">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="ac800-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ac800-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ac800-128">-Confirm</span></span>
<span data-ttu-id="ac800-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac800-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac800-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac800-130">-WhatIf</span></span>
<span data-ttu-id="ac800-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ac800-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac800-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac800-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac800-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac800-133">CommonParameters</span></span>
<span data-ttu-id="ac800-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac800-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac800-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac800-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac800-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac800-136">INPUTS</span></span>

### <span data-ttu-id="ac800-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ac800-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="ac800-138">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ac800-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ac800-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ac800-139">System.String</span></span>

## <span data-ttu-id="ac800-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac800-140">OUTPUTS</span></span>

### <span data-ttu-id="ac800-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac800-141">System.Boolean</span></span>

## <span data-ttu-id="ac800-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac800-142">NOTES</span></span>

## <span data-ttu-id="ac800-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac800-143">RELATED LINKS</span></span>
