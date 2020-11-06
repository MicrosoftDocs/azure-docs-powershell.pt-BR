---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 264978e5cf66436667434c265a7a3ae0c5a31a5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600929"
---
# <span data-ttu-id="12aac-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="12aac-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="12aac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12aac-102">SYNOPSIS</span></span>
<span data-ttu-id="12aac-103">Listar todos ou mostrar detalhes dos serviços de provisionamento do dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="12aac-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="12aac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12aac-104">SYNTAX</span></span>

### <span data-ttu-id="12aac-105">ListIotDpsByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="12aac-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12aac-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="12aac-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12aac-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12aac-107">DESCRIPTION</span></span>
<span data-ttu-id="12aac-108">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="12aac-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="12aac-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12aac-109">EXAMPLES</span></span>

### <span data-ttu-id="12aac-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12aac-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="12aac-111">Listar todos os serviços de provisionamento do dispositivo Hub IoT do Azure em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="12aac-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="12aac-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="12aac-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="12aac-113">Listar todos os serviços de provisionamento do dispositivo Hub IoT do Azure no grupo de recursos ' MyResource '.</span><span class="sxs-lookup"><span data-stu-id="12aac-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="12aac-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="12aac-114">Example 3</span></span>
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

<span data-ttu-id="12aac-115">Mostrar detalhes de um serviço de provisionamento de dispositivo Hub IoT do Azure ' myiotdps '.</span><span class="sxs-lookup"><span data-stu-id="12aac-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="12aac-116">OS</span><span class="sxs-lookup"><span data-stu-id="12aac-116">PARAMETERS</span></span>

### <span data-ttu-id="12aac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12aac-117">-DefaultProfile</span></span>
<span data-ttu-id="12aac-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12aac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12aac-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="12aac-119">-Name</span></span>
<span data-ttu-id="12aac-120">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="12aac-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="12aac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12aac-121">-ResourceGroupName</span></span>
<span data-ttu-id="12aac-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="12aac-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="12aac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12aac-123">CommonParameters</span></span>
<span data-ttu-id="12aac-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12aac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12aac-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12aac-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12aac-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12aac-126">INPUTS</span></span>

### <span data-ttu-id="12aac-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="12aac-127">None</span></span>

## <span data-ttu-id="12aac-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12aac-128">OUTPUTS</span></span>

### <span data-ttu-id="12aac-129">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="12aac-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="12aac-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12aac-130">NOTES</span></span>

## <span data-ttu-id="12aac-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12aac-131">RELATED LINKS</span></span>
