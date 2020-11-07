---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: 3828b6ef95c629362ce0082d6bb97e2af1ccb687
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776706"
---
# <span data-ttu-id="1a7c0-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="1a7c0-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="1a7c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a7c0-102">SYNOPSIS</span></span>
<span data-ttu-id="1a7c0-103">Criar uma rota no Hub IoT</span><span class="sxs-lookup"><span data-stu-id="1a7c0-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="1a7c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a7c0-104">SYNTAX</span></span>

### <span data-ttu-id="1a7c0-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1a7c0-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a7c0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1a7c0-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a7c0-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="1a7c0-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a7c0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a7c0-108">DESCRIPTION</span></span>
<span data-ttu-id="1a7c0-109">Crie uma rota para enviar uma fonte de dados específica e uma condição para um ponto de extremidade desejado.</span><span class="sxs-lookup"><span data-stu-id="1a7c0-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="1a7c0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a7c0-110">EXAMPLES</span></span>

### <span data-ttu-id="1a7c0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1a7c0-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="1a7c0-112">Criar uma nova rota "R1".</span><span class="sxs-lookup"><span data-stu-id="1a7c0-112">Create a new route "R1".</span></span>

## <span data-ttu-id="1a7c0-113">OS</span><span class="sxs-lookup"><span data-stu-id="1a7c0-113">PARAMETERS</span></span>

### <span data-ttu-id="1a7c0-114">-Condition</span><span class="sxs-lookup"><span data-stu-id="1a7c0-114">-Condition</span></span>
<span data-ttu-id="1a7c0-115">Condição que é avaliada para aplicar a regra de roteamento</span><span class="sxs-lookup"><span data-stu-id="1a7c0-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="1a7c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a7c0-116">-DefaultProfile</span></span>
<span data-ttu-id="1a7c0-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a7c0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a7c0-118">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="1a7c0-118">-Enabled</span></span>
<span data-ttu-id="1a7c0-119">Habilitar rota</span><span class="sxs-lookup"><span data-stu-id="1a7c0-119">Enable route</span></span>

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

### <span data-ttu-id="1a7c0-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1a7c0-120">-EndpointName</span></span>
<span data-ttu-id="1a7c0-121">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="1a7c0-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="1a7c0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a7c0-122">-InputObject</span></span>
<span data-ttu-id="1a7c0-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="1a7c0-123">IotHub Object</span></span>

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

### <span data-ttu-id="1a7c0-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a7c0-124">-Name</span></span>
<span data-ttu-id="1a7c0-125">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="1a7c0-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1a7c0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a7c0-126">-ResourceGroupName</span></span>
<span data-ttu-id="1a7c0-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1a7c0-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1a7c0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a7c0-128">-ResourceId</span></span>
<span data-ttu-id="1a7c0-129">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="1a7c0-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1a7c0-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="1a7c0-130">-RouteName</span></span>
<span data-ttu-id="1a7c0-131">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="1a7c0-131">Name of the Route</span></span>

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

### <span data-ttu-id="1a7c0-132">-Fonte</span><span class="sxs-lookup"><span data-stu-id="1a7c0-132">-Source</span></span>
<span data-ttu-id="1a7c0-133">Fonte da rota</span><span class="sxs-lookup"><span data-stu-id="1a7c0-133">Source of the route</span></span>

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

### <span data-ttu-id="1a7c0-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a7c0-134">-Confirm</span></span>
<span data-ttu-id="1a7c0-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a7c0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a7c0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a7c0-136">-WhatIf</span></span>
<span data-ttu-id="1a7c0-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a7c0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a7c0-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a7c0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a7c0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a7c0-139">CommonParameters</span></span>
<span data-ttu-id="1a7c0-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a7c0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a7c0-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a7c0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a7c0-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a7c0-142">INPUTS</span></span>

### <span data-ttu-id="1a7c0-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1a7c0-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1a7c0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1a7c0-144">System.String</span></span>

## <span data-ttu-id="1a7c0-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a7c0-145">OUTPUTS</span></span>

### <span data-ttu-id="1a7c0-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="1a7c0-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="1a7c0-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a7c0-147">NOTES</span></span>

## <span data-ttu-id="1a7c0-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a7c0-148">RELATED LINKS</span></span>