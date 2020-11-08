---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111118"
---
# <span data-ttu-id="3fca9-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3fca9-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="3fca9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fca9-102">SYNOPSIS</span></span>
<span data-ttu-id="3fca9-103">Adiciona um pool de endereços back-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3fca9-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="3fca9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3fca9-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fca9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3fca9-105">DESCRIPTION</span></span>
<span data-ttu-id="3fca9-106">O cmdlet **Add-AzApplicationGatewayBackendAddressPool** adiciona um pool de endereços back-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3fca9-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="3fca9-107">Um endereço de back-end pode ser especificado usando um endereço IP, um FQDN (nome de domínio totalmente qualificado) ou IDs de configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="3fca9-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="3fca9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3fca9-108">EXAMPLES</span></span>

### <span data-ttu-id="3fca9-109">Exemplo 1: adicionar um pool de endereços back-end usando um FQDN do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="3fca9-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="3fca9-110">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando adiciona o pool de endereços back-end do gateway do aplicativo armazenado no $AppGw usando FQDNs.</span><span class="sxs-lookup"><span data-stu-id="3fca9-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="3fca9-111">Exemplo 2: adicionar um pool de endereços back-end usando endereços IP do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="3fca9-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="3fca9-112">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando adiciona o pool de endereços back-end do gateway do aplicativo armazenado no $AppGw usando endereços IP.</span><span class="sxs-lookup"><span data-stu-id="3fca9-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="3fca9-113">OS</span><span class="sxs-lookup"><span data-stu-id="3fca9-113">PARAMETERS</span></span>

### <span data-ttu-id="3fca9-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3fca9-114">-ApplicationGateway</span></span>
<span data-ttu-id="3fca9-115">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona um pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="3fca9-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fca9-116">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="3fca9-116">-BackendFqdns</span></span>
<span data-ttu-id="3fca9-117">Especifica uma lista de FQDNs de back-end que esse cmdlet adiciona como um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="3fca9-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fca9-118">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="3fca9-118">-BackendIPAddresses</span></span>
<span data-ttu-id="3fca9-119">Especifica uma lista de endereços IP back-end que esse cmdlet adiciona como um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="3fca9-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fca9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fca9-120">-DefaultProfile</span></span>
<span data-ttu-id="3fca9-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3fca9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fca9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3fca9-122">-Name</span></span>
<span data-ttu-id="3fca9-123">Especifica o nome do pool de servidores back-end que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="3fca9-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fca9-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3fca9-124">-Confirm</span></span>
<span data-ttu-id="3fca9-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fca9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fca9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fca9-126">-WhatIf</span></span>
<span data-ttu-id="3fca9-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3fca9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fca9-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3fca9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fca9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fca9-129">CommonParameters</span></span>
<span data-ttu-id="3fca9-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fca9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fca9-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fca9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fca9-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3fca9-132">INPUTS</span></span>

### <span data-ttu-id="3fca9-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3fca9-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3fca9-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3fca9-134">OUTPUTS</span></span>

### <span data-ttu-id="3fca9-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3fca9-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3fca9-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3fca9-136">NOTES</span></span>

## <span data-ttu-id="3fca9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fca9-137">RELATED LINKS</span></span>

[<span data-ttu-id="3fca9-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3fca9-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3fca9-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3fca9-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3fca9-140">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3fca9-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3fca9-141">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3fca9-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3fca9-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3fca9-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3fca9-143">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3fca9-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
