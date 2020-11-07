---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: 767f725633560d79cb19e1caad61c08772107b42
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943341"
---
# <span data-ttu-id="c5d56-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c5d56-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="c5d56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5d56-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d56-103">Obtém um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="c5d56-103">Gets a load balancer.</span></span>

## <span data-ttu-id="c5d56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5d56-104">SYNTAX</span></span>

### <span data-ttu-id="c5d56-105">NOEXPAND (padrão)</span><span class="sxs-lookup"><span data-stu-id="c5d56-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5d56-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="c5d56-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5d56-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5d56-107">DESCRIPTION</span></span>
<span data-ttu-id="c5d56-108">O cmdlet **Get-AzLoadBalancer** Obtém um ou mais balanceadores de carga do Azure contidos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5d56-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="c5d56-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5d56-109">EXAMPLES</span></span>

### <span data-ttu-id="c5d56-110">Exemplo 1: obter um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="c5d56-110">Example 1: Get a load balancer</span></span>
```
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer1" -ResourceGroupName "MyResourceGroup"

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }
```

<span data-ttu-id="c5d56-111">Esse comando obtém o balanceador de carga chamado MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="c5d56-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="c5d56-112">Um balanceador de carga deve existir antes que você possa executar este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5d56-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="c5d56-113">Exemplo 2: listar balanceadores de carga usando filtragem</span><span class="sxs-lookup"><span data-stu-id="c5d56-113">Example 2: List load balancers using filtering</span></span>
```
PS C:\> Get-AzLoadBalancer -Name MyLoadBalancer*

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }

Name                     : MyLoadBalancer2
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }
```

<span data-ttu-id="c5d56-114">Esse comando obtém todos os balanceadores de carga com um nome que começa com "MyLoadBalancer"</span><span class="sxs-lookup"><span data-stu-id="c5d56-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="c5d56-115">OS</span><span class="sxs-lookup"><span data-stu-id="c5d56-115">PARAMETERS</span></span>

### <span data-ttu-id="c5d56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d56-116">-DefaultProfile</span></span>
<span data-ttu-id="c5d56-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5d56-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5d56-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c5d56-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d56-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5d56-119">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c5d56-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d56-120">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c5d56-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d56-121">CommonParameters</span></span>
<span data-ttu-id="c5d56-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5d56-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d56-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5d56-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d56-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5d56-124">INPUTS</span></span>

### <span data-ttu-id="c5d56-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c5d56-125">System.String</span></span>

## <span data-ttu-id="c5d56-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5d56-126">OUTPUTS</span></span>

### <span data-ttu-id="c5d56-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c5d56-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c5d56-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5d56-128">NOTES</span></span>

## <span data-ttu-id="c5d56-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5d56-129">RELATED LINKS</span></span>

[<span data-ttu-id="c5d56-130">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c5d56-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="c5d56-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c5d56-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="c5d56-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c5d56-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


