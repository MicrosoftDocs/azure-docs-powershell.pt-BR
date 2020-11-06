---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: b3a813623ed11a64a23dc35afe2f81c3f5de61da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431965"
---
# <span data-ttu-id="885aa-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="885aa-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="885aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="885aa-102">SYNOPSIS</span></span>
<span data-ttu-id="885aa-103">Excluir uma política de acesso compartilhado em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="885aa-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="885aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="885aa-104">SYNTAX</span></span>

### <span data-ttu-id="885aa-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="885aa-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="885aa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="885aa-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="885aa-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="885aa-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="885aa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="885aa-108">DESCRIPTION</span></span>
<span data-ttu-id="885aa-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="885aa-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="885aa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="885aa-110">EXAMPLES</span></span>

### <span data-ttu-id="885aa-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="885aa-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="885aa-112">Excluir a política de acesso compartilhado "MyPolicy" em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="885aa-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="885aa-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="885aa-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzureRmIoTDpsAccessPolicy
```

<span data-ttu-id="885aa-114">Excluir a política de acesso compartilhado "MyPolicy" em um serviço de provisionamento de dispositivo Hub do Azure IoT usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="885aa-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="885aa-115">OS</span><span class="sxs-lookup"><span data-stu-id="885aa-115">PARAMETERS</span></span>

### <span data-ttu-id="885aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="885aa-116">-DefaultProfile</span></span>
<span data-ttu-id="885aa-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="885aa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="885aa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="885aa-118">-InputObject</span></span>
<span data-ttu-id="885aa-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="885aa-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="885aa-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="885aa-120">-KeyName</span></span>
<span data-ttu-id="885aa-121">Nome da chave da política de acesso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="885aa-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="885aa-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="885aa-122">-Name</span></span>
<span data-ttu-id="885aa-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="885aa-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="885aa-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="885aa-124">-PassThru</span></span>
<span data-ttu-id="885aa-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="885aa-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="885aa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="885aa-126">-ResourceGroupName</span></span>
<span data-ttu-id="885aa-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="885aa-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="885aa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="885aa-128">-ResourceId</span></span>
<span data-ttu-id="885aa-129">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="885aa-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="885aa-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="885aa-130">-Confirm</span></span>
<span data-ttu-id="885aa-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="885aa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="885aa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="885aa-132">-WhatIf</span></span>
<span data-ttu-id="885aa-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="885aa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="885aa-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="885aa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="885aa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="885aa-135">CommonParameters</span></span>
<span data-ttu-id="885aa-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="885aa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="885aa-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="885aa-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="885aa-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="885aa-138">INPUTS</span></span>

### <span data-ttu-id="885aa-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="885aa-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="885aa-140">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="885aa-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="885aa-141">System. String</span><span class="sxs-lookup"><span data-stu-id="885aa-141">System.String</span></span>

## <span data-ttu-id="885aa-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="885aa-142">OUTPUTS</span></span>

### <span data-ttu-id="885aa-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="885aa-143">System.Boolean</span></span>

## <span data-ttu-id="885aa-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="885aa-144">NOTES</span></span>

## <span data-ttu-id="885aa-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="885aa-145">RELATED LINKS</span></span>
