---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 53a4eb40d82a721c93102067c8c7e9fe0cbd86be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776587"
---
# <span data-ttu-id="6976f-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6976f-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="6976f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6976f-102">SYNOPSIS</span></span>

## <span data-ttu-id="6976f-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6976f-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6976f-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6976f-104">DESCRIPTION</span></span>

## <span data-ttu-id="6976f-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6976f-105">EXAMPLES</span></span>

### <span data-ttu-id="6976f-106">1:</span><span class="sxs-lookup"><span data-stu-id="6976f-106">1:</span></span>
```

```

## <span data-ttu-id="6976f-107">OS</span><span class="sxs-lookup"><span data-stu-id="6976f-107">PARAMETERS</span></span>

### <span data-ttu-id="6976f-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6976f-108">-AsJob</span></span>
<span data-ttu-id="6976f-109">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6976f-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6976f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6976f-110">-DefaultProfile</span></span>
<span data-ttu-id="6976f-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6976f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6976f-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="6976f-112">-GatewayVip</span></span>
<span data-ttu-id="6976f-113">O VIP do gateway para redefinir uma instância específica do gateway (por exemplo, no caso de Active-Active de gateway habilitados para recursos.) Por padrão, a instância primária do gateway será redefinida se nenhum valor for passado.</span><span class="sxs-lookup"><span data-stu-id="6976f-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="6976f-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6976f-114">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="6976f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6976f-115">CommonParameters</span></span>
<span data-ttu-id="6976f-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6976f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6976f-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6976f-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6976f-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6976f-118">INPUTS</span></span>

### <span data-ttu-id="6976f-119">String</span><span class="sxs-lookup"><span data-stu-id="6976f-119">String</span></span>
<span data-ttu-id="6976f-120">O parâmetro ' GatewayVip ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6976f-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="6976f-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6976f-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="6976f-122">O parâmetro ' VirtualNetworkGateway ' aceita o valor do tipo ' PSVirtualNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6976f-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="6976f-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6976f-123">OUTPUTS</span></span>

### <span data-ttu-id="6976f-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6976f-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="6976f-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6976f-125">NOTES</span></span>

## <span data-ttu-id="6976f-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6976f-126">RELATED LINKS</span></span>

[<span data-ttu-id="6976f-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6976f-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6976f-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6976f-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6976f-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6976f-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6976f-130">Redimensionar-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6976f-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6976f-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6976f-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)


