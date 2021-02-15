---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 3982279b8698a84f23bc83aeccd25083d98363f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115336"
---
# <span data-ttu-id="190ef-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="190ef-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="190ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="190ef-102">SYNOPSIS</span></span>
<span data-ttu-id="190ef-103">Atualizar um grupo de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="190ef-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="190ef-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="190ef-104">SYNTAX</span></span>

### <span data-ttu-id="190ef-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="190ef-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="190ef-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="190ef-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="190ef-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="190ef-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="190ef-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="190ef-108">DESCRIPTION</span></span>
<span data-ttu-id="190ef-109">Atualizar um grupo de inscrição em um Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="190ef-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="190ef-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="190ef-110">EXAMPLES</span></span>

### <span data-ttu-id="190ef-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="190ef-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="190ef-112">Atualize a política de alocação e os hubs de um grupo de inscrição.</span><span class="sxs-lookup"><span data-stu-id="190ef-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="190ef-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="190ef-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="190ef-114">Atualize o estado inicial do grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="190ef-114">Update an enrollment group's initial twin state.</span></span>

## <span data-ttu-id="190ef-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="190ef-115">PARAMETERS</span></span>

### <span data-ttu-id="190ef-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="190ef-116">-AllocationPolicy</span></span>
<span data-ttu-id="190ef-117">Tipo de alocação do dispositivo atribuído ao Hub.</span><span class="sxs-lookup"><span data-stu-id="190ef-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="190ef-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="190ef-118">-ApiVersion</span></span>
<span data-ttu-id="190ef-119">A versão da API do serviço de provisionamento na solicitação de alocação personalizada.</span><span class="sxs-lookup"><span data-stu-id="190ef-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="190ef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="190ef-120">-DefaultProfile</span></span>
<span data-ttu-id="190ef-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="190ef-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="190ef-122">-Desejado</span><span class="sxs-lookup"><span data-stu-id="190ef-122">-Desired</span></span>
<span data-ttu-id="190ef-123">Propriedades iniciais desejadas.</span><span class="sxs-lookup"><span data-stu-id="190ef-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="190ef-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="190ef-124">-DpsName</span></span>
<span data-ttu-id="190ef-125">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="190ef-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="190ef-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="190ef-126">-DpsObject</span></span>
<span data-ttu-id="190ef-127">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="190ef-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="190ef-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="190ef-128">-EdgeEnabled</span></span>
<span data-ttu-id="190ef-129">Sinalizador indicando a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="190ef-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="190ef-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="190ef-130">-IotHub</span></span>
<span data-ttu-id="190ef-131">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="190ef-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="190ef-132">Use uma lista separada por espaço para vários Hubs de IoT.</span><span class="sxs-lookup"><span data-stu-id="190ef-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="190ef-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="190ef-133">-IotHubHostName</span></span>
<span data-ttu-id="190ef-134">Nome do host do Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="190ef-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="190ef-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="190ef-135">-Name</span></span>
<span data-ttu-id="190ef-136">Nome do grupo de inscrição.</span><span class="sxs-lookup"><span data-stu-id="190ef-136">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="190ef-137">-ProvisionandoStatus</span><span class="sxs-lookup"><span data-stu-id="190ef-137">-ProvisioningStatus</span></span>
<span data-ttu-id="190ef-138">Habilitar ou desabilitar a entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="190ef-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="190ef-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="190ef-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="190ef-140">Dados do dispositivo a serem tratados na provisionamento de novo para o Hub Iot diferente.</span><span class="sxs-lookup"><span data-stu-id="190ef-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="190ef-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="190ef-141">-ResourceGroupName</span></span>
<span data-ttu-id="190ef-142">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="190ef-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="190ef-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="190ef-143">-ResourceId</span></span>
<span data-ttu-id="190ef-144">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="190ef-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="190ef-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="190ef-145">-Tag</span></span>
<span data-ttu-id="190ef-146">Marcas iniciais de brilho.</span><span class="sxs-lookup"><span data-stu-id="190ef-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="190ef-147">-WebçãoUrl</span><span class="sxs-lookup"><span data-stu-id="190ef-147">-WebhookUrl</span></span>
<span data-ttu-id="190ef-148">A URL web url usada para solicitações de alocação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="190ef-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="190ef-149">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="190ef-149">-Confirm</span></span>
<span data-ttu-id="190ef-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="190ef-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="190ef-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="190ef-151">-WhatIf</span></span>
<span data-ttu-id="190ef-152">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="190ef-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="190ef-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="190ef-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="190ef-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="190ef-154">CommonParameters</span></span>
<span data-ttu-id="190ef-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="190ef-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="190ef-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="190ef-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="190ef-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="190ef-157">INPUTS</span></span>

### <span data-ttu-id="190ef-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="190ef-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="190ef-159">System.String</span><span class="sxs-lookup"><span data-stu-id="190ef-159">System.String</span></span>

## <span data-ttu-id="190ef-160">Saídas</span><span class="sxs-lookup"><span data-stu-id="190ef-160">OUTPUTS</span></span>

### <span data-ttu-id="190ef-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="190ef-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="190ef-162">Notas</span><span class="sxs-lookup"><span data-stu-id="190ef-162">NOTES</span></span>

## <span data-ttu-id="190ef-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="190ef-163">RELATED LINKS</span></span>
