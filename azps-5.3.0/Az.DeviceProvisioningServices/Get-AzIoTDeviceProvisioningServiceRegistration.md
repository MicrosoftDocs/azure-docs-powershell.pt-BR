---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428368"
---
# <span data-ttu-id="97ebb-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="97ebb-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="97ebb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="97ebb-103">Obtém o estado do registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97ebb-103">Gets the device registration state.</span></span>

## <span data-ttu-id="97ebb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97ebb-104">SYNTAX</span></span>

### <span data-ttu-id="97ebb-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="97ebb-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97ebb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="97ebb-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97ebb-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="97ebb-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97ebb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97ebb-108">DESCRIPTION</span></span>
<span data-ttu-id="97ebb-109">Obtenha o estado do registro do dispositivo ou o estado de registro de dispositivos sob o registro em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="97ebb-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="97ebb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97ebb-110">EXAMPLES</span></span>

### <span data-ttu-id="97ebb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="97ebb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="97ebb-112">Obtenha os detalhes do estado do registro do dispositivo em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="97ebb-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="97ebb-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="97ebb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="97ebb-114">Listar todo o estado de registro de dispositivos neste subdispositivo de registro.</span><span class="sxs-lookup"><span data-stu-id="97ebb-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="97ebb-115">OS</span><span class="sxs-lookup"><span data-stu-id="97ebb-115">PARAMETERS</span></span>

### <span data-ttu-id="97ebb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ebb-116">-DefaultProfile</span></span>
<span data-ttu-id="97ebb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97ebb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97ebb-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="97ebb-118">-DpsName</span></span>
<span data-ttu-id="97ebb-119">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="97ebb-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="97ebb-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="97ebb-120">-DpsObject</span></span>
<span data-ttu-id="97ebb-121">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="97ebb-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="97ebb-122">-Enrollmentidid</span><span class="sxs-lookup"><span data-stu-id="97ebb-122">-EnrollmentId</span></span>
<span data-ttu-id="97ebb-123">ID do grupo de inscrição.</span><span class="sxs-lookup"><span data-stu-id="97ebb-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="97ebb-124">-Consulta</span><span class="sxs-lookup"><span data-stu-id="97ebb-124">-Query</span></span>
<span data-ttu-id="97ebb-125">Consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="97ebb-125">Sql query.</span></span>

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

### <span data-ttu-id="97ebb-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="97ebb-126">-RegistrationId</span></span>
<span data-ttu-id="97ebb-127">ID do registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97ebb-127">ID of device registration.</span></span>

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

### <span data-ttu-id="97ebb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97ebb-128">-ResourceGroupName</span></span>
<span data-ttu-id="97ebb-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="97ebb-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="97ebb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97ebb-130">-ResourceId</span></span>
<span data-ttu-id="97ebb-131">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="97ebb-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="97ebb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ebb-132">CommonParameters</span></span>
<span data-ttu-id="97ebb-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97ebb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ebb-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97ebb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ebb-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97ebb-135">INPUTS</span></span>

### <span data-ttu-id="97ebb-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="97ebb-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="97ebb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="97ebb-137">System.String</span></span>

## <span data-ttu-id="97ebb-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97ebb-138">OUTPUTS</span></span>

### <span data-ttu-id="97ebb-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="97ebb-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="97ebb-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates []</span><span class="sxs-lookup"><span data-stu-id="97ebb-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="97ebb-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97ebb-141">NOTES</span></span>

## <span data-ttu-id="97ebb-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97ebb-142">RELATED LINKS</span></span>
