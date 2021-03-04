---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 9e82946d13ac830d50affc621c965cfe8b81c503
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885321"
---
# <span data-ttu-id="5c274-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="5c274-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="5c274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c274-102">SYNOPSIS</span></span>
<span data-ttu-id="5c274-103">Atualizar um Par em um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5c274-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="5c274-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5c274-104">SYNTAX</span></span>

### <span data-ttu-id="5c274-105">VirtualRouterNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5c274-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c274-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c274-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c274-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c274-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c274-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c274-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c274-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5c274-109">DESCRIPTION</span></span>
<span data-ttu-id="5c274-110">O cmdlet **Update-AzVirtualRouterPeer** atualiza um Par virtualRouter para um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5c274-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="5c274-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c274-111">EXAMPLES</span></span>

### <span data-ttu-id="5c274-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5c274-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="5c274-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5c274-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="5c274-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5c274-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="5c274-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5c274-115">PARAMETERS</span></span>

### <span data-ttu-id="5c274-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c274-116">-AsJob</span></span>
<span data-ttu-id="5c274-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5c274-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c274-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c274-118">-DefaultProfile</span></span>
<span data-ttu-id="5c274-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c274-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c274-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5c274-120">-Force</span></span>
<span data-ttu-id="5c274-121">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="5c274-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5c274-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c274-122">-InputObject</span></span>
<span data-ttu-id="5c274-123">O objeto de entrada par do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="5c274-123">The virtual router peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c274-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="5c274-124">-PeerAsn</span></span>
<span data-ttu-id="5c274-125">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="5c274-125">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c274-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="5c274-126">-PeerIp</span></span>
<span data-ttu-id="5c274-127">Peer Ip.</span><span class="sxs-lookup"><span data-stu-id="5c274-127">Peer Ip.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c274-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="5c274-128">-PeerName</span></span>
<span data-ttu-id="5c274-129">O nome do roteador virtual Peer.</span><span class="sxs-lookup"><span data-stu-id="5c274-129">The name of the virtual router Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c274-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c274-130">-ResourceGroupName</span></span>
<span data-ttu-id="5c274-131">O nome do grupo de recursos do roteador virtual/par.</span><span class="sxs-lookup"><span data-stu-id="5c274-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="5c274-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c274-132">-ResourceId</span></span>
<span data-ttu-id="5c274-133">A ID de recurso de ponto do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="5c274-133">The virtual router peer resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c274-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="5c274-134">-VirtualRouterName</span></span>
<span data-ttu-id="5c274-135">O roteador virtual onde o par existe.</span><span class="sxs-lookup"><span data-stu-id="5c274-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="5c274-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c274-136">-Confirm</span></span>
<span data-ttu-id="5c274-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c274-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c274-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c274-138">-WhatIf</span></span>
<span data-ttu-id="5c274-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c274-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c274-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c274-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c274-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c274-141">CommonParameters</span></span>
<span data-ttu-id="5c274-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c274-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c274-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c274-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c274-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c274-144">INPUTS</span></span>

### <span data-ttu-id="5c274-145">System.String</span><span class="sxs-lookup"><span data-stu-id="5c274-145">System.String</span></span>

### <span data-ttu-id="5c274-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="5c274-146">System.UInt32</span></span>

### <span data-ttu-id="5c274-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="5c274-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="5c274-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5c274-148">OUTPUTS</span></span>

### <span data-ttu-id="5c274-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5c274-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="5c274-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="5c274-150">NOTES</span></span>

## <span data-ttu-id="5c274-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c274-151">RELATED LINKS</span></span>
