---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 87c6bdd72229baec8e65c40d4e2e4309bde59aba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116823"
---
# <span data-ttu-id="90b2e-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="90b2e-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="90b2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="90b2e-103">Liste todos os detalhes das políticas de acesso compartilhado em um serviço de provisionamento de dispositivos do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="90b2e-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="90b2e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90b2e-104">SYNTAX</span></span>

### <span data-ttu-id="90b2e-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="90b2e-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90b2e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="90b2e-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90b2e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="90b2e-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90b2e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="90b2e-108">DESCRIPTION</span></span>
<span data-ttu-id="90b2e-109">Para uma introdução ao Serviço de Provisionamento de Dispositivo do Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="90b2e-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="90b2e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="90b2e-110">EXAMPLES</span></span>

### <span data-ttu-id="90b2e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="90b2e-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="90b2e-112">Liste todas as políticas de acesso compartilhado em "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="90b2e-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="90b2e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="90b2e-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="90b2e-114">Mostrar detalhes da política de acesso compartilhado "mypolicy" em um serviço de provisionamento de dispositivos do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="90b2e-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="90b2e-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90b2e-115">PARAMETERS</span></span>

### <span data-ttu-id="90b2e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b2e-116">-DefaultProfile</span></span>
<span data-ttu-id="90b2e-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90b2e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90b2e-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="90b2e-118">-DpsObject</span></span>
<span data-ttu-id="90b2e-119">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="90b2e-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="90b2e-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="90b2e-120">-KeyName</span></span>
<span data-ttu-id="90b2e-121">Nome da chave da política de acesso do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="90b2e-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="90b2e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="90b2e-122">-Name</span></span>
<span data-ttu-id="90b2e-123">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="90b2e-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="90b2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90b2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="90b2e-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="90b2e-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="90b2e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90b2e-126">-ResourceId</span></span>
<span data-ttu-id="90b2e-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="90b2e-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="90b2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b2e-128">CommonParameters</span></span>
<span data-ttu-id="90b2e-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90b2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b2e-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90b2e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b2e-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="90b2e-131">INPUTS</span></span>

### <span data-ttu-id="90b2e-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="90b2e-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="90b2e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="90b2e-133">System.String</span></span>

## <span data-ttu-id="90b2e-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="90b2e-134">OUTPUTS</span></span>

### <span data-ttu-id="90b2e-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="90b2e-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="90b2e-136">Notas</span><span class="sxs-lookup"><span data-stu-id="90b2e-136">NOTES</span></span>

## <span data-ttu-id="90b2e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90b2e-137">RELATED LINKS</span></span>
