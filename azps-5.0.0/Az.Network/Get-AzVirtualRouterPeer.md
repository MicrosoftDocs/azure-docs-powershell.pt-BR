---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116903"
---
# <span data-ttu-id="06f15-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="06f15-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="06f15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06f15-102">SYNOPSIS</span></span>
<span data-ttu-id="06f15-103">Obtém um par VirtualRouter em um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="06f15-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="06f15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06f15-104">SYNTAX</span></span>

### <span data-ttu-id="06f15-105">VirtualRouterPeerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="06f15-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06f15-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06f15-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06f15-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06f15-107">DESCRIPTION</span></span>
<span data-ttu-id="06f15-108">O cmdlet **Get-AzVirtualRouterPeer** Obtém um par em um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="06f15-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="06f15-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06f15-109">EXAMPLES</span></span>

### <span data-ttu-id="06f15-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06f15-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="06f15-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="06f15-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="06f15-112">OS</span><span class="sxs-lookup"><span data-stu-id="06f15-112">PARAMETERS</span></span>

### <span data-ttu-id="06f15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f15-113">-DefaultProfile</span></span>
<span data-ttu-id="06f15-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06f15-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06f15-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="06f15-115">-PeerName</span></span>
<span data-ttu-id="06f15-116">O nome do par de roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="06f15-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="06f15-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f15-117">-ResourceGroupName</span></span>
<span data-ttu-id="06f15-118">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="06f15-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="06f15-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06f15-119">-ResourceId</span></span>
<span data-ttu-id="06f15-120">ResourceId do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="06f15-120">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="06f15-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="06f15-121">-VirtualRouterName</span></span>
<span data-ttu-id="06f15-122">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="06f15-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="06f15-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f15-123">CommonParameters</span></span>
<span data-ttu-id="06f15-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06f15-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f15-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06f15-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f15-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06f15-126">INPUTS</span></span>

### <span data-ttu-id="06f15-127">System. String</span><span class="sxs-lookup"><span data-stu-id="06f15-127">System.String</span></span>

## <span data-ttu-id="06f15-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06f15-128">OUTPUTS</span></span>

### <span data-ttu-id="06f15-129">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="06f15-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="06f15-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06f15-130">NOTES</span></span>

## <span data-ttu-id="06f15-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06f15-131">RELATED LINKS</span></span>
