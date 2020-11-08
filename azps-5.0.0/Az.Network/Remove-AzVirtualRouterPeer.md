---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116073"
---
# <span data-ttu-id="18400-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="18400-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="18400-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18400-102">SYNOPSIS</span></span>
<span data-ttu-id="18400-103">Remove um par de um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="18400-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="18400-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18400-104">SYNTAX</span></span>

### <span data-ttu-id="18400-105">VirtualRouterPeerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="18400-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18400-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18400-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18400-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18400-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18400-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18400-108">DESCRIPTION</span></span>
<span data-ttu-id="18400-109">O cmdlet **Remove-AzVirtualRouterPeer** remove um par VirtualRouter de um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="18400-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="18400-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18400-110">EXAMPLES</span></span>

### <span data-ttu-id="18400-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18400-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="18400-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="18400-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="18400-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="18400-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="18400-114">OS</span><span class="sxs-lookup"><span data-stu-id="18400-114">PARAMETERS</span></span>

### <span data-ttu-id="18400-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18400-115">-AsJob</span></span>
<span data-ttu-id="18400-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="18400-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18400-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18400-117">-DefaultProfile</span></span>
<span data-ttu-id="18400-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18400-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18400-119">-Force</span><span class="sxs-lookup"><span data-stu-id="18400-119">-Force</span></span>
<span data-ttu-id="18400-120">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="18400-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="18400-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18400-121">-InputObject</span></span>
<span data-ttu-id="18400-122">O objeto de entrada de par do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="18400-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="18400-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="18400-123">-PeerName</span></span>
<span data-ttu-id="18400-124">O nome do par de roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="18400-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="18400-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18400-125">-ResourceGroupName</span></span>
<span data-ttu-id="18400-126">O nome do grupo de recursos do roteador virtual/par.</span><span class="sxs-lookup"><span data-stu-id="18400-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="18400-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18400-127">-ResourceId</span></span>
<span data-ttu-id="18400-128">A ID do recurso par do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="18400-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="18400-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="18400-129">-VirtualRouterName</span></span>
<span data-ttu-id="18400-130">O roteador virtual em que existe o par.</span><span class="sxs-lookup"><span data-stu-id="18400-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="18400-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18400-131">-Confirm</span></span>
<span data-ttu-id="18400-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18400-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18400-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18400-133">-WhatIf</span></span>
<span data-ttu-id="18400-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18400-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18400-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18400-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18400-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18400-136">CommonParameters</span></span>
<span data-ttu-id="18400-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18400-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18400-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18400-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18400-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18400-139">INPUTS</span></span>

### <span data-ttu-id="18400-140">System. String</span><span class="sxs-lookup"><span data-stu-id="18400-140">System.String</span></span>

### <span data-ttu-id="18400-141">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="18400-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="18400-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18400-142">OUTPUTS</span></span>

### <span data-ttu-id="18400-143">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="18400-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="18400-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18400-144">NOTES</span></span>

## <span data-ttu-id="18400-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18400-145">RELATED LINKS</span></span>
