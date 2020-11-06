---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f5d750dc795619f32f6c4f16a5fe1e3b5e111106
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610602"
---
# <span data-ttu-id="c6ce0-101">Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c6ce0-101">Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="c6ce0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="c6ce0-103">Atualizar uma política de acesso compartilhado em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6ce0-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6ce0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6ce0-104">SYNTAX</span></span>

### <span data-ttu-id="c6ce0-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c6ce0-105">ResourceSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6ce0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c6ce0-106">InputObjectSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6ce0-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="c6ce0-107">ResourceIdSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6ce0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6ce0-108">DESCRIPTION</span></span>
<span data-ttu-id="c6ce0-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="c6ce0-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c6ce0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6ce0-110">EXAMPLES</span></span>

### <span data-ttu-id="c6ce0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6ce0-111">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="c6ce0-112">Atualize a política de acesso "MyPolicy" em um serviço de provisionamento de dispositivo Hub do Azure IoT com EnrollmentWrite Right.</span><span class="sxs-lookup"><span data-stu-id="c6ce0-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="c6ce0-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6ce0-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzureRmIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="c6ce0-114">Atualize a política de acesso "MyPolicy" em um serviço de provisionamento de dispositivo Hub do Azure IoT com EnrollmentWrite Right usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="c6ce0-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="c6ce0-115">OS</span><span class="sxs-lookup"><span data-stu-id="c6ce0-115">PARAMETERS</span></span>

### <span data-ttu-id="c6ce0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6ce0-116">-DefaultProfile</span></span>
<span data-ttu-id="c6ce0-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6ce0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6ce0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6ce0-118">-InputObject</span></span>
<span data-ttu-id="c6ce0-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="c6ce0-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6ce0-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c6ce0-120">-KeyName</span></span>
<span data-ttu-id="c6ce0-121">Nome da chave da política de acesso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="c6ce0-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ce0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6ce0-122">-Name</span></span>
<span data-ttu-id="c6ce0-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="c6ce0-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c6ce0-124">-Permissões</span><span class="sxs-lookup"><span data-stu-id="c6ce0-124">-Permissions</span></span>
<span data-ttu-id="c6ce0-125">Permissões de política de acesso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="c6ce0-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="c6ce0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6ce0-126">-ResourceGroupName</span></span>
<span data-ttu-id="c6ce0-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c6ce0-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c6ce0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6ce0-128">-ResourceId</span></span>
<span data-ttu-id="c6ce0-129">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="c6ce0-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c6ce0-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c6ce0-130">-Confirm</span></span>
<span data-ttu-id="c6ce0-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6ce0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6ce0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6ce0-132">-WhatIf</span></span>
<span data-ttu-id="c6ce0-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c6ce0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6ce0-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c6ce0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6ce0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6ce0-135">CommonParameters</span></span>
<span data-ttu-id="c6ce0-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6ce0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6ce0-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6ce0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6ce0-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6ce0-138">INPUTS</span></span>

### <span data-ttu-id="c6ce0-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="c6ce0-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="c6ce0-140">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c6ce0-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c6ce0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c6ce0-141">System.String</span></span>

## <span data-ttu-id="c6ce0-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6ce0-142">OUTPUTS</span></span>

### <span data-ttu-id="c6ce0-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="c6ce0-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="c6ce0-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6ce0-144">NOTES</span></span>

## <span data-ttu-id="c6ce0-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6ce0-145">RELATED LINKS</span></span>
