---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113219"
---
# <span data-ttu-id="5a737-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="5a737-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="5a737-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a737-102">SYNOPSIS</span></span>
<span data-ttu-id="5a737-103">Obtém o estado de registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a737-103">Gets the device registration state.</span></span>

## <span data-ttu-id="5a737-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a737-104">SYNTAX</span></span>

### <span data-ttu-id="5a737-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5a737-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a737-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5a737-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a737-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5a737-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a737-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a737-108">DESCRIPTION</span></span>
<span data-ttu-id="5a737-109">Obter o estado de registro do dispositivo ou o estado de registro de dispositivos sob o grupo de inscrição em um Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5a737-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="5a737-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5a737-110">EXAMPLES</span></span>

### <span data-ttu-id="5a737-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5a737-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="5a737-112">Obter os detalhes do estado de registro do dispositivo em um Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5a737-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="5a737-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5a737-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="5a737-114">Listar todos os estados de registro de dispositivos neste grupo de inscrição.</span><span class="sxs-lookup"><span data-stu-id="5a737-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="5a737-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a737-115">PARAMETERS</span></span>

### <span data-ttu-id="5a737-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a737-116">-DefaultProfile</span></span>
<span data-ttu-id="5a737-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a737-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a737-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="5a737-118">-DpsName</span></span>
<span data-ttu-id="5a737-119">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5a737-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5a737-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5a737-120">-DpsObject</span></span>
<span data-ttu-id="5a737-121">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5a737-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5a737-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="5a737-122">-EnrollmentId</span></span>
<span data-ttu-id="5a737-123">ID do grupo de inscrição.</span><span class="sxs-lookup"><span data-stu-id="5a737-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="5a737-124">-Consulta</span><span class="sxs-lookup"><span data-stu-id="5a737-124">-Query</span></span>
<span data-ttu-id="5a737-125">Consulta sql.</span><span class="sxs-lookup"><span data-stu-id="5a737-125">Sql query.</span></span>

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

### <span data-ttu-id="5a737-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="5a737-126">-RegistrationId</span></span>
<span data-ttu-id="5a737-127">ID do registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a737-127">ID of device registration.</span></span>

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

### <span data-ttu-id="5a737-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a737-128">-ResourceGroupName</span></span>
<span data-ttu-id="5a737-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5a737-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5a737-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a737-130">-ResourceId</span></span>
<span data-ttu-id="5a737-131">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="5a737-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5a737-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a737-132">CommonParameters</span></span>
<span data-ttu-id="5a737-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a737-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a737-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a737-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a737-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="5a737-135">INPUTS</span></span>

### <span data-ttu-id="5a737-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5a737-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5a737-137">System.String</span><span class="sxs-lookup"><span data-stu-id="5a737-137">System.String</span></span>

## <span data-ttu-id="5a737-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="5a737-138">OUTPUTS</span></span>

### <span data-ttu-id="5a737-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="5a737-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="5a737-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span><span class="sxs-lookup"><span data-stu-id="5a737-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="5a737-141">Notas</span><span class="sxs-lookup"><span data-stu-id="5a737-141">NOTES</span></span>

## <span data-ttu-id="5a737-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a737-142">RELATED LINKS</span></span>
