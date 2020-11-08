---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114135"
---
# <span data-ttu-id="1c5ff-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1c5ff-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="1c5ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="1c5ff-103">Get-AzLoadBalancerBackendAddressPool recupera um ou mais pools de endereços back-end associados a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1c5ff-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="1c5ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c5ff-104">SYNTAX</span></span>

### <span data-ttu-id="1c5ff-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c5ff-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c5ff-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c5ff-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c5ff-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c5ff-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c5ff-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c5ff-108">DESCRIPTION</span></span>
<span data-ttu-id="1c5ff-109">Get-AzLoadBalancerBackendAddressPool recupera um ou mais pools de endereços back-end associados a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1c5ff-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="1c5ff-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c5ff-110">EXAMPLES</span></span>

### <span data-ttu-id="1c5ff-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1c5ff-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="1c5ff-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1c5ff-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="1c5ff-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1c5ff-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="1c5ff-114">OS</span><span class="sxs-lookup"><span data-stu-id="1c5ff-114">PARAMETERS</span></span>

### <span data-ttu-id="1c5ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c5ff-115">-DefaultProfile</span></span>
<span data-ttu-id="1c5ff-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c5ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c5ff-117">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="1c5ff-117">-LoadBalancer</span></span>
<span data-ttu-id="1c5ff-118">{{Filler descrição do loadbalador}}</span><span class="sxs-lookup"><span data-stu-id="1c5ff-118">{{ Fill LoadBalancer Description }}</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c5ff-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="1c5ff-119">-LoadBalancerName</span></span>
<span data-ttu-id="1c5ff-120">O nome do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1c5ff-120">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c5ff-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c5ff-121">-Name</span></span>
<span data-ttu-id="1c5ff-122">O nome do pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="1c5ff-122">The name of the backend address pool.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c5ff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c5ff-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c5ff-124">O nome do grupo de recursos do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1c5ff-124">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c5ff-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c5ff-125">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c5ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c5ff-126">CommonParameters</span></span>
<span data-ttu-id="1c5ff-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c5ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c5ff-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c5ff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c5ff-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c5ff-129">INPUTS</span></span>

### <span data-ttu-id="1c5ff-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1c5ff-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="1c5ff-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1c5ff-131">System.String</span></span>

## <span data-ttu-id="1c5ff-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c5ff-132">OUTPUTS</span></span>

### <span data-ttu-id="1c5ff-133">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1c5ff-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="1c5ff-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c5ff-134">NOTES</span></span>

## <span data-ttu-id="1c5ff-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c5ff-135">RELATED LINKS</span></span>
