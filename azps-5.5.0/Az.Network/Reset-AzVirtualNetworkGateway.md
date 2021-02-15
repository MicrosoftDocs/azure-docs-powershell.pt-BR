---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112783"
---
# <span data-ttu-id="20485-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20485-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="20485-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20485-102">SYNOPSIS</span></span>
<span data-ttu-id="20485-103">Redefine o Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="20485-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="20485-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20485-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20485-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="20485-105">DESCRIPTION</span></span>
<span data-ttu-id="20485-106">Redefine o Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="20485-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="20485-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="20485-107">EXAMPLES</span></span>

### <span data-ttu-id="20485-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="20485-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="20485-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20485-109">PARAMETERS</span></span>

### <span data-ttu-id="20485-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20485-110">-AsJob</span></span>
<span data-ttu-id="20485-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="20485-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20485-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20485-112">-DefaultProfile</span></span>
<span data-ttu-id="20485-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="20485-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20485-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="20485-114">-GatewayVip</span></span>
<span data-ttu-id="20485-115">O gateway vip para redefinir uma instância de gateway específica (por exemplo, no caso Active-Active gateways habilitados para recursos).) Por padrão, a instância principal do gateway será redefinida se nenhum valor for passado.</span><span class="sxs-lookup"><span data-stu-id="20485-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="20485-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20485-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="20485-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20485-117">CommonParameters</span></span>
<span data-ttu-id="20485-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20485-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20485-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20485-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20485-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="20485-120">INPUTS</span></span>

### <span data-ttu-id="20485-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20485-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="20485-122">System.String</span><span class="sxs-lookup"><span data-stu-id="20485-122">System.String</span></span>

## <span data-ttu-id="20485-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="20485-123">OUTPUTS</span></span>

### <span data-ttu-id="20485-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20485-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="20485-125">Notas</span><span class="sxs-lookup"><span data-stu-id="20485-125">NOTES</span></span>

## <span data-ttu-id="20485-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20485-126">RELATED LINKS</span></span>

[<span data-ttu-id="20485-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20485-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="20485-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20485-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="20485-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20485-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="20485-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20485-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="20485-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20485-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
