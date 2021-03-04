---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: f72aa2ab648de33baaf50e181afa98e12ac921a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889541"
---
# <span data-ttu-id="6a860-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="6a860-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="6a860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a860-102">SYNOPSIS</span></span>
<span data-ttu-id="6a860-103">Exclui o registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a860-103">Deletes the device registration.</span></span>

## <span data-ttu-id="6a860-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6a860-104">SYNTAX</span></span>

### <span data-ttu-id="6a860-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6a860-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a860-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6a860-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a860-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6a860-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a860-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6a860-108">DESCRIPTION</span></span>
<span data-ttu-id="6a860-109">Exclua um registro de dispositivo em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="6a860-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6a860-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a860-110">EXAMPLES</span></span>

### <span data-ttu-id="6a860-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6a860-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="6a860-112">Exclua um registro de dispositivo em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="6a860-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6a860-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6a860-113">PARAMETERS</span></span>

### <span data-ttu-id="6a860-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a860-114">-DefaultProfile</span></span>
<span data-ttu-id="6a860-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a860-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a860-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="6a860-116">-DpsName</span></span>
<span data-ttu-id="6a860-117">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="6a860-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6a860-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="6a860-118">-DpsObject</span></span>
<span data-ttu-id="6a860-119">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="6a860-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="6a860-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a860-120">-PassThru</span></span>
<span data-ttu-id="6a860-121">Permite retornar o objeto booleano.</span><span class="sxs-lookup"><span data-stu-id="6a860-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="6a860-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="6a860-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6a860-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="6a860-123">-RegistrationId</span></span>
<span data-ttu-id="6a860-124">ID do registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a860-124">ID of device registration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a860-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a860-125">-ResourceGroupName</span></span>
<span data-ttu-id="6a860-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="6a860-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6a860-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a860-127">-ResourceId</span></span>
<span data-ttu-id="6a860-128">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="6a860-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="6a860-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a860-129">-Confirm</span></span>
<span data-ttu-id="6a860-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a860-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a860-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a860-131">-WhatIf</span></span>
<span data-ttu-id="6a860-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6a860-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a860-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6a860-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a860-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a860-134">CommonParameters</span></span>
<span data-ttu-id="6a860-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a860-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a860-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a860-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a860-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a860-137">INPUTS</span></span>

### <span data-ttu-id="6a860-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="6a860-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="6a860-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6a860-139">System.String</span></span>

## <span data-ttu-id="6a860-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6a860-140">OUTPUTS</span></span>

### <span data-ttu-id="6a860-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a860-141">System.Boolean</span></span>

## <span data-ttu-id="6a860-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="6a860-142">NOTES</span></span>

## <span data-ttu-id="6a860-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a860-143">RELATED LINKS</span></span>
