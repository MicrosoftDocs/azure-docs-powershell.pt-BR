---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8a81df2081420f8d218e094ff43f22e8dd9cc5c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113611"
---
# <span data-ttu-id="2f1eb-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="2f1eb-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="2f1eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f1eb-102">SYNOPSIS</span></span>
<span data-ttu-id="2f1eb-103">Atualize um registro de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="2f1eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f1eb-104">SYNTAX</span></span>

### <span data-ttu-id="2f1eb-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f1eb-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f1eb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2f1eb-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f1eb-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="2f1eb-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f1eb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f1eb-108">DESCRIPTION</span></span>
<span data-ttu-id="2f1eb-109">Atualizar um registro de dispositivo em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="2f1eb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f1eb-110">EXAMPLES</span></span>

### <span data-ttu-id="2f1eb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f1eb-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="2f1eb-112">Atualize os hubs e diretivas de alocação para um registro de inscrição.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-112">Update allocation policy and hubs for an enrollment record.</span></span>

## <span data-ttu-id="2f1eb-113">OS</span><span class="sxs-lookup"><span data-stu-id="2f1eb-113">PARAMETERS</span></span>

### <span data-ttu-id="2f1eb-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="2f1eb-114">-AllocationPolicy</span></span>
<span data-ttu-id="2f1eb-115">Tipo de atribuição do dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-115">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f1eb-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2f1eb-116">-ApiVersion</span></span>
<span data-ttu-id="2f1eb-117">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="2f1eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f1eb-118">-DefaultProfile</span></span>
<span data-ttu-id="2f1eb-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f1eb-120">-Desejado</span><span class="sxs-lookup"><span data-stu-id="2f1eb-120">-Desired</span></span>
<span data-ttu-id="2f1eb-121">Propriedades desejadas de a "a) inicial.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-121">Initial twin desired properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f1eb-122">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="2f1eb-122">-DeviceId</span></span>
<span data-ttu-id="2f1eb-123">ID do dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-123">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="2f1eb-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="2f1eb-124">-DpsName</span></span>
<span data-ttu-id="2f1eb-125">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="2f1eb-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2f1eb-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2f1eb-126">-DpsObject</span></span>
<span data-ttu-id="2f1eb-127">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="2f1eb-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2f1eb-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="2f1eb-128">-EdgeEnabled</span></span>
<span data-ttu-id="2f1eb-129">Sinalizador que indica a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-129">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f1eb-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="2f1eb-130">-IotHub</span></span>
<span data-ttu-id="2f1eb-131">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="2f1eb-132">Use a lista separada por espaços para vários hubs IoT.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-132">Use space-separated list for multiple IoT Hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f1eb-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="2f1eb-133">-IotHubHostName</span></span>
<span data-ttu-id="2f1eb-134">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="2f1eb-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="2f1eb-135">-ProvisioningStatus</span></span>
<span data-ttu-id="2f1eb-136">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-136">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f1eb-137">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="2f1eb-137">-RegistrationId</span></span>
<span data-ttu-id="2f1eb-138">ID de registro de inscrição individual.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-138">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="2f1eb-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="2f1eb-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="2f1eb-140">Dados do dispositivo a serem manuseados no reprovisionamento para um hub IOT diferente.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f1eb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f1eb-141">-ResourceGroupName</span></span>
<span data-ttu-id="2f1eb-142">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2f1eb-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2f1eb-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f1eb-143">-ResourceId</span></span>
<span data-ttu-id="2f1eb-144">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="2f1eb-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2f1eb-145">-Marca</span><span class="sxs-lookup"><span data-stu-id="2f1eb-145">-Tag</span></span>
<span data-ttu-id="2f1eb-146">Rótulos de rótulos de cima iniciais.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-146">Initial twin tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f1eb-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="2f1eb-147">-WebhookUrl</span></span>
<span data-ttu-id="2f1eb-148">A URL do webhook usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="2f1eb-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2f1eb-149">-Confirm</span></span>
<span data-ttu-id="2f1eb-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f1eb-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f1eb-151">-WhatIf</span></span>
<span data-ttu-id="2f1eb-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f1eb-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f1eb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f1eb-154">CommonParameters</span></span>
<span data-ttu-id="2f1eb-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f1eb-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f1eb-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f1eb-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f1eb-157">INPUTS</span></span>

### <span data-ttu-id="2f1eb-158">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2f1eb-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2f1eb-159">System. String</span><span class="sxs-lookup"><span data-stu-id="2f1eb-159">System.String</span></span>

## <span data-ttu-id="2f1eb-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f1eb-160">OUTPUTS</span></span>

### <span data-ttu-id="2f1eb-161">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="2f1eb-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="2f1eb-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f1eb-162">NOTES</span></span>

## <span data-ttu-id="2f1eb-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f1eb-163">RELATED LINKS</span></span>
