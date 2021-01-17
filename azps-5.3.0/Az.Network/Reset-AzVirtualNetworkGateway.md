---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428888"
---
# <span data-ttu-id="9aa06-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9aa06-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="9aa06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9aa06-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa06-103">Redefine o gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="9aa06-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="9aa06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9aa06-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9aa06-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9aa06-105">DESCRIPTION</span></span>
<span data-ttu-id="9aa06-106">Redefine o gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="9aa06-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="9aa06-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9aa06-107">EXAMPLES</span></span>

### <span data-ttu-id="9aa06-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="9aa06-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="9aa06-109">OS</span><span class="sxs-lookup"><span data-stu-id="9aa06-109">PARAMETERS</span></span>

### <span data-ttu-id="9aa06-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9aa06-110">-AsJob</span></span>
<span data-ttu-id="9aa06-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9aa06-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9aa06-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa06-112">-DefaultProfile</span></span>
<span data-ttu-id="9aa06-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9aa06-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa06-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="9aa06-114">-GatewayVip</span></span>
<span data-ttu-id="9aa06-115">O VIP do gateway para redefinir uma instância específica do gateway (por exemplo, no caso de Active-Active de gateway habilitados para recursos.) Por padrão, a instância primária do gateway será redefinida se nenhum valor for passado.</span><span class="sxs-lookup"><span data-stu-id="9aa06-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="9aa06-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9aa06-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="9aa06-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa06-117">CommonParameters</span></span>
<span data-ttu-id="9aa06-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9aa06-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa06-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aa06-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa06-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9aa06-120">INPUTS</span></span>

### <span data-ttu-id="9aa06-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9aa06-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="9aa06-122">System. String</span><span class="sxs-lookup"><span data-stu-id="9aa06-122">System.String</span></span>

## <span data-ttu-id="9aa06-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9aa06-123">OUTPUTS</span></span>

### <span data-ttu-id="9aa06-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9aa06-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9aa06-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9aa06-125">NOTES</span></span>

## <span data-ttu-id="9aa06-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9aa06-126">RELATED LINKS</span></span>

[<span data-ttu-id="9aa06-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9aa06-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9aa06-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9aa06-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9aa06-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9aa06-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9aa06-130">Redimensionar-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9aa06-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9aa06-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9aa06-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
