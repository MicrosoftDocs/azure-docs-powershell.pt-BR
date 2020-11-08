---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115515"
---
# <span data-ttu-id="6e1a3-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="6e1a3-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="6e1a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e1a3-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1a3-103">Obter um grupo de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="6e1a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e1a3-104">SYNTAX</span></span>

### <span data-ttu-id="6e1a3-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6e1a3-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e1a3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6e1a3-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e1a3-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="6e1a3-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e1a3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e1a3-108">DESCRIPTION</span></span>
<span data-ttu-id="6e1a3-109">Obtenha os detalhes de um grupo de inscrição ou liste todos os grupos de inscrição em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6e1a3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e1a3-110">EXAMPLES</span></span>

### <span data-ttu-id="6e1a3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e1a3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="6e1a3-112">Obter o grupo de registro de dispositivo em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="6e1a3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6e1a3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="6e1a3-114">Listar todos os grupos de inscrição de dispositivos em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6e1a3-115">OS</span><span class="sxs-lookup"><span data-stu-id="6e1a3-115">PARAMETERS</span></span>

### <span data-ttu-id="6e1a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1a3-116">-DefaultProfile</span></span>
<span data-ttu-id="6e1a3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e1a3-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="6e1a3-118">-DpsName</span></span>
<span data-ttu-id="6e1a3-119">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="6e1a3-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6e1a3-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="6e1a3-120">-DpsObject</span></span>
<span data-ttu-id="6e1a3-121">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="6e1a3-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="6e1a3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e1a3-122">-Name</span></span>
<span data-ttu-id="6e1a3-123">Nome do grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="6e1a3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e1a3-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e1a3-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6e1a3-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6e1a3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e1a3-126">-ResourceId</span></span>
<span data-ttu-id="6e1a3-127">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="6e1a3-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="6e1a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1a3-128">CommonParameters</span></span>
<span data-ttu-id="6e1a3-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1a3-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e1a3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1a3-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e1a3-131">INPUTS</span></span>

### <span data-ttu-id="6e1a3-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="6e1a3-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="6e1a3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6e1a3-133">System.String</span></span>

## <span data-ttu-id="6e1a3-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e1a3-134">OUTPUTS</span></span>

### <span data-ttu-id="6e1a3-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="6e1a3-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="6e1a3-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroups []</span><span class="sxs-lookup"><span data-stu-id="6e1a3-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="6e1a3-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e1a3-137">NOTES</span></span>

## <span data-ttu-id="6e1a3-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e1a3-138">RELATED LINKS</span></span>
