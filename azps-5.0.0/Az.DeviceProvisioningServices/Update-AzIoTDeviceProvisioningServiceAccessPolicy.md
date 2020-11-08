---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: ab23988d5594c2285ac8d6eee02b18b0ae4dbf43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115484"
---
# <span data-ttu-id="5936b-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5936b-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="5936b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5936b-102">SYNOPSIS</span></span>
<span data-ttu-id="5936b-103">Atualizar uma política de acesso compartilhado em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="5936b-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5936b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5936b-104">SYNTAX</span></span>

### <span data-ttu-id="5936b-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5936b-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5936b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5936b-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5936b-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="5936b-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5936b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5936b-108">DESCRIPTION</span></span>
<span data-ttu-id="5936b-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5936b-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5936b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5936b-110">EXAMPLES</span></span>

### <span data-ttu-id="5936b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5936b-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="5936b-112">Atualize a política de acesso "MyPolicy" em um serviço de provisionamento de dispositivo Hub do Azure IoT com EnrollmentWrite Right.</span><span class="sxs-lookup"><span data-stu-id="5936b-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="5936b-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5936b-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="5936b-114">Atualize a política de acesso "MyPolicy" em um serviço de provisionamento de dispositivo Hub do Azure IoT com EnrollmentWrite Right usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="5936b-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="5936b-115">OS</span><span class="sxs-lookup"><span data-stu-id="5936b-115">PARAMETERS</span></span>

### <span data-ttu-id="5936b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5936b-116">-DefaultProfile</span></span>
<span data-ttu-id="5936b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5936b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5936b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5936b-118">-InputObject</span></span>
<span data-ttu-id="5936b-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5936b-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5936b-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5936b-120">-KeyName</span></span>
<span data-ttu-id="5936b-121">Nome da chave da política de acesso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5936b-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="5936b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5936b-122">-Name</span></span>
<span data-ttu-id="5936b-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5936b-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5936b-124">-Permissões</span><span class="sxs-lookup"><span data-stu-id="5936b-124">-Permissions</span></span>
<span data-ttu-id="5936b-125">Permissões de política de acesso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5936b-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="5936b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5936b-126">-ResourceGroupName</span></span>
<span data-ttu-id="5936b-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5936b-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5936b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5936b-128">-ResourceId</span></span>
<span data-ttu-id="5936b-129">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="5936b-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5936b-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5936b-130">-Confirm</span></span>
<span data-ttu-id="5936b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5936b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5936b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5936b-132">-WhatIf</span></span>
<span data-ttu-id="5936b-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5936b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5936b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5936b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5936b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5936b-135">CommonParameters</span></span>
<span data-ttu-id="5936b-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5936b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5936b-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5936b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5936b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5936b-138">INPUTS</span></span>

### <span data-ttu-id="5936b-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="5936b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="5936b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5936b-140">System.String</span></span>

## <span data-ttu-id="5936b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5936b-141">OUTPUTS</span></span>

### <span data-ttu-id="5936b-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="5936b-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="5936b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5936b-143">NOTES</span></span>

## <span data-ttu-id="5936b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5936b-144">RELATED LINKS</span></span>
