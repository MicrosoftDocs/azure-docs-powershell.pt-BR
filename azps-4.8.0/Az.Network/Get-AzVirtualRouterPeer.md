---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114126"
---
# <span data-ttu-id="e8440-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="e8440-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="e8440-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8440-102">SYNOPSIS</span></span>
<span data-ttu-id="e8440-103">Obtém um par VirtualRouter em um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="e8440-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="e8440-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8440-104">SYNTAX</span></span>

### <span data-ttu-id="e8440-105">VirtualRouterPeerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e8440-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8440-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8440-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8440-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8440-107">DESCRIPTION</span></span>
<span data-ttu-id="e8440-108">O cmdlet **Get-AzVirtualRouterPeer** Obtém um par em um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="e8440-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="e8440-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8440-109">EXAMPLES</span></span>

### <span data-ttu-id="e8440-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8440-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="e8440-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e8440-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="e8440-112">OS</span><span class="sxs-lookup"><span data-stu-id="e8440-112">PARAMETERS</span></span>

### <span data-ttu-id="e8440-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8440-113">-DefaultProfile</span></span>
<span data-ttu-id="e8440-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8440-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8440-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="e8440-115">-PeerName</span></span>
<span data-ttu-id="e8440-116">O nome do par de roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="e8440-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="e8440-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8440-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8440-118">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="e8440-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="e8440-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8440-119">-ResourceId</span></span>
<span data-ttu-id="e8440-120">ResourceId do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="e8440-120">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="e8440-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="e8440-121">-VirtualRouterName</span></span>
<span data-ttu-id="e8440-122">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="e8440-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="e8440-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8440-123">CommonParameters</span></span>
<span data-ttu-id="e8440-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8440-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8440-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8440-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8440-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8440-126">INPUTS</span></span>

### <span data-ttu-id="e8440-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e8440-127">System.String</span></span>

## <span data-ttu-id="e8440-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8440-128">OUTPUTS</span></span>

### <span data-ttu-id="e8440-129">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="e8440-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="e8440-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8440-130">NOTES</span></span>

## <span data-ttu-id="e8440-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8440-131">RELATED LINKS</span></span>
