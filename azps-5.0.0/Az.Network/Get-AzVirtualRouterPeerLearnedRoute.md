---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116901"
---
# <span data-ttu-id="cd3d2-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="cd3d2-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="cd3d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3d2-103">Listar rotas aprendidas por um par de roteador virtual específico</span><span class="sxs-lookup"><span data-stu-id="cd3d2-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="cd3d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd3d2-104">SYNTAX</span></span>

### <span data-ttu-id="cd3d2-105">VirtualRouterPeerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cd3d2-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd3d2-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd3d2-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd3d2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd3d2-107">DESCRIPTION</span></span>
<span data-ttu-id="cd3d2-108">Enumere rotas aprendidas por um roteador virtual peer de outras fontes.</span><span class="sxs-lookup"><span data-stu-id="cd3d2-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="cd3d2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd3d2-109">EXAMPLES</span></span>

### <span data-ttu-id="cd3d2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd3d2-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="cd3d2-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cd3d2-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="cd3d2-112">OS</span><span class="sxs-lookup"><span data-stu-id="cd3d2-112">PARAMETERS</span></span>

### <span data-ttu-id="cd3d2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd3d2-113">-AsJob</span></span>
<span data-ttu-id="cd3d2-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cd3d2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd3d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3d2-115">-DefaultProfile</span></span>
<span data-ttu-id="cd3d2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd3d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd3d2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd3d2-117">-InputObject</span></span>
<span data-ttu-id="cd3d2-118">O objeto de entrada de par do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="cd3d2-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="cd3d2-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="cd3d2-119">-PeerName</span></span>
<span data-ttu-id="cd3d2-120">Nome de par do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="cd3d2-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="cd3d2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd3d2-121">-ResourceGroupName</span></span>
<span data-ttu-id="cd3d2-122">Nome do grupo de recursos de par do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="cd3d2-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="cd3d2-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="cd3d2-123">-VirtualRouterName</span></span>
<span data-ttu-id="cd3d2-124">Nome do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="cd3d2-124">Virtual router name</span></span>

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

### <span data-ttu-id="cd3d2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3d2-125">CommonParameters</span></span>
<span data-ttu-id="cd3d2-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd3d2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3d2-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd3d2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3d2-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd3d2-128">INPUTS</span></span>

### <span data-ttu-id="cd3d2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cd3d2-129">System.String</span></span>

### <span data-ttu-id="cd3d2-130">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="cd3d2-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="cd3d2-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd3d2-131">OUTPUTS</span></span>

### <span data-ttu-id="cd3d2-132">Microsoft. Azure. Commands. Network. Models. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="cd3d2-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="cd3d2-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd3d2-133">NOTES</span></span>

## <span data-ttu-id="cd3d2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd3d2-134">RELATED LINKS</span></span>
