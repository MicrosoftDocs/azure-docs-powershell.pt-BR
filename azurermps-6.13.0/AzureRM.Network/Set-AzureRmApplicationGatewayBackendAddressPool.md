---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d62afff67d1b5e7722b107b70810ac82e5b151d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603143"
---
# <span data-ttu-id="dc405-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc405-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="dc405-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc405-102">SYNOPSIS</span></span>
<span data-ttu-id="dc405-103">Atualiza um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dc405-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc405-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc405-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc405-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc405-105">DESCRIPTION</span></span>
<span data-ttu-id="dc405-106">O cmdlet **set-AzureRmApplicationGatewayBackendAddressPool** atualiza um pool de endereços back-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc405-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="dc405-107">Os endereços back-end podem ser especificados como endereços IP, FQDN (nome de domínio totalmente qualificado) ou IDs de configurações de IP.</span><span class="sxs-lookup"><span data-stu-id="dc405-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="dc405-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc405-108">EXAMPLES</span></span>

### <span data-ttu-id="dc405-109">Exemplo 1: Configurando um pool de endereços back-end usando FQDNs</span><span class="sxs-lookup"><span data-stu-id="dc405-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="dc405-110">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="dc405-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dc405-111">O segundo comando atualiza o pool de endereços back-end do gateway do aplicativo em $AppGw usando FQDNs.</span><span class="sxs-lookup"><span data-stu-id="dc405-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="dc405-112">Exemplo 2: Configurando um pool de endereços back-end usando endereços IP do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="dc405-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="dc405-113">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="dc405-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dc405-114">O segundo comando atualiza o pool de endereços back-end do gateway do aplicativo em $AppGw usando endereços IP.</span><span class="sxs-lookup"><span data-stu-id="dc405-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="dc405-115">OS</span><span class="sxs-lookup"><span data-stu-id="dc405-115">PARAMETERS</span></span>

### <span data-ttu-id="dc405-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc405-116">-ApplicationGateway</span></span>
<span data-ttu-id="dc405-117">Especifica o gateway do aplicativo com o qual esse cmdlet associa o pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="dc405-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="dc405-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="dc405-118">-BackendFqdns</span></span>
<span data-ttu-id="dc405-119">Especifica uma lista de endereços IP de back-end a serem usados como um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="dc405-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc405-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="dc405-120">-BackendIPAddresses</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc405-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc405-121">-DefaultProfile</span></span>
<span data-ttu-id="dc405-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc405-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc405-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc405-123">-Name</span></span>
<span data-ttu-id="dc405-124">Especifica o nome do pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="dc405-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="dc405-125">Este pool de endereços back-end deve existir no Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dc405-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="dc405-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dc405-126">-Confirm</span></span>
<span data-ttu-id="dc405-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc405-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc405-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc405-128">-WhatIf</span></span>
<span data-ttu-id="dc405-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc405-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc405-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc405-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc405-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc405-131">CommonParameters</span></span>
<span data-ttu-id="dc405-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc405-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc405-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc405-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc405-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc405-134">INPUTS</span></span>

### <span data-ttu-id="dc405-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc405-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="dc405-136">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dc405-136">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="dc405-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc405-137">OUTPUTS</span></span>

### <span data-ttu-id="dc405-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc405-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc405-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc405-139">NOTES</span></span>

## <span data-ttu-id="dc405-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc405-140">RELATED LINKS</span></span>

[<span data-ttu-id="dc405-141">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc405-141">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dc405-142">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc405-142">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dc405-143">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc405-143">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dc405-144">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc405-144">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


