---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117614"
---
# <span data-ttu-id="d7837-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="d7837-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="d7837-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7837-102">SYNOPSIS</span></span>
<span data-ttu-id="d7837-103">Obter informações sobre a rota no Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="d7837-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="d7837-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7837-104">SYNTAX</span></span>

### <span data-ttu-id="d7837-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d7837-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7837-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d7837-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7837-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d7837-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7837-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7837-108">DESCRIPTION</span></span>
<span data-ttu-id="d7837-109">Obter informações sobre a rota. Você pode obter todas as rotas de um Hub de IoT, obter rotas para um tipo de ponto de extremidade ou obter rotas para um ponto de extremidade específico.</span><span class="sxs-lookup"><span data-stu-id="d7837-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="d7837-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7837-110">EXAMPLES</span></span>

### <span data-ttu-id="d7837-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d7837-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="d7837-112">Obter toda a rota do Hub de IoT do "myiothub".</span><span class="sxs-lookup"><span data-stu-id="d7837-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="d7837-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d7837-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="d7837-114">Obter informações de rota do Hub de IoT do "myiothub".</span><span class="sxs-lookup"><span data-stu-id="d7837-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="d7837-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7837-115">PARAMETERS</span></span>

### <span data-ttu-id="d7837-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7837-116">-DefaultProfile</span></span>
<span data-ttu-id="d7837-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7837-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7837-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7837-118">-InputObject</span></span>
<span data-ttu-id="d7837-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="d7837-119">IotHub Object</span></span>

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

### <span data-ttu-id="d7837-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7837-120">-Name</span></span>
<span data-ttu-id="d7837-121">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="d7837-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d7837-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7837-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7837-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d7837-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d7837-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7837-124">-ResourceId</span></span>
<span data-ttu-id="d7837-125">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="d7837-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d7837-126">-Nomeda Roteada</span><span class="sxs-lookup"><span data-stu-id="d7837-126">-RouteName</span></span>
<span data-ttu-id="d7837-127">Nome da Rota</span><span class="sxs-lookup"><span data-stu-id="d7837-127">Name of the Route</span></span>

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

### <span data-ttu-id="d7837-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7837-128">CommonParameters</span></span>
<span data-ttu-id="d7837-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7837-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7837-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7837-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7837-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="d7837-131">INPUTS</span></span>

### <span data-ttu-id="d7837-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d7837-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d7837-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d7837-133">System.String</span></span>

## <span data-ttu-id="d7837-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="d7837-134">OUTPUTS</span></span>

### <span data-ttu-id="d7837-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="d7837-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="d7837-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="d7837-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="d7837-137">Notas</span><span class="sxs-lookup"><span data-stu-id="d7837-137">NOTES</span></span>

## <span data-ttu-id="d7837-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7837-138">RELATED LINKS</span></span>
