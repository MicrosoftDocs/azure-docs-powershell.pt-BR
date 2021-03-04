---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
ms.openlocfilehash: 3c0be49a09758648bcd2301f2643577ea8dcd951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885337"
---
# <span data-ttu-id="bd807-101">Update-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="bd807-101">Update-AzRouteServerPeer</span></span>

## <span data-ttu-id="bd807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd807-102">SYNOPSIS</span></span>
<span data-ttu-id="bd807-103">Atualizar um Par em um RouteServer do Azure</span><span class="sxs-lookup"><span data-stu-id="bd807-103">Update a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="bd807-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bd807-104">SYNTAX</span></span>

### <span data-ttu-id="bd807-105">RouteServerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bd807-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd807-106">RouteServerNPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd807-106">RouteServerNPeerNameParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd807-107">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd807-107">RouteServerNPeerInputObjectParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -InputObject <PSRouteServerPeer>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd807-108">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd807-108">RouteServerNPeerResourceIdParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -ResourceId <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd807-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bd807-109">DESCRIPTION</span></span>
<span data-ttu-id="bd807-110">O cmdlet **Update-AzRouteServerPeer** atualiza um RouteServer Peer para um RouteServer do Azure</span><span class="sxs-lookup"><span data-stu-id="bd807-110">The **Update-AzRouteServerPeer** cmdlet updates a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="bd807-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd807-111">EXAMPLES</span></span>

### <span data-ttu-id="bd807-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bd807-112">Example 1</span></span>
```powershell
PS C:\> Update-AzRouteServerPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="bd807-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bd807-113">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/csr'
Update-AzRouteServerPeer -ResourceId $routeServerPeerId  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="bd807-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bd807-114">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServer -RouteServerName routeServer -PeerName csr
Update-AzRouteServerPeer -ResourceGroupName routeServerRG -InputObject $routeServerPeer  -RouteServerName routeServer
```

## <span data-ttu-id="bd807-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bd807-115">PARAMETERS</span></span>

### <span data-ttu-id="bd807-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd807-116">-AsJob</span></span>
<span data-ttu-id="bd807-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bd807-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd807-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd807-118">-DefaultProfile</span></span>
<span data-ttu-id="bd807-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd807-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd807-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bd807-120">-Force</span></span>
<span data-ttu-id="bd807-121">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="bd807-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bd807-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd807-122">-InputObject</span></span>
<span data-ttu-id="bd807-123">O objeto de entrada de ponto de servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="bd807-123">The route server peer input object.</span></span>

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

### <span data-ttu-id="bd807-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="bd807-124">-PeerAsn</span></span>
<span data-ttu-id="bd807-125">ASN do par de servidor de rota remota.</span><span class="sxs-lookup"><span data-stu-id="bd807-125">ASN of remote route server peer.</span></span>

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

### <span data-ttu-id="bd807-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="bd807-126">-PeerIp</span></span>
<span data-ttu-id="bd807-127">Ip do ponto de servidor de rota remota.</span><span class="sxs-lookup"><span data-stu-id="bd807-127">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="bd807-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="bd807-128">-PeerName</span></span>
<span data-ttu-id="bd807-129">O nome do servidor de rota Peer.</span><span class="sxs-lookup"><span data-stu-id="bd807-129">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="bd807-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd807-130">-ResourceGroupName</span></span>
<span data-ttu-id="bd807-131">O nome do grupo de recursos do servidor/ponto de rota.</span><span class="sxs-lookup"><span data-stu-id="bd807-131">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="bd807-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd807-132">-ResourceId</span></span>
<span data-ttu-id="bd807-133">A ID de recurso de par do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="bd807-133">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="bd807-134">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="bd807-134">-RouteServerName</span></span>
<span data-ttu-id="bd807-135">O servidor de rota onde o par existe.</span><span class="sxs-lookup"><span data-stu-id="bd807-135">The route server where peer exists.</span></span>

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

### <span data-ttu-id="bd807-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd807-136">-Confirm</span></span>
<span data-ttu-id="bd807-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd807-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd807-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd807-138">-WhatIf</span></span>
<span data-ttu-id="bd807-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bd807-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd807-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd807-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd807-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd807-141">CommonParameters</span></span>
<span data-ttu-id="bd807-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd807-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd807-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd807-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd807-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd807-144">INPUTS</span></span>

### <span data-ttu-id="bd807-145">System.String</span><span class="sxs-lookup"><span data-stu-id="bd807-145">System.String</span></span>

### <span data-ttu-id="bd807-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="bd807-146">System.UInt32</span></span>

### <span data-ttu-id="bd807-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="bd807-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="bd807-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bd807-148">OUTPUTS</span></span>

### <span data-ttu-id="bd807-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="bd807-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="bd807-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="bd807-150">NOTES</span></span>

## <span data-ttu-id="bd807-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd807-151">RELATED LINKS</span></span>
