---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113422"
---
# <span data-ttu-id="ee7f1-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ee7f1-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="ee7f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee7f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ee7f1-103">Modifica um Hub Virtual para adicionar uma Tabela de Rota virtual do HUb a ele.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="ee7f1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee7f1-104">SYNTAX</span></span>

### <span data-ttu-id="ee7f1-105">ByVirtualHubName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ee7f1-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee7f1-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ee7f1-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee7f1-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ee7f1-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee7f1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee7f1-108">DESCRIPTION</span></span>
<span data-ttu-id="ee7f1-109">{{ Preencha a Descrição }}</span><span class="sxs-lookup"><span data-stu-id="ee7f1-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="ee7f1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ee7f1-110">EXAMPLES</span></span>

### <span data-ttu-id="ee7f1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ee7f1-111">Example 1</span></span>
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

<span data-ttu-id="ee7f1-112">Primeiro, criamos um objeto de Rota do Hub Virtual e o usamos para criar um recurso de Tabela de Rota do Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="ee7f1-113">Em seguida, definimos esse recurso de tabela de rota para o hub virtual usando o comando Set-AzVirtualHub de rotação.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="ee7f1-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee7f1-114">PARAMETERS</span></span>

### <span data-ttu-id="ee7f1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee7f1-115">-AsJob</span></span>
<span data-ttu-id="ee7f1-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ee7f1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee7f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee7f1-117">-DefaultProfile</span></span>
<span data-ttu-id="ee7f1-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee7f1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee7f1-119">-InputObject</span></span>
<span data-ttu-id="ee7f1-120">O objeto do hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="ee7f1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee7f1-121">-Name</span></span>
<span data-ttu-id="ee7f1-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-122">The resource name.</span></span>

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

### <span data-ttu-id="ee7f1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee7f1-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee7f1-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-124">The resource group name.</span></span>

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

### <span data-ttu-id="ee7f1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee7f1-125">-ResourceId</span></span>
<span data-ttu-id="ee7f1-126">A ID do recurso do hub Virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="ee7f1-127">-Tabela de Rota</span><span class="sxs-lookup"><span data-stu-id="ee7f1-127">-RouteTable</span></span>
<span data-ttu-id="ee7f1-128">As tabelas de rota associadas a este Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-128">The route tables associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="ee7f1-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee7f1-129">-Tag</span></span>
<span data-ttu-id="ee7f1-130">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ee7f1-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ee7f1-131">-Confirm</span></span>
<span data-ttu-id="ee7f1-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee7f1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee7f1-133">-WhatIf</span></span>
<span data-ttu-id="ee7f1-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee7f1-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee7f1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee7f1-136">CommonParameters</span></span>
<span data-ttu-id="ee7f1-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee7f1-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee7f1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee7f1-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="ee7f1-139">INPUTS</span></span>

### <span data-ttu-id="ee7f1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ee7f1-140">System.String</span></span>

### <span data-ttu-id="ee7f1-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ee7f1-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="ee7f1-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="ee7f1-142">OUTPUTS</span></span>

### <span data-ttu-id="ee7f1-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ee7f1-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="ee7f1-144">Notas</span><span class="sxs-lookup"><span data-stu-id="ee7f1-144">NOTES</span></span>

## <span data-ttu-id="ee7f1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee7f1-145">RELATED LINKS</span></span>
