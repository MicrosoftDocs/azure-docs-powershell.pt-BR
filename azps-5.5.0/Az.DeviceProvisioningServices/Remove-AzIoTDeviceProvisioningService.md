---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 4701070ae7810b86ff7567f73b39606909d7fa10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126999"
---
# <span data-ttu-id="0bb47-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="0bb47-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="0bb47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0bb47-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb47-103">Exclua um serviço de provisionamento de dispositivo do Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb47-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0bb47-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bb47-104">SYNTAX</span></span>

### <span data-ttu-id="0bb47-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0bb47-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bb47-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0bb47-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bb47-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0bb47-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bb47-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bb47-108">DESCRIPTION</span></span>
<span data-ttu-id="0bb47-109">Para uma introdução ao Serviço de Provisionamento de Dispositivo do Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0bb47-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0bb47-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0bb47-110">EXAMPLES</span></span>

### <span data-ttu-id="0bb47-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0bb47-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="0bb47-112">Exclua um serviço de provisionamento de dispositivos do Hub IoT do Azure 'myiotdps'.</span><span class="sxs-lookup"><span data-stu-id="0bb47-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="0bb47-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0bb47-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="0bb47-114">Exclua um serviço de provisionamento de dispositivos do Hub do Azure IoT "myiotdps" usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="0bb47-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="0bb47-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bb47-115">PARAMETERS</span></span>

### <span data-ttu-id="0bb47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb47-116">-DefaultProfile</span></span>
<span data-ttu-id="0bb47-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb47-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bb47-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bb47-118">-InputObject</span></span>
<span data-ttu-id="0bb47-119">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="0bb47-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0bb47-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bb47-120">-Name</span></span>
<span data-ttu-id="0bb47-121">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="0bb47-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0bb47-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bb47-122">-PassThru</span></span>
<span data-ttu-id="0bb47-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0bb47-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0bb47-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bb47-124">-ResourceGroupName</span></span>
<span data-ttu-id="0bb47-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="0bb47-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0bb47-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bb47-126">-ResourceId</span></span>
<span data-ttu-id="0bb47-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="0bb47-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0bb47-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0bb47-128">-Confirm</span></span>
<span data-ttu-id="0bb47-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bb47-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bb47-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bb47-130">-WhatIf</span></span>
<span data-ttu-id="0bb47-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0bb47-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bb47-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0bb47-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bb47-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb47-133">CommonParameters</span></span>
<span data-ttu-id="0bb47-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb47-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb47-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bb47-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb47-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="0bb47-136">INPUTS</span></span>

### <span data-ttu-id="0bb47-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0bb47-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="0bb47-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0bb47-138">System.String</span></span>

## <span data-ttu-id="0bb47-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="0bb47-139">OUTPUTS</span></span>

### <span data-ttu-id="0bb47-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0bb47-140">System.Boolean</span></span>

## <span data-ttu-id="0bb47-141">Notas</span><span class="sxs-lookup"><span data-stu-id="0bb47-141">NOTES</span></span>

## <span data-ttu-id="0bb47-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bb47-142">RELATED LINKS</span></span>
