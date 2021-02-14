---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
ms.openlocfilehash: d177c0dfa5ff59fde0adfe8ac4e3598ae70127f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117340"
---
# <span data-ttu-id="ea47d-101">Remove-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="ea47d-101">Remove-AzRouteServerPeer</span></span>

## <span data-ttu-id="ea47d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea47d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea47d-103">Remove um Ponto de um Servidor de Rota do Azure</span><span class="sxs-lookup"><span data-stu-id="ea47d-103">Removes a Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="ea47d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea47d-104">SYNTAX</span></span>

### <span data-ttu-id="ea47d-105">RouteServerNPeerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ea47d-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea47d-106">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea47d-106">RouteServerNPeerInputObjectParameterSet</span></span>
```
Remove-AzRouteServerPeer -InputObject <PSRouteServerPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea47d-107">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea47d-107">RouteServerNPeerResourceIdParameterSet</span></span>
```
Remove-AzRouteServerPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea47d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea47d-108">DESCRIPTION</span></span>
<span data-ttu-id="ea47d-109">O cmdlet **Remove-AzRouteServerPeer** remove um Ponto de RouteServer de um Servidor de Rota do Azure</span><span class="sxs-lookup"><span data-stu-id="ea47d-109">The **Remove-AzRouteServerPeer** cmdlet removes a RouteServer Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="ea47d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ea47d-110">EXAMPLES</span></span>

### <span data-ttu-id="ea47d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea47d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServerPeer -PeerName peer -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="ea47d-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ea47d-112">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Remove-AzRouteServerPeer -ResourceId $RouteServerPeerId
```

### <span data-ttu-id="ea47d-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ea47d-113">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
Remove-AzRouteServerPeer -InputObject $RouteServerPeer
```
## <span data-ttu-id="ea47d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea47d-114">PARAMETERS</span></span>

### <span data-ttu-id="ea47d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea47d-115">-AsJob</span></span>
<span data-ttu-id="ea47d-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ea47d-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea47d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea47d-117">-DefaultProfile</span></span>
<span data-ttu-id="ea47d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea47d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea47d-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="ea47d-119">-Force</span></span>
<span data-ttu-id="ea47d-120">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="ea47d-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea47d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea47d-121">-InputObject</span></span>
<span data-ttu-id="ea47d-122">O objeto de entrada por ponto do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="ea47d-122">The route server peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer
Parameter Sets: RouteServerNPeerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea47d-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="ea47d-123">-PeerName</span></span>
<span data-ttu-id="ea47d-124">O nome do peer do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="ea47d-124">The name of the route server Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea47d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea47d-125">-ResourceGroupName</span></span>
<span data-ttu-id="ea47d-126">O nome do grupo de recursos do servidor/ponto de rota.</span><span class="sxs-lookup"><span data-stu-id="ea47d-126">The resource group name of the route server/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea47d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea47d-127">-ResourceId</span></span>
<span data-ttu-id="ea47d-128">A ID do recurso de ponto do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="ea47d-128">The route server peer resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea47d-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="ea47d-129">-RouteServerName</span></span>
<span data-ttu-id="ea47d-130">O servidor de rota onde existe ponto.</span><span class="sxs-lookup"><span data-stu-id="ea47d-130">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea47d-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ea47d-131">-Confirm</span></span>
<span data-ttu-id="ea47d-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea47d-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea47d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea47d-133">-WhatIf</span></span>
<span data-ttu-id="ea47d-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ea47d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea47d-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea47d-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea47d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea47d-136">CommonParameters</span></span>
<span data-ttu-id="ea47d-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea47d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea47d-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea47d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea47d-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="ea47d-139">INPUTS</span></span>

### <span data-ttu-id="ea47d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ea47d-140">System.String</span></span>

### <span data-ttu-id="ea47d-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="ea47d-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="ea47d-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="ea47d-142">OUTPUTS</span></span>

### <span data-ttu-id="ea47d-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="ea47d-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="ea47d-144">Notas</span><span class="sxs-lookup"><span data-stu-id="ea47d-144">NOTES</span></span>

## <span data-ttu-id="ea47d-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea47d-145">RELATED LINKS</span></span>
