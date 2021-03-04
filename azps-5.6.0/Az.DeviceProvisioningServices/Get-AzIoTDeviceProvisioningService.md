---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ee86af7862ad22b34e159f1d5097d5d30a4cba8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901496"
---
# <span data-ttu-id="c545b-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="c545b-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="c545b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c545b-102">SYNOPSIS</span></span>
<span data-ttu-id="c545b-103">Listar todos ou mostrar detalhes dos serviços de provisionamento de dispositivos do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c545b-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="c545b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c545b-104">SYNTAX</span></span>

### <span data-ttu-id="c545b-105">ListIotDpsByResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c545b-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c545b-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="c545b-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c545b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c545b-107">DESCRIPTION</span></span>
<span data-ttu-id="c545b-108">Para uma introdução ao Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="c545b-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c545b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c545b-109">EXAMPLES</span></span>

### <span data-ttu-id="c545b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c545b-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="c545b-111">Listar todos os serviços de provisionamento de dispositivo do Azure IoT Hub em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="c545b-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="c545b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c545b-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="c545b-113">Listar todos os serviços de provisionamento de dispositivo do Azure IoT Hub no grupo de recursos "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="c545b-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="c545b-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c545b-114">Example 3</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="c545b-115">Mostrar detalhes de um serviço de provisionamento de dispositivo do Azure IoT Hub 'myiotdps'.</span><span class="sxs-lookup"><span data-stu-id="c545b-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="c545b-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c545b-116">PARAMETERS</span></span>

### <span data-ttu-id="c545b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c545b-117">-DefaultProfile</span></span>
<span data-ttu-id="c545b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c545b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c545b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c545b-119">-Name</span></span>
<span data-ttu-id="c545b-120">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="c545b-120">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c545b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c545b-121">-ResourceGroupName</span></span>
<span data-ttu-id="c545b-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c545b-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotDpsByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c545b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c545b-123">CommonParameters</span></span>
<span data-ttu-id="c545b-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c545b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c545b-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c545b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c545b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c545b-126">INPUTS</span></span>

### <span data-ttu-id="c545b-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c545b-127">None</span></span>

## <span data-ttu-id="c545b-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c545b-128">OUTPUTS</span></span>

### <span data-ttu-id="c545b-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c545b-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="c545b-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="c545b-130">NOTES</span></span>

## <span data-ttu-id="c545b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c545b-131">RELATED LINKS</span></span>
