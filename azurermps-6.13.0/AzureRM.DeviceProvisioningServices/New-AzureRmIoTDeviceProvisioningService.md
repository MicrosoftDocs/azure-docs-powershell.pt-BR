---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: 9665b0ae486c12aec350db572aee6fc4f718ed43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429549"
---
# <span data-ttu-id="05632-101">New-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="05632-101">New-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="05632-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05632-102">SYNOPSIS</span></span>
<span data-ttu-id="05632-103">Criar um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="05632-103">Create an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05632-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05632-104">SYNTAX</span></span>

```
New-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05632-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05632-105">DESCRIPTION</span></span>
<span data-ttu-id="05632-106">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="05632-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="05632-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05632-107">EXAMPLES</span></span>

### <span data-ttu-id="05632-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="05632-108">Example 1</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="05632-109">Crie um serviço de provisionamento de dispositivo Hub IoT do Azure com o tipo de preço padrão S1 na região do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="05632-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="05632-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="05632-110">Example 2</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

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

<span data-ttu-id="05632-111">Crie um serviço de provisionamento de dispositivo Hub IoT do Azure com o tipo de preço padrão S1 na região ' eastus '.</span><span class="sxs-lookup"><span data-stu-id="05632-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="05632-112">OS</span><span class="sxs-lookup"><span data-stu-id="05632-112">PARAMETERS</span></span>

### <span data-ttu-id="05632-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="05632-113">-AllocationPolicy</span></span>
<span data-ttu-id="05632-114">Política de alocação do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="05632-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="05632-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05632-115">-DefaultProfile</span></span>
<span data-ttu-id="05632-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05632-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05632-117">-Local</span><span class="sxs-lookup"><span data-stu-id="05632-117">-Location</span></span>
<span data-ttu-id="05632-118">Ponto</span><span class="sxs-lookup"><span data-stu-id="05632-118">Location</span></span>

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

### <span data-ttu-id="05632-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="05632-119">-Name</span></span>
<span data-ttu-id="05632-120">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="05632-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="05632-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05632-121">-ResourceGroupName</span></span>
<span data-ttu-id="05632-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="05632-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="05632-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="05632-123">-SkuName</span></span>
<span data-ttu-id="05632-124">SKU</span><span class="sxs-lookup"><span data-stu-id="05632-124">Sku</span></span>

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

### <span data-ttu-id="05632-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="05632-125">-Confirm</span></span>
<span data-ttu-id="05632-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05632-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05632-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05632-127">-WhatIf</span></span>
<span data-ttu-id="05632-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05632-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05632-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05632-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05632-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05632-130">CommonParameters</span></span>
<span data-ttu-id="05632-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05632-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05632-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05632-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05632-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05632-133">INPUTS</span></span>

### <span data-ttu-id="05632-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="05632-134">None</span></span>

## <span data-ttu-id="05632-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05632-135">OUTPUTS</span></span>

### <span data-ttu-id="05632-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="05632-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="05632-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05632-137">NOTES</span></span>

## <span data-ttu-id="05632-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05632-138">RELATED LINKS</span></span>
