---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 6caad4faec3dd292f902689757b82b90091afcde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440408"
---
# <span data-ttu-id="25b52-101">Remove-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="25b52-101">Remove-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="25b52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25b52-102">SYNOPSIS</span></span>
<span data-ttu-id="25b52-103">Excluir um ponto de extremidade para o seu hub IoT</span><span class="sxs-lookup"><span data-stu-id="25b52-103">Delete an endpoint for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25b52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25b52-104">SYNTAX</span></span>

### <span data-ttu-id="25b52-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="25b52-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25b52-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="25b52-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25b52-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="25b52-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25b52-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25b52-108">DESCRIPTION</span></span>
<span data-ttu-id="25b52-109">Excluir um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="25b52-109">Delete an endpoint.</span></span> <span data-ttu-id="25b52-110">Lembre-se de excluir qualquer rota que use esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="25b52-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="25b52-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25b52-111">EXAMPLES</span></span>

### <span data-ttu-id="25b52-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="25b52-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="25b52-113">Exclua o ponto de extremidade "E2" do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="25b52-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="25b52-114">OS</span><span class="sxs-lookup"><span data-stu-id="25b52-114">PARAMETERS</span></span>

### <span data-ttu-id="25b52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b52-115">-DefaultProfile</span></span>
<span data-ttu-id="25b52-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25b52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25b52-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="25b52-117">-EndpointName</span></span>
<span data-ttu-id="25b52-118">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="25b52-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="25b52-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="25b52-119">-EndpointType</span></span>
<span data-ttu-id="25b52-120">Tipo de ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="25b52-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b52-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25b52-121">-InputObject</span></span>
<span data-ttu-id="25b52-122">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="25b52-122">IotHub Object</span></span>

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

### <span data-ttu-id="25b52-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="25b52-123">-Name</span></span>
<span data-ttu-id="25b52-124">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="25b52-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="25b52-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25b52-125">-PassThru</span></span>
<span data-ttu-id="25b52-126">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="25b52-126">Allows to return the boolean object.</span></span> <span data-ttu-id="25b52-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="25b52-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b52-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b52-128">-ResourceGroupName</span></span>
<span data-ttu-id="25b52-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="25b52-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="25b52-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25b52-130">-ResourceId</span></span>
<span data-ttu-id="25b52-131">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="25b52-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="25b52-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="25b52-132">-Confirm</span></span>
<span data-ttu-id="25b52-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25b52-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25b52-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25b52-134">-WhatIf</span></span>
<span data-ttu-id="25b52-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25b52-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25b52-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25b52-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25b52-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b52-137">CommonParameters</span></span>
<span data-ttu-id="25b52-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b52-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b52-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25b52-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b52-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25b52-140">INPUTS</span></span>

### <span data-ttu-id="25b52-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="25b52-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="25b52-142">System. String</span><span class="sxs-lookup"><span data-stu-id="25b52-142">System.String</span></span>

## <span data-ttu-id="25b52-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25b52-143">OUTPUTS</span></span>

### <span data-ttu-id="25b52-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="25b52-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="25b52-145">System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint System. Collections. Collections. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="25b52-145">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="25b52-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25b52-146">NOTES</span></span>

## <span data-ttu-id="25b52-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25b52-147">RELATED LINKS</span></span>
