---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: a84d432e5771b5f04a7d9f478cd8ef446e08620a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116750"
---
# <span data-ttu-id="8cc92-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="8cc92-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="8cc92-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8cc92-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc92-103">Criar uma rota no Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="8cc92-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="8cc92-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cc92-104">SYNTAX</span></span>

### <span data-ttu-id="8cc92-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8cc92-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc92-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8cc92-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc92-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8cc92-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cc92-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8cc92-108">DESCRIPTION</span></span>
<span data-ttu-id="8cc92-109">Crie uma rota para enviar uma fonte de dados e uma condição específicas para um ponto de extremidade desejado.</span><span class="sxs-lookup"><span data-stu-id="8cc92-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="8cc92-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8cc92-110">EXAMPLES</span></span>

### <span data-ttu-id="8cc92-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8cc92-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="8cc92-112">Crie uma nova rota "R1".</span><span class="sxs-lookup"><span data-stu-id="8cc92-112">Create a new route "R1".</span></span>

## <span data-ttu-id="8cc92-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cc92-113">PARAMETERS</span></span>

### <span data-ttu-id="8cc92-114">-Condição</span><span class="sxs-lookup"><span data-stu-id="8cc92-114">-Condition</span></span>
<span data-ttu-id="8cc92-115">Condição avaliada para aplicar a regra de roteamento</span><span class="sxs-lookup"><span data-stu-id="8cc92-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="8cc92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc92-116">-DefaultProfile</span></span>
<span data-ttu-id="8cc92-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc92-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cc92-118">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="8cc92-118">-Enabled</span></span>
<span data-ttu-id="8cc92-119">Habilitar rota</span><span class="sxs-lookup"><span data-stu-id="8cc92-119">Enable route</span></span>

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

### <span data-ttu-id="8cc92-120">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="8cc92-120">-EndpointName</span></span>
<span data-ttu-id="8cc92-121">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="8cc92-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="8cc92-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cc92-122">-InputObject</span></span>
<span data-ttu-id="8cc92-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="8cc92-123">IotHub Object</span></span>

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

### <span data-ttu-id="8cc92-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cc92-124">-Name</span></span>
<span data-ttu-id="8cc92-125">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="8cc92-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8cc92-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cc92-126">-ResourceGroupName</span></span>
<span data-ttu-id="8cc92-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8cc92-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8cc92-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cc92-128">-ResourceId</span></span>
<span data-ttu-id="8cc92-129">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="8cc92-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8cc92-130">-Nomeda Roteada</span><span class="sxs-lookup"><span data-stu-id="8cc92-130">-RouteName</span></span>
<span data-ttu-id="8cc92-131">Nome da Rota</span><span class="sxs-lookup"><span data-stu-id="8cc92-131">Name of the Route</span></span>

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

### <span data-ttu-id="8cc92-132">-Origem</span><span class="sxs-lookup"><span data-stu-id="8cc92-132">-Source</span></span>
<span data-ttu-id="8cc92-133">Origem da rota</span><span class="sxs-lookup"><span data-stu-id="8cc92-133">Source of the route</span></span>

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

### <span data-ttu-id="8cc92-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8cc92-134">-Confirm</span></span>
<span data-ttu-id="8cc92-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc92-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cc92-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc92-136">-WhatIf</span></span>
<span data-ttu-id="8cc92-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8cc92-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cc92-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8cc92-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cc92-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc92-139">CommonParameters</span></span>
<span data-ttu-id="8cc92-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc92-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc92-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cc92-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc92-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="8cc92-142">INPUTS</span></span>

### <span data-ttu-id="8cc92-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8cc92-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8cc92-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8cc92-144">System.String</span></span>

## <span data-ttu-id="8cc92-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="8cc92-145">OUTPUTS</span></span>

### <span data-ttu-id="8cc92-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="8cc92-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="8cc92-147">Notas</span><span class="sxs-lookup"><span data-stu-id="8cc92-147">NOTES</span></span>

## <span data-ttu-id="8cc92-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cc92-148">RELATED LINKS</span></span>
