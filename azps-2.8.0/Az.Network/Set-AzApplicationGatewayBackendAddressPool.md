---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 9315b279fd7ac6842a65c78898f1d5da23a8e1c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771475"
---
# <span data-ttu-id="9c10c-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9c10c-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="9c10c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c10c-102">SYNOPSIS</span></span>
<span data-ttu-id="9c10c-103">Atualiza um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9c10c-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="9c10c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c10c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c10c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c10c-105">DESCRIPTION</span></span>
<span data-ttu-id="9c10c-106">O cmdlet **set-AzApplicationGatewayBackendAddressPool** atualiza um pool de endereços back-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c10c-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="9c10c-107">Os endereços back-end podem ser especificados como endereços IP, FQDN (nome de domínio totalmente qualificado) ou IDs de configurações de IP.</span><span class="sxs-lookup"><span data-stu-id="9c10c-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="9c10c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c10c-108">EXAMPLES</span></span>

### <span data-ttu-id="9c10c-109">Exemplo 1: Configurando um pool de endereços back-end usando FQDNs</span><span class="sxs-lookup"><span data-stu-id="9c10c-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="9c10c-110">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9c10c-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9c10c-111">O segundo comando atualiza o pool de endereços back-end do gateway do aplicativo em $AppGw usando FQDNs.</span><span class="sxs-lookup"><span data-stu-id="9c10c-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="9c10c-112">Exemplo 2: Configurando um pool de endereços back-end usando endereços IP do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="9c10c-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="9c10c-113">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9c10c-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9c10c-114">O segundo comando atualiza o pool de endereços back-end do gateway do aplicativo em $AppGw usando endereços IP.</span><span class="sxs-lookup"><span data-stu-id="9c10c-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="9c10c-115">OS</span><span class="sxs-lookup"><span data-stu-id="9c10c-115">PARAMETERS</span></span>

### <span data-ttu-id="9c10c-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c10c-116">-ApplicationGateway</span></span>
<span data-ttu-id="9c10c-117">Especifica o gateway do aplicativo com o qual esse cmdlet associa o pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="9c10c-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="9c10c-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="9c10c-118">-BackendFqdns</span></span>
<span data-ttu-id="9c10c-119">Especifica uma lista de endereços IP de back-end a serem usados como um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="9c10c-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="9c10c-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="9c10c-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="9c10c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c10c-121">-DefaultProfile</span></span>
<span data-ttu-id="9c10c-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c10c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c10c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c10c-123">-Name</span></span>
<span data-ttu-id="9c10c-124">Especifica o nome do pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="9c10c-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="9c10c-125">Este pool de endereços back-end deve existir no Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9c10c-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="9c10c-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c10c-126">-Confirm</span></span>
<span data-ttu-id="9c10c-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c10c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c10c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c10c-128">-WhatIf</span></span>
<span data-ttu-id="9c10c-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c10c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c10c-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c10c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c10c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c10c-131">CommonParameters</span></span>
<span data-ttu-id="9c10c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c10c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c10c-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c10c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c10c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c10c-134">INPUTS</span></span>

### <span data-ttu-id="9c10c-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c10c-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c10c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c10c-136">OUTPUTS</span></span>

### <span data-ttu-id="9c10c-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c10c-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c10c-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c10c-138">NOTES</span></span>

## <span data-ttu-id="9c10c-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c10c-139">RELATED LINKS</span></span>

[<span data-ttu-id="9c10c-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9c10c-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9c10c-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9c10c-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9c10c-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9c10c-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9c10c-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9c10c-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


