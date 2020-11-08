---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124446"
---
# <span data-ttu-id="3675b-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3675b-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="3675b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3675b-102">SYNOPSIS</span></span>
<span data-ttu-id="3675b-103">Modifica um hub virtual para adicionar uma tabela de roteiros do HUb virtual a ele.</span><span class="sxs-lookup"><span data-stu-id="3675b-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="3675b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3675b-104">SYNTAX</span></span>

### <span data-ttu-id="3675b-105">ByVirtualHubName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3675b-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3675b-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="3675b-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3675b-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="3675b-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3675b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3675b-108">DESCRIPTION</span></span>
<span data-ttu-id="3675b-109">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="3675b-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="3675b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3675b-110">EXAMPLES</span></span>

### <span data-ttu-id="3675b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3675b-111">Example 1</span></span>
```powershell
PS C:\> $existingHub�=�Get-AzVirtualHub�-ResourceGroupName�"testRg"�-Name�"westushub"
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> $routeTable1�=�Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"
PS C:\> Set-AzVirtualHub�-VirtualHub�$existingHub�-RouteTable�@($routeTable1)

VirtualWan                            : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/testWan
ResourceGroupName                     : testRg
Name                                  : westushub
Id                                    : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubswestushub
AddressPrefix                         : 10.40.0.0/16
RouteTable                            : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkExpressRouteConnections :
RouteTables                           : {routeTable1}
Location                              : westus
Sku                                   : Standard
Type                                  : Microsoft.Network/virtualHubs
ProvisioningState                     : Succeeded
```

<span data-ttu-id="3675b-112">Primeiro, criamos um objeto de rota de Hub virtual e o usamos para criar um recurso de tabela de rota de Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="3675b-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="3675b-113">Em seguida, definimos esse recurso de tabela de rota para o Hub virtual usando o comando Set-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="3675b-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="3675b-114">OS</span><span class="sxs-lookup"><span data-stu-id="3675b-114">PARAMETERS</span></span>

### <span data-ttu-id="3675b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3675b-115">-AsJob</span></span>
<span data-ttu-id="3675b-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3675b-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3675b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3675b-117">-DefaultProfile</span></span>
<span data-ttu-id="3675b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3675b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3675b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3675b-119">-InputObject</span></span>
<span data-ttu-id="3675b-120">O objeto de Hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="3675b-120">The Virtual hub object to be modified.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3675b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3675b-121">-Name</span></span>
<span data-ttu-id="3675b-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3675b-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3675b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3675b-123">-ResourceGroupName</span></span>
<span data-ttu-id="3675b-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3675b-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3675b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3675b-125">-ResourceId</span></span>
<span data-ttu-id="3675b-126">A ID do recurso do Hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="3675b-126">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3675b-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="3675b-127">-RouteTable</span></span>
<span data-ttu-id="3675b-128">As tabelas de rota associadas a esse Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="3675b-128">The route tables associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3675b-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="3675b-129">-Tag</span></span>
<span data-ttu-id="3675b-130">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="3675b-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3675b-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3675b-131">-Confirm</span></span>
<span data-ttu-id="3675b-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3675b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3675b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3675b-133">-WhatIf</span></span>
<span data-ttu-id="3675b-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3675b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3675b-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3675b-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3675b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3675b-136">CommonParameters</span></span>
<span data-ttu-id="3675b-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3675b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3675b-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3675b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3675b-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3675b-139">INPUTS</span></span>

### <span data-ttu-id="3675b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3675b-140">System.String</span></span>

### <span data-ttu-id="3675b-141">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3675b-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="3675b-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3675b-142">OUTPUTS</span></span>

### <span data-ttu-id="3675b-143">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3675b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="3675b-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3675b-144">NOTES</span></span>

## <span data-ttu-id="3675b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3675b-145">RELATED LINKS</span></span>
