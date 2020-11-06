---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f978e6c0a496273535551663a442989b2ab1648e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596590"
---
# <span data-ttu-id="5ab19-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5ab19-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="5ab19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ab19-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab19-103">Listar todos ou mostrar detalhes das políticas de acesso compartilhado em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5ab19-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5ab19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ab19-104">SYNTAX</span></span>

### <span data-ttu-id="5ab19-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5ab19-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ab19-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5ab19-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ab19-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="5ab19-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ab19-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ab19-108">DESCRIPTION</span></span>
<span data-ttu-id="5ab19-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5ab19-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5ab19-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ab19-110">EXAMPLES</span></span>

### <span data-ttu-id="5ab19-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5ab19-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="5ab19-112">Listar todas as políticas de acesso compartilhado em "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="5ab19-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="5ab19-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5ab19-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="5ab19-114">Mostrar detalhes da política de acesso compartilhado "MyPolicy" em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5ab19-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5ab19-115">OS</span><span class="sxs-lookup"><span data-stu-id="5ab19-115">PARAMETERS</span></span>

### <span data-ttu-id="5ab19-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab19-116">-DefaultProfile</span></span>
<span data-ttu-id="5ab19-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab19-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ab19-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5ab19-118">-DpsObject</span></span>
<span data-ttu-id="5ab19-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5ab19-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5ab19-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5ab19-120">-KeyName</span></span>
<span data-ttu-id="5ab19-121">Nome da chave da política de acesso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5ab19-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="5ab19-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ab19-122">-Name</span></span>
<span data-ttu-id="5ab19-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5ab19-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5ab19-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab19-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ab19-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5ab19-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5ab19-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ab19-126">-ResourceId</span></span>
<span data-ttu-id="5ab19-127">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5ab19-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5ab19-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab19-128">CommonParameters</span></span>
<span data-ttu-id="5ab19-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab19-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab19-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab19-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab19-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ab19-131">INPUTS</span></span>

### <span data-ttu-id="5ab19-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5ab19-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5ab19-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5ab19-133">System.String</span></span>

## <span data-ttu-id="5ab19-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ab19-134">OUTPUTS</span></span>

### <span data-ttu-id="5ab19-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="5ab19-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="5ab19-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ab19-136">NOTES</span></span>

## <span data-ttu-id="5ab19-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ab19-137">RELATED LINKS</span></span>
