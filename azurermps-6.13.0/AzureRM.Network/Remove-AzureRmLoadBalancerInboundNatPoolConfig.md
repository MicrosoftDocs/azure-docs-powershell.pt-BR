---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 6f9fd09aa87c8a812bf43a14068feb1604d8de8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426334"
---
# <span data-ttu-id="b27da-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b27da-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="b27da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b27da-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b27da-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b27da-103">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b27da-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b27da-104">DESCRIPTION</span></span>

## <span data-ttu-id="b27da-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b27da-105">EXAMPLES</span></span>

### <span data-ttu-id="b27da-106">1: remover</span><span class="sxs-lookup"><span data-stu-id="b27da-106">1: Remove</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="b27da-107">OS</span><span class="sxs-lookup"><span data-stu-id="b27da-107">PARAMETERS</span></span>

### <span data-ttu-id="b27da-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27da-108">-DefaultProfile</span></span>
<span data-ttu-id="b27da-109">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b27da-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b27da-110">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="b27da-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="b27da-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="b27da-111">-Name</span></span>
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

### <span data-ttu-id="b27da-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b27da-112">-Confirm</span></span>
<span data-ttu-id="b27da-113">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b27da-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b27da-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b27da-114">-WhatIf</span></span>
<span data-ttu-id="b27da-115">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b27da-115">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b27da-116">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b27da-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b27da-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27da-117">CommonParameters</span></span>
<span data-ttu-id="b27da-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b27da-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27da-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b27da-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27da-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b27da-120">INPUTS</span></span>

### <span data-ttu-id="b27da-121">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b27da-121">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="b27da-122">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b27da-122">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="b27da-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b27da-123">OUTPUTS</span></span>

### <span data-ttu-id="b27da-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b27da-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b27da-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b27da-125">NOTES</span></span>

## <span data-ttu-id="b27da-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b27da-126">RELATED LINKS</span></span>
