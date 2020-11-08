---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126214"
---
# <span data-ttu-id="56c9a-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="56c9a-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="56c9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="56c9a-103">Obter informações sobre a rota no Hub IoT</span><span class="sxs-lookup"><span data-stu-id="56c9a-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="56c9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56c9a-104">SYNTAX</span></span>

### <span data-ttu-id="56c9a-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="56c9a-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56c9a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="56c9a-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56c9a-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="56c9a-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56c9a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56c9a-108">DESCRIPTION</span></span>
<span data-ttu-id="56c9a-109">Obter informações sobre a rota. Você pode obter todas as rotas de um hub IoT, obter rotas para um tipo de ponto de extremidade ou obter rotas para um ponto de extremidade específico.</span><span class="sxs-lookup"><span data-stu-id="56c9a-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="56c9a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56c9a-110">EXAMPLES</span></span>

### <span data-ttu-id="56c9a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="56c9a-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="56c9a-112">Obter toda a rota do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="56c9a-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="56c9a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="56c9a-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="56c9a-114">Obter informações de rota do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="56c9a-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="56c9a-115">OS</span><span class="sxs-lookup"><span data-stu-id="56c9a-115">PARAMETERS</span></span>

### <span data-ttu-id="56c9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c9a-116">-DefaultProfile</span></span>
<span data-ttu-id="56c9a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56c9a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56c9a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56c9a-118">-InputObject</span></span>
<span data-ttu-id="56c9a-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="56c9a-119">IotHub Object</span></span>

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

### <span data-ttu-id="56c9a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="56c9a-120">-Name</span></span>
<span data-ttu-id="56c9a-121">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="56c9a-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="56c9a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56c9a-122">-ResourceGroupName</span></span>
<span data-ttu-id="56c9a-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="56c9a-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="56c9a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56c9a-124">-ResourceId</span></span>
<span data-ttu-id="56c9a-125">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="56c9a-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="56c9a-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="56c9a-126">-RouteName</span></span>
<span data-ttu-id="56c9a-127">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="56c9a-127">Name of the Route</span></span>

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

### <span data-ttu-id="56c9a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c9a-128">CommonParameters</span></span>
<span data-ttu-id="56c9a-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c9a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c9a-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56c9a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c9a-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56c9a-131">INPUTS</span></span>

### <span data-ttu-id="56c9a-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="56c9a-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="56c9a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="56c9a-133">System.String</span></span>

## <span data-ttu-id="56c9a-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56c9a-134">OUTPUTS</span></span>

### <span data-ttu-id="56c9a-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="56c9a-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="56c9a-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="56c9a-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="56c9a-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56c9a-137">NOTES</span></span>

## <span data-ttu-id="56c9a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56c9a-138">RELATED LINKS</span></span>
