---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: bb6094644b9f2cbd831aa8d64a142d5888a5bcc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893358"
---
# <span data-ttu-id="45699-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="45699-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="45699-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45699-102">SYNOPSIS</span></span>
<span data-ttu-id="45699-103">Crie um serviço de provisionamento de dispositivo do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="45699-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="45699-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="45699-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45699-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="45699-105">DESCRIPTION</span></span>
<span data-ttu-id="45699-106">Para uma introdução ao Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="45699-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="45699-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45699-107">EXAMPLES</span></span>

### <span data-ttu-id="45699-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45699-108">Example 1</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {[key1, value1]}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="45699-109">Crie um serviço de provisionamento de dispositivo do Azure IoT Hub com a faixa de preços padrão S1 e marcas, na região do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45699-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="45699-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="45699-110">Example 2</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : eastus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="45699-111">Crie um serviço de provisionamento de dispositivo do Azure IoT Hub com a camada de preços padrão S1, na região 'eastus'.</span><span class="sxs-lookup"><span data-stu-id="45699-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="45699-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="45699-112">PARAMETERS</span></span>

### <span data-ttu-id="45699-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="45699-113">-AllocationPolicy</span></span>
<span data-ttu-id="45699-114">Política de Alocação de Serviço de Provisionamento de Dispositivos IoT</span><span class="sxs-lookup"><span data-stu-id="45699-114">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45699-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45699-115">-DefaultProfile</span></span>
<span data-ttu-id="45699-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45699-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45699-117">-Location</span><span class="sxs-lookup"><span data-stu-id="45699-117">-Location</span></span>
<span data-ttu-id="45699-118">Local</span><span class="sxs-lookup"><span data-stu-id="45699-118">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45699-119">-Name</span><span class="sxs-lookup"><span data-stu-id="45699-119">-Name</span></span>
<span data-ttu-id="45699-120">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="45699-120">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45699-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45699-121">-ResourceGroupName</span></span>
<span data-ttu-id="45699-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="45699-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45699-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="45699-123">-SkuName</span></span>
<span data-ttu-id="45699-124">Sku</span><span class="sxs-lookup"><span data-stu-id="45699-124">Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45699-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="45699-125">-Tag</span></span>
<span data-ttu-id="45699-126">Marcas de instância do Serviço de Provisionamento de Dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="45699-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="45699-127">Bolsa de propriedades em pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="45699-127">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45699-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45699-128">-Confirm</span></span>
<span data-ttu-id="45699-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45699-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45699-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45699-130">-WhatIf</span></span>
<span data-ttu-id="45699-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45699-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45699-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45699-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45699-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45699-133">CommonParameters</span></span>
<span data-ttu-id="45699-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45699-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45699-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45699-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45699-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45699-136">INPUTS</span></span>

### <span data-ttu-id="45699-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="45699-137">None</span></span>

## <span data-ttu-id="45699-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="45699-138">OUTPUTS</span></span>

### <span data-ttu-id="45699-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="45699-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="45699-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="45699-140">NOTES</span></span>

## <span data-ttu-id="45699-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45699-141">RELATED LINKS</span></span>
