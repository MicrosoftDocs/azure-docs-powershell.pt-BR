---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5885f98d66e6226273215dcde856f5fc50d0bd56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429216"
---
# <span data-ttu-id="8fd98-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8fd98-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8fd98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8fd98-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd98-103">Configura uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8fd98-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fd98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fd98-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fd98-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8fd98-105">DESCRIPTION</span></span>
<span data-ttu-id="8fd98-106">O cmdlet **set-AzureRmVirtualNetworkGatewayConnection** configura uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8fd98-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="8fd98-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fd98-107">EXAMPLES</span></span>

## <span data-ttu-id="8fd98-108">OS</span><span class="sxs-lookup"><span data-stu-id="8fd98-108">PARAMETERS</span></span>

### <span data-ttu-id="8fd98-109">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="8fd98-109">-EnableBgp</span></span>
<span data-ttu-id="8fd98-110">Se você deve usar uma sessão BGP em um túnel VPN S2S</span><span class="sxs-lookup"><span data-stu-id="8fd98-110">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd98-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8fd98-111">-Force</span></span>
<span data-ttu-id="8fd98-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8fd98-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8fd98-113">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="8fd98-113">-IpsecPolicies</span></span>
<span data-ttu-id="8fd98-114">Uma lista de diretivas IPSec.</span><span class="sxs-lookup"><span data-stu-id="8fd98-114">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="8fd98-115">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="8fd98-115">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="8fd98-116">Se os seletores de tráfego baseados em políticas devem ser usados para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="8fd98-116">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd98-117">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8fd98-117">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="8fd98-118">Especifica o objeto PSVirtualNetworkGatewayConnection que este cmdlet usa para modificar a conexão do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8fd98-118">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd98-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8fd98-119">-Confirm</span></span>
<span data-ttu-id="8fd98-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fd98-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd98-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd98-121">-WhatIf</span></span>
<span data-ttu-id="8fd98-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8fd98-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd98-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8fd98-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd98-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd98-124">-DefaultProfile</span></span>
<span data-ttu-id="8fd98-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd98-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fd98-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd98-126">CommonParameters</span></span>
<span data-ttu-id="8fd98-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd98-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd98-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd98-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd98-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8fd98-129">INPUTS</span></span>

### <span data-ttu-id="8fd98-130">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8fd98-130">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="8fd98-131">O parâmetro ' VirtualNetworkGatewayConnection ' aceita o valor do tipo ' PSVirtualNetworkGatewayConnection ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8fd98-131">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="8fd98-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8fd98-132">OUTPUTS</span></span>

### <span data-ttu-id="8fd98-133">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8fd98-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8fd98-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8fd98-134">NOTES</span></span>

## <span data-ttu-id="8fd98-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fd98-135">RELATED LINKS</span></span>

[<span data-ttu-id="8fd98-136">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8fd98-136">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="8fd98-137">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8fd98-137">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="8fd98-138">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8fd98-138">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


