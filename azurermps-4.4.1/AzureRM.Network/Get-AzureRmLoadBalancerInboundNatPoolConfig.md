---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9f9e14b94cbe38ba643d2c39beca5e1fe52138b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603105"
---
# <span data-ttu-id="d5af9-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d5af9-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="d5af9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5af9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5af9-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5af9-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5af9-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5af9-104">DESCRIPTION</span></span>

## <span data-ttu-id="d5af9-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5af9-105">EXAMPLES</span></span>

### <span data-ttu-id="d5af9-106">1:</span><span class="sxs-lookup"><span data-stu-id="d5af9-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d5af9-107">OS</span><span class="sxs-lookup"><span data-stu-id="d5af9-107">PARAMETERS</span></span>

### <span data-ttu-id="d5af9-108">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="d5af9-108">-LoadBalancer</span></span>
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

### <span data-ttu-id="d5af9-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5af9-109">-Name</span></span>
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

### <span data-ttu-id="d5af9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5af9-110">-DefaultProfile</span></span>
<span data-ttu-id="d5af9-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5af9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5af9-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5af9-112">CommonParameters</span></span>
<span data-ttu-id="d5af9-113">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5af9-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5af9-114">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5af9-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5af9-115">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5af9-115">INPUTS</span></span>

### <span data-ttu-id="d5af9-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d5af9-116">PSLoadBalancer</span></span>
<span data-ttu-id="d5af9-117">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d5af9-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d5af9-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5af9-118">OUTPUTS</span></span>

### <span data-ttu-id="d5af9-119">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="d5af9-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="d5af9-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5af9-120">NOTES</span></span>

## <span data-ttu-id="d5af9-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5af9-121">RELATED LINKS</span></span>

