---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: d88d764bc45c4ad767448979348000fbbcec3989
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889531"
---
# <span data-ttu-id="7546a-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7546a-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="7546a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7546a-102">SYNOPSIS</span></span>
<span data-ttu-id="7546a-103">Atualize uma política de acesso compartilhado em um serviço de provisionamento de dispositivo do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="7546a-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="7546a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7546a-104">SYNTAX</span></span>

### <span data-ttu-id="7546a-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7546a-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7546a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7546a-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7546a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7546a-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7546a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7546a-108">DESCRIPTION</span></span>
<span data-ttu-id="7546a-109">Para uma introdução ao Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="7546a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="7546a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7546a-110">EXAMPLES</span></span>

### <span data-ttu-id="7546a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7546a-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="7546a-112">Atualizar a política de acesso "mypolicy" em um serviço de provisionamento de dispositivos do Hub do Azure IoT com EnrollmentWrite à direita.</span><span class="sxs-lookup"><span data-stu-id="7546a-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="7546a-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7546a-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="7546a-114">Atualizar a política de acesso "mypolicy" em um serviço de provisionamento de dispositivo do Azure IoT Hub com EnrollmentWrite usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="7546a-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="7546a-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7546a-115">PARAMETERS</span></span>

### <span data-ttu-id="7546a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7546a-116">-DefaultProfile</span></span>
<span data-ttu-id="7546a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7546a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7546a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7546a-118">-InputObject</span></span>
<span data-ttu-id="7546a-119">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="7546a-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7546a-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7546a-120">-KeyName</span></span>
<span data-ttu-id="7546a-121">Nome da chave da política de acesso ao Serviço de Provisionamento de Dispositivos IoT</span><span class="sxs-lookup"><span data-stu-id="7546a-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="7546a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7546a-122">-Name</span></span>
<span data-ttu-id="7546a-123">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="7546a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7546a-124">-Permissões</span><span class="sxs-lookup"><span data-stu-id="7546a-124">-Permissions</span></span>
<span data-ttu-id="7546a-125">Permissões de política de acesso ao Serviço de Provisionamento de Dispositivos IoT</span><span class="sxs-lookup"><span data-stu-id="7546a-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="7546a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7546a-126">-ResourceGroupName</span></span>
<span data-ttu-id="7546a-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7546a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7546a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7546a-128">-ResourceId</span></span>
<span data-ttu-id="7546a-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="7546a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7546a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7546a-130">-Confirm</span></span>
<span data-ttu-id="7546a-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7546a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7546a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7546a-132">-WhatIf</span></span>
<span data-ttu-id="7546a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7546a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7546a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7546a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7546a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7546a-135">CommonParameters</span></span>
<span data-ttu-id="7546a-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7546a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7546a-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7546a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7546a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7546a-138">INPUTS</span></span>

### <span data-ttu-id="7546a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="7546a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="7546a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7546a-140">System.String</span></span>

## <span data-ttu-id="7546a-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7546a-141">OUTPUTS</span></span>

### <span data-ttu-id="7546a-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="7546a-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="7546a-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="7546a-143">NOTES</span></span>

## <span data-ttu-id="7546a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7546a-144">RELATED LINKS</span></span>
