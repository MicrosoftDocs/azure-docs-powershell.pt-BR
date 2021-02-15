---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
ms.openlocfilehash: 20021b2d557b4590a9853d3124930db27286313a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112885"
---
# <span data-ttu-id="0d54f-101">Get-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="0d54f-101">Get-AzRouteServer</span></span>

## <span data-ttu-id="0d54f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d54f-102">SYNOPSIS</span></span>
<span data-ttu-id="0d54f-103">Obter um Servidor de Rota do Azure</span><span class="sxs-lookup"><span data-stu-id="0d54f-103">Get an Azure RouteServer</span></span>

## <span data-ttu-id="0d54f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d54f-104">SYNTAX</span></span>

### <span data-ttu-id="0d54f-105">RouteServerSubscriptionIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0d54f-105">RouteServerSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzRouteServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d54f-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d54f-106">RouteServerNameParameterSet</span></span>
```
Get-AzRouteServer -ResourceGroupName <String> [-RouteServerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d54f-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d54f-107">RouteServerResourceIdParameterSet</span></span>
```
Get-AzRouteServer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d54f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d54f-108">DESCRIPTION</span></span>
<span data-ttu-id="0d54f-109">O cmdlet **Get-AzRouteServer** obtém um Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="0d54f-109">The **Get-AzRouteServer** cmdlet gets an Azure RouteServer</span></span>

## <span data-ttu-id="0d54f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d54f-110">EXAMPLES</span></span>

### <span data-ttu-id="0d54f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d54f-111">Example 1</span></span>
```powershell
Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="0d54f-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0d54f-112">Example 2</span></span>
```powershell
$routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Get-AzRouteServer -ResourceId $routeServerId
```
## <span data-ttu-id="0d54f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d54f-113">PARAMETERS</span></span>

### <span data-ttu-id="0d54f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d54f-114">-DefaultProfile</span></span>
<span data-ttu-id="0d54f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d54f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d54f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d54f-116">-ResourceGroupName</span></span>
<span data-ttu-id="0d54f-117">O nome do grupo de recursos do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="0d54f-117">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d54f-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d54f-118">-ResourceId</span></span>
<span data-ttu-id="0d54f-119">ResourceId do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="0d54f-119">ResourceId of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d54f-120">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="0d54f-120">-RouteServerName</span></span>
<span data-ttu-id="0d54f-121">O nome do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="0d54f-121">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d54f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d54f-122">CommonParameters</span></span>
<span data-ttu-id="0d54f-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d54f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d54f-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d54f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d54f-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="0d54f-125">INPUTS</span></span>

### <span data-ttu-id="0d54f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0d54f-126">System.String</span></span>

## <span data-ttu-id="0d54f-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="0d54f-127">OUTPUTS</span></span>

### <span data-ttu-id="0d54f-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="0d54f-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="0d54f-129">Notas</span><span class="sxs-lookup"><span data-stu-id="0d54f-129">NOTES</span></span>

## <span data-ttu-id="0d54f-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d54f-130">RELATED LINKS</span></span>
