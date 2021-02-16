---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 173e84e3587a6844896791ef38a185db522d4e4b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113118"
---
# <span data-ttu-id="e23b2-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="e23b2-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="e23b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e23b2-102">SYNOPSIS</span></span>
<span data-ttu-id="e23b2-103">Rotas de teste no Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="e23b2-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="e23b2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e23b2-104">SYNTAX</span></span>

### <span data-ttu-id="e23b2-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e23b2-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e23b2-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="e23b2-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e23b2-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="e23b2-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e23b2-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="e23b2-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e23b2-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="e23b2-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e23b2-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="e23b2-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e23b2-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="e23b2-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e23b2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e23b2-112">DESCRIPTION</span></span>
<span data-ttu-id="e23b2-113">Testar uma rota específica.</span><span class="sxs-lookup"><span data-stu-id="e23b2-113">Test a specific route.</span></span>

## <span data-ttu-id="e23b2-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e23b2-114">EXAMPLES</span></span>

### <span data-ttu-id="e23b2-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e23b2-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="e23b2-116">Teste toda a rota com "DeviceMessages" de origem.</span><span class="sxs-lookup"><span data-stu-id="e23b2-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="e23b2-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e23b2-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="e23b2-118">Testar uma rota específica.</span><span class="sxs-lookup"><span data-stu-id="e23b2-118">Test a specific route.</span></span>

### <span data-ttu-id="e23b2-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e23b2-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="e23b2-120">Teste uma rota específica e mostrando o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="e23b2-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="e23b2-121">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="e23b2-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="e23b2-122">Teste uma rota específica com AppProperty e SystemProperty.</span><span class="sxs-lookup"><span data-stu-id="e23b2-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="e23b2-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e23b2-123">PARAMETERS</span></span>

### <span data-ttu-id="e23b2-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="e23b2-124">-AppProperty</span></span>
<span data-ttu-id="e23b2-125">Propriedades do aplicativo da mensagem de rota</span><span class="sxs-lookup"><span data-stu-id="e23b2-125">App properties of the route message</span></span>

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

### <span data-ttu-id="e23b2-126">-Corpo</span><span class="sxs-lookup"><span data-stu-id="e23b2-126">-Body</span></span>
<span data-ttu-id="e23b2-127">Corpo da mensagem de rota</span><span class="sxs-lookup"><span data-stu-id="e23b2-127">Body of the route message</span></span>

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

### <span data-ttu-id="e23b2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e23b2-128">-DefaultProfile</span></span>
<span data-ttu-id="e23b2-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e23b2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e23b2-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e23b2-130">-InputObject</span></span>
<span data-ttu-id="e23b2-131">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="e23b2-131">IotHub Object</span></span>

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

### <span data-ttu-id="e23b2-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="e23b2-132">-Name</span></span>
<span data-ttu-id="e23b2-133">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="e23b2-133">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e23b2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e23b2-134">-ResourceGroupName</span></span>
<span data-ttu-id="e23b2-135">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e23b2-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e23b2-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e23b2-136">-ResourceId</span></span>
<span data-ttu-id="e23b2-137">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="e23b2-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e23b2-138">-Nomeda Roteada</span><span class="sxs-lookup"><span data-stu-id="e23b2-138">-RouteName</span></span>
<span data-ttu-id="e23b2-139">Nome da Rota</span><span class="sxs-lookup"><span data-stu-id="e23b2-139">Name of the Route</span></span>

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

### <span data-ttu-id="e23b2-140">-MostrarError</span><span class="sxs-lookup"><span data-stu-id="e23b2-140">-ShowError</span></span>
<span data-ttu-id="e23b2-141">Mostrar erro detalhado, se existir</span><span class="sxs-lookup"><span data-stu-id="e23b2-141">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="e23b2-142">-Origem</span><span class="sxs-lookup"><span data-stu-id="e23b2-142">-Source</span></span>
<span data-ttu-id="e23b2-143">Origem da rota</span><span class="sxs-lookup"><span data-stu-id="e23b2-143">Source of the route</span></span>

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

### <span data-ttu-id="e23b2-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="e23b2-144">-SystemProperty</span></span>
<span data-ttu-id="e23b2-145">Propriedades do sistema da mensagem de rota</span><span class="sxs-lookup"><span data-stu-id="e23b2-145">System properties of the route message</span></span>

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

### <span data-ttu-id="e23b2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e23b2-146">CommonParameters</span></span>
<span data-ttu-id="e23b2-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e23b2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e23b2-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e23b2-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e23b2-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="e23b2-149">INPUTS</span></span>

### <span data-ttu-id="e23b2-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e23b2-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e23b2-151">System.String</span><span class="sxs-lookup"><span data-stu-id="e23b2-151">System.String</span></span>

## <span data-ttu-id="e23b2-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="e23b2-152">OUTPUTS</span></span>

### <span data-ttu-id="e23b2-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="e23b2-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="e23b2-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="e23b2-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="e23b2-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="e23b2-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="e23b2-156">Notas</span><span class="sxs-lookup"><span data-stu-id="e23b2-156">NOTES</span></span>

## <span data-ttu-id="e23b2-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e23b2-157">RELATED LINKS</span></span>
