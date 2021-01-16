---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: 259fb6948abee3a00788e68c8d362196e5c12d51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271833"
---
# <span data-ttu-id="28a2b-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="28a2b-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="28a2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="28a2b-103">Rotas de lista sendo anunciadas pelo par roteador virtual específico</span><span class="sxs-lookup"><span data-stu-id="28a2b-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="28a2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28a2b-104">SYNTAX</span></span>

### <span data-ttu-id="28a2b-105">VirtualRouterPeerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="28a2b-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28a2b-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28a2b-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28a2b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28a2b-107">DESCRIPTION</span></span>
<span data-ttu-id="28a2b-108">Considerando um par de roteador virtual por nome ou por objeto, enumere as rotas sendo anunciadas para esse ponto por um roteador virtual específico.</span><span class="sxs-lookup"><span data-stu-id="28a2b-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="28a2b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28a2b-109">EXAMPLES</span></span>

### <span data-ttu-id="28a2b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28a2b-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="28a2b-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="28a2b-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="28a2b-112">OS</span><span class="sxs-lookup"><span data-stu-id="28a2b-112">PARAMETERS</span></span>

### <span data-ttu-id="28a2b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28a2b-113">-AsJob</span></span>
<span data-ttu-id="28a2b-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="28a2b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28a2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a2b-115">-DefaultProfile</span></span>
<span data-ttu-id="28a2b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28a2b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a2b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28a2b-117">-InputObject</span></span>
<span data-ttu-id="28a2b-118">O objeto de entrada de par do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="28a2b-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="28a2b-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="28a2b-119">-PeerName</span></span>
<span data-ttu-id="28a2b-120">Nome de par do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="28a2b-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="28a2b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28a2b-121">-ResourceGroupName</span></span>
<span data-ttu-id="28a2b-122">Nome do grupo de recursos de par do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="28a2b-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="28a2b-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="28a2b-123">-VirtualRouterName</span></span>
<span data-ttu-id="28a2b-124">Nome do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="28a2b-124">Virtual router name</span></span>

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

### <span data-ttu-id="28a2b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a2b-125">CommonParameters</span></span>
<span data-ttu-id="28a2b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a2b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a2b-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28a2b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a2b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28a2b-128">INPUTS</span></span>

### <span data-ttu-id="28a2b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="28a2b-129">System.String</span></span>

### <span data-ttu-id="28a2b-130">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="28a2b-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="28a2b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28a2b-131">OUTPUTS</span></span>

### <span data-ttu-id="28a2b-132">Microsoft. Azure. Commands. Network. Models. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="28a2b-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="28a2b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28a2b-133">NOTES</span></span>

## <span data-ttu-id="28a2b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28a2b-134">RELATED LINKS</span></span>
