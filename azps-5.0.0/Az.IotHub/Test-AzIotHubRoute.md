---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: eb9d6a7b847c360861fd13bb285bc6f09bb70fbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280525"
---
# <span data-ttu-id="4fbff-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="4fbff-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="4fbff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fbff-102">SYNOPSIS</span></span>
<span data-ttu-id="4fbff-103">Testar rotas no Hub IoT</span><span class="sxs-lookup"><span data-stu-id="4fbff-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="4fbff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fbff-104">SYNTAX</span></span>

### <span data-ttu-id="4fbff-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4fbff-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fbff-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="4fbff-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fbff-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="4fbff-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4fbff-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="4fbff-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fbff-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="4fbff-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4fbff-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="4fbff-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fbff-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="4fbff-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fbff-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4fbff-112">DESCRIPTION</span></span>
<span data-ttu-id="4fbff-113">Testar uma rota específica.</span><span class="sxs-lookup"><span data-stu-id="4fbff-113">Test a specific route.</span></span>

## <span data-ttu-id="4fbff-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fbff-114">EXAMPLES</span></span>

### <span data-ttu-id="4fbff-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4fbff-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="4fbff-116">Testar toda a rota com a fonte "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="4fbff-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="4fbff-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4fbff-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="4fbff-118">Testar uma rota específica.</span><span class="sxs-lookup"><span data-stu-id="4fbff-118">Test a specific route.</span></span>

### <span data-ttu-id="4fbff-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4fbff-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="4fbff-120">Testar uma rota específica e mostrar o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="4fbff-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="4fbff-121">OS</span><span class="sxs-lookup"><span data-stu-id="4fbff-121">PARAMETERS</span></span>

### <span data-ttu-id="4fbff-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="4fbff-122">-AppProperty</span></span>
<span data-ttu-id="4fbff-123">Propriedades do aplicativo da mensagem de roteiro</span><span class="sxs-lookup"><span data-stu-id="4fbff-123">App properties of the route message</span></span>

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

### <span data-ttu-id="4fbff-124">-Corpo</span><span class="sxs-lookup"><span data-stu-id="4fbff-124">-Body</span></span>
<span data-ttu-id="4fbff-125">Corpo da mensagem de roteiro</span><span class="sxs-lookup"><span data-stu-id="4fbff-125">Body of the route message</span></span>

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

### <span data-ttu-id="4fbff-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fbff-126">-DefaultProfile</span></span>
<span data-ttu-id="4fbff-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fbff-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fbff-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fbff-128">-InputObject</span></span>
<span data-ttu-id="4fbff-129">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="4fbff-129">IotHub Object</span></span>

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

### <span data-ttu-id="4fbff-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fbff-130">-Name</span></span>
<span data-ttu-id="4fbff-131">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="4fbff-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4fbff-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fbff-132">-ResourceGroupName</span></span>
<span data-ttu-id="4fbff-133">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4fbff-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4fbff-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fbff-134">-ResourceId</span></span>
<span data-ttu-id="4fbff-135">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="4fbff-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4fbff-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="4fbff-136">-RouteName</span></span>
<span data-ttu-id="4fbff-137">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="4fbff-137">Name of the Route</span></span>

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

### <span data-ttu-id="4fbff-138">-Conerror</span><span class="sxs-lookup"><span data-stu-id="4fbff-138">-ShowError</span></span>
<span data-ttu-id="4fbff-139">Mostrar erro detalhado, se existir</span><span class="sxs-lookup"><span data-stu-id="4fbff-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="4fbff-140">-Fonte</span><span class="sxs-lookup"><span data-stu-id="4fbff-140">-Source</span></span>
<span data-ttu-id="4fbff-141">Fonte da rota</span><span class="sxs-lookup"><span data-stu-id="4fbff-141">Source of the route</span></span>

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

### <span data-ttu-id="4fbff-142">-Systemproperty</span><span class="sxs-lookup"><span data-stu-id="4fbff-142">-SystemProperty</span></span>
<span data-ttu-id="4fbff-143">Propriedades do sistema da mensagem de roteiro</span><span class="sxs-lookup"><span data-stu-id="4fbff-143">System properties of the route message</span></span>

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

### <span data-ttu-id="4fbff-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fbff-144">CommonParameters</span></span>
<span data-ttu-id="4fbff-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fbff-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fbff-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fbff-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fbff-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4fbff-147">INPUTS</span></span>

### <span data-ttu-id="4fbff-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4fbff-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4fbff-149">System. String</span><span class="sxs-lookup"><span data-stu-id="4fbff-149">System.String</span></span>

## <span data-ttu-id="4fbff-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4fbff-150">OUTPUTS</span></span>

### <span data-ttu-id="4fbff-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="4fbff-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="4fbff-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="4fbff-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="4fbff-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="4fbff-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="4fbff-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4fbff-154">NOTES</span></span>

## <span data-ttu-id="4fbff-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fbff-155">RELATED LINKS</span></span>
