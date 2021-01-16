---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 482acd4f82320bbc14c5bf95c113304a8720019b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259532"
---
# <span data-ttu-id="cab97-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="cab97-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="cab97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cab97-102">SYNOPSIS</span></span>
<span data-ttu-id="cab97-103">Criar um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="cab97-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="cab97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cab97-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cab97-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cab97-105">DESCRIPTION</span></span>
<span data-ttu-id="cab97-106">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="cab97-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="cab97-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cab97-107">EXAMPLES</span></span>

### <span data-ttu-id="cab97-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cab97-108">Example 1</span></span>
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

<span data-ttu-id="cab97-109">Crie um serviço de provisionamento de dispositivo Hub IoT do Azure com o tipo de preço padrão S1 e Tags na região do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cab97-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="cab97-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cab97-110">Example 2</span></span>
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

<span data-ttu-id="cab97-111">Crie um serviço de provisionamento de dispositivo Hub IoT do Azure com o tipo de preço padrão S1 na região ' eastus '.</span><span class="sxs-lookup"><span data-stu-id="cab97-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="cab97-112">OS</span><span class="sxs-lookup"><span data-stu-id="cab97-112">PARAMETERS</span></span>

### <span data-ttu-id="cab97-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="cab97-113">-AllocationPolicy</span></span>
<span data-ttu-id="cab97-114">Política de alocação do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="cab97-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="cab97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab97-115">-DefaultProfile</span></span>
<span data-ttu-id="cab97-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cab97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cab97-117">-Local</span><span class="sxs-lookup"><span data-stu-id="cab97-117">-Location</span></span>
<span data-ttu-id="cab97-118">Ponto</span><span class="sxs-lookup"><span data-stu-id="cab97-118">Location</span></span>

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

### <span data-ttu-id="cab97-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cab97-119">-Name</span></span>
<span data-ttu-id="cab97-120">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="cab97-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="cab97-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cab97-121">-ResourceGroupName</span></span>
<span data-ttu-id="cab97-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cab97-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cab97-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cab97-123">-SkuName</span></span>
<span data-ttu-id="cab97-124">SKU</span><span class="sxs-lookup"><span data-stu-id="cab97-124">Sku</span></span>

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

### <span data-ttu-id="cab97-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="cab97-125">-Tag</span></span>
<span data-ttu-id="cab97-126">Marcas de instância do serviço de provisionamento de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="cab97-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="cab97-127">Recipiente de propriedades em pares de chave-valor na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cab97-127">Property bag in key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="cab97-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cab97-128">-Confirm</span></span>
<span data-ttu-id="cab97-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cab97-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cab97-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cab97-130">-WhatIf</span></span>
<span data-ttu-id="cab97-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cab97-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cab97-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cab97-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cab97-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab97-133">CommonParameters</span></span>
<span data-ttu-id="cab97-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab97-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab97-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab97-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab97-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cab97-136">INPUTS</span></span>

### <span data-ttu-id="cab97-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cab97-137">None</span></span>

## <span data-ttu-id="cab97-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cab97-138">OUTPUTS</span></span>

### <span data-ttu-id="cab97-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="cab97-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="cab97-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cab97-140">NOTES</span></span>

## <span data-ttu-id="cab97-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cab97-141">RELATED LINKS</span></span>
