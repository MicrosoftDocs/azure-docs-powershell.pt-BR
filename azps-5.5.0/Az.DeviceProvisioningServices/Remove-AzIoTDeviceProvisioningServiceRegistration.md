---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: b0fa84887a54eb1f4e9c689c49fb08a1300cd62b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115811"
---
# <span data-ttu-id="43650-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="43650-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="43650-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43650-102">SYNOPSIS</span></span>
<span data-ttu-id="43650-103">Exclui o registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43650-103">Deletes the device registration.</span></span>

## <span data-ttu-id="43650-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43650-104">SYNTAX</span></span>

### <span data-ttu-id="43650-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="43650-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43650-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="43650-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43650-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="43650-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43650-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="43650-108">DESCRIPTION</span></span>
<span data-ttu-id="43650-109">Exclua um registro de dispositivo em um Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="43650-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="43650-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="43650-110">EXAMPLES</span></span>

### <span data-ttu-id="43650-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43650-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="43650-112">Exclua um registro de dispositivo em um Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="43650-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="43650-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43650-113">PARAMETERS</span></span>

### <span data-ttu-id="43650-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43650-114">-DefaultProfile</span></span>
<span data-ttu-id="43650-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43650-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43650-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="43650-116">-DpsName</span></span>
<span data-ttu-id="43650-117">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="43650-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="43650-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="43650-118">-DpsObject</span></span>
<span data-ttu-id="43650-119">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="43650-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="43650-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43650-120">-PassThru</span></span>
<span data-ttu-id="43650-121">Permite retornar o objeto boolano.</span><span class="sxs-lookup"><span data-stu-id="43650-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="43650-122">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="43650-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43650-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="43650-123">-RegistrationId</span></span>
<span data-ttu-id="43650-124">ID do registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43650-124">ID of device registration.</span></span>

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

### <span data-ttu-id="43650-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43650-125">-ResourceGroupName</span></span>
<span data-ttu-id="43650-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="43650-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="43650-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43650-127">-ResourceId</span></span>
<span data-ttu-id="43650-128">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="43650-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="43650-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="43650-129">-Confirm</span></span>
<span data-ttu-id="43650-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43650-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43650-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43650-131">-WhatIf</span></span>
<span data-ttu-id="43650-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="43650-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43650-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43650-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43650-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43650-134">CommonParameters</span></span>
<span data-ttu-id="43650-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43650-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43650-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43650-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43650-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="43650-137">INPUTS</span></span>

### <span data-ttu-id="43650-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="43650-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="43650-139">System.String</span><span class="sxs-lookup"><span data-stu-id="43650-139">System.String</span></span>

## <span data-ttu-id="43650-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="43650-140">OUTPUTS</span></span>

### <span data-ttu-id="43650-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43650-141">System.Boolean</span></span>

## <span data-ttu-id="43650-142">Notas</span><span class="sxs-lookup"><span data-stu-id="43650-142">NOTES</span></span>

## <span data-ttu-id="43650-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43650-143">RELATED LINKS</span></span>
