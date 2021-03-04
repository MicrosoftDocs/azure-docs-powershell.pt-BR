---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 6d3997e8a58ecab6a31e233d4ee3c0e2c66ae9ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890857"
---
# <span data-ttu-id="0507e-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="0507e-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="0507e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0507e-102">SYNOPSIS</span></span>
<span data-ttu-id="0507e-103">Obtém o estado de registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0507e-103">Gets the device registration state.</span></span>

## <span data-ttu-id="0507e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0507e-104">SYNTAX</span></span>

### <span data-ttu-id="0507e-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0507e-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0507e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0507e-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0507e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0507e-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0507e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0507e-108">DESCRIPTION</span></span>
<span data-ttu-id="0507e-109">Obter o estado de registro do dispositivo ou o estado de registro de dispositivos no enrollmentGroup em um Serviço de Provisionamento de Dispositivo de Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="0507e-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="0507e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0507e-110">EXAMPLES</span></span>

### <span data-ttu-id="0507e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0507e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="0507e-112">Obter os detalhes do estado de registro do dispositivo em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="0507e-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="0507e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0507e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="0507e-114">Listar todo o estado de registro de dispositivos neste enrollmentGroup.</span><span class="sxs-lookup"><span data-stu-id="0507e-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="0507e-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0507e-115">PARAMETERS</span></span>

### <span data-ttu-id="0507e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0507e-116">-DefaultProfile</span></span>
<span data-ttu-id="0507e-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0507e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0507e-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="0507e-118">-DpsName</span></span>
<span data-ttu-id="0507e-119">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="0507e-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0507e-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="0507e-120">-DpsObject</span></span>
<span data-ttu-id="0507e-121">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="0507e-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0507e-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="0507e-122">-EnrollmentId</span></span>
<span data-ttu-id="0507e-123">ID do grupo de inscrição.</span><span class="sxs-lookup"><span data-stu-id="0507e-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="0507e-124">-Query</span><span class="sxs-lookup"><span data-stu-id="0507e-124">-Query</span></span>
<span data-ttu-id="0507e-125">Consulta sql.</span><span class="sxs-lookup"><span data-stu-id="0507e-125">Sql query.</span></span>

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

### <span data-ttu-id="0507e-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="0507e-126">-RegistrationId</span></span>
<span data-ttu-id="0507e-127">ID do registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0507e-127">ID of device registration.</span></span>

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

### <span data-ttu-id="0507e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0507e-128">-ResourceGroupName</span></span>
<span data-ttu-id="0507e-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="0507e-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0507e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0507e-130">-ResourceId</span></span>
<span data-ttu-id="0507e-131">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="0507e-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0507e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0507e-132">CommonParameters</span></span>
<span data-ttu-id="0507e-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0507e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0507e-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0507e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0507e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0507e-135">INPUTS</span></span>

### <span data-ttu-id="0507e-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0507e-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="0507e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0507e-137">System.String</span></span>

## <span data-ttu-id="0507e-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0507e-138">OUTPUTS</span></span>

### <span data-ttu-id="0507e-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="0507e-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="0507e-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span><span class="sxs-lookup"><span data-stu-id="0507e-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="0507e-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="0507e-141">NOTES</span></span>

## <span data-ttu-id="0507e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0507e-142">RELATED LINKS</span></span>
