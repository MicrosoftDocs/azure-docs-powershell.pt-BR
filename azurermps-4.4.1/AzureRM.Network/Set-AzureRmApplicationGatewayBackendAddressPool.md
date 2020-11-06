---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: dd5a0a14a0c2146ce6187a3ae08fda1bc3e60702
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611087"
---
# <span data-ttu-id="11a62-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="11a62-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="11a62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11a62-102">SYNOPSIS</span></span>
<span data-ttu-id="11a62-103">Atualiza um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11a62-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11a62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11a62-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11a62-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11a62-105">DESCRIPTION</span></span>
<span data-ttu-id="11a62-106">O cmdlet **set-AzureRmApplicationGatewayBackendAddressPool** atualiza um pool de endereços back-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="11a62-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="11a62-107">Os endereços back-end podem ser especificados como endereços IP, FQDN (nome de domínio totalmente qualificado) ou IDs de configurações de IP.</span><span class="sxs-lookup"><span data-stu-id="11a62-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="11a62-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11a62-108">EXAMPLES</span></span>

### <span data-ttu-id="11a62-109">Exemplo 1: Configurando um pool de endereços back-end usando FQDNs</span><span class="sxs-lookup"><span data-stu-id="11a62-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="11a62-110">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="11a62-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="11a62-111">O segundo comando atualiza o pool de endereços back-end do gateway do aplicativo em $AppGw usando FQDNs.</span><span class="sxs-lookup"><span data-stu-id="11a62-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="11a62-112">Exemplo 2: Configurando um pool de endereços back-end usando endereços IP do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="11a62-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="11a62-113">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="11a62-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="11a62-114">O segundo comando atualiza o pool de endereços back-end do gateway do aplicativo em $AppGw usando endereços IP.</span><span class="sxs-lookup"><span data-stu-id="11a62-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="11a62-115">Exemplo 3: definindo um pool de endereços back-end usando a ID do endereço IP do servidor back-end? s</span><span class="sxs-lookup"><span data-stu-id="11a62-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="11a62-116">O primeiro comando obtém um objeto de interface de rede chamado Nic01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável de 01 $Nic.</span><span class="sxs-lookup"><span data-stu-id="11a62-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="11a62-117">O segundo comando obtém um objeto de interface de rede chamado Nic02 que pertence ao grupo de recursos chamado ResourceGroup02 e o armazena na variável $Nic 02.</span><span class="sxs-lookup"><span data-stu-id="11a62-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="11a62-118">O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="11a62-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="11a62-119">O comando avançar usa as IDs de configuração de IP back-end de $Nic 01 e $Nic 02 para atualizar o pool de endereços back-end do gateway do aplicativo em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="11a62-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="11a62-120">OS</span><span class="sxs-lookup"><span data-stu-id="11a62-120">PARAMETERS</span></span>

### <span data-ttu-id="11a62-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11a62-121">-ApplicationGateway</span></span>
<span data-ttu-id="11a62-122">Especifica o gateway do aplicativo com o qual esse cmdlet associa o pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="11a62-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="11a62-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="11a62-123">-BackendFqdns</span></span>
<span data-ttu-id="11a62-124">Especifica uma lista de endereços IP de back-end a serem usados como um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="11a62-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="11a62-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="11a62-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="11a62-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="11a62-126">-Name</span></span>
<span data-ttu-id="11a62-127">Especifica o nome do pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="11a62-127">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="11a62-128">Este pool de endereços back-end deve existir no Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="11a62-128">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="11a62-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="11a62-129">-Confirm</span></span>
<span data-ttu-id="11a62-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11a62-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11a62-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11a62-131">-WhatIf</span></span>
<span data-ttu-id="11a62-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11a62-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11a62-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11a62-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11a62-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a62-134">-DefaultProfile</span></span>
<span data-ttu-id="11a62-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11a62-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11a62-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a62-136">CommonParameters</span></span>
<span data-ttu-id="11a62-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11a62-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a62-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11a62-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a62-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11a62-139">INPUTS</span></span>

### <span data-ttu-id="11a62-140">System. String</span><span class="sxs-lookup"><span data-stu-id="11a62-140">System.String</span></span>

## <span data-ttu-id="11a62-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11a62-141">OUTPUTS</span></span>

### <span data-ttu-id="11a62-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11a62-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11a62-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11a62-143">NOTES</span></span>

## <span data-ttu-id="11a62-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11a62-144">RELATED LINKS</span></span>

[<span data-ttu-id="11a62-145">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="11a62-145">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="11a62-146">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="11a62-146">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="11a62-147">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="11a62-147">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="11a62-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="11a62-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


