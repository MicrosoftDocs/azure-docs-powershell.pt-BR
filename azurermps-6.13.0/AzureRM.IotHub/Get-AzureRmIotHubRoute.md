---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
ms.openlocfilehash: 0711bd1d6290191c2d5311a7375e6f81c4ecd573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610329"
---
# <span data-ttu-id="bcfca-101">Get-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="bcfca-101">Get-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="bcfca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bcfca-102">SYNOPSIS</span></span>
<span data-ttu-id="bcfca-103">Obter informações sobre a rota no Hub IoT</span><span class="sxs-lookup"><span data-stu-id="bcfca-103">Get information about the route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcfca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcfca-104">SYNTAX</span></span>

### <span data-ttu-id="bcfca-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bcfca-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcfca-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bcfca-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcfca-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="bcfca-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcfca-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bcfca-108">DESCRIPTION</span></span>
<span data-ttu-id="bcfca-109">Obter informações sobre a rota. Você pode obter todas as rotas de um hub IoT, obter rotas para um tipo de ponto de extremidade ou obter rotas para um ponto de extremidade específico.</span><span class="sxs-lookup"><span data-stu-id="bcfca-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="bcfca-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcfca-110">EXAMPLES</span></span>

### <span data-ttu-id="bcfca-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bcfca-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="bcfca-112">Obter toda a rota do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="bcfca-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="bcfca-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bcfca-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="bcfca-114">Obter informações de rota do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="bcfca-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="bcfca-115">OS</span><span class="sxs-lookup"><span data-stu-id="bcfca-115">PARAMETERS</span></span>

### <span data-ttu-id="bcfca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcfca-116">-DefaultProfile</span></span>
<span data-ttu-id="bcfca-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bcfca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcfca-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcfca-118">-InputObject</span></span>
<span data-ttu-id="bcfca-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="bcfca-119">IotHub Object</span></span>

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

### <span data-ttu-id="bcfca-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcfca-120">-Name</span></span>
<span data-ttu-id="bcfca-121">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="bcfca-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bcfca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcfca-122">-ResourceGroupName</span></span>
<span data-ttu-id="bcfca-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bcfca-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bcfca-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcfca-124">-ResourceId</span></span>
<span data-ttu-id="bcfca-125">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="bcfca-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="bcfca-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="bcfca-126">-RouteName</span></span>
<span data-ttu-id="bcfca-127">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="bcfca-127">Name of the Route</span></span>

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

### <span data-ttu-id="bcfca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcfca-128">CommonParameters</span></span>
<span data-ttu-id="bcfca-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcfca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcfca-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcfca-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcfca-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bcfca-131">INPUTS</span></span>

### <span data-ttu-id="bcfca-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bcfca-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="bcfca-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bcfca-133">System.String</span></span>

## <span data-ttu-id="bcfca-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bcfca-134">OUTPUTS</span></span>

### <span data-ttu-id="bcfca-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="bcfca-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>
<span data-ttu-id="bcfca-136">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bcfca-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bcfca-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bcfca-137">NOTES</span></span>

## <span data-ttu-id="bcfca-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcfca-138">RELATED LINKS</span></span>
