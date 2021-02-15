---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: dd887874540a216cc826f807059e6534b99e28f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111687"
---
# <span data-ttu-id="07b6a-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07b6a-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="07b6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="07b6a-103">Obtém um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="07b6a-103">Gets a load balancer.</span></span>

## <span data-ttu-id="07b6a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07b6a-104">SYNTAX</span></span>

### <span data-ttu-id="07b6a-105">NoExpand (Padrão)</span><span class="sxs-lookup"><span data-stu-id="07b6a-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07b6a-106">Expandir</span><span class="sxs-lookup"><span data-stu-id="07b6a-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07b6a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="07b6a-107">DESCRIPTION</span></span>
<span data-ttu-id="07b6a-108">O **cmdlet Get-AzLoadBalancer** obtém um ou mais balanceadores de carga do Azure contidos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07b6a-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="07b6a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="07b6a-109">EXAMPLES</span></span>

### <span data-ttu-id="07b6a-110">Exemplo 1: Obter um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="07b6a-110">Example 1: Get a load balancer</span></span>
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

<span data-ttu-id="07b6a-111">Esse comando obtém o balanceador de carga chamado MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="07b6a-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="07b6a-112">Um balanceador de carga deve existir antes que você possa executar este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07b6a-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="07b6a-113">Exemplo 2: Balanceadores de carga de lista usando filtragem</span><span class="sxs-lookup"><span data-stu-id="07b6a-113">Example 2: List load balancers using filtering</span></span>
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

<span data-ttu-id="07b6a-114">Esse comando obtém todos os balanceadores de carga com um nome que começa com "MyLoadBalancer"</span><span class="sxs-lookup"><span data-stu-id="07b6a-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="07b6a-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07b6a-115">PARAMETERS</span></span>

### <span data-ttu-id="07b6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b6a-116">-DefaultProfile</span></span>
<span data-ttu-id="07b6a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="07b6a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07b6a-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="07b6a-118">-ExpandResource</span></span>
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

### <span data-ttu-id="07b6a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="07b6a-119">-Name</span></span>
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

### <span data-ttu-id="07b6a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07b6a-120">-ResourceGroupName</span></span>
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

### <span data-ttu-id="07b6a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b6a-121">CommonParameters</span></span>
<span data-ttu-id="07b6a-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07b6a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b6a-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07b6a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b6a-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="07b6a-124">INPUTS</span></span>

### <span data-ttu-id="07b6a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="07b6a-125">System.String</span></span>

## <span data-ttu-id="07b6a-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="07b6a-126">OUTPUTS</span></span>

### <span data-ttu-id="07b6a-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07b6a-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="07b6a-128">Notas</span><span class="sxs-lookup"><span data-stu-id="07b6a-128">NOTES</span></span>

## <span data-ttu-id="07b6a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07b6a-129">RELATED LINKS</span></span>

[<span data-ttu-id="07b6a-130">Novo-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07b6a-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="07b6a-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07b6a-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="07b6a-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07b6a-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


