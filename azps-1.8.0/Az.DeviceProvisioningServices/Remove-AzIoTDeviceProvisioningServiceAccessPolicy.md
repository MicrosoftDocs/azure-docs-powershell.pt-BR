---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 1efd429489be41f619454fd2b772c7cbb1ebc5c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600917"
---
# <span data-ttu-id="9861a-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9861a-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="9861a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9861a-102">SYNOPSIS</span></span>
<span data-ttu-id="9861a-103">Excluir uma política de acesso compartilhado em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="9861a-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="9861a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9861a-104">SYNTAX</span></span>

### <span data-ttu-id="9861a-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9861a-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9861a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9861a-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9861a-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="9861a-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9861a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9861a-108">DESCRIPTION</span></span>
<span data-ttu-id="9861a-109">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="9861a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="9861a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9861a-110">EXAMPLES</span></span>

### <span data-ttu-id="9861a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9861a-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="9861a-112">Excluir a política de acesso compartilhado "MyPolicy" em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="9861a-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="9861a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9861a-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="9861a-114">Excluir a política de acesso compartilhado "MyPolicy" em um serviço de provisionamento de dispositivo Hub do Azure IoT usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="9861a-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="9861a-115">OS</span><span class="sxs-lookup"><span data-stu-id="9861a-115">PARAMETERS</span></span>

### <span data-ttu-id="9861a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9861a-116">-DefaultProfile</span></span>
<span data-ttu-id="9861a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9861a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9861a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9861a-118">-InputObject</span></span>
<span data-ttu-id="9861a-119">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="9861a-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9861a-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9861a-120">-KeyName</span></span>
<span data-ttu-id="9861a-121">Nome da chave da política de acesso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="9861a-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="9861a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9861a-122">-Name</span></span>
<span data-ttu-id="9861a-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="9861a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9861a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9861a-124">-PassThru</span></span>
<span data-ttu-id="9861a-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="9861a-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9861a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9861a-126">-ResourceGroupName</span></span>
<span data-ttu-id="9861a-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9861a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9861a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9861a-128">-ResourceId</span></span>
<span data-ttu-id="9861a-129">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="9861a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9861a-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9861a-130">-Confirm</span></span>
<span data-ttu-id="9861a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9861a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9861a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9861a-132">-WhatIf</span></span>
<span data-ttu-id="9861a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9861a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9861a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9861a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9861a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9861a-135">CommonParameters</span></span>
<span data-ttu-id="9861a-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9861a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9861a-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9861a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9861a-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9861a-138">INPUTS</span></span>

### <span data-ttu-id="9861a-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="9861a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="9861a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9861a-140">System.String</span></span>

## <span data-ttu-id="9861a-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9861a-141">OUTPUTS</span></span>

### <span data-ttu-id="9861a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9861a-142">System.Boolean</span></span>

## <span data-ttu-id="9861a-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9861a-143">NOTES</span></span>

## <span data-ttu-id="9861a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9861a-144">RELATED LINKS</span></span>
