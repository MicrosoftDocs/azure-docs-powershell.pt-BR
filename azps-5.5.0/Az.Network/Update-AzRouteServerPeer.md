---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
ms.openlocfilehash: 79d907a5ac1b75bdc65d6ea79ffc6c9dea911479
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115042"
---
# <span data-ttu-id="612cb-101">Update-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="612cb-101">Update-AzRouteServerPeer</span></span>

## <span data-ttu-id="612cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="612cb-102">SYNOPSIS</span></span>
<span data-ttu-id="612cb-103">Atualizar um Ponto em um Servidor de Rota do Azure</span><span class="sxs-lookup"><span data-stu-id="612cb-103">Update a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="612cb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="612cb-104">SYNTAX</span></span>

### <span data-ttu-id="612cb-105">RouteServerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="612cb-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="612cb-106">RouteServerNPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="612cb-106">RouteServerNPeerNameParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="612cb-107">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="612cb-107">RouteServerNPeerInputObjectParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -InputObject <PSRouteServerPeer>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="612cb-108">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="612cb-108">RouteServerNPeerResourceIdParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -ResourceId <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="612cb-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="612cb-109">DESCRIPTION</span></span>
<span data-ttu-id="612cb-110">O cmdlet **Update-AzRouteServerPeer** atualiza um Ponto de RouteServer para um Servidor de Rota do Azure</span><span class="sxs-lookup"><span data-stu-id="612cb-110">The **Update-AzRouteServerPeer** cmdlet updates a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="612cb-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="612cb-111">EXAMPLES</span></span>

### <span data-ttu-id="612cb-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="612cb-112">Example 1</span></span>
```powershell
PS C:\> Update-AzRouteServerPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="612cb-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="612cb-113">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/csr'
Update-AzRouteServerPeer -ResourceId $routeServerPeerId  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="612cb-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="612cb-114">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServer -RouteServerName routeServer -PeerName csr
Update-AzRouteServerPeer -ResourceGroupName routeServerRG -InputObject $routeServerPeer  -RouteServerName routeServer
```

## <span data-ttu-id="612cb-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="612cb-115">PARAMETERS</span></span>

### <span data-ttu-id="612cb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="612cb-116">-AsJob</span></span>
<span data-ttu-id="612cb-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="612cb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="612cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="612cb-118">-DefaultProfile</span></span>
<span data-ttu-id="612cb-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="612cb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="612cb-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="612cb-120">-Force</span></span>
<span data-ttu-id="612cb-121">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="612cb-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="612cb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="612cb-122">-InputObject</span></span>
<span data-ttu-id="612cb-123">O objeto de entrada por ponto do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="612cb-123">The route server peer input object.</span></span>

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

### <span data-ttu-id="612cb-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="612cb-124">-PeerAsn</span></span>
<span data-ttu-id="612cb-125">ASN do ponto do servidor de roteamento remoto.</span><span class="sxs-lookup"><span data-stu-id="612cb-125">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="612cb-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="612cb-126">-PeerIp</span></span>
<span data-ttu-id="612cb-127">Ip do ponto do servidor de rota remota.</span><span class="sxs-lookup"><span data-stu-id="612cb-127">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="612cb-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="612cb-128">-PeerName</span></span>
<span data-ttu-id="612cb-129">O nome do peer do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="612cb-129">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="612cb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="612cb-130">-ResourceGroupName</span></span>
<span data-ttu-id="612cb-131">O nome do grupo de recursos do servidor/ponto de rota.</span><span class="sxs-lookup"><span data-stu-id="612cb-131">The resource group name of the route server/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="612cb-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="612cb-132">-ResourceId</span></span>
<span data-ttu-id="612cb-133">A ID do recurso de ponto do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="612cb-133">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="612cb-134">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="612cb-134">-RouteServerName</span></span>
<span data-ttu-id="612cb-135">O servidor de rota onde existe ponto.</span><span class="sxs-lookup"><span data-stu-id="612cb-135">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="612cb-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="612cb-136">-Confirm</span></span>
<span data-ttu-id="612cb-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="612cb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="612cb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="612cb-138">-WhatIf</span></span>
<span data-ttu-id="612cb-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="612cb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="612cb-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="612cb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="612cb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="612cb-141">CommonParameters</span></span>
<span data-ttu-id="612cb-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="612cb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="612cb-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="612cb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="612cb-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="612cb-144">INPUTS</span></span>

### <span data-ttu-id="612cb-145">System.String</span><span class="sxs-lookup"><span data-stu-id="612cb-145">System.String</span></span>

### <span data-ttu-id="612cb-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="612cb-146">System.UInt32</span></span>

### <span data-ttu-id="612cb-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="612cb-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="612cb-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="612cb-148">OUTPUTS</span></span>

### <span data-ttu-id="612cb-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="612cb-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="612cb-150">Notas</span><span class="sxs-lookup"><span data-stu-id="612cb-150">NOTES</span></span>

## <span data-ttu-id="612cb-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="612cb-151">RELATED LINKS</span></span>
