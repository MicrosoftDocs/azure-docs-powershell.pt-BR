---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: dd887874540a216cc826f807059e6534b99e28f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263418"
---
# <span data-ttu-id="611d4-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="611d4-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="611d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="611d4-102">SYNOPSIS</span></span>
<span data-ttu-id="611d4-103">Obtém um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="611d4-103">Gets a load balancer.</span></span>

## <span data-ttu-id="611d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="611d4-104">SYNTAX</span></span>

### <span data-ttu-id="611d4-105">NOEXPAND (padrão)</span><span class="sxs-lookup"><span data-stu-id="611d4-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="611d4-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="611d4-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="611d4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="611d4-107">DESCRIPTION</span></span>
<span data-ttu-id="611d4-108">O cmdlet **Get-AzLoadBalancer** Obtém um ou mais balanceadores de carga do Azure contidos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="611d4-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="611d4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="611d4-109">EXAMPLES</span></span>

### <span data-ttu-id="611d4-110">Exemplo 1: obter um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="611d4-110">Example 1: Get a load balancer</span></span>
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
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="611d4-111">Esse comando obtém o balanceador de carga chamado MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="611d4-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="611d4-112">Um balanceador de carga deve existir antes que você possa executar este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="611d4-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="611d4-113">Exemplo 2: listar balanceadores de carga usando filtragem</span><span class="sxs-lookup"><span data-stu-id="611d4-113">Example 2: List load balancers using filtering</span></span>
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
                             "Name": "Basic",
                             "Tier": "Regional"
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
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="611d4-114">Esse comando obtém todos os balanceadores de carga com um nome que começa com "MyLoadBalancer"</span><span class="sxs-lookup"><span data-stu-id="611d4-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="611d4-115">OS</span><span class="sxs-lookup"><span data-stu-id="611d4-115">PARAMETERS</span></span>

### <span data-ttu-id="611d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="611d4-116">-DefaultProfile</span></span>
<span data-ttu-id="611d4-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="611d4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="611d4-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="611d4-118">-ExpandResource</span></span>
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

### <span data-ttu-id="611d4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="611d4-119">-Name</span></span>
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

### <span data-ttu-id="611d4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="611d4-120">-ResourceGroupName</span></span>
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

### <span data-ttu-id="611d4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="611d4-121">CommonParameters</span></span>
<span data-ttu-id="611d4-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="611d4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="611d4-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="611d4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="611d4-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="611d4-124">INPUTS</span></span>

### <span data-ttu-id="611d4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="611d4-125">System.String</span></span>

## <span data-ttu-id="611d4-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="611d4-126">OUTPUTS</span></span>

### <span data-ttu-id="611d4-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="611d4-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="611d4-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="611d4-128">NOTES</span></span>

## <span data-ttu-id="611d4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="611d4-129">RELATED LINKS</span></span>

[<span data-ttu-id="611d4-130">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="611d4-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="611d4-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="611d4-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="611d4-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="611d4-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


