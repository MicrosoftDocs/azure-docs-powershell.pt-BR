---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 47c5c5119e41f3feeaccda66871d902e631c9ac2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259087"
---
# <span data-ttu-id="be400-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="be400-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="be400-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be400-102">SYNOPSIS</span></span>
<span data-ttu-id="be400-103">Atualize um registro de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be400-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="be400-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be400-104">SYNTAX</span></span>

### <span data-ttu-id="be400-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="be400-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be400-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="be400-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be400-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="be400-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be400-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be400-108">DESCRIPTION</span></span>
<span data-ttu-id="be400-109">Atualizar um registro de dispositivo em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="be400-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="be400-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be400-110">EXAMPLES</span></span>

### <span data-ttu-id="be400-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="be400-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="be400-112">Atualize os hubs e diretivas de alocação para um registro de inscrição.</span><span class="sxs-lookup"><span data-stu-id="be400-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="be400-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="be400-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="be400-114">Atualize o estado inicial de uma inscrição.</span><span class="sxs-lookup"><span data-stu-id="be400-114">Update an enrollment's initial twin state.</span></span>

## <span data-ttu-id="be400-115">OS</span><span class="sxs-lookup"><span data-stu-id="be400-115">PARAMETERS</span></span>

### <span data-ttu-id="be400-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="be400-116">-AllocationPolicy</span></span>
<span data-ttu-id="be400-117">Tipo de atribuição do dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="be400-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="be400-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="be400-118">-ApiVersion</span></span>
<span data-ttu-id="be400-119">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="be400-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="be400-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be400-120">-DefaultProfile</span></span>
<span data-ttu-id="be400-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be400-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be400-122">-Desejado</span><span class="sxs-lookup"><span data-stu-id="be400-122">-Desired</span></span>
<span data-ttu-id="be400-123">Propriedades desejadas de a "a) inicial.</span><span class="sxs-lookup"><span data-stu-id="be400-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="be400-124">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="be400-124">-DeviceId</span></span>
<span data-ttu-id="be400-125">ID do dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="be400-125">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="be400-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="be400-126">-DpsName</span></span>
<span data-ttu-id="be400-127">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="be400-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="be400-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="be400-128">-DpsObject</span></span>
<span data-ttu-id="be400-129">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="be400-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="be400-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="be400-130">-EdgeEnabled</span></span>
<span data-ttu-id="be400-131">Sinalizador que indica a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="be400-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="be400-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="be400-132">-IotHub</span></span>
<span data-ttu-id="be400-133">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="be400-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="be400-134">Use a lista separada por espaços para vários hubs IoT.</span><span class="sxs-lookup"><span data-stu-id="be400-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="be400-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="be400-135">-IotHubHostName</span></span>
<span data-ttu-id="be400-136">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="be400-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="be400-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="be400-137">-ProvisioningStatus</span></span>
<span data-ttu-id="be400-138">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="be400-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="be400-139">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="be400-139">-RegistrationId</span></span>
<span data-ttu-id="be400-140">ID de registro de inscrição individual.</span><span class="sxs-lookup"><span data-stu-id="be400-140">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="be400-141">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="be400-141">-ReprovisionPolicy</span></span>
<span data-ttu-id="be400-142">Dados do dispositivo a serem manuseados no reprovisionamento para um hub IOT diferente.</span><span class="sxs-lookup"><span data-stu-id="be400-142">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="be400-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be400-143">-ResourceGroupName</span></span>
<span data-ttu-id="be400-144">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="be400-144">Name of the Resource Group</span></span>

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

### <span data-ttu-id="be400-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be400-145">-ResourceId</span></span>
<span data-ttu-id="be400-146">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="be400-146">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="be400-147">-Marca</span><span class="sxs-lookup"><span data-stu-id="be400-147">-Tag</span></span>
<span data-ttu-id="be400-148">Rótulos de rótulos de cima iniciais.</span><span class="sxs-lookup"><span data-stu-id="be400-148">Initial twin tags.</span></span>

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

### <span data-ttu-id="be400-149">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="be400-149">-WebhookUrl</span></span>
<span data-ttu-id="be400-150">A URL do webhook usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="be400-150">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="be400-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="be400-151">-Confirm</span></span>
<span data-ttu-id="be400-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be400-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be400-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be400-153">-WhatIf</span></span>
<span data-ttu-id="be400-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be400-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be400-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be400-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be400-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be400-156">CommonParameters</span></span>
<span data-ttu-id="be400-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be400-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be400-158">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be400-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be400-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be400-159">INPUTS</span></span>

### <span data-ttu-id="be400-160">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="be400-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="be400-161">System. String</span><span class="sxs-lookup"><span data-stu-id="be400-161">System.String</span></span>

## <span data-ttu-id="be400-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be400-162">OUTPUTS</span></span>

### <span data-ttu-id="be400-163">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="be400-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="be400-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be400-164">NOTES</span></span>

## <span data-ttu-id="be400-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be400-165">RELATED LINKS</span></span>
