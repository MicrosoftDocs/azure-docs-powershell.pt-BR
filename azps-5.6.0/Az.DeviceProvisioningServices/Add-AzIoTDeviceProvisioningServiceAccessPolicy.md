---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f34816ca77955c86f68b421efa221eab57e552cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892966"
---
# <span data-ttu-id="ed2ba-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ed2ba-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="ed2ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed2ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2ba-103">Adicione uma nova política de acesso compartilhado em um serviço de provisionamento de dispositivos do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="ed2ba-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="ed2ba-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ed2ba-104">SYNTAX</span></span>

### <span data-ttu-id="ed2ba-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ed2ba-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed2ba-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ed2ba-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed2ba-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ed2ba-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed2ba-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ed2ba-108">DESCRIPTION</span></span>
<span data-ttu-id="ed2ba-109">Para uma introdução ao Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="ed2ba-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="ed2ba-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed2ba-110">EXAMPLES</span></span>

### <span data-ttu-id="ed2ba-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed2ba-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="ed2ba-112">Adicione uma nova política de acesso compartilhado em um serviço de provisionamento de dispositivo do Azure IoT Hub com direitos EnrollmentWrite e ServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="ed2ba-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="ed2ba-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ed2ba-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="ed2ba-114">Adicione uma nova política de acesso compartilhado em um serviço de provisionamento de dispositivo do Azure IoT Hub com EnrollmentRead à direita.</span><span class="sxs-lookup"><span data-stu-id="ed2ba-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="ed2ba-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ed2ba-115">PARAMETERS</span></span>

### <span data-ttu-id="ed2ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2ba-116">-DefaultProfile</span></span>
<span data-ttu-id="ed2ba-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed2ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed2ba-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="ed2ba-118">-DpsObject</span></span>
<span data-ttu-id="ed2ba-119">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="ed2ba-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ed2ba-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ed2ba-120">-KeyName</span></span>
<span data-ttu-id="ed2ba-121">Nome da chave da política de acesso ao Serviço de Provisionamento de Dispositivos IoT</span><span class="sxs-lookup"><span data-stu-id="ed2ba-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="ed2ba-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ed2ba-122">-Name</span></span>
<span data-ttu-id="ed2ba-123">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="ed2ba-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ed2ba-124">-Permissões</span><span class="sxs-lookup"><span data-stu-id="ed2ba-124">-Permissions</span></span>
<span data-ttu-id="ed2ba-125">Permissões de política de acesso ao Serviço de Provisionamento de Dispositivos IoT</span><span class="sxs-lookup"><span data-stu-id="ed2ba-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="ed2ba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed2ba-126">-ResourceGroupName</span></span>
<span data-ttu-id="ed2ba-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ed2ba-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ed2ba-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed2ba-128">-ResourceId</span></span>
<span data-ttu-id="ed2ba-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="ed2ba-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ed2ba-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed2ba-130">-Confirm</span></span>
<span data-ttu-id="ed2ba-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed2ba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed2ba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed2ba-132">-WhatIf</span></span>
<span data-ttu-id="ed2ba-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ed2ba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed2ba-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed2ba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed2ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2ba-135">CommonParameters</span></span>
<span data-ttu-id="ed2ba-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed2ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2ba-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed2ba-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2ba-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed2ba-138">INPUTS</span></span>

### <span data-ttu-id="ed2ba-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ed2ba-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="ed2ba-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ed2ba-140">System.String</span></span>

## <span data-ttu-id="ed2ba-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ed2ba-141">OUTPUTS</span></span>

### <span data-ttu-id="ed2ba-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="ed2ba-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="ed2ba-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="ed2ba-143">NOTES</span></span>

## <span data-ttu-id="ed2ba-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed2ba-144">RELATED LINKS</span></span>
