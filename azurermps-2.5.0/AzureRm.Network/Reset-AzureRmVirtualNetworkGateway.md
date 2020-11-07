---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f4039fb8a616a474a858728b6e222537c2d75c66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786408"
---
# <span data-ttu-id="b3646-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3646-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="b3646-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3646-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3646-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3646-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3646-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3646-104">DESCRIPTION</span></span>

## <span data-ttu-id="b3646-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3646-105">EXAMPLES</span></span>

### <span data-ttu-id="b3646-106">1:</span><span class="sxs-lookup"><span data-stu-id="b3646-106">1:</span></span>
```

```

## <span data-ttu-id="b3646-107">OS</span><span class="sxs-lookup"><span data-stu-id="b3646-107">PARAMETERS</span></span>

### <span data-ttu-id="b3646-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3646-108">-AsJob</span></span>
<span data-ttu-id="b3646-109">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b3646-109">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3646-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3646-110">-DefaultProfile</span></span>
<span data-ttu-id="b3646-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3646-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3646-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="b3646-112">-GatewayVip</span></span>
<span data-ttu-id="b3646-113">O VIP do gateway para redefinir uma instância específica do gateway (por exemplo, no caso de Active-Active de gateway habilitados para recursos.) Por padrão, a instância primária do gateway será redefinida se nenhum valor for passado.</span><span class="sxs-lookup"><span data-stu-id="b3646-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3646-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3646-114">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3646-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3646-115">CommonParameters</span></span>
<span data-ttu-id="b3646-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3646-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3646-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3646-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3646-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3646-118">INPUTS</span></span>

### <span data-ttu-id="b3646-119">String</span><span class="sxs-lookup"><span data-stu-id="b3646-119">String</span></span>
<span data-ttu-id="b3646-120">O parâmetro ' GatewayVip ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b3646-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="b3646-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3646-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="b3646-122">O parâmetro ' VirtualNetworkGateway ' aceita o valor do tipo ' PSVirtualNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b3646-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="b3646-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3646-123">OUTPUTS</span></span>

### <span data-ttu-id="b3646-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3646-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b3646-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3646-125">NOTES</span></span>

## <span data-ttu-id="b3646-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3646-126">RELATED LINKS</span></span>

[<span data-ttu-id="b3646-127">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3646-127">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b3646-128">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3646-128">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b3646-129">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3646-129">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b3646-130">Redimensionar-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3646-130">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b3646-131">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3646-131">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


