---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 2af7a4518d551509089585877f74468510746dcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113776"
---
# <span data-ttu-id="4ae18-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ae18-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="4ae18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ae18-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae18-103">Adicionar um ponto de extremidade ao hub de IoT</span><span class="sxs-lookup"><span data-stu-id="4ae18-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="4ae18-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ae18-104">SYNTAX</span></span>

### <span data-ttu-id="4ae18-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4ae18-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ae18-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ae18-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ae18-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ae18-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ae18-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ae18-108">DESCRIPTION</span></span>
<span data-ttu-id="4ae18-109">Adicione um novo ponto de extremidade ao Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="4ae18-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="4ae18-110">Para saber mais sobre os pontos de extremidade com suporte, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="4ae18-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="4ae18-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4ae18-111">EXAMPLES</span></span>

### <span data-ttu-id="4ae18-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ae18-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="4ae18-113">Adicione um novo ponto de extremidade "E2" do tipo EventHub a um Hub de IoT do "myiothub".</span><span class="sxs-lookup"><span data-stu-id="4ae18-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="4ae18-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4ae18-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container -Encoding json

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : json
```

<span data-ttu-id="4ae18-115">Adicione um novo ponto de extremidade "S1" do tipo AzureStorageContainer a um Hub de IoT do "myiothub".</span><span class="sxs-lookup"><span data-stu-id="4ae18-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="4ae18-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ae18-116">PARAMETERS</span></span>

### <span data-ttu-id="4ae18-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="4ae18-117">-ConnectionString</span></span>
<span data-ttu-id="4ae18-118">Cadeia de conexão do Ponto de Extremidade de Roteamento</span><span class="sxs-lookup"><span data-stu-id="4ae18-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="4ae18-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae18-119">-DefaultProfile</span></span>
<span data-ttu-id="4ae18-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ae18-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ae18-121">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="4ae18-121">-EndpointName</span></span>
<span data-ttu-id="4ae18-122">Nome do Ponto de Extremidade de Roteamento</span><span class="sxs-lookup"><span data-stu-id="4ae18-122">Name of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae18-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4ae18-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="4ae18-124">Grupo de recursos do recurso Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="4ae18-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="4ae18-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ae18-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="4ae18-126">SubscriptionId do recurso Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="4ae18-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="4ae18-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="4ae18-127">-EndpointType</span></span>
<span data-ttu-id="4ae18-128">Tipo do Ponto de Extremidade de Roteamento</span><span class="sxs-lookup"><span data-stu-id="4ae18-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae18-129">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="4ae18-129">-ContainerName</span></span>
<span data-ttu-id="4ae18-130">Nome do contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4ae18-130">Name of the storage container</span></span>

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

### <span data-ttu-id="4ae18-131">-Codificação</span><span class="sxs-lookup"><span data-stu-id="4ae18-131">-Encoding</span></span>
<span data-ttu-id="4ae18-132">Selecione o formato no qual você deseja rotear seus dados.</span><span class="sxs-lookup"><span data-stu-id="4ae18-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="4ae18-133">Você pode selecionar JSON ou AVRO.</span><span class="sxs-lookup"><span data-stu-id="4ae18-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="4ae18-134">O padrão é definido como AVRO.</span><span class="sxs-lookup"><span data-stu-id="4ae18-134">The default is set to AVRO.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:
Accepted values: JSON, AVRO

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae18-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ae18-135">-InputObject</span></span>
<span data-ttu-id="4ae18-136">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="4ae18-136">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae18-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ae18-137">-Name</span></span>
<span data-ttu-id="4ae18-138">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="4ae18-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4ae18-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae18-139">-ResourceGroupName</span></span>
<span data-ttu-id="4ae18-140">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="4ae18-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4ae18-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ae18-141">-ResourceId</span></span>
<span data-ttu-id="4ae18-142">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="4ae18-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4ae18-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4ae18-143">-Confirm</span></span>
<span data-ttu-id="4ae18-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ae18-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ae18-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ae18-145">-WhatIf</span></span>
<span data-ttu-id="4ae18-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4ae18-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ae18-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ae18-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ae18-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae18-148">CommonParameters</span></span>
<span data-ttu-id="4ae18-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ae18-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae18-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ae18-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae18-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="4ae18-151">INPUTS</span></span>

### <span data-ttu-id="4ae18-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4ae18-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4ae18-153">System.String</span><span class="sxs-lookup"><span data-stu-id="4ae18-153">System.String</span></span>

## <span data-ttu-id="4ae18-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="4ae18-154">OUTPUTS</span></span>

### <span data-ttu-id="4ae18-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ae18-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="4ae18-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ae18-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="4ae18-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ae18-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="4ae18-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ae18-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="4ae18-159">Notas</span><span class="sxs-lookup"><span data-stu-id="4ae18-159">NOTES</span></span>

## <span data-ttu-id="4ae18-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ae18-160">RELATED LINKS</span></span>
