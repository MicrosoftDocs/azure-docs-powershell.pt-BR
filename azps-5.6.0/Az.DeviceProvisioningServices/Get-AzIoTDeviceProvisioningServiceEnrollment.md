---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 56aadda2d7f1dccb77795d5226fb79c8a0fc65ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886226"
---
# <span data-ttu-id="ce7b2-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="ce7b2-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="ce7b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ce7b2-103">Obter um registro de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce7b2-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="ce7b2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ce7b2-104">SYNTAX</span></span>

### <span data-ttu-id="ce7b2-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ce7b2-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce7b2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ce7b2-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce7b2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ce7b2-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce7b2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ce7b2-108">DESCRIPTION</span></span>
<span data-ttu-id="ce7b2-109">Obter detalhes de registro de dispositivo ou Listar registro de dispositivos em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ce7b2-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="ce7b2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce7b2-110">EXAMPLES</span></span>

### <span data-ttu-id="ce7b2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce7b2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="ce7b2-112">Obter detalhes do registro do dispositivo em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ce7b2-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="ce7b2-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce7b2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="ce7b2-114">Listar os registro de dispositivos em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ce7b2-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="ce7b2-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ce7b2-115">PARAMETERS</span></span>

### <span data-ttu-id="ce7b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce7b2-116">-DefaultProfile</span></span>
<span data-ttu-id="ce7b2-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce7b2-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="ce7b2-118">-DpsName</span></span>
<span data-ttu-id="ce7b2-119">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="ce7b2-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ce7b2-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="ce7b2-120">-DpsObject</span></span>
<span data-ttu-id="ce7b2-121">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="ce7b2-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ce7b2-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="ce7b2-122">-RegistrationId</span></span>
<span data-ttu-id="ce7b2-123">ID de registro de registro individual.</span><span class="sxs-lookup"><span data-stu-id="ce7b2-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="ce7b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce7b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce7b2-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ce7b2-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ce7b2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce7b2-126">-ResourceId</span></span>
<span data-ttu-id="ce7b2-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="ce7b2-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ce7b2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce7b2-128">CommonParameters</span></span>
<span data-ttu-id="ce7b2-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce7b2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce7b2-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce7b2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce7b2-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce7b2-131">INPUTS</span></span>

### <span data-ttu-id="ce7b2-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ce7b2-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="ce7b2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ce7b2-133">System.String</span></span>

## <span data-ttu-id="ce7b2-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ce7b2-134">OUTPUTS</span></span>

### <span data-ttu-id="ce7b2-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="ce7b2-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="ce7b2-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span><span class="sxs-lookup"><span data-stu-id="ce7b2-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="ce7b2-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="ce7b2-137">NOTES</span></span>

## <span data-ttu-id="ce7b2-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce7b2-138">RELATED LINKS</span></span>
