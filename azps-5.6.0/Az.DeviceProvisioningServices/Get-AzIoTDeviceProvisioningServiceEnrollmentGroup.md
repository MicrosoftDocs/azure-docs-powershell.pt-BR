---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 037e2d99b52e6be1aeca3e74f2a31f3c0323749d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901493"
---
# <span data-ttu-id="90124-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="90124-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="90124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90124-102">SYNOPSIS</span></span>
<span data-ttu-id="90124-103">Obter um grupo de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90124-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="90124-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="90124-104">SYNTAX</span></span>

### <span data-ttu-id="90124-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="90124-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90124-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="90124-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90124-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="90124-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90124-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="90124-108">DESCRIPTION</span></span>
<span data-ttu-id="90124-109">Obter os detalhes de um grupo de registro ou listar todos os grupos de registro em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="90124-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="90124-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90124-110">EXAMPLES</span></span>

### <span data-ttu-id="90124-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="90124-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="90124-112">Obter o grupo de registro de dispositivos em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="90124-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="90124-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="90124-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="90124-114">Listar todos os grupos de registro de dispositivo em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="90124-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="90124-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="90124-115">PARAMETERS</span></span>

### <span data-ttu-id="90124-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90124-116">-DefaultProfile</span></span>
<span data-ttu-id="90124-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90124-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90124-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="90124-118">-DpsName</span></span>
<span data-ttu-id="90124-119">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="90124-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="90124-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="90124-120">-DpsObject</span></span>
<span data-ttu-id="90124-121">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="90124-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="90124-122">-Name</span><span class="sxs-lookup"><span data-stu-id="90124-122">-Name</span></span>
<span data-ttu-id="90124-123">Nome do grupo de inscrição.</span><span class="sxs-lookup"><span data-stu-id="90124-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="90124-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90124-124">-ResourceGroupName</span></span>
<span data-ttu-id="90124-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="90124-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="90124-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90124-126">-ResourceId</span></span>
<span data-ttu-id="90124-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="90124-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="90124-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90124-128">CommonParameters</span></span>
<span data-ttu-id="90124-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90124-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90124-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90124-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90124-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90124-131">INPUTS</span></span>

### <span data-ttu-id="90124-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="90124-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="90124-133">System.String</span><span class="sxs-lookup"><span data-stu-id="90124-133">System.String</span></span>

## <span data-ttu-id="90124-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="90124-134">OUTPUTS</span></span>

### <span data-ttu-id="90124-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="90124-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="90124-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span><span class="sxs-lookup"><span data-stu-id="90124-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="90124-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="90124-137">NOTES</span></span>

## <span data-ttu-id="90124-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90124-138">RELATED LINKS</span></span>
