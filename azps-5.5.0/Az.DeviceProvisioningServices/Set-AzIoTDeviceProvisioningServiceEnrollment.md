---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 47c5c5119e41f3feeaccda66871d902e631c9ac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115339"
---
# <span data-ttu-id="0f488-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="0f488-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="0f488-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f488-102">SYNOPSIS</span></span>
<span data-ttu-id="0f488-103">Atualizar um registro de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0f488-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="0f488-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f488-104">SYNTAX</span></span>

### <span data-ttu-id="0f488-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0f488-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f488-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0f488-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f488-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0f488-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f488-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f488-108">DESCRIPTION</span></span>
<span data-ttu-id="0f488-109">Atualizar um registro de dispositivo em um Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="0f488-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="0f488-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0f488-110">EXAMPLES</span></span>

### <span data-ttu-id="0f488-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f488-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="0f488-112">Atualize a política de alocação e os hubs para um registro de registro.</span><span class="sxs-lookup"><span data-stu-id="0f488-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="0f488-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0f488-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="0f488-114">Atualize o estado inicial do registro.</span><span class="sxs-lookup"><span data-stu-id="0f488-114">Update an enrollment's initial twin state.</span></span>

## <span data-ttu-id="0f488-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f488-115">PARAMETERS</span></span>

### <span data-ttu-id="0f488-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0f488-116">-AllocationPolicy</span></span>
<span data-ttu-id="0f488-117">Tipo de alocação do dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="0f488-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="0f488-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0f488-118">-ApiVersion</span></span>
<span data-ttu-id="0f488-119">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="0f488-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="0f488-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f488-120">-DefaultProfile</span></span>
<span data-ttu-id="0f488-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f488-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f488-122">-Desejado</span><span class="sxs-lookup"><span data-stu-id="0f488-122">-Desired</span></span>
<span data-ttu-id="0f488-123">Propriedades iniciais desejadas.</span><span class="sxs-lookup"><span data-stu-id="0f488-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="0f488-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="0f488-124">-DeviceId</span></span>
<span data-ttu-id="0f488-125">ID do dispositivo IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="0f488-125">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="0f488-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="0f488-126">-DpsName</span></span>
<span data-ttu-id="0f488-127">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="0f488-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0f488-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="0f488-128">-DpsObject</span></span>
<span data-ttu-id="0f488-129">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="0f488-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0f488-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="0f488-130">-EdgeEnabled</span></span>
<span data-ttu-id="0f488-131">Sinalizador indicando a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="0f488-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="0f488-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="0f488-132">-IotHub</span></span>
<span data-ttu-id="0f488-133">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="0f488-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="0f488-134">Use uma lista separada por espaço para vários Hubs de IoT.</span><span class="sxs-lookup"><span data-stu-id="0f488-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="0f488-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="0f488-135">-IotHubHostName</span></span>
<span data-ttu-id="0f488-136">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="0f488-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="0f488-137">-ProvisionandoStatus</span><span class="sxs-lookup"><span data-stu-id="0f488-137">-ProvisioningStatus</span></span>
<span data-ttu-id="0f488-138">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="0f488-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="0f488-139">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="0f488-139">-RegistrationId</span></span>
<span data-ttu-id="0f488-140">ID do registro individual.</span><span class="sxs-lookup"><span data-stu-id="0f488-140">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="0f488-141">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="0f488-141">-ReprovisionPolicy</span></span>
<span data-ttu-id="0f488-142">Dados do dispositivo a serem tratados na provisionamento de novo para o Hub Iot diferente.</span><span class="sxs-lookup"><span data-stu-id="0f488-142">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="0f488-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f488-143">-ResourceGroupName</span></span>
<span data-ttu-id="0f488-144">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="0f488-144">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0f488-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f488-145">-ResourceId</span></span>
<span data-ttu-id="0f488-146">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="0f488-146">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0f488-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f488-147">-Tag</span></span>
<span data-ttu-id="0f488-148">Marcas iniciais de brilho.</span><span class="sxs-lookup"><span data-stu-id="0f488-148">Initial twin tags.</span></span>

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

### <span data-ttu-id="0f488-149">-WebçãoUrl</span><span class="sxs-lookup"><span data-stu-id="0f488-149">-WebhookUrl</span></span>
<span data-ttu-id="0f488-150">A URL web url usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="0f488-150">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="0f488-151">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0f488-151">-Confirm</span></span>
<span data-ttu-id="0f488-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f488-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f488-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f488-153">-WhatIf</span></span>
<span data-ttu-id="0f488-154">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0f488-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f488-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f488-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f488-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f488-156">CommonParameters</span></span>
<span data-ttu-id="0f488-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f488-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f488-158">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f488-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f488-159">Entradas</span><span class="sxs-lookup"><span data-stu-id="0f488-159">INPUTS</span></span>

### <span data-ttu-id="0f488-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0f488-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="0f488-161">System.String</span><span class="sxs-lookup"><span data-stu-id="0f488-161">System.String</span></span>

## <span data-ttu-id="0f488-162">Saídas</span><span class="sxs-lookup"><span data-stu-id="0f488-162">OUTPUTS</span></span>

### <span data-ttu-id="0f488-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="0f488-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="0f488-164">Notas</span><span class="sxs-lookup"><span data-stu-id="0f488-164">NOTES</span></span>

## <span data-ttu-id="0f488-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f488-165">RELATED LINKS</span></span>
