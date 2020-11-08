---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 7d373092f850dd25abe5b6d913ddcf2572d4be94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114833"
---
# <span data-ttu-id="75bf1-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="75bf1-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="75bf1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="75bf1-103">Retorna uma configuração de endereço back-end do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="75bf1-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="75bf1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75bf1-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75bf1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75bf1-105">DESCRIPTION</span></span>
<span data-ttu-id="75bf1-106">Retorna uma configuração de endereço back-end do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="75bf1-106">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="75bf1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75bf1-107">EXAMPLES</span></span>

### <span data-ttu-id="75bf1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75bf1-108">Example 1</span></span>
### <span data-ttu-id="75bf1-109">Exemplo 2: nova configuração de endereço de loadbalancer com referência de rede virtual</span><span class="sxs-lookup"><span data-stu-id="75bf1-109">Example 2: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

## <span data-ttu-id="75bf1-110">OS</span><span class="sxs-lookup"><span data-stu-id="75bf1-110">PARAMETERS</span></span>

### <span data-ttu-id="75bf1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75bf1-111">-DefaultProfile</span></span>
<span data-ttu-id="75bf1-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75bf1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75bf1-113">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="75bf1-113">-IpAddress</span></span>
<span data-ttu-id="75bf1-114">O IPAddress a ser adicionado ao pool de back-end</span><span class="sxs-lookup"><span data-stu-id="75bf1-114">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bf1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="75bf1-115">-Name</span></span>
<span data-ttu-id="75bf1-116">O nome da configuração do endereço de back-end</span><span class="sxs-lookup"><span data-stu-id="75bf1-116">The name of the Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bf1-117">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="75bf1-117">-VirtualNetworkId</span></span>
<span data-ttu-id="75bf1-118">A rede virtual associada à configuração de endereço de back-end</span><span class="sxs-lookup"><span data-stu-id="75bf1-118">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bf1-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75bf1-119">-Confirm</span></span>
<span data-ttu-id="75bf1-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75bf1-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bf1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75bf1-121">-WhatIf</span></span>
<span data-ttu-id="75bf1-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75bf1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75bf1-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75bf1-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bf1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75bf1-124">CommonParameters</span></span>
<span data-ttu-id="75bf1-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75bf1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75bf1-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75bf1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75bf1-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75bf1-127">INPUTS</span></span>

### <span data-ttu-id="75bf1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="75bf1-128">System.String</span></span>

### <span data-ttu-id="75bf1-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="75bf1-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="75bf1-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75bf1-130">OUTPUTS</span></span>

### <span data-ttu-id="75bf1-131">Microsoft. Azure. Commands. Network. Models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="75bf1-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="75bf1-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75bf1-132">NOTES</span></span>

## <span data-ttu-id="75bf1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75bf1-133">RELATED LINKS</span></span>
