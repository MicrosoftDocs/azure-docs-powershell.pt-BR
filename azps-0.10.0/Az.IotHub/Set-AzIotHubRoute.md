---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: 4df4b5415a0fffc2f2482540088b36964cfa89ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775811"
---
# <span data-ttu-id="79b74-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="79b74-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="79b74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79b74-102">SYNOPSIS</span></span>
<span data-ttu-id="79b74-103">Atualizar uma rota no Hub IoT</span><span class="sxs-lookup"><span data-stu-id="79b74-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="79b74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79b74-104">SYNTAX</span></span>

### <span data-ttu-id="79b74-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="79b74-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b74-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="79b74-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b74-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="79b74-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79b74-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79b74-108">DESCRIPTION</span></span>
<span data-ttu-id="79b74-109">Editar uma rota.</span><span class="sxs-lookup"><span data-stu-id="79b74-109">Edit a route.</span></span> <span data-ttu-id="79b74-110">Você pode atualizar todos os campos em uma rota, incluindo fonte de dados, ponto de extremidade, consulta de roteamento e também habilitar ou desabilitar a rota.</span><span class="sxs-lookup"><span data-stu-id="79b74-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="79b74-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79b74-111">EXAMPLES</span></span>

### <span data-ttu-id="79b74-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="79b74-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="79b74-113">Atualizando as informações da rota.</span><span class="sxs-lookup"><span data-stu-id="79b74-113">Updating the route information.</span></span>

### <span data-ttu-id="79b74-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="79b74-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="79b74-115">Atualizando as informações da rota.</span><span class="sxs-lookup"><span data-stu-id="79b74-115">Updating the route information.</span></span>

### <span data-ttu-id="79b74-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="79b74-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="79b74-117">Atualizando as informações da rota.</span><span class="sxs-lookup"><span data-stu-id="79b74-117">Updating the route information.</span></span>

## <span data-ttu-id="79b74-118">OS</span><span class="sxs-lookup"><span data-stu-id="79b74-118">PARAMETERS</span></span>

### <span data-ttu-id="79b74-119">-Condition</span><span class="sxs-lookup"><span data-stu-id="79b74-119">-Condition</span></span>
<span data-ttu-id="79b74-120">Condição que é avaliada para aplicar a regra de roteamento</span><span class="sxs-lookup"><span data-stu-id="79b74-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="79b74-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b74-121">-DefaultProfile</span></span>
<span data-ttu-id="79b74-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79b74-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79b74-123">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="79b74-123">-Enabled</span></span>
<span data-ttu-id="79b74-124">Habilitar rota</span><span class="sxs-lookup"><span data-stu-id="79b74-124">Enable route</span></span>

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

### <span data-ttu-id="79b74-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="79b74-125">-EndpointName</span></span>
<span data-ttu-id="79b74-126">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="79b74-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="79b74-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79b74-127">-InputObject</span></span>
<span data-ttu-id="79b74-128">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="79b74-128">IotHub Object</span></span>

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

### <span data-ttu-id="79b74-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="79b74-129">-Name</span></span>
<span data-ttu-id="79b74-130">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="79b74-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="79b74-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b74-131">-ResourceGroupName</span></span>
<span data-ttu-id="79b74-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="79b74-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="79b74-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79b74-133">-ResourceId</span></span>
<span data-ttu-id="79b74-134">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="79b74-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="79b74-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="79b74-135">-RouteName</span></span>
<span data-ttu-id="79b74-136">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="79b74-136">Name of the Route</span></span>

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

### <span data-ttu-id="79b74-137">-Fonte</span><span class="sxs-lookup"><span data-stu-id="79b74-137">-Source</span></span>
<span data-ttu-id="79b74-138">Fonte da rota</span><span class="sxs-lookup"><span data-stu-id="79b74-138">Source of the route</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource]
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b74-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="79b74-139">-Confirm</span></span>
<span data-ttu-id="79b74-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79b74-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b74-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b74-141">-WhatIf</span></span>
<span data-ttu-id="79b74-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="79b74-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79b74-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79b74-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b74-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b74-144">CommonParameters</span></span>
<span data-ttu-id="79b74-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b74-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b74-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b74-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b74-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79b74-147">INPUTS</span></span>

### <span data-ttu-id="79b74-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="79b74-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="79b74-149">System. String</span><span class="sxs-lookup"><span data-stu-id="79b74-149">System.String</span></span>

## <span data-ttu-id="79b74-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79b74-150">OUTPUTS</span></span>

### <span data-ttu-id="79b74-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="79b74-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="79b74-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79b74-152">NOTES</span></span>

## <span data-ttu-id="79b74-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79b74-153">RELATED LINKS</span></span>
