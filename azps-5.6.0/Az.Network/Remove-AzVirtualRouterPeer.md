---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 2c88ac8c0f3f089a4a26bf0e29ec855281e7f8c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892393"
---
# <span data-ttu-id="547b9-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="547b9-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="547b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="547b9-102">SYNOPSIS</span></span>
<span data-ttu-id="547b9-103">Remove um Par de um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="547b9-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="547b9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="547b9-104">SYNTAX</span></span>

### <span data-ttu-id="547b9-105">VirtualRouterPeerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="547b9-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="547b9-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="547b9-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="547b9-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="547b9-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="547b9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="547b9-108">DESCRIPTION</span></span>
<span data-ttu-id="547b9-109">O cmdlet **Remove-AzVirtualRouterPeer** remove um Par virtualRouter de um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="547b9-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="547b9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="547b9-110">EXAMPLES</span></span>

### <span data-ttu-id="547b9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="547b9-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="547b9-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="547b9-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="547b9-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="547b9-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="547b9-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="547b9-114">PARAMETERS</span></span>

### <span data-ttu-id="547b9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="547b9-115">-AsJob</span></span>
<span data-ttu-id="547b9-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="547b9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="547b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547b9-117">-DefaultProfile</span></span>
<span data-ttu-id="547b9-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="547b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="547b9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="547b9-119">-Force</span></span>
<span data-ttu-id="547b9-120">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="547b9-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="547b9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="547b9-121">-InputObject</span></span>
<span data-ttu-id="547b9-122">O objeto de entrada par do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="547b9-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="547b9-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="547b9-123">-PeerName</span></span>
<span data-ttu-id="547b9-124">O nome do roteador virtual Peer.</span><span class="sxs-lookup"><span data-stu-id="547b9-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="547b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="547b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="547b9-126">O nome do grupo de recursos do roteador virtual/par.</span><span class="sxs-lookup"><span data-stu-id="547b9-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="547b9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="547b9-127">-ResourceId</span></span>
<span data-ttu-id="547b9-128">A ID de recurso de ponto do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="547b9-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="547b9-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="547b9-129">-VirtualRouterName</span></span>
<span data-ttu-id="547b9-130">O roteador virtual onde o par existe.</span><span class="sxs-lookup"><span data-stu-id="547b9-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="547b9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="547b9-131">-Confirm</span></span>
<span data-ttu-id="547b9-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="547b9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="547b9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="547b9-133">-WhatIf</span></span>
<span data-ttu-id="547b9-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="547b9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="547b9-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="547b9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="547b9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547b9-136">CommonParameters</span></span>
<span data-ttu-id="547b9-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="547b9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547b9-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="547b9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547b9-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="547b9-139">INPUTS</span></span>

### <span data-ttu-id="547b9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="547b9-140">System.String</span></span>

### <span data-ttu-id="547b9-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="547b9-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="547b9-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="547b9-142">OUTPUTS</span></span>

### <span data-ttu-id="547b9-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="547b9-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="547b9-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="547b9-144">NOTES</span></span>

## <span data-ttu-id="547b9-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="547b9-145">RELATED LINKS</span></span>
