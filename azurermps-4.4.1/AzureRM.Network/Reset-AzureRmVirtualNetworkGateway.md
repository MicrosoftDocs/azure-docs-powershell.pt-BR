---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 2b2947ec86e928506624aea49b380db3c4f24bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610209"
---
# <span data-ttu-id="4da55-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4da55-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="4da55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4da55-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4da55-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4da55-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4da55-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4da55-104">DESCRIPTION</span></span>

## <span data-ttu-id="4da55-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4da55-105">EXAMPLES</span></span>

## <span data-ttu-id="4da55-106">OS</span><span class="sxs-lookup"><span data-stu-id="4da55-106">PARAMETERS</span></span>

### <span data-ttu-id="4da55-107">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="4da55-107">-GatewayVip</span></span>
<span data-ttu-id="4da55-108">O VIP do gateway para redefinir uma instância específica do gateway (por exemplo, no caso de Active-Active de gateway habilitados para recursos.) Por padrão, a instância primária do gateway será redefinida se nenhum valor for passado.</span><span class="sxs-lookup"><span data-stu-id="4da55-108">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4da55-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4da55-109">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4da55-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da55-110">-DefaultProfile</span></span>
<span data-ttu-id="4da55-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4da55-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4da55-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da55-112">CommonParameters</span></span>
<span data-ttu-id="4da55-113">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4da55-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da55-114">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4da55-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da55-115">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4da55-115">INPUTS</span></span>

### <span data-ttu-id="4da55-116">String</span><span class="sxs-lookup"><span data-stu-id="4da55-116">String</span></span>
<span data-ttu-id="4da55-117">O parâmetro ' GatewayVip ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4da55-117">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="4da55-118">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4da55-118">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="4da55-119">O parâmetro ' VirtualNetworkGateway ' aceita o valor do tipo ' PSVirtualNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4da55-119">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="4da55-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4da55-120">OUTPUTS</span></span>

### <span data-ttu-id="4da55-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4da55-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="4da55-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4da55-122">NOTES</span></span>

## <span data-ttu-id="4da55-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4da55-123">RELATED LINKS</span></span>

[<span data-ttu-id="4da55-124">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4da55-124">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="4da55-125">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4da55-125">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="4da55-126">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4da55-126">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="4da55-127">Redimensionar-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4da55-127">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="4da55-128">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4da55-128">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


