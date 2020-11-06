---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/test-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Test-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Test-AzureRmIotHubRoute.md
ms.openlocfilehash: f51ba85215d252959b974a39ea864b1c98fce460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610323"
---
# <span data-ttu-id="55963-101">Test-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="55963-101">Test-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="55963-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55963-102">SYNOPSIS</span></span>
<span data-ttu-id="55963-103">Testar rotas no Hub IoT</span><span class="sxs-lookup"><span data-stu-id="55963-103">Test routes in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55963-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55963-104">SYNTAX</span></span>

### <span data-ttu-id="55963-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="55963-105">ResourceSet (Default)</span></span>
```
Test-AzureRmIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55963-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="55963-106">InputObjectTestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55963-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="55963-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55963-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="55963-108">TestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55963-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="55963-109">TestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource>
 [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55963-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="55963-110">ResourceIdTestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55963-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="55963-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55963-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55963-112">DESCRIPTION</span></span>
<span data-ttu-id="55963-113">Testar uma rota específica.</span><span class="sxs-lookup"><span data-stu-id="55963-113">Test a specific route.</span></span>

## <span data-ttu-id="55963-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55963-114">EXAMPLES</span></span>

### <span data-ttu-id="55963-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="55963-115">Example 1</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="55963-116">Testar toda a rota com a fonte "DeviceMessges".</span><span class="sxs-lookup"><span data-stu-id="55963-116">Test all route with source "DeviceMessges".</span></span>

### <span data-ttu-id="55963-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="55963-117">Example 2</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="55963-118">Testar uma rota específica.</span><span class="sxs-lookup"><span data-stu-id="55963-118">Test a specific route.</span></span>

### <span data-ttu-id="55963-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="55963-119">Example 3</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="55963-120">Testar uma rota específica e mostrar o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="55963-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="55963-121">OS</span><span class="sxs-lookup"><span data-stu-id="55963-121">PARAMETERS</span></span>

### <span data-ttu-id="55963-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="55963-122">-AppProperty</span></span>
<span data-ttu-id="55963-123">Propriedades do aplicativo da mensagem de roteiro</span><span class="sxs-lookup"><span data-stu-id="55963-123">App properties of the route message</span></span>

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

### <span data-ttu-id="55963-124">-Corpo</span><span class="sxs-lookup"><span data-stu-id="55963-124">-Body</span></span>
<span data-ttu-id="55963-125">Corpo da mensagem de roteiro</span><span class="sxs-lookup"><span data-stu-id="55963-125">Body of the route message</span></span>

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

### <span data-ttu-id="55963-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55963-126">-DefaultProfile</span></span>
<span data-ttu-id="55963-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55963-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55963-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55963-128">-InputObject</span></span>
<span data-ttu-id="55963-129">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="55963-129">IotHub Object</span></span>

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

### <span data-ttu-id="55963-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="55963-130">-Name</span></span>
<span data-ttu-id="55963-131">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="55963-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="55963-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55963-132">-ResourceGroupName</span></span>
<span data-ttu-id="55963-133">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="55963-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="55963-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55963-134">-ResourceId</span></span>
<span data-ttu-id="55963-135">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="55963-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="55963-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="55963-136">-RouteName</span></span>
<span data-ttu-id="55963-137">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="55963-137">Name of the Route</span></span>

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

### <span data-ttu-id="55963-138">-Conerror</span><span class="sxs-lookup"><span data-stu-id="55963-138">-ShowError</span></span>
<span data-ttu-id="55963-139">Mostrar erro detalhado, se existir</span><span class="sxs-lookup"><span data-stu-id="55963-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="55963-140">-Fonte</span><span class="sxs-lookup"><span data-stu-id="55963-140">-Source</span></span>
<span data-ttu-id="55963-141">Fonte da rota</span><span class="sxs-lookup"><span data-stu-id="55963-141">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55963-142">-Systemproperty</span><span class="sxs-lookup"><span data-stu-id="55963-142">-SystemProperty</span></span>
<span data-ttu-id="55963-143">Propriedades do sistema da mensagem de roteiro</span><span class="sxs-lookup"><span data-stu-id="55963-143">System properties of the route message</span></span>

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

### <span data-ttu-id="55963-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55963-144">CommonParameters</span></span>
<span data-ttu-id="55963-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55963-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55963-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55963-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55963-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55963-147">INPUTS</span></span>

### <span data-ttu-id="55963-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="55963-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="55963-149">System. String</span><span class="sxs-lookup"><span data-stu-id="55963-149">System.String</span></span>

## <span data-ttu-id="55963-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55963-150">OUTPUTS</span></span>

### <span data-ttu-id="55963-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="55963-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>
<span data-ttu-id="55963-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteCompilationError System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="55963-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="55963-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55963-153">NOTES</span></span>

## <span data-ttu-id="55963-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55963-154">RELATED LINKS</span></span>
