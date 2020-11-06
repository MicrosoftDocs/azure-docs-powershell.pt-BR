---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: dd9bc81ef24530369a26ff290270a39c8ab1ff40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426358"
---
# <span data-ttu-id="e4bef-101">Get-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="e4bef-101">Get-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="e4bef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4bef-102">SYNOPSIS</span></span>
<span data-ttu-id="e4bef-103">Listar todos ou mostrar detalhes dos serviços de provisionamento do dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e4bef-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4bef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4bef-104">SYNTAX</span></span>

### <span data-ttu-id="e4bef-105">ListIotDpsByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4bef-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningService [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4bef-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="e4bef-106">GetIotDpsByName</span></span>
```
Get-AzureRmIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4bef-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4bef-107">DESCRIPTION</span></span>
<span data-ttu-id="e4bef-108">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="e4bef-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="e4bef-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4bef-109">EXAMPLES</span></span>

### <span data-ttu-id="e4bef-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4bef-110">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="e4bef-111">Listar todos os serviços de provisionamento do dispositivo Hub IoT do Azure em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="e4bef-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="e4bef-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e4bef-112">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="e4bef-113">Listar todos os serviços de provisionamento do dispositivo Hub IoT do Azure no grupo de recursos ' MyResource '.</span><span class="sxs-lookup"><span data-stu-id="e4bef-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="e4bef-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e4bef-114">Example 3</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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

<span data-ttu-id="e4bef-115">Mostrar detalhes de um serviço de provisionamento de dispositivo Hub IoT do Azure ' myiotdps '.</span><span class="sxs-lookup"><span data-stu-id="e4bef-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="e4bef-116">OS</span><span class="sxs-lookup"><span data-stu-id="e4bef-116">PARAMETERS</span></span>

### <span data-ttu-id="e4bef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bef-117">-DefaultProfile</span></span>
<span data-ttu-id="e4bef-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4bef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4bef-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4bef-119">-Name</span></span>
<span data-ttu-id="e4bef-120">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="e4bef-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e4bef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4bef-121">-ResourceGroupName</span></span>
<span data-ttu-id="e4bef-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e4bef-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e4bef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bef-123">CommonParameters</span></span>
<span data-ttu-id="e4bef-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4bef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bef-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4bef-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bef-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4bef-126">INPUTS</span></span>

### <span data-ttu-id="e4bef-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e4bef-127">None</span></span>

## <span data-ttu-id="e4bef-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4bef-128">OUTPUTS</span></span>

### <span data-ttu-id="e4bef-129">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="e4bef-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="e4bef-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4bef-130">NOTES</span></span>

## <span data-ttu-id="e4bef-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4bef-131">RELATED LINKS</span></span>
