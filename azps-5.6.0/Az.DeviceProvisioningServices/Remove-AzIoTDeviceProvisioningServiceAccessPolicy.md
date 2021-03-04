---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: a39604b21b8a754ede78fb789f71c3b653320fa7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889278"
---
# <span data-ttu-id="cddfd-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cddfd-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="cddfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cddfd-102">SYNOPSIS</span></span>
<span data-ttu-id="cddfd-103">Exclua políticas de acesso compartilhado em um serviço de provisionamento de dispositivos do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="cddfd-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="cddfd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cddfd-104">SYNTAX</span></span>

### <span data-ttu-id="cddfd-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cddfd-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cddfd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cddfd-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddfd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cddfd-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cddfd-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cddfd-108">DESCRIPTION</span></span>
<span data-ttu-id="cddfd-109">Para uma introdução ao Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="cddfd-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="cddfd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cddfd-110">EXAMPLES</span></span>

### <span data-ttu-id="cddfd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cddfd-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="cddfd-112">Exclua a política de acesso compartilhado "mypolicy" em um serviço de provisionamento de dispositivo do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="cddfd-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="cddfd-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cddfd-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="cddfd-114">Exclua a política de acesso compartilhado "mypolicy" em um serviço de provisionamento de dispositivo do Azure IoT Hub usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="cddfd-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="cddfd-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cddfd-115">PARAMETERS</span></span>

### <span data-ttu-id="cddfd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cddfd-116">-DefaultProfile</span></span>
<span data-ttu-id="cddfd-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cddfd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cddfd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cddfd-118">-InputObject</span></span>
<span data-ttu-id="cddfd-119">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="cddfd-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="cddfd-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="cddfd-120">-KeyName</span></span>
<span data-ttu-id="cddfd-121">Nome da chave da política de acesso ao Serviço de Provisionamento de Dispositivos IoT</span><span class="sxs-lookup"><span data-stu-id="cddfd-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="cddfd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cddfd-122">-Name</span></span>
<span data-ttu-id="cddfd-123">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="cddfd-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="cddfd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cddfd-124">-PassThru</span></span>
<span data-ttu-id="cddfd-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cddfd-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cddfd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cddfd-126">-ResourceGroupName</span></span>
<span data-ttu-id="cddfd-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="cddfd-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cddfd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cddfd-128">-ResourceId</span></span>
<span data-ttu-id="cddfd-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="cddfd-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="cddfd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cddfd-130">-Confirm</span></span>
<span data-ttu-id="cddfd-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cddfd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cddfd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cddfd-132">-WhatIf</span></span>
<span data-ttu-id="cddfd-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cddfd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cddfd-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cddfd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cddfd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cddfd-135">CommonParameters</span></span>
<span data-ttu-id="cddfd-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cddfd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cddfd-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cddfd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cddfd-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cddfd-138">INPUTS</span></span>

### <span data-ttu-id="cddfd-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="cddfd-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="cddfd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cddfd-140">System.String</span></span>

## <span data-ttu-id="cddfd-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cddfd-141">OUTPUTS</span></span>

### <span data-ttu-id="cddfd-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cddfd-142">System.Boolean</span></span>

## <span data-ttu-id="cddfd-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="cddfd-143">NOTES</span></span>

## <span data-ttu-id="cddfd-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cddfd-144">RELATED LINKS</span></span>
