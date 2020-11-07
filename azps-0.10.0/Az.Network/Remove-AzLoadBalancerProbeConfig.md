---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 11de4e8966b5e57e817b6c5d829536deacf229f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775290"
---
# <span data-ttu-id="0219e-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0219e-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="0219e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0219e-102">SYNOPSIS</span></span>
<span data-ttu-id="0219e-103">Remove uma configuração de teste de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0219e-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="0219e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0219e-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0219e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0219e-105">DESCRIPTION</span></span>
<span data-ttu-id="0219e-106">O cmdlet **Remove-AzLoadBalancerProbeConfig** remove uma configuração de teste de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0219e-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="0219e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0219e-107">EXAMPLES</span></span>

### <span data-ttu-id="0219e-108">Exemplo 1: remover uma configuração de teste de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="0219e-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="0219e-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="0219e-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="0219e-110">O segundo comando exclui a configuração nomeada myprobe do balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="0219e-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="0219e-111">OS</span><span class="sxs-lookup"><span data-stu-id="0219e-111">PARAMETERS</span></span>

### <span data-ttu-id="0219e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0219e-112">-DefaultProfile</span></span>
<span data-ttu-id="0219e-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0219e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0219e-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="0219e-114">-LoadBalancer</span></span>
<span data-ttu-id="0219e-115">Especifica o balanceador de carga que contém a configuração de sonda que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="0219e-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0219e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0219e-116">-Name</span></span>
<span data-ttu-id="0219e-117">Especifica o nome da configuração de sondagem que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="0219e-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0219e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0219e-118">CommonParameters</span></span>
<span data-ttu-id="0219e-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0219e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0219e-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0219e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0219e-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0219e-121">INPUTS</span></span>

### <span data-ttu-id="0219e-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0219e-122">PSLoadBalancer</span></span>
<span data-ttu-id="0219e-123">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0219e-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0219e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0219e-124">OUTPUTS</span></span>

### <span data-ttu-id="0219e-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0219e-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0219e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0219e-126">NOTES</span></span>

## <span data-ttu-id="0219e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0219e-127">RELATED LINKS</span></span>

[<span data-ttu-id="0219e-128">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0219e-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="0219e-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0219e-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0219e-130">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0219e-130">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="0219e-131">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0219e-131">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="0219e-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0219e-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


