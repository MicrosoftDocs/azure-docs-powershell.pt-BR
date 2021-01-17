---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 242a3985d75e0a741c5e2175c098139b448f3e70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434594"
---
# <span data-ttu-id="9b244-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="9b244-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="9b244-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b244-102">SYNOPSIS</span></span>
<span data-ttu-id="9b244-103">Atualizar um par em um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="9b244-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="9b244-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b244-104">SYNTAX</span></span>

### <span data-ttu-id="9b244-105">VirtualRouterNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9b244-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b244-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b244-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b244-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b244-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b244-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b244-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b244-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b244-109">DESCRIPTION</span></span>
<span data-ttu-id="9b244-110">O cmdlet **Update-AzVirtualRouterPeer** atualiza um par VirtualRouter para um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="9b244-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="9b244-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b244-111">EXAMPLES</span></span>

### <span data-ttu-id="9b244-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b244-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="9b244-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9b244-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="9b244-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9b244-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="9b244-115">OS</span><span class="sxs-lookup"><span data-stu-id="9b244-115">PARAMETERS</span></span>

### <span data-ttu-id="9b244-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b244-116">-AsJob</span></span>
<span data-ttu-id="9b244-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9b244-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b244-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b244-118">-DefaultProfile</span></span>
<span data-ttu-id="9b244-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b244-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b244-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9b244-120">-Force</span></span>
<span data-ttu-id="9b244-121">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="9b244-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9b244-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b244-122">-InputObject</span></span>
<span data-ttu-id="9b244-123">O objeto de entrada de par do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="9b244-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="9b244-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="9b244-124">-PeerAsn</span></span>
<span data-ttu-id="9b244-125">ASN peer.</span><span class="sxs-lookup"><span data-stu-id="9b244-125">Peer ASN.</span></span>

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

### <span data-ttu-id="9b244-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="9b244-126">-PeerIp</span></span>
<span data-ttu-id="9b244-127">IP de par.</span><span class="sxs-lookup"><span data-stu-id="9b244-127">Peer Ip.</span></span>

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

### <span data-ttu-id="9b244-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="9b244-128">-PeerName</span></span>
<span data-ttu-id="9b244-129">O nome do par de roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="9b244-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="9b244-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b244-130">-ResourceGroupName</span></span>
<span data-ttu-id="9b244-131">O nome do grupo de recursos do roteador virtual/par.</span><span class="sxs-lookup"><span data-stu-id="9b244-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="9b244-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b244-132">-ResourceId</span></span>
<span data-ttu-id="9b244-133">A ID do recurso par do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="9b244-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="9b244-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="9b244-134">-VirtualRouterName</span></span>
<span data-ttu-id="9b244-135">O roteador virtual em que existe o par.</span><span class="sxs-lookup"><span data-stu-id="9b244-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="9b244-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b244-136">-Confirm</span></span>
<span data-ttu-id="9b244-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b244-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b244-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b244-138">-WhatIf</span></span>
<span data-ttu-id="9b244-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b244-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b244-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b244-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b244-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b244-141">CommonParameters</span></span>
<span data-ttu-id="9b244-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b244-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b244-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b244-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b244-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b244-144">INPUTS</span></span>

### <span data-ttu-id="9b244-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9b244-145">System.String</span></span>

### <span data-ttu-id="9b244-146">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="9b244-146">System.UInt32</span></span>

### <span data-ttu-id="9b244-147">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="9b244-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="9b244-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b244-148">OUTPUTS</span></span>

### <span data-ttu-id="9b244-149">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="9b244-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="9b244-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b244-150">NOTES</span></span>

## <span data-ttu-id="9b244-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b244-151">RELATED LINKS</span></span>
