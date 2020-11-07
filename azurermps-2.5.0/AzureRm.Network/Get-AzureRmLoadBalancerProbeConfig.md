---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: 30989d3b9c71821c2eae3cdfd97f9e4e5fc0cb15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786468"
---
# <span data-ttu-id="1a2a0-101">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1a2a0-101">Get-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="1a2a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="1a2a0-103">Obtém uma configuração de teste para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1a2a0-103">Gets a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a2a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a2a0-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a2a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a2a0-105">DESCRIPTION</span></span>
<span data-ttu-id="1a2a0-106">O cmdlet **Get-AzureRmLoadBalancerProbeConfig** Obtém uma ou mais configurações de teste para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1a2a0-106">The **Get-AzureRmLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="1a2a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a2a0-107">EXAMPLES</span></span>

### <span data-ttu-id="1a2a0-108">Exemplo 1: obter a configuração de teste de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="1a2a0-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="1a2a0-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="1a2a0-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="1a2a0-110">O segundo comando obtém a configuração de teste associada chamada myprobe do balanceador de carga em $slb.</span><span class="sxs-lookup"><span data-stu-id="1a2a0-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="1a2a0-111">OS</span><span class="sxs-lookup"><span data-stu-id="1a2a0-111">PARAMETERS</span></span>

### <span data-ttu-id="1a2a0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a2a0-112">-DefaultProfile</span></span>
<span data-ttu-id="1a2a0-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a2a0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a2a0-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="1a2a0-114">-LoadBalancer</span></span>
<span data-ttu-id="1a2a0-115">Especifica o balanceador de carga associado à configuração de sonda a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="1a2a0-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="1a2a0-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a2a0-116">-Name</span></span>
<span data-ttu-id="1a2a0-117">Especifica o nome da configuração de teste a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="1a2a0-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="1a2a0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a2a0-118">CommonParameters</span></span>
<span data-ttu-id="1a2a0-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a2a0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a2a0-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a2a0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a2a0-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a2a0-121">INPUTS</span></span>

### <span data-ttu-id="1a2a0-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a2a0-122">PSLoadBalancer</span></span>
<span data-ttu-id="1a2a0-123">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1a2a0-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="1a2a0-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a2a0-124">OUTPUTS</span></span>

### <span data-ttu-id="1a2a0-125">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="1a2a0-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="1a2a0-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a2a0-126">NOTES</span></span>

## <span data-ttu-id="1a2a0-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a2a0-127">RELATED LINKS</span></span>

[<span data-ttu-id="1a2a0-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1a2a0-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="1a2a0-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a2a0-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="1a2a0-130">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1a2a0-130">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="1a2a0-131">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1a2a0-131">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="1a2a0-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1a2a0-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


