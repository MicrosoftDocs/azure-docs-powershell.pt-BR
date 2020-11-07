---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b38ef9d212ceeb519e29d99391b17099177236a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776508"
---
# <span data-ttu-id="18b84-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18b84-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="18b84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18b84-102">SYNOPSIS</span></span>
<span data-ttu-id="18b84-103">Configura uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="18b84-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="18b84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18b84-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18b84-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18b84-105">DESCRIPTION</span></span>
<span data-ttu-id="18b84-106">O cmdlet **set-AzVirtualNetworkGatewayConnection** configura uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="18b84-106">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="18b84-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18b84-107">EXAMPLES</span></span>

### <span data-ttu-id="18b84-108">1:</span><span class="sxs-lookup"><span data-stu-id="18b84-108">1:</span></span>
```

```

## <span data-ttu-id="18b84-109">OS</span><span class="sxs-lookup"><span data-stu-id="18b84-109">PARAMETERS</span></span>

### <span data-ttu-id="18b84-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18b84-110">-AsJob</span></span>
<span data-ttu-id="18b84-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="18b84-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18b84-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b84-112">-DefaultProfile</span></span>
<span data-ttu-id="18b84-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18b84-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18b84-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="18b84-114">-EnableBgp</span></span>
<span data-ttu-id="18b84-115">Se você deve usar uma sessão BGP em um túnel VPN S2S</span><span class="sxs-lookup"><span data-stu-id="18b84-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="18b84-116">-Force</span><span class="sxs-lookup"><span data-stu-id="18b84-116">-Force</span></span>
<span data-ttu-id="18b84-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="18b84-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="18b84-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="18b84-118">-IpsecPolicies</span></span>
<span data-ttu-id="18b84-119">Uma lista de diretivas IPSec.</span><span class="sxs-lookup"><span data-stu-id="18b84-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="18b84-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="18b84-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="18b84-121">Se os seletores de tráfego baseados em políticas devem ser usados para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="18b84-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="18b84-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18b84-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="18b84-123">Especifica o objeto PSVirtualNetworkGatewayConnection que este cmdlet usa para modificar a conexão do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="18b84-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="18b84-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18b84-124">-Confirm</span></span>
<span data-ttu-id="18b84-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18b84-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18b84-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b84-126">-WhatIf</span></span>
<span data-ttu-id="18b84-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18b84-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18b84-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18b84-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18b84-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b84-129">CommonParameters</span></span>
<span data-ttu-id="18b84-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18b84-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b84-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b84-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b84-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18b84-132">INPUTS</span></span>

### <span data-ttu-id="18b84-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18b84-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="18b84-134">O parâmetro ' VirtualNetworkGatewayConnection ' aceita o valor do tipo ' PSVirtualNetworkGatewayConnection ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="18b84-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="18b84-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18b84-135">OUTPUTS</span></span>

### <span data-ttu-id="18b84-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18b84-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="18b84-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18b84-137">NOTES</span></span>

## <span data-ttu-id="18b84-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18b84-138">RELATED LINKS</span></span>

[<span data-ttu-id="18b84-139">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18b84-139">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="18b84-140">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18b84-140">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="18b84-141">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="18b84-141">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


