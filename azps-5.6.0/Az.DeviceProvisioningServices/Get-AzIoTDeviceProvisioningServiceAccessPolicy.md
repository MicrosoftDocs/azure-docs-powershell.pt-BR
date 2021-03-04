---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 6fff4be5fb4d0c8b76643e215dfda6d2f3d34ab8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888361"
---
# <span data-ttu-id="2ff6f-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ff6f-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="2ff6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ff6f-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff6f-103">Listar todos ou mostrar detalhes das políticas de acesso compartilhado em um serviço de provisionamento de dispositivo do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="2ff6f-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="2ff6f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2ff6f-104">SYNTAX</span></span>

### <span data-ttu-id="2ff6f-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2ff6f-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ff6f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2ff6f-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ff6f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2ff6f-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ff6f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2ff6f-108">DESCRIPTION</span></span>
<span data-ttu-id="2ff6f-109">Para uma introdução ao Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="2ff6f-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="2ff6f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ff6f-110">EXAMPLES</span></span>

### <span data-ttu-id="2ff6f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ff6f-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="2ff6f-112">Listar todas as políticas de acesso compartilhado em "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="2ff6f-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="2ff6f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2ff6f-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="2ff6f-114">Mostrar detalhes da política de acesso compartilhado "mypolicy" em um serviço de provisionamento de dispositivos do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="2ff6f-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="2ff6f-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2ff6f-115">PARAMETERS</span></span>

### <span data-ttu-id="2ff6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff6f-116">-DefaultProfile</span></span>
<span data-ttu-id="2ff6f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ff6f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ff6f-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2ff6f-118">-DpsObject</span></span>
<span data-ttu-id="2ff6f-119">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="2ff6f-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2ff6f-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="2ff6f-120">-KeyName</span></span>
<span data-ttu-id="2ff6f-121">Nome da chave da política de acesso ao Serviço de Provisionamento de Dispositivos IoT</span><span class="sxs-lookup"><span data-stu-id="2ff6f-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="2ff6f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2ff6f-122">-Name</span></span>
<span data-ttu-id="2ff6f-123">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="2ff6f-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2ff6f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ff6f-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ff6f-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2ff6f-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2ff6f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ff6f-126">-ResourceId</span></span>
<span data-ttu-id="2ff6f-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="2ff6f-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2ff6f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff6f-128">CommonParameters</span></span>
<span data-ttu-id="2ff6f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff6f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff6f-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ff6f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff6f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ff6f-131">INPUTS</span></span>

### <span data-ttu-id="2ff6f-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2ff6f-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2ff6f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2ff6f-133">System.String</span></span>

## <span data-ttu-id="2ff6f-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2ff6f-134">OUTPUTS</span></span>

### <span data-ttu-id="2ff6f-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="2ff6f-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="2ff6f-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="2ff6f-136">NOTES</span></span>

## <span data-ttu-id="2ff6f-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ff6f-137">RELATED LINKS</span></span>
