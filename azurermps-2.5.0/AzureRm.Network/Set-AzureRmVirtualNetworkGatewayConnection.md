---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: bb098e23f6e55cc28fcae02b7094a953c5179308
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786070"
---
# <span data-ttu-id="77f7d-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77f7d-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="77f7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="77f7d-103">Configura uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="77f7d-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77f7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77f7d-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77f7d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="77f7d-106">O cmdlet **set-AzureRmVirtualNetworkGatewayConnection** configura uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="77f7d-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="77f7d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77f7d-107">EXAMPLES</span></span>

### <span data-ttu-id="77f7d-108">1:</span><span class="sxs-lookup"><span data-stu-id="77f7d-108">1:</span></span>
```

```

## <span data-ttu-id="77f7d-109">OS</span><span class="sxs-lookup"><span data-stu-id="77f7d-109">PARAMETERS</span></span>

### <span data-ttu-id="77f7d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77f7d-110">-AsJob</span></span>
<span data-ttu-id="77f7d-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="77f7d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77f7d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f7d-112">-DefaultProfile</span></span>
<span data-ttu-id="77f7d-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77f7d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77f7d-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="77f7d-114">-EnableBgp</span></span>
<span data-ttu-id="77f7d-115">Se você deve usar uma sessão BGP em um túnel VPN S2S</span><span class="sxs-lookup"><span data-stu-id="77f7d-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f7d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="77f7d-116">-Force</span></span>
<span data-ttu-id="77f7d-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="77f7d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77f7d-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="77f7d-118">-IpsecPolicies</span></span>
<span data-ttu-id="77f7d-119">Uma lista de diretivas IPSec.</span><span class="sxs-lookup"><span data-stu-id="77f7d-119">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f7d-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="77f7d-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="77f7d-121">Se os seletores de tráfego baseados em políticas devem ser usados para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="77f7d-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f7d-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77f7d-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="77f7d-123">Especifica o objeto PSVirtualNetworkGatewayConnection que este cmdlet usa para modificar a conexão do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="77f7d-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77f7d-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="77f7d-124">-Confirm</span></span>
<span data-ttu-id="77f7d-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77f7d-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f7d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77f7d-126">-WhatIf</span></span>
<span data-ttu-id="77f7d-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="77f7d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77f7d-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="77f7d-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f7d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f7d-129">CommonParameters</span></span>
<span data-ttu-id="77f7d-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f7d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f7d-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77f7d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f7d-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77f7d-132">INPUTS</span></span>

### <span data-ttu-id="77f7d-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77f7d-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="77f7d-134">O parâmetro ' VirtualNetworkGatewayConnection ' aceita o valor do tipo ' PSVirtualNetworkGatewayConnection ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="77f7d-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="77f7d-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77f7d-135">OUTPUTS</span></span>

### <span data-ttu-id="77f7d-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77f7d-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="77f7d-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77f7d-137">NOTES</span></span>

## <span data-ttu-id="77f7d-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77f7d-138">RELATED LINKS</span></span>

[<span data-ttu-id="77f7d-139">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77f7d-139">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="77f7d-140">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77f7d-140">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="77f7d-141">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77f7d-141">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


