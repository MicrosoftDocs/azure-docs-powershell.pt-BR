---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 3982279b8698a84f23bc83aeccd25083d98363f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260563"
---
# <span data-ttu-id="6f75a-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="6f75a-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="6f75a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f75a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f75a-103">Atualize um grupo de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f75a-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="6f75a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f75a-104">SYNTAX</span></span>

### <span data-ttu-id="6f75a-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6f75a-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f75a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6f75a-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f75a-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="6f75a-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f75a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f75a-108">DESCRIPTION</span></span>
<span data-ttu-id="6f75a-109">Atualizar um grupo de inscrição em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="6f75a-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6f75a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f75a-110">EXAMPLES</span></span>

### <span data-ttu-id="6f75a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f75a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="6f75a-112">Atualize o Hub e a política de alocação para um grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="6f75a-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="6f75a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6f75a-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="6f75a-114">Atualize o estado de atualização inicial do grupo de registros.</span><span class="sxs-lookup"><span data-stu-id="6f75a-114">Update an enrollment group's initial twin state.</span></span>

## <span data-ttu-id="6f75a-115">OS</span><span class="sxs-lookup"><span data-stu-id="6f75a-115">PARAMETERS</span></span>

### <span data-ttu-id="6f75a-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="6f75a-116">-AllocationPolicy</span></span>
<span data-ttu-id="6f75a-117">Tipo de atribuição do dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="6f75a-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="6f75a-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6f75a-118">-ApiVersion</span></span>
<span data-ttu-id="6f75a-119">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="6f75a-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="6f75a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f75a-120">-DefaultProfile</span></span>
<span data-ttu-id="6f75a-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f75a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f75a-122">-Desejado</span><span class="sxs-lookup"><span data-stu-id="6f75a-122">-Desired</span></span>
<span data-ttu-id="6f75a-123">Propriedades desejadas de a "a) inicial.</span><span class="sxs-lookup"><span data-stu-id="6f75a-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="6f75a-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="6f75a-124">-DpsName</span></span>
<span data-ttu-id="6f75a-125">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="6f75a-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6f75a-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="6f75a-126">-DpsObject</span></span>
<span data-ttu-id="6f75a-127">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="6f75a-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="6f75a-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="6f75a-128">-EdgeEnabled</span></span>
<span data-ttu-id="6f75a-129">Sinalizador que indica a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="6f75a-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="6f75a-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="6f75a-130">-IotHub</span></span>
<span data-ttu-id="6f75a-131">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="6f75a-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="6f75a-132">Use a lista separada por espaços para vários hubs IoT.</span><span class="sxs-lookup"><span data-stu-id="6f75a-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="6f75a-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="6f75a-133">-IotHubHostName</span></span>
<span data-ttu-id="6f75a-134">Nome do host do Hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="6f75a-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="6f75a-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f75a-135">-Name</span></span>
<span data-ttu-id="6f75a-136">Nome do grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="6f75a-136">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="6f75a-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="6f75a-137">-ProvisioningStatus</span></span>
<span data-ttu-id="6f75a-138">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="6f75a-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="6f75a-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="6f75a-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="6f75a-140">Dados do dispositivo a serem manuseados no reprovisionamento para um hub IOT diferente.</span><span class="sxs-lookup"><span data-stu-id="6f75a-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="6f75a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f75a-141">-ResourceGroupName</span></span>
<span data-ttu-id="6f75a-142">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6f75a-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6f75a-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f75a-143">-ResourceId</span></span>
<span data-ttu-id="6f75a-144">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="6f75a-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="6f75a-145">-Marca</span><span class="sxs-lookup"><span data-stu-id="6f75a-145">-Tag</span></span>
<span data-ttu-id="6f75a-146">Rótulos de rótulos de cima iniciais.</span><span class="sxs-lookup"><span data-stu-id="6f75a-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="6f75a-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="6f75a-147">-WebhookUrl</span></span>
<span data-ttu-id="6f75a-148">A URL do webhook usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6f75a-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="6f75a-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6f75a-149">-Confirm</span></span>
<span data-ttu-id="6f75a-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f75a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f75a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f75a-151">-WhatIf</span></span>
<span data-ttu-id="6f75a-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6f75a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f75a-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6f75a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f75a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f75a-154">CommonParameters</span></span>
<span data-ttu-id="6f75a-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f75a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f75a-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f75a-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f75a-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f75a-157">INPUTS</span></span>

### <span data-ttu-id="6f75a-158">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="6f75a-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="6f75a-159">System. String</span><span class="sxs-lookup"><span data-stu-id="6f75a-159">System.String</span></span>

## <span data-ttu-id="6f75a-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f75a-160">OUTPUTS</span></span>

### <span data-ttu-id="6f75a-161">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="6f75a-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="6f75a-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f75a-162">NOTES</span></span>

## <span data-ttu-id="6f75a-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f75a-163">RELATED LINKS</span></span>
