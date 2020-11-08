---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: e7b0a5296147408633316ed27f0cba87a65d3a2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115490"
---
# <span data-ttu-id="65d5e-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="65d5e-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="65d5e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="65d5e-103">Atualize um grupo de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="65d5e-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="65d5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65d5e-104">SYNTAX</span></span>

### <span data-ttu-id="65d5e-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="65d5e-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d5e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="65d5e-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d5e-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="65d5e-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65d5e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65d5e-108">DESCRIPTION</span></span>
<span data-ttu-id="65d5e-109">Atualizar um grupo de inscrição em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="65d5e-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="65d5e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65d5e-110">EXAMPLES</span></span>

### <span data-ttu-id="65d5e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65d5e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="65d5e-112">Atualize o Hub e a política de alocação para um grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="65d5e-112">Update allocation policy and hubs for an enrollment group.</span></span>

## <span data-ttu-id="65d5e-113">OS</span><span class="sxs-lookup"><span data-stu-id="65d5e-113">PARAMETERS</span></span>

### <span data-ttu-id="65d5e-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="65d5e-114">-AllocationPolicy</span></span>
<span data-ttu-id="65d5e-115">Tipo de atribuição do dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="65d5e-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="65d5e-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="65d5e-116">-ApiVersion</span></span>
<span data-ttu-id="65d5e-117">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="65d5e-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="65d5e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d5e-118">-DefaultProfile</span></span>
<span data-ttu-id="65d5e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65d5e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d5e-120">-Desejado</span><span class="sxs-lookup"><span data-stu-id="65d5e-120">-Desired</span></span>
<span data-ttu-id="65d5e-121">Propriedades desejadas de a "a) inicial.</span><span class="sxs-lookup"><span data-stu-id="65d5e-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="65d5e-122">-DpsName</span><span class="sxs-lookup"><span data-stu-id="65d5e-122">-DpsName</span></span>
<span data-ttu-id="65d5e-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="65d5e-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="65d5e-124">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="65d5e-124">-DpsObject</span></span>
<span data-ttu-id="65d5e-125">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="65d5e-125">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="65d5e-126">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="65d5e-126">-EdgeEnabled</span></span>
<span data-ttu-id="65d5e-127">Sinalizador que indica a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="65d5e-127">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="65d5e-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="65d5e-128">-IotHub</span></span>
<span data-ttu-id="65d5e-129">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="65d5e-129">Host name of target IoT Hub.</span></span>
<span data-ttu-id="65d5e-130">Use a lista separada por espaços para vários hubs IoT.</span><span class="sxs-lookup"><span data-stu-id="65d5e-130">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="65d5e-131">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="65d5e-131">-IotHubHostName</span></span>
<span data-ttu-id="65d5e-132">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="65d5e-132">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="65d5e-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="65d5e-133">-Name</span></span>
<span data-ttu-id="65d5e-134">Nome do grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="65d5e-134">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="65d5e-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="65d5e-135">-ProvisioningStatus</span></span>
<span data-ttu-id="65d5e-136">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="65d5e-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="65d5e-137">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="65d5e-137">-ReprovisionPolicy</span></span>
<span data-ttu-id="65d5e-138">Dados do dispositivo a serem manuseados no reprovisionamento para um hub IOT diferente.</span><span class="sxs-lookup"><span data-stu-id="65d5e-138">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="65d5e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d5e-139">-ResourceGroupName</span></span>
<span data-ttu-id="65d5e-140">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="65d5e-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="65d5e-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65d5e-141">-ResourceId</span></span>
<span data-ttu-id="65d5e-142">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="65d5e-142">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="65d5e-143">-Marca</span><span class="sxs-lookup"><span data-stu-id="65d5e-143">-Tag</span></span>
<span data-ttu-id="65d5e-144">Rótulos de rótulos de cima iniciais.</span><span class="sxs-lookup"><span data-stu-id="65d5e-144">Initial twin tags.</span></span>

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

### <span data-ttu-id="65d5e-145">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="65d5e-145">-WebhookUrl</span></span>
<span data-ttu-id="65d5e-146">A URL do webhook usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="65d5e-146">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="65d5e-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="65d5e-147">-Confirm</span></span>
<span data-ttu-id="65d5e-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65d5e-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d5e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d5e-149">-WhatIf</span></span>
<span data-ttu-id="65d5e-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65d5e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d5e-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65d5e-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d5e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d5e-152">CommonParameters</span></span>
<span data-ttu-id="65d5e-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65d5e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d5e-154">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d5e-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d5e-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65d5e-155">INPUTS</span></span>

### <span data-ttu-id="65d5e-156">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="65d5e-156">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="65d5e-157">System. String</span><span class="sxs-lookup"><span data-stu-id="65d5e-157">System.String</span></span>

## <span data-ttu-id="65d5e-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65d5e-158">OUTPUTS</span></span>

### <span data-ttu-id="65d5e-159">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="65d5e-159">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="65d5e-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65d5e-160">NOTES</span></span>

## <span data-ttu-id="65d5e-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65d5e-161">RELATED LINKS</span></span>
