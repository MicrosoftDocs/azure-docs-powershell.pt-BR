---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 63859bb6b7520264671a9190919c43e1f79e0341
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432106"
---
# <span data-ttu-id="878fe-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="878fe-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="878fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="878fe-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="878fe-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="878fe-103">SYNTAX</span></span>

### <span data-ttu-id="878fe-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="878fe-104">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="878fe-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="878fe-105">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="878fe-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="878fe-106">DESCRIPTION</span></span>

## <span data-ttu-id="878fe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="878fe-107">EXAMPLES</span></span>

### <span data-ttu-id="878fe-108">1:</span><span class="sxs-lookup"><span data-stu-id="878fe-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="878fe-109">OS</span><span class="sxs-lookup"><span data-stu-id="878fe-109">PARAMETERS</span></span>

### <span data-ttu-id="878fe-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="878fe-110">-BackendPort</span></span>
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

### <span data-ttu-id="878fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="878fe-111">-DefaultProfile</span></span>
<span data-ttu-id="878fe-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="878fe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="878fe-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="878fe-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="878fe-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="878fe-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="878fe-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="878fe-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="878fe-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="878fe-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="878fe-117">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="878fe-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="878fe-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="878fe-118">-Name</span></span>
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

### <span data-ttu-id="878fe-119">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="878fe-119">-Protocol</span></span>
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

### <span data-ttu-id="878fe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="878fe-120">CommonParameters</span></span>
<span data-ttu-id="878fe-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="878fe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="878fe-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="878fe-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="878fe-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="878fe-123">INPUTS</span></span>

### <span data-ttu-id="878fe-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="878fe-124">PSLoadBalancer</span></span>
<span data-ttu-id="878fe-125">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="878fe-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="878fe-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="878fe-126">OUTPUTS</span></span>

### <span data-ttu-id="878fe-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="878fe-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="878fe-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="878fe-128">NOTES</span></span>

## <span data-ttu-id="878fe-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="878fe-129">RELATED LINKS</span></span>

