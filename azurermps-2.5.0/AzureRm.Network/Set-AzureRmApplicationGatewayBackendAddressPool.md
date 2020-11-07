---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 66ca482f2b284118ccf5095ec833a5278a5ea73d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786394"
---
# <span data-ttu-id="81f89-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81f89-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="81f89-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81f89-102">SYNOPSIS</span></span>
<span data-ttu-id="81f89-103">Atualiza um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81f89-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81f89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81f89-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81f89-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81f89-105">DESCRIPTION</span></span>
<span data-ttu-id="81f89-106">O cmdlet **set-AzureRmApplicationGatewayBackendAddressPool** atualiza um pool de endereços back-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="81f89-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="81f89-107">Os endereços back-end podem ser especificados como endereços IP, FQDN (nome de domínio totalmente qualificado) ou IDs de configurações de IP.</span><span class="sxs-lookup"><span data-stu-id="81f89-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="81f89-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81f89-108">EXAMPLES</span></span>

### <span data-ttu-id="81f89-109">Exemplo 1: Configurando um pool de endereços back-end usando FQDNs</span><span class="sxs-lookup"><span data-stu-id="81f89-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="81f89-110">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="81f89-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="81f89-111">O segundo comando atualiza o pool de endereços back-end do gateway do aplicativo em $AppGw usando FQDNs.</span><span class="sxs-lookup"><span data-stu-id="81f89-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="81f89-112">Exemplo 2: Configurando um pool de endereços back-end usando endereços IP do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="81f89-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="81f89-113">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="81f89-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="81f89-114">O segundo comando atualiza o pool de endereços back-end do gateway do aplicativo em $AppGw usando endereços IP.</span><span class="sxs-lookup"><span data-stu-id="81f89-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="81f89-115">Exemplo 3: definindo um pool de endereços back-end usando a ID do endereço IP do servidor back-end? s</span><span class="sxs-lookup"><span data-stu-id="81f89-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\> $Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="81f89-116">O primeiro comando obtém um objeto de interface de rede chamado Nic01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável de 01 $Nic.</span><span class="sxs-lookup"><span data-stu-id="81f89-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="81f89-117">O segundo comando obtém um objeto de interface de rede chamado Nic02 que pertence ao grupo de recursos chamado ResourceGroup02 e o armazena na variável $Nic 02.</span><span class="sxs-lookup"><span data-stu-id="81f89-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="81f89-118">O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="81f89-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="81f89-119">O comando avançar usa as IDs de configuração de IP back-end de $Nic 01 e $Nic 02 para atualizar o pool de endereços back-end do gateway do aplicativo em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="81f89-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="81f89-120">OS</span><span class="sxs-lookup"><span data-stu-id="81f89-120">PARAMETERS</span></span>

### <span data-ttu-id="81f89-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81f89-121">-ApplicationGateway</span></span>
<span data-ttu-id="81f89-122">Especifica o gateway do aplicativo com o qual esse cmdlet associa o pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="81f89-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81f89-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="81f89-123">-BackendFqdns</span></span>
<span data-ttu-id="81f89-124">Especifica uma lista de endereços IP de back-end a serem usados como um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="81f89-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="81f89-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="81f89-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="81f89-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f89-126">-DefaultProfile</span></span>
<span data-ttu-id="81f89-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81f89-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81f89-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="81f89-128">-Name</span></span>
<span data-ttu-id="81f89-129">Especifica o nome do pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="81f89-129">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="81f89-130">Este pool de endereços back-end deve existir no Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="81f89-130">This back-end address pool must exist in the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f89-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81f89-131">-Confirm</span></span>
<span data-ttu-id="81f89-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81f89-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81f89-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81f89-133">-WhatIf</span></span>
<span data-ttu-id="81f89-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81f89-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81f89-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81f89-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81f89-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f89-136">CommonParameters</span></span>
<span data-ttu-id="81f89-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f89-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f89-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81f89-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f89-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81f89-139">INPUTS</span></span>

### <span data-ttu-id="81f89-140">System. String</span><span class="sxs-lookup"><span data-stu-id="81f89-140">System.String</span></span>

## <span data-ttu-id="81f89-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81f89-141">OUTPUTS</span></span>

### <span data-ttu-id="81f89-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81f89-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="81f89-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81f89-143">NOTES</span></span>

## <span data-ttu-id="81f89-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81f89-144">RELATED LINKS</span></span>

[<span data-ttu-id="81f89-145">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81f89-145">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="81f89-146">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81f89-146">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="81f89-147">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81f89-147">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="81f89-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81f89-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


