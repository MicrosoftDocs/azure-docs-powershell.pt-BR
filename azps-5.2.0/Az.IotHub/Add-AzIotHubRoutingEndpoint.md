---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 2af7a4518d551509089585877f74468510746dcd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260503"
---
# <span data-ttu-id="11443-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="11443-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="11443-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11443-102">SYNOPSIS</span></span>
<span data-ttu-id="11443-103">Adicionar um ponto de extremidade ao seu hub IoT</span><span class="sxs-lookup"><span data-stu-id="11443-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="11443-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11443-104">SYNTAX</span></span>

### <span data-ttu-id="11443-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="11443-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11443-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11443-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11443-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="11443-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11443-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11443-108">DESCRIPTION</span></span>
<span data-ttu-id="11443-109">Adicione um novo ponto de extremidade ao seu hub IoT.</span><span class="sxs-lookup"><span data-stu-id="11443-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="11443-110">Para saber mais sobre os pontos de extremidade que têm suporte, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="11443-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="11443-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11443-111">EXAMPLES</span></span>

### <span data-ttu-id="11443-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11443-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="11443-113">Adicione um novo ponto de extremidade "E2" do tipo EventHub a um hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="11443-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="11443-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="11443-114">Example 2</span></span>
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

<span data-ttu-id="11443-115">Adicione um novo ponto de extremidade "S1" do tipo AzureStorageContainer a um hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="11443-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="11443-116">OS</span><span class="sxs-lookup"><span data-stu-id="11443-116">PARAMETERS</span></span>

### <span data-ttu-id="11443-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="11443-117">-ConnectionString</span></span>
<span data-ttu-id="11443-118">Cadeia de conexão do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="11443-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="11443-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11443-119">-DefaultProfile</span></span>
<span data-ttu-id="11443-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11443-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11443-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="11443-121">-EndpointName</span></span>
<span data-ttu-id="11443-122">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="11443-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="11443-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11443-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="11443-124">Grupo de recursos do recurso de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="11443-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="11443-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11443-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="11443-126">SubscriptionId do recurso de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="11443-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="11443-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="11443-127">-EndpointType</span></span>
<span data-ttu-id="11443-128">Tipo de ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="11443-128">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="11443-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="11443-129">-ContainerName</span></span>
<span data-ttu-id="11443-130">Nome do contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="11443-130">Name of the storage container</span></span>

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

### <span data-ttu-id="11443-131">-Encoding</span><span class="sxs-lookup"><span data-stu-id="11443-131">-Encoding</span></span>
<span data-ttu-id="11443-132">Selecione o formato no qual você deseja encaminhar seus dados.</span><span class="sxs-lookup"><span data-stu-id="11443-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="11443-133">Você pode selecionar JSON ou AVRO.</span><span class="sxs-lookup"><span data-stu-id="11443-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="11443-134">O padrão é definido como AVRO.</span><span class="sxs-lookup"><span data-stu-id="11443-134">The default is set to AVRO.</span></span>

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

### <span data-ttu-id="11443-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11443-135">-InputObject</span></span>
<span data-ttu-id="11443-136">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="11443-136">IotHub Object</span></span>

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

### <span data-ttu-id="11443-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="11443-137">-Name</span></span>
<span data-ttu-id="11443-138">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="11443-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="11443-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11443-139">-ResourceGroupName</span></span>
<span data-ttu-id="11443-140">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="11443-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="11443-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11443-141">-ResourceId</span></span>
<span data-ttu-id="11443-142">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="11443-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="11443-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="11443-143">-Confirm</span></span>
<span data-ttu-id="11443-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11443-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11443-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11443-145">-WhatIf</span></span>
<span data-ttu-id="11443-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11443-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11443-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11443-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11443-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11443-148">CommonParameters</span></span>
<span data-ttu-id="11443-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11443-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11443-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11443-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11443-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11443-151">INPUTS</span></span>

### <span data-ttu-id="11443-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="11443-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="11443-153">System. String</span><span class="sxs-lookup"><span data-stu-id="11443-153">System.String</span></span>

## <span data-ttu-id="11443-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11443-154">OUTPUTS</span></span>

### <span data-ttu-id="11443-155">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="11443-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="11443-156">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="11443-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="11443-157">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="11443-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="11443-158">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="11443-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="11443-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11443-159">NOTES</span></span>

## <span data-ttu-id="11443-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11443-160">RELATED LINKS</span></span>
