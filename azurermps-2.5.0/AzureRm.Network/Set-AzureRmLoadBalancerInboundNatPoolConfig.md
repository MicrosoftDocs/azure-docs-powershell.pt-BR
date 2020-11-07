---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 6f4981469bf9468de7fd05ec79b1d3d2b28daa93
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786269"
---
# <span data-ttu-id="dc2a4-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dc2a4-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="dc2a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc2a4-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc2a4-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc2a4-103">SYNTAX</span></span>

### <span data-ttu-id="dc2a4-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc2a4-104">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc2a4-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dc2a4-105">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc2a4-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc2a4-106">DESCRIPTION</span></span>

## <span data-ttu-id="dc2a4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc2a4-107">EXAMPLES</span></span>

### <span data-ttu-id="dc2a4-108">1:</span><span class="sxs-lookup"><span data-stu-id="dc2a4-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="dc2a4-109">OS</span><span class="sxs-lookup"><span data-stu-id="dc2a4-109">PARAMETERS</span></span>

### <span data-ttu-id="dc2a4-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="dc2a4-110">-BackendPort</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc2a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc2a4-111">-DefaultProfile</span></span>
<span data-ttu-id="dc2a4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc2a4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc2a4-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc2a4-113">-FrontendIpConfiguration</span></span>
```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc2a4-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dc2a4-114">-FrontendIpConfigurationId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc2a4-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="dc2a4-115">-FrontendPortRangeEnd</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc2a4-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="dc2a4-116">-FrontendPortRangeStart</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc2a4-117">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="dc2a4-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="dc2a4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc2a4-118">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc2a4-119">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="dc2a4-119">-Protocol</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc2a4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc2a4-120">CommonParameters</span></span>
<span data-ttu-id="dc2a4-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc2a4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc2a4-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc2a4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc2a4-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc2a4-123">INPUTS</span></span>

### <span data-ttu-id="dc2a4-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dc2a4-124">PSLoadBalancer</span></span>
<span data-ttu-id="dc2a4-125">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="dc2a4-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="dc2a4-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc2a4-126">OUTPUTS</span></span>

### <span data-ttu-id="dc2a4-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dc2a4-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dc2a4-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc2a4-128">NOTES</span></span>

## <span data-ttu-id="dc2a4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc2a4-129">RELATED LINKS</span></span>

[<span data-ttu-id="dc2a4-130">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dc2a4-130">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="dc2a4-131">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dc2a4-131">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="dc2a4-132">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dc2a4-132">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./New-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="dc2a4-133">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dc2a4-133">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatPoolConfig.md)


