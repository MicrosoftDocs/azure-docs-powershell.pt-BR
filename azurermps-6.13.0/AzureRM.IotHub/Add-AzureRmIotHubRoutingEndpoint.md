---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: d251d3159111437cd06880a49069aee7aca6d80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429527"
---
# <span data-ttu-id="af002-101">Add-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="af002-101">Add-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="af002-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af002-102">SYNOPSIS</span></span>
<span data-ttu-id="af002-103">Adicionar um ponto de extremidade ao seu hub IoT</span><span class="sxs-lookup"><span data-stu-id="af002-103">Add an endpoint to your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af002-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af002-104">SYNTAX</span></span>

### <span data-ttu-id="af002-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="af002-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af002-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="af002-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af002-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="af002-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af002-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af002-108">DESCRIPTION</span></span>
<span data-ttu-id="af002-109">Adicione um novo ponto de extremidade ao seu hub IoT.</span><span class="sxs-lookup"><span data-stu-id="af002-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="af002-110">Para saber mais sobre os pontos de extremidade que têm suporte, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="af002-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="af002-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af002-111">EXAMPLES</span></span>

### <span data-ttu-id="af002-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af002-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="af002-113">Adicione um novo ponto de extremidade "E2" do tipo EventHub a um hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="af002-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="af002-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="af002-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : avro
```

<span data-ttu-id="af002-115">Adicione um novo ponto de extremidade "S1" do tipo AzureStorageContainer a um hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="af002-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="af002-116">OS</span><span class="sxs-lookup"><span data-stu-id="af002-116">PARAMETERS</span></span>

### <span data-ttu-id="af002-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="af002-117">-ConnectionString</span></span>
<span data-ttu-id="af002-118">Cadeia de conexão do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="af002-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af002-119">-DefaultProfile</span></span>
<span data-ttu-id="af002-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af002-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="af002-121">-EndpointName</span></span>
<span data-ttu-id="af002-122">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="af002-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="af002-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="af002-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="af002-124">Grupo de recursos do ponto de extremidade nivelamento</span><span class="sxs-lookup"><span data-stu-id="af002-124">Resource group of the Endpoint resoure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af002-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="af002-126">SubscriptionId do recurso de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="af002-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="af002-127">-EndpointType</span></span>
<span data-ttu-id="af002-128">Tipo de ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="af002-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af002-129">-InputObject</span></span>
<span data-ttu-id="af002-130">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="af002-130">IotHub Object</span></span>

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

### <span data-ttu-id="af002-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="af002-131">-Name</span></span>
<span data-ttu-id="af002-132">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="af002-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="af002-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af002-133">-ResourceGroupName</span></span>
<span data-ttu-id="af002-134">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="af002-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="af002-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af002-135">-ResourceId</span></span>
<span data-ttu-id="af002-136">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="af002-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="af002-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af002-137">-Confirm</span></span>
<span data-ttu-id="af002-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af002-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af002-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af002-139">-WhatIf</span></span>
<span data-ttu-id="af002-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af002-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af002-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af002-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af002-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af002-142">CommonParameters</span></span>
<span data-ttu-id="af002-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af002-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af002-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af002-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af002-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af002-145">INPUTS</span></span>

### <span data-ttu-id="af002-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="af002-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="af002-147">System. String</span><span class="sxs-lookup"><span data-stu-id="af002-147">System.String</span></span>

## <span data-ttu-id="af002-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af002-148">OUTPUTS</span></span>

### <span data-ttu-id="af002-149">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="af002-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="af002-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="af002-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="af002-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af002-151">NOTES</span></span>

## <span data-ttu-id="af002-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af002-152">RELATED LINKS</span></span>
