---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948295"
---
# <span data-ttu-id="c6c98-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="c6c98-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="c6c98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6c98-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c98-103">Obter um registro de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6c98-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="c6c98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6c98-104">SYNTAX</span></span>

### <span data-ttu-id="c6c98-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c6c98-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6c98-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c6c98-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6c98-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="c6c98-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6c98-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6c98-108">DESCRIPTION</span></span>
<span data-ttu-id="c6c98-109">Obter detalhes de inscrição do dispositivo ou listar registros de dispositivo em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="c6c98-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c6c98-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6c98-110">EXAMPLES</span></span>

### <span data-ttu-id="c6c98-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6c98-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="c6c98-112">Obter detalhes de registro do dispositivo em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c98-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="c6c98-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c6c98-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="c6c98-114">Listar registros de dispositivo em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c98-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c6c98-115">OS</span><span class="sxs-lookup"><span data-stu-id="c6c98-115">PARAMETERS</span></span>

### <span data-ttu-id="c6c98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c98-116">-DefaultProfile</span></span>
<span data-ttu-id="c6c98-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c98-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c98-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="c6c98-118">-DpsName</span></span>
<span data-ttu-id="c6c98-119">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="c6c98-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c6c98-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c6c98-120">-DpsObject</span></span>
<span data-ttu-id="c6c98-121">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="c6c98-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c6c98-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="c6c98-122">-RegistrationId</span></span>
<span data-ttu-id="c6c98-123">ID de registro de inscrição individual.</span><span class="sxs-lookup"><span data-stu-id="c6c98-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="c6c98-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c98-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6c98-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c6c98-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c6c98-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c98-126">-ResourceId</span></span>
<span data-ttu-id="c6c98-127">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="c6c98-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c6c98-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c98-128">CommonParameters</span></span>
<span data-ttu-id="c6c98-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6c98-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c98-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6c98-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c98-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6c98-131">INPUTS</span></span>

### <span data-ttu-id="c6c98-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c6c98-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c6c98-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c6c98-133">System.String</span></span>

## <span data-ttu-id="c6c98-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6c98-134">OUTPUTS</span></span>

### <span data-ttu-id="c6c98-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="c6c98-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="c6c98-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollments []</span><span class="sxs-lookup"><span data-stu-id="c6c98-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="c6c98-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6c98-137">NOTES</span></span>

## <span data-ttu-id="c6c98-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6c98-138">RELATED LINKS</span></span>
