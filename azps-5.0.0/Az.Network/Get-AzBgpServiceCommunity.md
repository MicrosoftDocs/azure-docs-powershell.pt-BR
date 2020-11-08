---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azbgpservicecommunity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
ms.openlocfilehash: 334c10d1fdeb8dae4379d495975934572fe7e340
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125826"
---
# <span data-ttu-id="69f29-101">Get-AzBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="69f29-101">Get-AzBgpServiceCommunity</span></span>

## <span data-ttu-id="69f29-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69f29-102">SYNOPSIS</span></span>
<span data-ttu-id="69f29-103">Fornece uma lista de todos os serviços/regiões, comunidades BGP e prefixos associados.</span><span class="sxs-lookup"><span data-stu-id="69f29-103">Provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="69f29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69f29-104">SYNTAX</span></span>

```
Get-AzBgpServiceCommunity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69f29-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69f29-105">DESCRIPTION</span></span>
<span data-ttu-id="69f29-106">Esse cmdlet fornece uma lista de todos os serviços/regiões, comunidades BGP e prefixos associados.</span><span class="sxs-lookup"><span data-stu-id="69f29-106">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="69f29-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69f29-107">EXAMPLES</span></span>

### <span data-ttu-id="69f29-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69f29-108">Example 1</span></span>
```
Get-AzBgpServiceCommunity

...

Name           : AzureCentralIndia
Id             : /subscriptions//resourceGroups//providers/Microsoft.Network/bgpServiceCommunities/AzureCentralIndia
Type           : Microsoft.Network/bgpServiceCommunities
BgpCommunities : [
                   {
                     "ServiceSupportedRegion": "Global",
                     "CommunityName": "Azure Central India",
                     "CommunityValue": "12076:51017",
                     "CommunityPrefixes": [
                       "13.71.0.0/18",
                       "20.190.146.0/25",
                       "40.79.214.0/24",
                       "40.81.224.0/19",
                       "40.87.224.0/22",
                       "40.112.39.0/25",
                       "40.112.39.128/26",
                       "40.126.18.0/25",
                       "52.136.24.0/24",
                       "52.140.64.0/18",
                       "52.159.64.0/19",
                       "52.172.128.0/17",
                       "52.239.135.64/26",
                       "52.239.202.0/24",
                       "52.245.96.0/22",
                       "52.253.168.0/22",
                       "104.47.210.0/23",
                       "104.211.64.0/20",
                       "104.211.81.0/24",
                       "104.211.82.0/23",
                       "104.211.84.0/22",
                       "104.211.88.0/21",
                       "104.211.96.0/19"
                     ],
                     "IsAuthorizedToUse": true,
                     "ServiceGroup": "Azure"
                   }
                 ]
...
```

<span data-ttu-id="69f29-109">Esse cmdlet fornece uma lista de todos os serviços/regiões, comunidades BGP e prefixos associados.</span><span class="sxs-lookup"><span data-stu-id="69f29-109">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="69f29-110">OS</span><span class="sxs-lookup"><span data-stu-id="69f29-110">PARAMETERS</span></span>

### <span data-ttu-id="69f29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f29-111">-DefaultProfile</span></span>
<span data-ttu-id="69f29-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69f29-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69f29-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f29-113">CommonParameters</span></span>
<span data-ttu-id="69f29-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69f29-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f29-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69f29-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f29-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69f29-116">INPUTS</span></span>

### <span data-ttu-id="69f29-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="69f29-117">None</span></span>

## <span data-ttu-id="69f29-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69f29-118">OUTPUTS</span></span>

### <span data-ttu-id="69f29-119">Microsoft. Azure. Commands. Network. Models. PSBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="69f29-119">Microsoft.Azure.Commands.Network.Models.PSBgpServiceCommunity</span></span>

## <span data-ttu-id="69f29-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69f29-120">NOTES</span></span>

## <span data-ttu-id="69f29-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69f29-121">RELATED LINKS</span></span>

[<span data-ttu-id="69f29-122">Mover-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="69f29-122">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="69f29-123">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="69f29-123">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="69f29-124">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="69f29-124">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="69f29-125">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="69f29-125">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="69f29-126">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="69f29-126">Get-AzRouteFilter</span></span>](Get-AzRouteFilter.md)

[<span data-ttu-id="69f29-127">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69f29-127">Get-AzRouteFilterRuleConfig</span></span>](Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="69f29-128">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="69f29-128">Remove-AzRouteFilter</span></span>](Remove-AzRouteFilter.md)

[<span data-ttu-id="69f29-129">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69f29-129">Remove-AzRouteFilterRuleConfig</span></span>](Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="69f29-130">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="69f29-130">Set-AzRouteFilter</span></span>](Set-AzRouteFilter.md)

[<span data-ttu-id="69f29-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69f29-131">Set-AzRouteFilterRuleConfig</span></span>](Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="69f29-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="69f29-132">New-AzRouteFilter</span></span>](New-AzRouteFilter.md)

[<span data-ttu-id="69f29-133">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69f29-133">New-AzRouteFilterRuleConfig</span></span>](New-AzRouteFilterRuleConfig.md)
