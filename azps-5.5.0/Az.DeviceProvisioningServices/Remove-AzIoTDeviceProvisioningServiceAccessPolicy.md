---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 5f4cfe702b975bf69098aa3c002c756b5cf3da78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116820"
---
# <span data-ttu-id="c3093-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c3093-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="c3093-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3093-102">SYNOPSIS</span></span>
<span data-ttu-id="c3093-103">Exclua políticas de acesso compartilhado em um serviço de provisionamento de dispositivos do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="c3093-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c3093-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3093-104">SYNTAX</span></span>

### <span data-ttu-id="c3093-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c3093-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3093-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3093-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3093-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c3093-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3093-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3093-108">DESCRIPTION</span></span>
<span data-ttu-id="c3093-109">Para uma introdução ao Serviço de Provisionamento de Dispositivo do Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="c3093-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c3093-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c3093-110">EXAMPLES</span></span>

### <span data-ttu-id="c3093-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3093-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="c3093-112">Exclua a política de acesso compartilhado "mypolicy" em um serviço de provisionamento de dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="c3093-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="c3093-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c3093-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="c3093-114">Exclua a política de acesso compartilhado "mypolicy" em um serviço de provisionamento de dispositivo do Hub do Azure IoT usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3093-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="c3093-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3093-115">PARAMETERS</span></span>

### <span data-ttu-id="c3093-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3093-116">-DefaultProfile</span></span>
<span data-ttu-id="c3093-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3093-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3093-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3093-118">-InputObject</span></span>
<span data-ttu-id="c3093-119">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="c3093-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c3093-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c3093-120">-KeyName</span></span>
<span data-ttu-id="c3093-121">Nome da chave da política de acesso do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="c3093-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="c3093-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3093-122">-Name</span></span>
<span data-ttu-id="c3093-123">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="c3093-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c3093-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3093-124">-PassThru</span></span>
<span data-ttu-id="c3093-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c3093-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c3093-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3093-126">-ResourceGroupName</span></span>
<span data-ttu-id="c3093-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c3093-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c3093-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3093-128">-ResourceId</span></span>
<span data-ttu-id="c3093-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="c3093-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c3093-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c3093-130">-Confirm</span></span>
<span data-ttu-id="c3093-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3093-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3093-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3093-132">-WhatIf</span></span>
<span data-ttu-id="c3093-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c3093-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3093-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3093-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3093-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3093-135">CommonParameters</span></span>
<span data-ttu-id="c3093-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3093-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3093-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3093-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3093-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="c3093-138">INPUTS</span></span>

### <span data-ttu-id="c3093-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="c3093-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="c3093-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c3093-140">System.String</span></span>

## <span data-ttu-id="c3093-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="c3093-141">OUTPUTS</span></span>

### <span data-ttu-id="c3093-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c3093-142">System.Boolean</span></span>

## <span data-ttu-id="c3093-143">Notas</span><span class="sxs-lookup"><span data-stu-id="c3093-143">NOTES</span></span>

## <span data-ttu-id="c3093-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3093-144">RELATED LINKS</span></span>
