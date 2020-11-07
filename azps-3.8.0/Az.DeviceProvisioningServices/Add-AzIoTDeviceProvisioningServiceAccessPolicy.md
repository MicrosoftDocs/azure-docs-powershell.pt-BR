---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942382"
---
# <span data-ttu-id="96a0e-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96a0e-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="96a0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="96a0e-103">Adicione uma nova política de acesso compartilhado a um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="96a0e-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="96a0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96a0e-104">SYNTAX</span></span>

### <span data-ttu-id="96a0e-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="96a0e-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96a0e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="96a0e-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96a0e-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="96a0e-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96a0e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96a0e-108">DESCRIPTION</span></span>
<span data-ttu-id="96a0e-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="96a0e-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="96a0e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96a0e-110">EXAMPLES</span></span>

### <span data-ttu-id="96a0e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96a0e-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="96a0e-112">Adicione uma nova política de acesso compartilhado a um serviço de provisionamento de dispositivo Hub IoT do Azure com os direitos EnrollmentWrite e ServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="96a0e-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="96a0e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="96a0e-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="96a0e-114">Adicione uma nova política de acesso compartilhado a um serviço de provisionamento de dispositivo Hub IoT do Azure com o EnrollmentRead Right.</span><span class="sxs-lookup"><span data-stu-id="96a0e-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="96a0e-115">OS</span><span class="sxs-lookup"><span data-stu-id="96a0e-115">PARAMETERS</span></span>

### <span data-ttu-id="96a0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a0e-116">-DefaultProfile</span></span>
<span data-ttu-id="96a0e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96a0e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96a0e-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="96a0e-118">-DpsObject</span></span>
<span data-ttu-id="96a0e-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="96a0e-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="96a0e-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="96a0e-120">-KeyName</span></span>
<span data-ttu-id="96a0e-121">Nome da chave da política de acesso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="96a0e-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a0e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="96a0e-122">-Name</span></span>
<span data-ttu-id="96a0e-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="96a0e-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="96a0e-124">-Permissões</span><span class="sxs-lookup"><span data-stu-id="96a0e-124">-Permissions</span></span>
<span data-ttu-id="96a0e-125">Permissões de política de acesso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="96a0e-125">IoT Device Provisioning Service access policy permissions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ServiceConfig, EnrollmentRead, EnrollmentWrite, DeviceConnect, RegistrationStatusRead, RegistrationStatusWrite

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a0e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96a0e-126">-ResourceGroupName</span></span>
<span data-ttu-id="96a0e-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="96a0e-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="96a0e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96a0e-128">-ResourceId</span></span>
<span data-ttu-id="96a0e-129">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="96a0e-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="96a0e-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="96a0e-130">-Confirm</span></span>
<span data-ttu-id="96a0e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96a0e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a0e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a0e-132">-WhatIf</span></span>
<span data-ttu-id="96a0e-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="96a0e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96a0e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96a0e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a0e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a0e-135">CommonParameters</span></span>
<span data-ttu-id="96a0e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a0e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a0e-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96a0e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a0e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96a0e-138">INPUTS</span></span>

### <span data-ttu-id="96a0e-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="96a0e-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="96a0e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="96a0e-140">System.String</span></span>

## <span data-ttu-id="96a0e-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96a0e-141">OUTPUTS</span></span>

### <span data-ttu-id="96a0e-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="96a0e-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="96a0e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96a0e-143">NOTES</span></span>

## <span data-ttu-id="96a0e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96a0e-144">RELATED LINKS</span></span>
