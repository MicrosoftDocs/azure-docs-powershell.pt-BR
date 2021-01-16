---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 173e84e3587a6844896791ef38a185db522d4e4b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272783"
---
# <span data-ttu-id="64ebb-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="64ebb-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="64ebb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="64ebb-103">Testar rotas no Hub IoT</span><span class="sxs-lookup"><span data-stu-id="64ebb-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="64ebb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64ebb-104">SYNTAX</span></span>

### <span data-ttu-id="64ebb-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="64ebb-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ebb-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="64ebb-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ebb-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="64ebb-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64ebb-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="64ebb-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ebb-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="64ebb-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64ebb-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="64ebb-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ebb-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="64ebb-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64ebb-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64ebb-112">DESCRIPTION</span></span>
<span data-ttu-id="64ebb-113">Testar uma rota específica.</span><span class="sxs-lookup"><span data-stu-id="64ebb-113">Test a specific route.</span></span>

## <span data-ttu-id="64ebb-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64ebb-114">EXAMPLES</span></span>

### <span data-ttu-id="64ebb-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64ebb-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="64ebb-116">Testar toda a rota com a fonte "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="64ebb-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="64ebb-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="64ebb-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="64ebb-118">Testar uma rota específica.</span><span class="sxs-lookup"><span data-stu-id="64ebb-118">Test a specific route.</span></span>

### <span data-ttu-id="64ebb-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="64ebb-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="64ebb-120">Testar uma rota específica e mostrar o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="64ebb-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="64ebb-121">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="64ebb-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="64ebb-122">Teste uma rota específica com o AppProperty e o Systemproperty.</span><span class="sxs-lookup"><span data-stu-id="64ebb-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="64ebb-123">OS</span><span class="sxs-lookup"><span data-stu-id="64ebb-123">PARAMETERS</span></span>

### <span data-ttu-id="64ebb-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="64ebb-124">-AppProperty</span></span>
<span data-ttu-id="64ebb-125">Propriedades do aplicativo da mensagem de roteiro</span><span class="sxs-lookup"><span data-stu-id="64ebb-125">App properties of the route message</span></span>

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

### <span data-ttu-id="64ebb-126">-Corpo</span><span class="sxs-lookup"><span data-stu-id="64ebb-126">-Body</span></span>
<span data-ttu-id="64ebb-127">Corpo da mensagem de roteiro</span><span class="sxs-lookup"><span data-stu-id="64ebb-127">Body of the route message</span></span>

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

### <span data-ttu-id="64ebb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ebb-128">-DefaultProfile</span></span>
<span data-ttu-id="64ebb-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64ebb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64ebb-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64ebb-130">-InputObject</span></span>
<span data-ttu-id="64ebb-131">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="64ebb-131">IotHub Object</span></span>

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

### <span data-ttu-id="64ebb-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="64ebb-132">-Name</span></span>
<span data-ttu-id="64ebb-133">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="64ebb-133">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="64ebb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64ebb-134">-ResourceGroupName</span></span>
<span data-ttu-id="64ebb-135">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="64ebb-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="64ebb-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64ebb-136">-ResourceId</span></span>
<span data-ttu-id="64ebb-137">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="64ebb-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="64ebb-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="64ebb-138">-RouteName</span></span>
<span data-ttu-id="64ebb-139">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="64ebb-139">Name of the Route</span></span>

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

### <span data-ttu-id="64ebb-140">-Conerror</span><span class="sxs-lookup"><span data-stu-id="64ebb-140">-ShowError</span></span>
<span data-ttu-id="64ebb-141">Mostrar erro detalhado, se existir</span><span class="sxs-lookup"><span data-stu-id="64ebb-141">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="64ebb-142">-Fonte</span><span class="sxs-lookup"><span data-stu-id="64ebb-142">-Source</span></span>
<span data-ttu-id="64ebb-143">Fonte da rota</span><span class="sxs-lookup"><span data-stu-id="64ebb-143">Source of the route</span></span>

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

### <span data-ttu-id="64ebb-144">-Systemproperty</span><span class="sxs-lookup"><span data-stu-id="64ebb-144">-SystemProperty</span></span>
<span data-ttu-id="64ebb-145">Propriedades do sistema da mensagem de roteiro</span><span class="sxs-lookup"><span data-stu-id="64ebb-145">System properties of the route message</span></span>

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

### <span data-ttu-id="64ebb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ebb-146">CommonParameters</span></span>
<span data-ttu-id="64ebb-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64ebb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ebb-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64ebb-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ebb-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64ebb-149">INPUTS</span></span>

### <span data-ttu-id="64ebb-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="64ebb-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="64ebb-151">System. String</span><span class="sxs-lookup"><span data-stu-id="64ebb-151">System.String</span></span>

## <span data-ttu-id="64ebb-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64ebb-152">OUTPUTS</span></span>

### <span data-ttu-id="64ebb-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="64ebb-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="64ebb-154">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="64ebb-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="64ebb-155">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="64ebb-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="64ebb-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64ebb-156">NOTES</span></span>

## <span data-ttu-id="64ebb-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64ebb-157">RELATED LINKS</span></span>
