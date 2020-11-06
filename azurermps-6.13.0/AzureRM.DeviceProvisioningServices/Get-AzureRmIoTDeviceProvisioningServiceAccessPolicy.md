---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: e0685e82a4db2c786d4bb578544f6cbbd5dbadc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426360"
---
# <span data-ttu-id="87939-101">Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87939-101">Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="87939-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87939-102">SYNOPSIS</span></span>
<span data-ttu-id="87939-103">Listar todos ou mostrar detalhes das políticas de acesso compartilhado em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="87939-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87939-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87939-104">SYNTAX</span></span>

### <span data-ttu-id="87939-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="87939-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87939-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="87939-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87939-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="87939-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87939-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87939-108">DESCRIPTION</span></span>
<span data-ttu-id="87939-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="87939-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="87939-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87939-110">EXAMPLES</span></span>

### <span data-ttu-id="87939-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="87939-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="87939-112">Listar todas as políticas de acesso compartilhado em "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="87939-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="87939-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="87939-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="87939-114">Mostrar detalhes da política de acesso compartilhado "MyPolicy" em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="87939-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="87939-115">OS</span><span class="sxs-lookup"><span data-stu-id="87939-115">PARAMETERS</span></span>

### <span data-ttu-id="87939-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87939-116">-DefaultProfile</span></span>
<span data-ttu-id="87939-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87939-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87939-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="87939-118">-DpsObject</span></span>
<span data-ttu-id="87939-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="87939-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="87939-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="87939-120">-KeyName</span></span>
<span data-ttu-id="87939-121">Nome da chave da política de acesso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="87939-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="87939-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="87939-122">-Name</span></span>
<span data-ttu-id="87939-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="87939-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="87939-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87939-124">-ResourceGroupName</span></span>
<span data-ttu-id="87939-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="87939-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="87939-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87939-126">-ResourceId</span></span>
<span data-ttu-id="87939-127">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="87939-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="87939-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87939-128">CommonParameters</span></span>
<span data-ttu-id="87939-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87939-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87939-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87939-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87939-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87939-131">INPUTS</span></span>

### <span data-ttu-id="87939-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="87939-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="87939-133">Parâmetros: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="87939-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="87939-134">System. String</span><span class="sxs-lookup"><span data-stu-id="87939-134">System.String</span></span>

## <span data-ttu-id="87939-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87939-135">OUTPUTS</span></span>

### <span data-ttu-id="87939-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="87939-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="87939-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87939-137">NOTES</span></span>

## <span data-ttu-id="87939-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87939-138">RELATED LINKS</span></span>
