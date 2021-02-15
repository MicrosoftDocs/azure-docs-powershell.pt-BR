---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a5b0fa1054136354725ec404960bcf680a104d06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115070"
---
# <span data-ttu-id="c987b-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c987b-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="c987b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c987b-102">SYNOPSIS</span></span>
<span data-ttu-id="c987b-103">Atualiza um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c987b-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="c987b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c987b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c987b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c987b-105">DESCRIPTION</span></span>
<span data-ttu-id="c987b-106">O cmdlet **Set-AzApplicationGatewayBackendAddressPool** atualiza um pool de endereços back-end para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="c987b-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="c987b-107">Endereços back-end podem ser especificados como endereços IP, nomes de domínio totalmente qualificados (FQDN) ou IDs de configurações IP.</span><span class="sxs-lookup"><span data-stu-id="c987b-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="c987b-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c987b-108">EXAMPLES</span></span>

### <span data-ttu-id="c987b-109">Exemplo 1: Definir um pool de endereços back-end usando FQDNs</span><span class="sxs-lookup"><span data-stu-id="c987b-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="c987b-110">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw usuário.</span><span class="sxs-lookup"><span data-stu-id="c987b-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c987b-111">O segundo comando atualiza o pool de endereços back-end do gateway de aplicativo no $AppGw usando FQDNs.</span><span class="sxs-lookup"><span data-stu-id="c987b-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="c987b-112">Exemplo 2: Configurando um pool de endereços back-end usando endereços IP do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="c987b-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="c987b-113">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw usuário.</span><span class="sxs-lookup"><span data-stu-id="c987b-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c987b-114">O segundo comando atualiza o pool de endereços back-end do gateway do aplicativo no $AppGw usando endereços IP.</span><span class="sxs-lookup"><span data-stu-id="c987b-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="c987b-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c987b-115">PARAMETERS</span></span>

### <span data-ttu-id="c987b-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c987b-116">-ApplicationGateway</span></span>
<span data-ttu-id="c987b-117">Especifica o gateway do aplicativo ao qual este cmdlet associa o pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="c987b-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="c987b-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="c987b-118">-BackendFqdns</span></span>
<span data-ttu-id="c987b-119">Especifica uma lista de endereços IP de back-end para usar como um pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="c987b-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="c987b-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="c987b-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="c987b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c987b-121">-DefaultProfile</span></span>
<span data-ttu-id="c987b-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c987b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c987b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c987b-123">-Name</span></span>
<span data-ttu-id="c987b-124">Especifica o nome do pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="c987b-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="c987b-125">Esse pool de endereços back-end deve existir no gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c987b-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="c987b-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c987b-126">-Confirm</span></span>
<span data-ttu-id="c987b-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c987b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c987b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c987b-128">-WhatIf</span></span>
<span data-ttu-id="c987b-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c987b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c987b-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c987b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c987b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c987b-131">CommonParameters</span></span>
<span data-ttu-id="c987b-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c987b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c987b-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c987b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c987b-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="c987b-134">INPUTS</span></span>

### <span data-ttu-id="c987b-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c987b-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c987b-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="c987b-136">OUTPUTS</span></span>

### <span data-ttu-id="c987b-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c987b-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c987b-138">Notas</span><span class="sxs-lookup"><span data-stu-id="c987b-138">NOTES</span></span>

## <span data-ttu-id="c987b-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c987b-139">RELATED LINKS</span></span>

[<span data-ttu-id="c987b-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c987b-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c987b-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c987b-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c987b-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c987b-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c987b-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c987b-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


