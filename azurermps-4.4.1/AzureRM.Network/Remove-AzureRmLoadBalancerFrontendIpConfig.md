---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: c4809371792a2add8510b1bf7f4db39dd344b037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426896"
---
# <span data-ttu-id="4092d-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4092d-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="4092d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4092d-102">SYNOPSIS</span></span>
<span data-ttu-id="4092d-103">Remove uma configuração de IP de front-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4092d-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4092d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4092d-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4092d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4092d-105">DESCRIPTION</span></span>
<span data-ttu-id="4092d-106">O cmdlet **Remove-AzureRmLoadBalancerFrontendIpConfig** remove uma configuração de IP de front-end de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="4092d-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="4092d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4092d-107">EXAMPLES</span></span>

### <span data-ttu-id="4092d-108">Exemplo 1: remover uma configuração de IP de front-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="4092d-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="4092d-109">O primeiro comando obtém o balanceador de carga associado à configuração de IP de front-end que você deseja remover e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="4092d-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="4092d-110">O segundo comando Remove a configuração de IP de front-end associada do balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="4092d-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="4092d-111">OS</span><span class="sxs-lookup"><span data-stu-id="4092d-111">PARAMETERS</span></span>

### <span data-ttu-id="4092d-112">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="4092d-112">-LoadBalancer</span></span>
<span data-ttu-id="4092d-113">Especifica o balanceador de carga que contém a configuração de IP de front-end a ser removida.</span><span class="sxs-lookup"><span data-stu-id="4092d-113">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4092d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="4092d-114">-Name</span></span>
<span data-ttu-id="4092d-115">Especifica o nome da configuração de endereço IP de front-end a ser removida.</span><span class="sxs-lookup"><span data-stu-id="4092d-115">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="4092d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4092d-116">-DefaultProfile</span></span>
<span data-ttu-id="4092d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4092d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4092d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4092d-118">CommonParameters</span></span>
<span data-ttu-id="4092d-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4092d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4092d-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4092d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4092d-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4092d-121">INPUTS</span></span>

### <span data-ttu-id="4092d-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4092d-122">PSLoadBalancer</span></span>
<span data-ttu-id="4092d-123">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4092d-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4092d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4092d-124">OUTPUTS</span></span>

### <span data-ttu-id="4092d-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4092d-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4092d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4092d-126">NOTES</span></span>

## <span data-ttu-id="4092d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4092d-127">RELATED LINKS</span></span>

[<span data-ttu-id="4092d-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4092d-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4092d-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4092d-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="4092d-130">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4092d-130">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4092d-131">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4092d-131">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4092d-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4092d-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)

