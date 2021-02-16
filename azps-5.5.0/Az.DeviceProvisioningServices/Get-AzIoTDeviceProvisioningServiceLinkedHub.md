---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 62f9a2d77ce3a5b34b25c98d681bcfba55ae62e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113220"
---
# <span data-ttu-id="8c8e5-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="8c8e5-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="8c8e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c8e5-102">SYNOPSIS</span></span>
<span data-ttu-id="8c8e5-103">Liste todos ou mostre detalhes dos hubs de IoT vinculados em um serviço de provisionamento de dispositivos do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="8c8e5-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="8c8e5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c8e5-104">SYNTAX</span></span>

### <span data-ttu-id="8c8e5-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8c8e5-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c8e5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8c8e5-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c8e5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8c8e5-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c8e5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c8e5-108">DESCRIPTION</span></span>
<span data-ttu-id="8c8e5-109">Para uma introdução ao Serviço de Provisionamento de Dispositivo do Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="8c8e5-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="8c8e5-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8c8e5-110">EXAMPLES</span></span>

### <span data-ttu-id="8c8e5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8c8e5-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="8c8e5-112">Liste todos os hubs de IoT vinculados em "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="8c8e5-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="8c8e5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8c8e5-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="8c8e5-114">Mostrar detalhes do hub IoT vinculado "myiothub1" em um serviço de provisionamento de dispositivos do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="8c8e5-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="8c8e5-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c8e5-115">PARAMETERS</span></span>

### <span data-ttu-id="8c8e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c8e5-116">-DefaultProfile</span></span>
<span data-ttu-id="8c8e5-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c8e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c8e5-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="8c8e5-118">-DpsObject</span></span>
<span data-ttu-id="8c8e5-119">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="8c8e5-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="8c8e5-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="8c8e5-120">-LinkedHubName</span></span>
<span data-ttu-id="8c8e5-121">Nome do host do Hub de IoT vinculado</span><span class="sxs-lookup"><span data-stu-id="8c8e5-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="8c8e5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c8e5-122">-Name</span></span>
<span data-ttu-id="8c8e5-123">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="8c8e5-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8c8e5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c8e5-124">-ResourceGroupName</span></span>
<span data-ttu-id="8c8e5-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8c8e5-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8c8e5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c8e5-126">-ResourceId</span></span>
<span data-ttu-id="8c8e5-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="8c8e5-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="8c8e5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c8e5-128">CommonParameters</span></span>
<span data-ttu-id="8c8e5-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c8e5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c8e5-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c8e5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c8e5-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="8c8e5-131">INPUTS</span></span>

### <span data-ttu-id="8c8e5-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8c8e5-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="8c8e5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8c8e5-133">System.String</span></span>

## <span data-ttu-id="8c8e5-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="8c8e5-134">OUTPUTS</span></span>

### <span data-ttu-id="8c8e5-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="8c8e5-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="8c8e5-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="8c8e5-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="8c8e5-137">Notas</span><span class="sxs-lookup"><span data-stu-id="8c8e5-137">NOTES</span></span>

## <span data-ttu-id="8c8e5-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c8e5-138">RELATED LINKS</span></span>
