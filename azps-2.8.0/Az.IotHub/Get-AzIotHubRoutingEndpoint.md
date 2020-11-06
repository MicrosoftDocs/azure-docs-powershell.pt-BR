---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8852139cfcedc5ff0ee42c234c44b1505042ef1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596267"
---
# <span data-ttu-id="e5c13-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5c13-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="e5c13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5c13-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c13-103">Obter informações sobre todos os pontos de extremidade para o seu hub IoT</span><span class="sxs-lookup"><span data-stu-id="e5c13-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="e5c13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5c13-104">SYNTAX</span></span>

### <span data-ttu-id="e5c13-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e5c13-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c13-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e5c13-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c13-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="e5c13-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5c13-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5c13-108">DESCRIPTION</span></span>
<span data-ttu-id="e5c13-109">Obter informações sobre o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="e5c13-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="e5c13-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5c13-110">EXAMPLES</span></span>

### <span data-ttu-id="e5c13-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e5c13-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="e5c13-112">Obtenha todos os pontos de extremidade do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="e5c13-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="e5c13-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e5c13-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="e5c13-114">Obtenha todos os pontos de extremidade do tipo EventHub do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="e5c13-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="e5c13-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e5c13-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="e5c13-116">Obtenha todos os pontos de extremidade do tipo EventHub do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="e5c13-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="e5c13-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="e5c13-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="e5c13-118">Obter informações de ponto de extremidade do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="e5c13-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="e5c13-119">OS</span><span class="sxs-lookup"><span data-stu-id="e5c13-119">PARAMETERS</span></span>

### <span data-ttu-id="e5c13-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c13-120">-DefaultProfile</span></span>
<span data-ttu-id="e5c13-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c13-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5c13-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e5c13-122">-EndpointName</span></span>
<span data-ttu-id="e5c13-123">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="e5c13-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="e5c13-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="e5c13-124">-EndpointType</span></span>
<span data-ttu-id="e5c13-125">Tipo de ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="e5c13-125">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5c13-126">-InputObject</span></span>
<span data-ttu-id="e5c13-127">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c13-127">IotHub Object</span></span>

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

### <span data-ttu-id="e5c13-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5c13-128">-Name</span></span>
<span data-ttu-id="e5c13-129">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="e5c13-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e5c13-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c13-130">-ResourceGroupName</span></span>
<span data-ttu-id="e5c13-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e5c13-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e5c13-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c13-132">-ResourceId</span></span>
<span data-ttu-id="e5c13-133">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c13-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e5c13-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c13-134">CommonParameters</span></span>
<span data-ttu-id="e5c13-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c13-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c13-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c13-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c13-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5c13-137">INPUTS</span></span>

### <span data-ttu-id="e5c13-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e5c13-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e5c13-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e5c13-139">System.String</span></span>

## <span data-ttu-id="e5c13-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5c13-140">OUTPUTS</span></span>

### <span data-ttu-id="e5c13-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5c13-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="e5c13-142">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubProperties, Microsoft. Azure. PowerShell. cmdlets. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e5c13-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e5c13-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5c13-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="e5c13-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="e5c13-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="e5c13-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5c13-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="e5c13-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="e5c13-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="e5c13-147">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5c13-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="e5c13-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerProperties []</span><span class="sxs-lookup"><span data-stu-id="e5c13-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="e5c13-149">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingCustomEndpoint []</span><span class="sxs-lookup"><span data-stu-id="e5c13-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="e5c13-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5c13-150">NOTES</span></span>

## <span data-ttu-id="e5c13-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5c13-151">RELATED LINKS</span></span>
