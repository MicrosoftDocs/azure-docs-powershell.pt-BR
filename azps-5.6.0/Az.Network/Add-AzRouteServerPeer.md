---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 430292ba3a387a0b2a0285b26c147c375f114398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888858"
---
# <span data-ttu-id="2685b-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="2685b-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="2685b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2685b-102">SYNOPSIS</span></span>
<span data-ttu-id="2685b-103">Adicionar um par a um RouteServer do Azure</span><span class="sxs-lookup"><span data-stu-id="2685b-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="2685b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2685b-104">SYNTAX</span></span>

### <span data-ttu-id="2685b-105">RouteServerNPeerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2685b-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2685b-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2685b-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2685b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2685b-107">DESCRIPTION</span></span>
<span data-ttu-id="2685b-108">O cmdlet **Add-AzRouteServerPeer** adiciona um RouteServer Peer a um RouteServer do Azure</span><span class="sxs-lookup"><span data-stu-id="2685b-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="2685b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2685b-109">EXAMPLES</span></span>

### <span data-ttu-id="2685b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2685b-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="2685b-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2685b-111">PARAMETERS</span></span>

### <span data-ttu-id="2685b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2685b-112">-AsJob</span></span>
<span data-ttu-id="2685b-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2685b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2685b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2685b-114">-DefaultProfile</span></span>
<span data-ttu-id="2685b-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2685b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2685b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2685b-116">-Force</span></span>
<span data-ttu-id="2685b-117">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="2685b-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2685b-118">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="2685b-118">-PeerAsn</span></span>
<span data-ttu-id="2685b-119">ASN do par de servidor de rota remota.</span><span class="sxs-lookup"><span data-stu-id="2685b-119">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2685b-120">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="2685b-120">-PeerIp</span></span>
<span data-ttu-id="2685b-121">Ip do ponto de servidor de rota remota.</span><span class="sxs-lookup"><span data-stu-id="2685b-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="2685b-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="2685b-122">-PeerName</span></span>
<span data-ttu-id="2685b-123">O nome do par de servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="2685b-123">The name of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2685b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2685b-124">-ResourceGroupName</span></span>
<span data-ttu-id="2685b-125">O nome do grupo de recursos do servidor/ponto de rota.</span><span class="sxs-lookup"><span data-stu-id="2685b-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="2685b-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="2685b-126">-RouteServerName</span></span>
<span data-ttu-id="2685b-127">O servidor de rota onde o par existe.</span><span class="sxs-lookup"><span data-stu-id="2685b-127">The route server where peer exists.</span></span>

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

### <span data-ttu-id="2685b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2685b-128">-Confirm</span></span>
<span data-ttu-id="2685b-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2685b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2685b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2685b-130">-WhatIf</span></span>
<span data-ttu-id="2685b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2685b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2685b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2685b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2685b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2685b-133">CommonParameters</span></span>
<span data-ttu-id="2685b-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2685b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2685b-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2685b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2685b-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2685b-136">INPUTS</span></span>

### <span data-ttu-id="2685b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2685b-137">System.String</span></span>

### <span data-ttu-id="2685b-138">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="2685b-138">System.UInt32</span></span>

## <span data-ttu-id="2685b-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2685b-139">OUTPUTS</span></span>

### <span data-ttu-id="2685b-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="2685b-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="2685b-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="2685b-141">NOTES</span></span>

## <span data-ttu-id="2685b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2685b-142">RELATED LINKS</span></span>
