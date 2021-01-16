---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261491"
---
# <span data-ttu-id="4aa86-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="4aa86-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="4aa86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4aa86-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa86-103">Listar rotas aprendidas por um par de roteador virtual específico</span><span class="sxs-lookup"><span data-stu-id="4aa86-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="4aa86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aa86-104">SYNTAX</span></span>

### <span data-ttu-id="4aa86-105">VirtualRouterPeerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4aa86-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aa86-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aa86-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aa86-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4aa86-107">DESCRIPTION</span></span>
<span data-ttu-id="4aa86-108">Enumere rotas aprendidas por um roteador virtual peer de outras fontes.</span><span class="sxs-lookup"><span data-stu-id="4aa86-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="4aa86-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4aa86-109">EXAMPLES</span></span>

### <span data-ttu-id="4aa86-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4aa86-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="4aa86-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4aa86-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="4aa86-112">OS</span><span class="sxs-lookup"><span data-stu-id="4aa86-112">PARAMETERS</span></span>

### <span data-ttu-id="4aa86-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4aa86-113">-AsJob</span></span>
<span data-ttu-id="4aa86-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4aa86-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4aa86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa86-115">-DefaultProfile</span></span>
<span data-ttu-id="4aa86-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4aa86-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aa86-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4aa86-117">-InputObject</span></span>
<span data-ttu-id="4aa86-118">O objeto de entrada de par do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="4aa86-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="4aa86-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="4aa86-119">-PeerName</span></span>
<span data-ttu-id="4aa86-120">Nome de par do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="4aa86-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="4aa86-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aa86-121">-ResourceGroupName</span></span>
<span data-ttu-id="4aa86-122">Nome do grupo de recursos de par do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="4aa86-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="4aa86-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="4aa86-123">-VirtualRouterName</span></span>
<span data-ttu-id="4aa86-124">Nome do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="4aa86-124">Virtual router name</span></span>

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

### <span data-ttu-id="4aa86-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa86-125">CommonParameters</span></span>
<span data-ttu-id="4aa86-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aa86-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa86-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4aa86-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa86-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4aa86-128">INPUTS</span></span>

### <span data-ttu-id="4aa86-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4aa86-129">System.String</span></span>

### <span data-ttu-id="4aa86-130">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="4aa86-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="4aa86-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4aa86-131">OUTPUTS</span></span>

### <span data-ttu-id="4aa86-132">Microsoft. Azure. Commands. Network. Models. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="4aa86-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="4aa86-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4aa86-133">NOTES</span></span>

## <span data-ttu-id="4aa86-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4aa86-134">RELATED LINKS</span></span>
