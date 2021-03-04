---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 56ac931259de9705e0d6703e1387853aba77b028
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892162"
---
# <span data-ttu-id="f56e0-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="f56e0-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="f56e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f56e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f56e0-103">Rotas de teste no Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="f56e0-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="f56e0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f56e0-104">SYNTAX</span></span>

### <span data-ttu-id="f56e0-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f56e0-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f56e0-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="f56e0-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f56e0-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="f56e0-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f56e0-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="f56e0-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f56e0-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="f56e0-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f56e0-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="f56e0-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f56e0-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="f56e0-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f56e0-112">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f56e0-112">DESCRIPTION</span></span>
<span data-ttu-id="f56e0-113">Teste uma rota específica.</span><span class="sxs-lookup"><span data-stu-id="f56e0-113">Test a specific route.</span></span>

## <span data-ttu-id="f56e0-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f56e0-114">EXAMPLES</span></span>

### <span data-ttu-id="f56e0-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f56e0-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="f56e0-116">Teste toda a rota com a origem "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="f56e0-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="f56e0-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f56e0-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="f56e0-118">Teste uma rota específica.</span><span class="sxs-lookup"><span data-stu-id="f56e0-118">Test a specific route.</span></span>

### <span data-ttu-id="f56e0-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f56e0-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="f56e0-120">Teste uma rota específica e mostrando o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="f56e0-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="f56e0-121">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="f56e0-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="f56e0-122">Teste uma rota específica com AppProperty e SystemProperty.</span><span class="sxs-lookup"><span data-stu-id="f56e0-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="f56e0-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f56e0-123">PARAMETERS</span></span>

### <span data-ttu-id="f56e0-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="f56e0-124">-AppProperty</span></span>
<span data-ttu-id="f56e0-125">Propriedades do aplicativo da mensagem de rota</span><span class="sxs-lookup"><span data-stu-id="f56e0-125">App properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f56e0-126">-Body</span><span class="sxs-lookup"><span data-stu-id="f56e0-126">-Body</span></span>
<span data-ttu-id="f56e0-127">Corpo da mensagem de rota</span><span class="sxs-lookup"><span data-stu-id="f56e0-127">Body of the route message</span></span>

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

### <span data-ttu-id="f56e0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f56e0-128">-DefaultProfile</span></span>
<span data-ttu-id="f56e0-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f56e0-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f56e0-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f56e0-130">-InputObject</span></span>
<span data-ttu-id="f56e0-131">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="f56e0-131">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectTestRouteSet, InputObjectTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f56e0-132">-Name</span><span class="sxs-lookup"><span data-stu-id="f56e0-132">-Name</span></span>
<span data-ttu-id="f56e0-133">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="f56e0-133">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f56e0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f56e0-134">-ResourceGroupName</span></span>
<span data-ttu-id="f56e0-135">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f56e0-135">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f56e0-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f56e0-136">-ResourceId</span></span>
<span data-ttu-id="f56e0-137">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="f56e0-137">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdTestRouteSet, ResourceIdTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f56e0-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="f56e0-138">-RouteName</span></span>
<span data-ttu-id="f56e0-139">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="f56e0-139">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f56e0-140">-ShowError</span><span class="sxs-lookup"><span data-stu-id="f56e0-140">-ShowError</span></span>
<span data-ttu-id="f56e0-141">Mostrar erro detalhado, se existir</span><span class="sxs-lookup"><span data-stu-id="f56e0-141">Show detailed error, if exist</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f56e0-142">-Source</span><span class="sxs-lookup"><span data-stu-id="f56e0-142">-Source</span></span>
<span data-ttu-id="f56e0-143">Origem da rota</span><span class="sxs-lookup"><span data-stu-id="f56e0-143">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f56e0-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="f56e0-144">-SystemProperty</span></span>
<span data-ttu-id="f56e0-145">Propriedades do sistema da mensagem de rota</span><span class="sxs-lookup"><span data-stu-id="f56e0-145">System properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f56e0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f56e0-146">CommonParameters</span></span>
<span data-ttu-id="f56e0-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f56e0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f56e0-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f56e0-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f56e0-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f56e0-149">INPUTS</span></span>

### <span data-ttu-id="f56e0-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f56e0-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f56e0-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f56e0-151">System.String</span></span>

## <span data-ttu-id="f56e0-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f56e0-152">OUTPUTS</span></span>

### <span data-ttu-id="f56e0-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="f56e0-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="f56e0-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="f56e0-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="f56e0-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="f56e0-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="f56e0-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="f56e0-156">NOTES</span></span>

## <span data-ttu-id="f56e0-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f56e0-157">RELATED LINKS</span></span>
