---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: 259fb6948abee3a00788e68c8d362196e5c12d51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112865"
---
# <span data-ttu-id="d7ed6-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="d7ed6-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="d7ed6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ed6-103">Rotas de lista sendo anunciadas por ponto de roteador virtual específico</span><span class="sxs-lookup"><span data-stu-id="d7ed6-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="d7ed6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7ed6-104">SYNTAX</span></span>

### <span data-ttu-id="d7ed6-105">VirtualRouterPeerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d7ed6-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7ed6-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7ed6-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7ed6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7ed6-107">DESCRIPTION</span></span>
<span data-ttu-id="d7ed6-108">Dado um ponto de roteador virtual por nome ou por objeto, enumerar rotas que estão sendo anunciadas para esse ponto por um roteador virtual específico.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="d7ed6-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7ed6-109">EXAMPLES</span></span>

### <span data-ttu-id="d7ed6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d7ed6-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="d7ed6-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d7ed6-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="d7ed6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7ed6-112">PARAMETERS</span></span>

### <span data-ttu-id="d7ed6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7ed6-113">-AsJob</span></span>
<span data-ttu-id="d7ed6-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d7ed6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7ed6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ed6-115">-DefaultProfile</span></span>
<span data-ttu-id="d7ed6-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7ed6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7ed6-117">-InputObject</span></span>
<span data-ttu-id="d7ed6-118">O objeto de entrada de ponto de roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="d7ed6-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="d7ed6-119">-PeerName</span></span>
<span data-ttu-id="d7ed6-120">Nome de ponto do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="d7ed6-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="d7ed6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7ed6-121">-ResourceGroupName</span></span>
<span data-ttu-id="d7ed6-122">Nome do grupo de recursos de ponto de roteador virtual</span><span class="sxs-lookup"><span data-stu-id="d7ed6-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="d7ed6-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="d7ed6-123">-VirtualRouterName</span></span>
<span data-ttu-id="d7ed6-124">Nome do roteador virtual</span><span class="sxs-lookup"><span data-stu-id="d7ed6-124">Virtual router name</span></span>

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

### <span data-ttu-id="d7ed6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ed6-125">CommonParameters</span></span>
<span data-ttu-id="d7ed6-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ed6-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7ed6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ed6-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="d7ed6-128">INPUTS</span></span>

### <span data-ttu-id="d7ed6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d7ed6-129">System.String</span></span>

### <span data-ttu-id="d7ed6-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="d7ed6-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="d7ed6-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="d7ed6-131">OUTPUTS</span></span>

### <span data-ttu-id="d7ed6-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="d7ed6-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="d7ed6-133">Notas</span><span class="sxs-lookup"><span data-stu-id="d7ed6-133">NOTES</span></span>

## <span data-ttu-id="d7ed6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7ed6-134">RELATED LINKS</span></span>
