---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b9782d56fb18f0f00c52e9ff37ef0d62a609f980
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775299"
---
# <span data-ttu-id="8d794-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d794-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="8d794-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d794-102">SYNOPSIS</span></span>
<span data-ttu-id="8d794-103">Remove uma configuração de IP de front-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="8d794-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="8d794-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d794-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d794-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d794-105">DESCRIPTION</span></span>
<span data-ttu-id="8d794-106">O cmdlet **Remove-AzLoadBalancerFrontendIpConfig** remove uma configuração de IP de front-end de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d794-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="8d794-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d794-107">EXAMPLES</span></span>

### <span data-ttu-id="8d794-108">Exemplo 1: remover uma configuração de IP de front-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="8d794-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="8d794-109">O primeiro comando obtém o balanceador de carga associado à configuração de IP de front-end que você deseja remover e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="8d794-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="8d794-110">O segundo comando Remove a configuração de IP de front-end associada do balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="8d794-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="8d794-111">OS</span><span class="sxs-lookup"><span data-stu-id="8d794-111">PARAMETERS</span></span>

### <span data-ttu-id="8d794-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d794-112">-DefaultProfile</span></span>
<span data-ttu-id="8d794-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d794-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d794-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="8d794-114">-LoadBalancer</span></span>
<span data-ttu-id="8d794-115">Especifica o balanceador de carga que contém a configuração de IP de front-end a ser removida.</span><span class="sxs-lookup"><span data-stu-id="8d794-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="8d794-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d794-116">-Name</span></span>
<span data-ttu-id="8d794-117">Especifica o nome da configuração de endereço IP de front-end a ser removida.</span><span class="sxs-lookup"><span data-stu-id="8d794-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="8d794-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d794-118">CommonParameters</span></span>
<span data-ttu-id="8d794-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d794-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d794-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d794-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d794-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d794-121">INPUTS</span></span>

### <span data-ttu-id="8d794-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d794-122">PSLoadBalancer</span></span>
<span data-ttu-id="8d794-123">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8d794-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="8d794-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d794-124">OUTPUTS</span></span>

### <span data-ttu-id="8d794-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d794-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8d794-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d794-126">NOTES</span></span>

## <span data-ttu-id="8d794-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d794-127">RELATED LINKS</span></span>

[<span data-ttu-id="8d794-128">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d794-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8d794-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d794-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8d794-130">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d794-130">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8d794-131">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d794-131">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8d794-132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d794-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


