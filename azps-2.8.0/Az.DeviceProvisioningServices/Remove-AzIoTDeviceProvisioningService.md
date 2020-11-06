---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: a2700c1872e53234d97e82c41a93ef6e9e328391
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596580"
---
# <span data-ttu-id="4cdc2-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="4cdc2-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="4cdc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cdc2-102">SYNOPSIS</span></span>
<span data-ttu-id="4cdc2-103">Excluir um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="4cdc2-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="4cdc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cdc2-104">SYNTAX</span></span>

### <span data-ttu-id="4cdc2-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4cdc2-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cdc2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4cdc2-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cdc2-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="4cdc2-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cdc2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4cdc2-108">DESCRIPTION</span></span>
<span data-ttu-id="4cdc2-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="4cdc2-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="4cdc2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cdc2-110">EXAMPLES</span></span>

### <span data-ttu-id="4cdc2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4cdc2-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="4cdc2-112">Excluir um serviço de provisionamento de dispositivo Hub IoT do Azure ' myiotdps '.</span><span class="sxs-lookup"><span data-stu-id="4cdc2-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="4cdc2-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4cdc2-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="4cdc2-114">Excluir um serviço de provisionamento de dispositivo Hub IoT do Azure ' myiotdps ' usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="4cdc2-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="4cdc2-115">OS</span><span class="sxs-lookup"><span data-stu-id="4cdc2-115">PARAMETERS</span></span>

### <span data-ttu-id="4cdc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cdc2-116">-DefaultProfile</span></span>
<span data-ttu-id="4cdc2-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4cdc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cdc2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cdc2-118">-InputObject</span></span>
<span data-ttu-id="4cdc2-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="4cdc2-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4cdc2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cdc2-120">-Name</span></span>
<span data-ttu-id="4cdc2-121">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="4cdc2-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4cdc2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cdc2-122">-PassThru</span></span>
<span data-ttu-id="4cdc2-123">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="4cdc2-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4cdc2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cdc2-124">-ResourceGroupName</span></span>
<span data-ttu-id="4cdc2-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4cdc2-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4cdc2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cdc2-126">-ResourceId</span></span>
<span data-ttu-id="4cdc2-127">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="4cdc2-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4cdc2-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4cdc2-128">-Confirm</span></span>
<span data-ttu-id="4cdc2-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cdc2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cdc2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cdc2-130">-WhatIf</span></span>
<span data-ttu-id="4cdc2-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4cdc2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cdc2-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4cdc2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cdc2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cdc2-133">CommonParameters</span></span>
<span data-ttu-id="4cdc2-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cdc2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cdc2-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cdc2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cdc2-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4cdc2-136">INPUTS</span></span>

### <span data-ttu-id="4cdc2-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4cdc2-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4cdc2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4cdc2-138">System.String</span></span>

## <span data-ttu-id="4cdc2-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4cdc2-139">OUTPUTS</span></span>

### <span data-ttu-id="4cdc2-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4cdc2-140">System.Boolean</span></span>

## <span data-ttu-id="4cdc2-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4cdc2-141">NOTES</span></span>

## <span data-ttu-id="4cdc2-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cdc2-142">RELATED LINKS</span></span>
