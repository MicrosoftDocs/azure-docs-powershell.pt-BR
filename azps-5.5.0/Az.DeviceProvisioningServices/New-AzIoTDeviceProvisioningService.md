---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 482acd4f82320bbc14c5bf95c113304a8720019b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113218"
---
# <span data-ttu-id="d0af2-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="d0af2-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="d0af2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0af2-102">SYNOPSIS</span></span>
<span data-ttu-id="d0af2-103">Crie um serviço de provisionamento de dispositivo do Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0af2-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d0af2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0af2-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0af2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0af2-105">DESCRIPTION</span></span>
<span data-ttu-id="d0af2-106">Para uma introdução ao Serviço de Provisionamento de Dispositivo do Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="d0af2-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="d0af2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d0af2-107">EXAMPLES</span></span>

### <span data-ttu-id="d0af2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0af2-108">Example 1</span></span>
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

<span data-ttu-id="d0af2-109">Crie um serviço de provisionamento de dispositivo do Hub IoT do Azure com o nível de preços padrão S1 e marcas, na região do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0af2-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="d0af2-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d0af2-110">Example 2</span></span>
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

<span data-ttu-id="d0af2-111">Crie um serviço de provisionamento de dispositivos do Hub do Azure IoT com o nível de preços padrão S1, na região "eastus".</span><span class="sxs-lookup"><span data-stu-id="d0af2-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="d0af2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0af2-112">PARAMETERS</span></span>

### <span data-ttu-id="d0af2-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="d0af2-113">-AllocationPolicy</span></span>
<span data-ttu-id="d0af2-114">Política de Alocação de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="d0af2-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="d0af2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0af2-115">-DefaultProfile</span></span>
<span data-ttu-id="d0af2-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0af2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0af2-117">-Local</span><span class="sxs-lookup"><span data-stu-id="d0af2-117">-Location</span></span>
<span data-ttu-id="d0af2-118">Localização</span><span class="sxs-lookup"><span data-stu-id="d0af2-118">Location</span></span>

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

### <span data-ttu-id="d0af2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0af2-119">-Name</span></span>
<span data-ttu-id="d0af2-120">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="d0af2-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d0af2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0af2-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0af2-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d0af2-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d0af2-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d0af2-123">-SkuName</span></span>
<span data-ttu-id="d0af2-124">Sku</span><span class="sxs-lookup"><span data-stu-id="d0af2-124">Sku</span></span>

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

### <span data-ttu-id="d0af2-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="d0af2-125">-Tag</span></span>
<span data-ttu-id="d0af2-126">Marcas de instância do Serviço de Provisionamento de Dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="d0af2-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="d0af2-127">Bolsa de propriedades em pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="d0af2-127">Property bag in key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="d0af2-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d0af2-128">-Confirm</span></span>
<span data-ttu-id="d0af2-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0af2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0af2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0af2-130">-WhatIf</span></span>
<span data-ttu-id="d0af2-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d0af2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0af2-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d0af2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0af2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0af2-133">CommonParameters</span></span>
<span data-ttu-id="d0af2-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0af2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0af2-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0af2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0af2-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="d0af2-136">INPUTS</span></span>

### <span data-ttu-id="d0af2-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d0af2-137">None</span></span>

## <span data-ttu-id="d0af2-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="d0af2-138">OUTPUTS</span></span>

### <span data-ttu-id="d0af2-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d0af2-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="d0af2-140">Notas</span><span class="sxs-lookup"><span data-stu-id="d0af2-140">NOTES</span></span>

## <span data-ttu-id="d0af2-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0af2-141">RELATED LINKS</span></span>
