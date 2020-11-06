---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 070680c1dc1c9fd091b311888867cda3f844ce4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430168"
---
# <span data-ttu-id="dfcb9-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dfcb9-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="dfcb9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfcb9-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcb9-103">Obtém uma configuração de IP de front-end em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="dfcb9-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfcb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfcb9-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfcb9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfcb9-105">DESCRIPTION</span></span>
<span data-ttu-id="dfcb9-106">O cmdlet **Get-AzureRmLoadBalancerFrontendIpConfig** Obtém uma configuração de IP de front-end ou uma lista de configurações de IP front-end em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="dfcb9-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="dfcb9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfcb9-107">EXAMPLES</span></span>

### <span data-ttu-id="dfcb9-108">Exemplo 1: obter uma configuração de IP front-end em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="dfcb9-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="dfcb9-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="dfcb9-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="dfcb9-110">O segundo comando obtém a configuração de IP de front-end associada a esse balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="dfcb9-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="dfcb9-111">OS</span><span class="sxs-lookup"><span data-stu-id="dfcb9-111">PARAMETERS</span></span>

### <span data-ttu-id="dfcb9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcb9-112">-DefaultProfile</span></span>
<span data-ttu-id="dfcb9-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfcb9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcb9-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="dfcb9-114">-LoadBalancer</span></span>
<span data-ttu-id="dfcb9-115">Especifica o balanceador de carga que está associado à configuração de IP de front-end a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="dfcb9-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfcb9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfcb9-116">-Name</span></span>
<span data-ttu-id="dfcb9-117">Especifica o nome do balanceador de carga que contém a configuração de IP de front-end a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="dfcb9-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcb9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcb9-118">CommonParameters</span></span>
<span data-ttu-id="dfcb9-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfcb9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcb9-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfcb9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcb9-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfcb9-121">INPUTS</span></span>

### <span data-ttu-id="dfcb9-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dfcb9-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="dfcb9-123">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dfcb9-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="dfcb9-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfcb9-124">OUTPUTS</span></span>

### <span data-ttu-id="dfcb9-125">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfcb9-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="dfcb9-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfcb9-126">NOTES</span></span>

## <span data-ttu-id="dfcb9-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfcb9-127">RELATED LINKS</span></span>

[<span data-ttu-id="dfcb9-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dfcb9-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dfcb9-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dfcb9-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="dfcb9-130">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dfcb9-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dfcb9-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dfcb9-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dfcb9-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dfcb9-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


