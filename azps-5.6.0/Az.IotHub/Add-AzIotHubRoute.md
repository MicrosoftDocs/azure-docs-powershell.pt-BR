---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: fbb0801dd586731a938c773711d72847e7a96e50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891352"
---
# <span data-ttu-id="1246e-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="1246e-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="1246e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1246e-102">SYNOPSIS</span></span>
<span data-ttu-id="1246e-103">Criar uma rota no Hub IoT</span><span class="sxs-lookup"><span data-stu-id="1246e-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="1246e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1246e-104">SYNTAX</span></span>

### <span data-ttu-id="1246e-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1246e-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1246e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1246e-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1246e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1246e-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1246e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1246e-108">DESCRIPTION</span></span>
<span data-ttu-id="1246e-109">Crie uma rota para enviar a fonte de dados e a condição específicas para um ponto de extremidade desejado.</span><span class="sxs-lookup"><span data-stu-id="1246e-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="1246e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1246e-110">EXAMPLES</span></span>

### <span data-ttu-id="1246e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1246e-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="1246e-112">Crie uma nova rota "R1".</span><span class="sxs-lookup"><span data-stu-id="1246e-112">Create a new route "R1".</span></span>

## <span data-ttu-id="1246e-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1246e-113">PARAMETERS</span></span>

### <span data-ttu-id="1246e-114">-Condition</span><span class="sxs-lookup"><span data-stu-id="1246e-114">-Condition</span></span>
<span data-ttu-id="1246e-115">Condição avaliada para aplicar a regra de roteamento</span><span class="sxs-lookup"><span data-stu-id="1246e-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="1246e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1246e-116">-DefaultProfile</span></span>
<span data-ttu-id="1246e-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1246e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1246e-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="1246e-118">-Enabled</span></span>
<span data-ttu-id="1246e-119">Habilitar rota</span><span class="sxs-lookup"><span data-stu-id="1246e-119">Enable route</span></span>

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

### <span data-ttu-id="1246e-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1246e-120">-EndpointName</span></span>
<span data-ttu-id="1246e-121">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="1246e-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="1246e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1246e-122">-InputObject</span></span>
<span data-ttu-id="1246e-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="1246e-123">IotHub Object</span></span>

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

### <span data-ttu-id="1246e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1246e-124">-Name</span></span>
<span data-ttu-id="1246e-125">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="1246e-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1246e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1246e-126">-ResourceGroupName</span></span>
<span data-ttu-id="1246e-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1246e-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1246e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1246e-128">-ResourceId</span></span>
<span data-ttu-id="1246e-129">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="1246e-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1246e-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="1246e-130">-RouteName</span></span>
<span data-ttu-id="1246e-131">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="1246e-131">Name of the Route</span></span>

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

### <span data-ttu-id="1246e-132">-Source</span><span class="sxs-lookup"><span data-stu-id="1246e-132">-Source</span></span>
<span data-ttu-id="1246e-133">Origem da rota</span><span class="sxs-lookup"><span data-stu-id="1246e-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1246e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1246e-134">-Confirm</span></span>
<span data-ttu-id="1246e-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1246e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1246e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1246e-136">-WhatIf</span></span>
<span data-ttu-id="1246e-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1246e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1246e-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1246e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1246e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1246e-139">CommonParameters</span></span>
<span data-ttu-id="1246e-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1246e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1246e-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1246e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1246e-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1246e-142">INPUTS</span></span>

### <span data-ttu-id="1246e-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1246e-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1246e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="1246e-144">System.String</span></span>

## <span data-ttu-id="1246e-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1246e-145">OUTPUTS</span></span>

### <span data-ttu-id="1246e-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="1246e-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="1246e-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="1246e-147">NOTES</span></span>

## <span data-ttu-id="1246e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1246e-148">RELATED LINKS</span></span>
