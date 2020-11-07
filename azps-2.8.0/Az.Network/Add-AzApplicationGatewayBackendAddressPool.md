---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: e59f09d44c1d6003122992cb5f14f51b411be25e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771845"
---
# <span data-ttu-id="c96c3-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c96c3-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="c96c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c96c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c96c3-103">Adiciona um pool de endereços back-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c96c3-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="c96c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c96c3-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c96c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c96c3-105">DESCRIPTION</span></span>
<span data-ttu-id="c96c3-106">O cmdlet **Add-AzApplicationGatewayBackendAddressPool** adiciona um pool de endereços back-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c96c3-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="c96c3-107">Um endereço de back-end pode ser especificado usando um endereço IP, um FQDN (nome de domínio totalmente qualificado) ou IDs de configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="c96c3-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="c96c3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c96c3-108">EXAMPLES</span></span>

### <span data-ttu-id="c96c3-109">Exemplo 1: adicionar um pool de endereços back-end usando um FQDN do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="c96c3-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="c96c3-110">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando adiciona o pool de endereços back-end do gateway do aplicativo armazenado no $AppGw usando FQDNs.</span><span class="sxs-lookup"><span data-stu-id="c96c3-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="c96c3-111">Exemplo 2: adicionar um pool de endereços back-end usando endereços IP do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="c96c3-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="c96c3-112">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando adiciona o pool de endereços back-end do gateway do aplicativo armazenado no $AppGw usando endereços IP.</span><span class="sxs-lookup"><span data-stu-id="c96c3-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="c96c3-113">Exemplo 3: pool de endereços back-end seta usando a ID do endereço IP do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="c96c3-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="c96c3-114">O primeiro comando obtém um objeto de interface de rede chamado Nic01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável de 01 $Nic. O segundo comando obtém um objeto de interface de rede chamado Nic02 que pertence ao grupo de recursos chamado ResourceGroup02 e o armazena na variável $Nic 02. O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O comando avançar usa as IDs de configuração de IP back-end de $Nic 01 e $Nic 02 para adicionar o pool de endereços back-end do gateway do aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c96c3-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c96c3-115">OS</span><span class="sxs-lookup"><span data-stu-id="c96c3-115">PARAMETERS</span></span>

### <span data-ttu-id="c96c3-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c96c3-116">-ApplicationGateway</span></span>
<span data-ttu-id="c96c3-117">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona um pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="c96c3-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="c96c3-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="c96c3-118">-BackendFqdns</span></span>
<span data-ttu-id="c96c3-119">Especifica uma lista de FQDNs de back-end que esse cmdlet adiciona como um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="c96c3-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="c96c3-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="c96c3-120">-BackendIPAddresses</span></span>
<span data-ttu-id="c96c3-121">Especifica uma lista de endereços IP back-end que esse cmdlet adiciona como um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="c96c3-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="c96c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c96c3-122">-DefaultProfile</span></span>
<span data-ttu-id="c96c3-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c96c3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c96c3-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c96c3-124">-Name</span></span>
<span data-ttu-id="c96c3-125">Especifica o nome do pool de servidores back-end que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="c96c3-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c96c3-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c96c3-126">-Confirm</span></span>
<span data-ttu-id="c96c3-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c96c3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c96c3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c96c3-128">-WhatIf</span></span>
<span data-ttu-id="c96c3-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c96c3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c96c3-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c96c3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c96c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c96c3-131">CommonParameters</span></span>
<span data-ttu-id="c96c3-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c96c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c96c3-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c96c3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c96c3-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c96c3-134">INPUTS</span></span>

### <span data-ttu-id="c96c3-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c96c3-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c96c3-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c96c3-136">OUTPUTS</span></span>

### <span data-ttu-id="c96c3-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c96c3-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c96c3-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c96c3-138">NOTES</span></span>

## <span data-ttu-id="c96c3-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c96c3-139">RELATED LINKS</span></span>

[<span data-ttu-id="c96c3-140">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c96c3-140">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c96c3-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c96c3-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c96c3-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c96c3-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c96c3-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c96c3-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c96c3-144">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c96c3-144">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


