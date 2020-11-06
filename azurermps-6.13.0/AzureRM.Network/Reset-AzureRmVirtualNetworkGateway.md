---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: c5d77619fa5f89c60ce20a097e096709e9a48bae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440325"
---
# <span data-ttu-id="36196-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36196-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="36196-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36196-102">SYNOPSIS</span></span>
<span data-ttu-id="36196-103">Redefine o gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="36196-103">Resets the Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36196-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36196-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36196-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36196-105">DESCRIPTION</span></span>
<span data-ttu-id="36196-106">Redefine o gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="36196-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="36196-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36196-107">EXAMPLES</span></span>

### <span data-ttu-id="36196-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="36196-108">Example 1:</span></span>
```
$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="36196-109">OS</span><span class="sxs-lookup"><span data-stu-id="36196-109">PARAMETERS</span></span>

### <span data-ttu-id="36196-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36196-110">-AsJob</span></span>
<span data-ttu-id="36196-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="36196-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36196-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36196-112">-DefaultProfile</span></span>
<span data-ttu-id="36196-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36196-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36196-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="36196-114">-GatewayVip</span></span>
<span data-ttu-id="36196-115">O VIP do gateway para redefinir uma instância específica do gateway (por exemplo, no caso de Active-Active de gateway habilitados para recursos.) Por padrão, a instância primária do gateway será redefinida se nenhum valor for passado.</span><span class="sxs-lookup"><span data-stu-id="36196-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="36196-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36196-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="36196-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36196-117">CommonParameters</span></span>
<span data-ttu-id="36196-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36196-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36196-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36196-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36196-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36196-120">INPUTS</span></span>

### <span data-ttu-id="36196-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36196-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="36196-122">Parâmetros: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36196-122">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="36196-123">System. String</span><span class="sxs-lookup"><span data-stu-id="36196-123">System.String</span></span>
<span data-ttu-id="36196-124">Parâmetros: GatewayVip (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36196-124">Parameters: GatewayVip (ByValue)</span></span>

## <span data-ttu-id="36196-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36196-125">OUTPUTS</span></span>

### <span data-ttu-id="36196-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36196-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="36196-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36196-127">NOTES</span></span>

## <span data-ttu-id="36196-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36196-128">RELATED LINKS</span></span>

[<span data-ttu-id="36196-129">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36196-129">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="36196-130">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36196-130">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="36196-131">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36196-131">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="36196-132">Redimensionar-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36196-132">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="36196-133">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36196-133">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


