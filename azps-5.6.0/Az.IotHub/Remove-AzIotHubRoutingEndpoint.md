---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 1b14ce37d03e1840336696792493e30701a09bfe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891355"
---
# <span data-ttu-id="312f0-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="312f0-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="312f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="312f0-102">SYNOPSIS</span></span>
<span data-ttu-id="312f0-103">Excluir um ponto de extremidade para seu Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="312f0-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="312f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="312f0-104">SYNTAX</span></span>

### <span data-ttu-id="312f0-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="312f0-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="312f0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="312f0-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="312f0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="312f0-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="312f0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="312f0-108">DESCRIPTION</span></span>
<span data-ttu-id="312f0-109">Exclua um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="312f0-109">Delete an endpoint.</span></span> <span data-ttu-id="312f0-110">Lembre-se de excluir todas as rotas que usam esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="312f0-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="312f0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="312f0-111">EXAMPLES</span></span>

### <span data-ttu-id="312f0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="312f0-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="312f0-113">Exclua o ponto de extremidade "E2" do Hub de IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="312f0-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="312f0-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="312f0-114">PARAMETERS</span></span>

### <span data-ttu-id="312f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="312f0-115">-DefaultProfile</span></span>
<span data-ttu-id="312f0-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="312f0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="312f0-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="312f0-117">-EndpointName</span></span>
<span data-ttu-id="312f0-118">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="312f0-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="312f0-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="312f0-119">-EndpointType</span></span>
<span data-ttu-id="312f0-120">Tipo do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="312f0-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="312f0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="312f0-121">-InputObject</span></span>
<span data-ttu-id="312f0-122">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="312f0-122">IotHub Object</span></span>

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

### <span data-ttu-id="312f0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="312f0-123">-Name</span></span>
<span data-ttu-id="312f0-124">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="312f0-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="312f0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="312f0-125">-PassThru</span></span>
<span data-ttu-id="312f0-126">Permite retornar o objeto booleano.</span><span class="sxs-lookup"><span data-stu-id="312f0-126">Allows to return the boolean object.</span></span> <span data-ttu-id="312f0-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="312f0-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="312f0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="312f0-128">-ResourceGroupName</span></span>
<span data-ttu-id="312f0-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="312f0-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="312f0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="312f0-130">-ResourceId</span></span>
<span data-ttu-id="312f0-131">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="312f0-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="312f0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="312f0-132">-Confirm</span></span>
<span data-ttu-id="312f0-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="312f0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="312f0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="312f0-134">-WhatIf</span></span>
<span data-ttu-id="312f0-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="312f0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="312f0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="312f0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="312f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="312f0-137">CommonParameters</span></span>
<span data-ttu-id="312f0-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="312f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="312f0-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="312f0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="312f0-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="312f0-140">INPUTS</span></span>

### <span data-ttu-id="312f0-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="312f0-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="312f0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="312f0-142">System.String</span></span>

## <span data-ttu-id="312f0-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="312f0-143">OUTPUTS</span></span>

### <span data-ttu-id="312f0-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="312f0-144">System.Boolean</span></span>

## <span data-ttu-id="312f0-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="312f0-145">NOTES</span></span>

## <span data-ttu-id="312f0-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="312f0-146">RELATED LINKS</span></span>
