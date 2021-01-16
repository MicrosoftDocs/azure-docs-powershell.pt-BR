---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: 259fb6948abee3a00788e68c8d362196e5c12d51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261493"
---
# <span data-ttu-id="baaa9-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="baaa9-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="baaa9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="baaa9-102">SYNOPSIS</span></span>
<span data-ttu-id="baaa9-103">Rotas de lista sendo anunciadas pelo par roteador virtual específico</span><span class="sxs-lookup"><span data-stu-id="baaa9-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="baaa9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="baaa9-104">SYNTAX</span></span>

### <span data-ttu-id="baaa9-105">VirtualRouterPeerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="baaa9-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baaa9-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="baaa9-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baaa9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="baaa9-107">DESCRIPTION</span></span>
<span data-ttu-id="baaa9-108">Considerando um par de roteador virtual por nome ou por objeto, enumere as rotas sendo anunciadas para esse ponto por um roteador virtual específico.</span><span class="sxs-lookup"><span data-stu-id="baaa9-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="baaa9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="baaa9-109">EXAMPLES</span></span>

### <span data-ttu-id="baaa9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="baaa9-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="baaa9-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="baaa9-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="baaa9-112">OS</span><span class="sxs-lookup"><span data-stu-id="baaa9-112">PARAMETERS</span></span>

### <span data-ttu-id="baaa9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="baaa9-113">-AsJob</span></span>
<span data-ttu-id="baaa9-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="baaa9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="baaa9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baaa9-115">-DefaultProfile</span></span>
<span data-ttu-id="baaa9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="baaa9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baaa9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="baaa9-117">-InputObject</span></span>
<span data-ttu-id="baaa9-118">O objeto de entrada de par do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="baaa9-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="baaa9-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="baaa9-119">-PeerName</span></span>
<span data-ttu-id="baaa9-120">Nome de par do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="baaa9-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="baaa9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baaa9-121">-ResourceGroupName</span></span>
<span data-ttu-id="baaa9-122">Nome do grupo de recursos de par do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="baaa9-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="baaa9-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="baaa9-123">-VirtualRouterName</span></span>
<span data-ttu-id="baaa9-124">Nome do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="baaa9-124">Virtual router name</span></span>

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

### <span data-ttu-id="baaa9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baaa9-125">CommonParameters</span></span>
<span data-ttu-id="baaa9-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baaa9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baaa9-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baaa9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baaa9-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="baaa9-128">INPUTS</span></span>

### <span data-ttu-id="baaa9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="baaa9-129">System.String</span></span>

### <span data-ttu-id="baaa9-130">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="baaa9-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="baaa9-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="baaa9-131">OUTPUTS</span></span>

### <span data-ttu-id="baaa9-132">Microsoft. Azure. Commands. Network. Models. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="baaa9-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="baaa9-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="baaa9-133">NOTES</span></span>

## <span data-ttu-id="baaa9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="baaa9-134">RELATED LINKS</span></span>
