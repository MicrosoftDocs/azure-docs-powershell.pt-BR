---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: a54bfdb26b7013e490ca36e4ae5608da228d9d70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113119"
---
# <span data-ttu-id="08633-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="08633-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="08633-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08633-102">SYNOPSIS</span></span>
<span data-ttu-id="08633-103">Atualizar uma rota no Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="08633-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="08633-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08633-104">SYNTAX</span></span>

### <span data-ttu-id="08633-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="08633-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08633-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="08633-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08633-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="08633-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08633-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="08633-108">DESCRIPTION</span></span>
<span data-ttu-id="08633-109">Editar uma rota.</span><span class="sxs-lookup"><span data-stu-id="08633-109">Edit a route.</span></span> <span data-ttu-id="08633-110">Você pode atualizar todos os campos em uma rota, incluindo a fonte de dados, o ponto de extremidade, a consulta de roteamento e também habilitar ou desabilitar a rota.</span><span class="sxs-lookup"><span data-stu-id="08633-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="08633-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="08633-111">EXAMPLES</span></span>

### <span data-ttu-id="08633-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="08633-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="08633-113">Atualizando as informações da rota.</span><span class="sxs-lookup"><span data-stu-id="08633-113">Updating the route information.</span></span>

### <span data-ttu-id="08633-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="08633-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="08633-115">Atualizando as informações da rota.</span><span class="sxs-lookup"><span data-stu-id="08633-115">Updating the route information.</span></span>

### <span data-ttu-id="08633-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="08633-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="08633-117">Atualizando as informações da rota.</span><span class="sxs-lookup"><span data-stu-id="08633-117">Updating the route information.</span></span>

## <span data-ttu-id="08633-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08633-118">PARAMETERS</span></span>

### <span data-ttu-id="08633-119">-Condição</span><span class="sxs-lookup"><span data-stu-id="08633-119">-Condition</span></span>
<span data-ttu-id="08633-120">Condição avaliada para aplicar a regra de roteamento</span><span class="sxs-lookup"><span data-stu-id="08633-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="08633-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08633-121">-DefaultProfile</span></span>
<span data-ttu-id="08633-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08633-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08633-123">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="08633-123">-Enabled</span></span>
<span data-ttu-id="08633-124">Habilitar rota</span><span class="sxs-lookup"><span data-stu-id="08633-124">Enable route</span></span>

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

### <span data-ttu-id="08633-125">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="08633-125">-EndpointName</span></span>
<span data-ttu-id="08633-126">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="08633-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="08633-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08633-127">-InputObject</span></span>
<span data-ttu-id="08633-128">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="08633-128">IotHub Object</span></span>

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

### <span data-ttu-id="08633-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="08633-129">-Name</span></span>
<span data-ttu-id="08633-130">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="08633-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="08633-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08633-131">-ResourceGroupName</span></span>
<span data-ttu-id="08633-132">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="08633-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="08633-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08633-133">-ResourceId</span></span>
<span data-ttu-id="08633-134">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="08633-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="08633-135">-Nomeda Roteada</span><span class="sxs-lookup"><span data-stu-id="08633-135">-RouteName</span></span>
<span data-ttu-id="08633-136">Nome da Rota</span><span class="sxs-lookup"><span data-stu-id="08633-136">Name of the Route</span></span>

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

### <span data-ttu-id="08633-137">-Origem</span><span class="sxs-lookup"><span data-stu-id="08633-137">-Source</span></span>
<span data-ttu-id="08633-138">Origem da rota</span><span class="sxs-lookup"><span data-stu-id="08633-138">Source of the route</span></span>

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

### <span data-ttu-id="08633-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="08633-139">-Confirm</span></span>
<span data-ttu-id="08633-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08633-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08633-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08633-141">-WhatIf</span></span>
<span data-ttu-id="08633-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="08633-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08633-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08633-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08633-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08633-144">CommonParameters</span></span>
<span data-ttu-id="08633-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08633-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08633-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08633-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08633-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="08633-147">INPUTS</span></span>

### <span data-ttu-id="08633-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="08633-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="08633-149">System.String</span><span class="sxs-lookup"><span data-stu-id="08633-149">System.String</span></span>

## <span data-ttu-id="08633-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="08633-150">OUTPUTS</span></span>

### <span data-ttu-id="08633-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="08633-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="08633-152">Notas</span><span class="sxs-lookup"><span data-stu-id="08633-152">NOTES</span></span>

## <span data-ttu-id="08633-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08633-153">RELATED LINKS</span></span>
