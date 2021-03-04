---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: de9d7d23a60d24fca6c383ab3db1208a5eae6864
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888832"
---
# <span data-ttu-id="42978-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42978-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="42978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42978-102">SYNOPSIS</span></span>
<span data-ttu-id="42978-103">Redefine o Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="42978-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="42978-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="42978-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42978-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="42978-105">DESCRIPTION</span></span>
<span data-ttu-id="42978-106">Redefine o Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="42978-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="42978-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42978-107">EXAMPLES</span></span>

### <span data-ttu-id="42978-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="42978-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="42978-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="42978-109">PARAMETERS</span></span>

### <span data-ttu-id="42978-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42978-110">-AsJob</span></span>
<span data-ttu-id="42978-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="42978-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42978-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42978-112">-DefaultProfile</span></span>
<span data-ttu-id="42978-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="42978-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42978-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="42978-114">-GatewayVip</span></span>
<span data-ttu-id="42978-115">O vip do gateway para redefinir uma instância de gateway específica (por exemplo, no caso de Active-Active gateways habilitados para recursos).) Por padrão, a instância primária do gateway será redefinida se nenhum valor for passado.</span><span class="sxs-lookup"><span data-stu-id="42978-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="42978-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42978-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="42978-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42978-117">CommonParameters</span></span>
<span data-ttu-id="42978-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42978-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42978-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42978-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42978-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42978-120">INPUTS</span></span>

### <span data-ttu-id="42978-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42978-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="42978-122">System.String</span><span class="sxs-lookup"><span data-stu-id="42978-122">System.String</span></span>

## <span data-ttu-id="42978-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="42978-123">OUTPUTS</span></span>

### <span data-ttu-id="42978-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42978-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="42978-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="42978-125">NOTES</span></span>

## <span data-ttu-id="42978-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42978-126">RELATED LINKS</span></span>

[<span data-ttu-id="42978-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42978-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="42978-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42978-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="42978-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42978-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="42978-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42978-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="42978-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42978-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
