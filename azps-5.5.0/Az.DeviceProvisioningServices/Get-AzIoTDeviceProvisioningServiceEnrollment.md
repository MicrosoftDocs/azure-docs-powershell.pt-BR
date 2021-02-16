---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117679"
---
# <span data-ttu-id="6906f-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="6906f-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="6906f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6906f-102">SYNOPSIS</span></span>
<span data-ttu-id="6906f-103">Obter um registro de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6906f-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="6906f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6906f-104">SYNTAX</span></span>

### <span data-ttu-id="6906f-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6906f-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6906f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6906f-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6906f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6906f-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6906f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6906f-108">DESCRIPTION</span></span>
<span data-ttu-id="6906f-109">Obter detalhes de registro do dispositivo ou listar o registro de dispositivos em um Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="6906f-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6906f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6906f-110">EXAMPLES</span></span>

### <span data-ttu-id="6906f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6906f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="6906f-112">Obter detalhes de registro do dispositivo em um Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="6906f-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="6906f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6906f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="6906f-114">Liste os registro de dispositivos em um Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="6906f-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6906f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6906f-115">PARAMETERS</span></span>

### <span data-ttu-id="6906f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6906f-116">-DefaultProfile</span></span>
<span data-ttu-id="6906f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6906f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6906f-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="6906f-118">-DpsName</span></span>
<span data-ttu-id="6906f-119">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="6906f-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6906f-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="6906f-120">-DpsObject</span></span>
<span data-ttu-id="6906f-121">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="6906f-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="6906f-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="6906f-122">-RegistrationId</span></span>
<span data-ttu-id="6906f-123">ID do registro individual.</span><span class="sxs-lookup"><span data-stu-id="6906f-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="6906f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6906f-124">-ResourceGroupName</span></span>
<span data-ttu-id="6906f-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="6906f-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6906f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6906f-126">-ResourceId</span></span>
<span data-ttu-id="6906f-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="6906f-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="6906f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6906f-128">CommonParameters</span></span>
<span data-ttu-id="6906f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6906f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6906f-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6906f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6906f-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="6906f-131">INPUTS</span></span>

### <span data-ttu-id="6906f-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="6906f-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="6906f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6906f-133">System.String</span></span>

## <span data-ttu-id="6906f-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="6906f-134">OUTPUTS</span></span>

### <span data-ttu-id="6906f-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="6906f-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="6906f-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span><span class="sxs-lookup"><span data-stu-id="6906f-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="6906f-137">Notas</span><span class="sxs-lookup"><span data-stu-id="6906f-137">NOTES</span></span>

## <span data-ttu-id="6906f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6906f-138">RELATED LINKS</span></span>
