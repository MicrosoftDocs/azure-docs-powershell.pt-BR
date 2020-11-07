---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a0b1acf49aa177d05be7361eedf644320b609797
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775541"
---
# <span data-ttu-id="b54ba-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b54ba-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b54ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b54ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b54ba-103">Obtém uma configuração de IP de front-end em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b54ba-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="b54ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b54ba-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b54ba-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b54ba-105">DESCRIPTION</span></span>
<span data-ttu-id="b54ba-106">O cmdlet **Get-AzLoadBalancerFrontendIpConfig** Obtém uma configuração de IP de front-end ou uma lista de configurações de IP front-end em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b54ba-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="b54ba-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b54ba-107">EXAMPLES</span></span>

### <span data-ttu-id="b54ba-108">Exemplo 1: obter uma configuração de IP front-end em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="b54ba-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="b54ba-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="b54ba-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="b54ba-110">O segundo comando obtém a configuração de IP de front-end associada a esse balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b54ba-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="b54ba-111">OS</span><span class="sxs-lookup"><span data-stu-id="b54ba-111">PARAMETERS</span></span>

### <span data-ttu-id="b54ba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b54ba-112">-DefaultProfile</span></span>
<span data-ttu-id="b54ba-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b54ba-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54ba-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="b54ba-114">-LoadBalancer</span></span>
<span data-ttu-id="b54ba-115">Especifica o balanceador de carga que está associado à configuração de IP de front-end a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="b54ba-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b54ba-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b54ba-116">-Name</span></span>
<span data-ttu-id="b54ba-117">Especifica o nome do balanceador de carga que contém a configuração de IP de front-end a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="b54ba-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54ba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b54ba-118">CommonParameters</span></span>
<span data-ttu-id="b54ba-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b54ba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b54ba-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b54ba-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b54ba-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b54ba-121">INPUTS</span></span>

### <span data-ttu-id="b54ba-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b54ba-122">PSLoadBalancer</span></span>
<span data-ttu-id="b54ba-123">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b54ba-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b54ba-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b54ba-124">OUTPUTS</span></span>

### <span data-ttu-id="b54ba-125">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b54ba-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="b54ba-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b54ba-126">NOTES</span></span>

## <span data-ttu-id="b54ba-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b54ba-127">RELATED LINKS</span></span>

[<span data-ttu-id="b54ba-128">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b54ba-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b54ba-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b54ba-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b54ba-130">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b54ba-130">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b54ba-131">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b54ba-131">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b54ba-132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b54ba-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


