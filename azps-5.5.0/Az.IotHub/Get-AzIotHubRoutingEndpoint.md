---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8b3d139d822452231451a1f07907ac20cdf3589c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113768"
---
# <span data-ttu-id="cbbb4-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="cbbb4-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="cbbb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbbb4-102">SYNOPSIS</span></span>
<span data-ttu-id="cbbb4-103">Obter informações sobre todos os pontos de extremidade do Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="cbbb4-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="cbbb4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbbb4-104">SYNTAX</span></span>

### <span data-ttu-id="cbbb4-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cbbb4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbbb4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cbbb4-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbbb4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cbbb4-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbbb4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbbb4-108">DESCRIPTION</span></span>
<span data-ttu-id="cbbb4-109">Obter informações sobre o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="cbbb4-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="cbbb4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cbbb4-110">EXAMPLES</span></span>

### <span data-ttu-id="cbbb4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cbbb4-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="cbbb4-112">Obter todos os pontos de extremidade do Hub de IoT do "myiothub".</span><span class="sxs-lookup"><span data-stu-id="cbbb4-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="cbbb4-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cbbb4-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="cbbb4-114">Obter todos os pontos de extremidade do tipo EventHub no Hub de IoT do "myiothub".</span><span class="sxs-lookup"><span data-stu-id="cbbb4-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="cbbb4-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="cbbb4-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="cbbb4-116">Obter todos os pontos de extremidade do tipo EventHub no Hub de IoT do "myiothub".</span><span class="sxs-lookup"><span data-stu-id="cbbb4-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="cbbb4-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="cbbb4-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="cbbb4-118">Obter informações de ponto de extremidade do Hub de IoT do "myiothub".</span><span class="sxs-lookup"><span data-stu-id="cbbb4-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="cbbb4-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbbb4-119">PARAMETERS</span></span>

### <span data-ttu-id="cbbb4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbbb4-120">-DefaultProfile</span></span>
<span data-ttu-id="cbbb4-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbbb4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbbb4-122">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="cbbb4-122">-EndpointName</span></span>
<span data-ttu-id="cbbb4-123">Nome do Ponto de Extremidade de Roteamento</span><span class="sxs-lookup"><span data-stu-id="cbbb4-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="cbbb4-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="cbbb4-124">-EndpointType</span></span>
<span data-ttu-id="cbbb4-125">Tipo do Ponto de Extremidade de Roteamento</span><span class="sxs-lookup"><span data-stu-id="cbbb4-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="cbbb4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbbb4-126">-InputObject</span></span>
<span data-ttu-id="cbbb4-127">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="cbbb4-127">IotHub Object</span></span>

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

### <span data-ttu-id="cbbb4-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbbb4-128">-Name</span></span>
<span data-ttu-id="cbbb4-129">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="cbbb4-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cbbb4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbbb4-130">-ResourceGroupName</span></span>
<span data-ttu-id="cbbb4-131">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="cbbb4-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cbbb4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbbb4-132">-ResourceId</span></span>
<span data-ttu-id="cbbb4-133">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="cbbb4-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cbbb4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbbb4-134">CommonParameters</span></span>
<span data-ttu-id="cbbb4-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbbb4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbbb4-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbbb4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbbb4-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="cbbb4-137">INPUTS</span></span>

### <span data-ttu-id="cbbb4-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cbbb4-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cbbb4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cbbb4-139">System.String</span></span>

## <span data-ttu-id="cbbb4-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="cbbb4-140">OUTPUTS</span></span>

### <span data-ttu-id="cbbb4-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="cbbb4-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="cbbb4-142">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0,0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="cbbb4-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cbbb4-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="cbbb4-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="cbbb4-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="cbbb4-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="cbbb4-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="cbbb4-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="cbbb4-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="cbbb4-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="cbbb4-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cbbb4-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="cbbb4-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span><span class="sxs-lookup"><span data-stu-id="cbbb4-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="cbbb4-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span><span class="sxs-lookup"><span data-stu-id="cbbb4-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="cbbb4-150">Notas</span><span class="sxs-lookup"><span data-stu-id="cbbb4-150">NOTES</span></span>

## <span data-ttu-id="cbbb4-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbbb4-151">RELATED LINKS</span></span>
