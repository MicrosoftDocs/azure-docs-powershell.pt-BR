---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: a5cd44d1b4b7ac1a1494047affa721dd21d85919
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775637"
---
# <span data-ttu-id="876e4-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="876e4-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="876e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="876e4-102">SYNOPSIS</span></span>

## <span data-ttu-id="876e4-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="876e4-103">SYNTAX</span></span>

### <span data-ttu-id="876e4-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="876e4-104">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="876e4-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="876e4-105">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="876e4-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="876e4-106">DESCRIPTION</span></span>

## <span data-ttu-id="876e4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="876e4-107">EXAMPLES</span></span>

### <span data-ttu-id="876e4-108">1:</span><span class="sxs-lookup"><span data-stu-id="876e4-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="876e4-109">OS</span><span class="sxs-lookup"><span data-stu-id="876e4-109">PARAMETERS</span></span>

### <span data-ttu-id="876e4-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="876e4-110">-BackendPort</span></span>
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

### <span data-ttu-id="876e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876e4-111">-DefaultProfile</span></span>
<span data-ttu-id="876e4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="876e4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="876e4-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="876e4-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="876e4-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="876e4-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="876e4-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="876e4-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="876e4-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="876e4-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="876e4-117">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="876e4-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="876e4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="876e4-118">-Name</span></span>
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

### <span data-ttu-id="876e4-119">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="876e4-119">-Protocol</span></span>
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

### <span data-ttu-id="876e4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876e4-120">CommonParameters</span></span>
<span data-ttu-id="876e4-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="876e4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876e4-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="876e4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876e4-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="876e4-123">INPUTS</span></span>

### <span data-ttu-id="876e4-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="876e4-124">PSLoadBalancer</span></span>
<span data-ttu-id="876e4-125">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="876e4-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="876e4-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="876e4-126">OUTPUTS</span></span>

### <span data-ttu-id="876e4-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="876e4-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="876e4-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="876e4-128">NOTES</span></span>

## <span data-ttu-id="876e4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="876e4-129">RELATED LINKS</span></span>

