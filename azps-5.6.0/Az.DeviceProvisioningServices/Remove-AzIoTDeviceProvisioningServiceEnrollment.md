---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: edf3845d9c4ac8a836212895fce2e5bbf4e40570
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889546"
---
# <span data-ttu-id="e3c58-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="e3c58-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="e3c58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3c58-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c58-103">Excluir um registro de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3c58-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="e3c58-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e3c58-104">SYNTAX</span></span>

### <span data-ttu-id="e3c58-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e3c58-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3c58-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e3c58-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3c58-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e3c58-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3c58-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e3c58-108">DESCRIPTION</span></span>
<span data-ttu-id="e3c58-109">Exclua um registro de dispositivo em um Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e3c58-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="e3c58-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3c58-110">EXAMPLES</span></span>

### <span data-ttu-id="e3c58-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3c58-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="e3c58-112">Exclua um registro de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="e3c58-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="e3c58-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e3c58-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="e3c58-114">Exclua todos os registros de registro.</span><span class="sxs-lookup"><span data-stu-id="e3c58-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="e3c58-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e3c58-115">PARAMETERS</span></span>

### <span data-ttu-id="e3c58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c58-116">-DefaultProfile</span></span>
<span data-ttu-id="e3c58-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c58-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3c58-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="e3c58-118">-DpsName</span></span>
<span data-ttu-id="e3c58-119">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="e3c58-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e3c58-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="e3c58-120">-DpsObject</span></span>
<span data-ttu-id="e3c58-121">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="e3c58-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="e3c58-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3c58-122">-PassThru</span></span>
<span data-ttu-id="e3c58-123">Permite retornar o objeto booleano.</span><span class="sxs-lookup"><span data-stu-id="e3c58-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="e3c58-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e3c58-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3c58-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="e3c58-125">-RegistrationId</span></span>
<span data-ttu-id="e3c58-126">ID de registro de registro individual.</span><span class="sxs-lookup"><span data-stu-id="e3c58-126">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="e3c58-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c58-127">-ResourceGroupName</span></span>
<span data-ttu-id="e3c58-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e3c58-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e3c58-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3c58-129">-ResourceId</span></span>
<span data-ttu-id="e3c58-130">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="e3c58-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="e3c58-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3c58-131">-Confirm</span></span>
<span data-ttu-id="e3c58-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3c58-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3c58-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3c58-133">-WhatIf</span></span>
<span data-ttu-id="e3c58-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3c58-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3c58-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3c58-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3c58-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c58-136">CommonParameters</span></span>
<span data-ttu-id="e3c58-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c58-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c58-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3c58-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c58-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3c58-139">INPUTS</span></span>

### <span data-ttu-id="e3c58-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="e3c58-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="e3c58-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e3c58-141">System.String</span></span>

## <span data-ttu-id="e3c58-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e3c58-142">OUTPUTS</span></span>

### <span data-ttu-id="e3c58-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3c58-143">System.Boolean</span></span>

## <span data-ttu-id="e3c58-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="e3c58-144">NOTES</span></span>

## <span data-ttu-id="e3c58-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3c58-145">RELATED LINKS</span></span>
