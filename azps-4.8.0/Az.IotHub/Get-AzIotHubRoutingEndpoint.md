---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8b3d139d822452231451a1f07907ac20cdf3589c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112734"
---
# <span data-ttu-id="4e139-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e139-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="4e139-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e139-102">SYNOPSIS</span></span>
<span data-ttu-id="4e139-103">Obter informações sobre todos os pontos de extremidade para o seu hub IoT</span><span class="sxs-lookup"><span data-stu-id="4e139-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="4e139-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e139-104">SYNTAX</span></span>

### <span data-ttu-id="4e139-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4e139-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e139-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4e139-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e139-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="4e139-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e139-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e139-108">DESCRIPTION</span></span>
<span data-ttu-id="4e139-109">Obter informações sobre o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="4e139-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="4e139-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e139-110">EXAMPLES</span></span>

### <span data-ttu-id="4e139-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4e139-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="4e139-112">Obtenha todos os pontos de extremidade do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="4e139-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="4e139-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4e139-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="4e139-114">Obtenha todos os pontos de extremidade do tipo EventHub do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="4e139-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="4e139-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4e139-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="4e139-116">Obtenha todos os pontos de extremidade do tipo EventHub do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="4e139-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="4e139-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="4e139-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="4e139-118">Obter informações de ponto de extremidade do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="4e139-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="4e139-119">OS</span><span class="sxs-lookup"><span data-stu-id="4e139-119">PARAMETERS</span></span>

### <span data-ttu-id="4e139-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e139-120">-DefaultProfile</span></span>
<span data-ttu-id="4e139-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e139-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e139-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4e139-122">-EndpointName</span></span>
<span data-ttu-id="4e139-123">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="4e139-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="4e139-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="4e139-124">-EndpointType</span></span>
<span data-ttu-id="4e139-125">Tipo de ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="4e139-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="4e139-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e139-126">-InputObject</span></span>
<span data-ttu-id="4e139-127">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="4e139-127">IotHub Object</span></span>

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

### <span data-ttu-id="4e139-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e139-128">-Name</span></span>
<span data-ttu-id="4e139-129">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="4e139-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4e139-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e139-130">-ResourceGroupName</span></span>
<span data-ttu-id="4e139-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4e139-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4e139-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e139-132">-ResourceId</span></span>
<span data-ttu-id="4e139-133">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="4e139-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4e139-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e139-134">CommonParameters</span></span>
<span data-ttu-id="4e139-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e139-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e139-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e139-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e139-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e139-137">INPUTS</span></span>

### <span data-ttu-id="4e139-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4e139-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4e139-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4e139-139">System.String</span></span>

## <span data-ttu-id="4e139-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e139-140">OUTPUTS</span></span>

### <span data-ttu-id="4e139-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e139-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="4e139-142">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubProperties, Microsoft. Azure. PowerShell. cmdlets. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4e139-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4e139-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e139-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="4e139-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="4e139-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="4e139-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e139-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="4e139-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="4e139-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="4e139-147">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e139-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="4e139-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerProperties []</span><span class="sxs-lookup"><span data-stu-id="4e139-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="4e139-149">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingCustomEndpoint []</span><span class="sxs-lookup"><span data-stu-id="4e139-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="4e139-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e139-150">NOTES</span></span>

## <span data-ttu-id="4e139-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e139-151">RELATED LINKS</span></span>
