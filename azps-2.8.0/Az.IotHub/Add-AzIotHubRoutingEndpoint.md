---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 9e017f48778c36db57dd6068496a9df03d8447ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596288"
---
# <span data-ttu-id="72a70-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="72a70-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="72a70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72a70-102">SYNOPSIS</span></span>
<span data-ttu-id="72a70-103">Adicionar um ponto de extremidade ao seu hub IoT</span><span class="sxs-lookup"><span data-stu-id="72a70-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="72a70-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72a70-104">SYNTAX</span></span>

### <span data-ttu-id="72a70-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="72a70-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72a70-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="72a70-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72a70-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="72a70-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72a70-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72a70-108">DESCRIPTION</span></span>
<span data-ttu-id="72a70-109">Adicione um novo ponto de extremidade ao seu hub IoT.</span><span class="sxs-lookup"><span data-stu-id="72a70-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="72a70-110">Para saber mais sobre os pontos de extremidade que têm suporte, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="72a70-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="72a70-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72a70-111">EXAMPLES</span></span>

### <span data-ttu-id="72a70-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="72a70-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="72a70-113">Adicione um novo ponto de extremidade "E2" do tipo EventHub a um hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="72a70-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="72a70-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="72a70-114">Example 2</span></span>
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

<span data-ttu-id="72a70-115">Adicione um novo ponto de extremidade "S1" do tipo AzureStorageContainer a um hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="72a70-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="72a70-116">OS</span><span class="sxs-lookup"><span data-stu-id="72a70-116">PARAMETERS</span></span>

### <span data-ttu-id="72a70-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="72a70-117">-ConnectionString</span></span>
<span data-ttu-id="72a70-118">Cadeia de conexão do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="72a70-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="72a70-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a70-119">-DefaultProfile</span></span>
<span data-ttu-id="72a70-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="72a70-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72a70-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="72a70-121">-EndpointName</span></span>
<span data-ttu-id="72a70-122">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="72a70-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="72a70-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72a70-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="72a70-124">Grupo de recursos do recurso de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="72a70-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="72a70-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72a70-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="72a70-126">SubscriptionId do recurso de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="72a70-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="72a70-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="72a70-127">-EndpointType</span></span>
<span data-ttu-id="72a70-128">Tipo de ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="72a70-128">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="72a70-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="72a70-129">-ContainerName</span></span>
<span data-ttu-id="72a70-130">Nome do contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="72a70-130">Name of the storage container</span></span>

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

### <span data-ttu-id="72a70-131">-Encoding</span><span class="sxs-lookup"><span data-stu-id="72a70-131">-Encoding</span></span>
<span data-ttu-id="72a70-132">Selecione o formato no qual você deseja encaminhar seus dados.</span><span class="sxs-lookup"><span data-stu-id="72a70-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="72a70-133">Você pode selecionar JSON ou AVRO.</span><span class="sxs-lookup"><span data-stu-id="72a70-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="72a70-134">O padrão é definido como AVRO.</span><span class="sxs-lookup"><span data-stu-id="72a70-134">The default is set to AVRO.</span></span>

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

### <span data-ttu-id="72a70-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72a70-135">-InputObject</span></span>
<span data-ttu-id="72a70-136">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="72a70-136">IotHub Object</span></span>

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

### <span data-ttu-id="72a70-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="72a70-137">-Name</span></span>
<span data-ttu-id="72a70-138">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="72a70-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="72a70-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72a70-139">-ResourceGroupName</span></span>
<span data-ttu-id="72a70-140">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="72a70-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="72a70-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72a70-141">-ResourceId</span></span>
<span data-ttu-id="72a70-142">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="72a70-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="72a70-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="72a70-143">-Confirm</span></span>
<span data-ttu-id="72a70-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72a70-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72a70-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72a70-145">-WhatIf</span></span>
<span data-ttu-id="72a70-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="72a70-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72a70-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="72a70-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72a70-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a70-148">CommonParameters</span></span>
<span data-ttu-id="72a70-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72a70-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a70-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72a70-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a70-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72a70-151">INPUTS</span></span>

### <span data-ttu-id="72a70-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="72a70-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="72a70-153">System. String</span><span class="sxs-lookup"><span data-stu-id="72a70-153">System.String</span></span>

## <span data-ttu-id="72a70-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72a70-154">OUTPUTS</span></span>

### <span data-ttu-id="72a70-155">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="72a70-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="72a70-156">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="72a70-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="72a70-157">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="72a70-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="72a70-158">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="72a70-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="72a70-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72a70-159">NOTES</span></span>

## <span data-ttu-id="72a70-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72a70-160">RELATED LINKS</span></span>
