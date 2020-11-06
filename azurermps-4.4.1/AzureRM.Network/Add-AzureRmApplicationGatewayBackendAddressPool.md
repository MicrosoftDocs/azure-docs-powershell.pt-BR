---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: ada3ab6c2539561f440816215049030960ff21a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427883"
---
# <span data-ttu-id="18823-101">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18823-101">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="18823-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18823-102">SYNOPSIS</span></span>
<span data-ttu-id="18823-103">Adiciona um pool de endereços back-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="18823-103">Adds a back-end address pool to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18823-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18823-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18823-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18823-105">DESCRIPTION</span></span>
<span data-ttu-id="18823-106">O cmdlet **Add-AzureRmApplicationGatewayBackendAddressPool** adiciona um pool de endereços back-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="18823-106">The **Add-AzureRmApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="18823-107">Um endereço de back-end pode ser especificado usando um endereço IP, um FQDN (nome de domínio totalmente qualificado) ou IDs de configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="18823-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="18823-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18823-108">EXAMPLES</span></span>

### <span data-ttu-id="18823-109">Exemplo 1: adicionar um pool de endereços back-end usando um FQDN do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="18823-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="18823-110">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando adiciona o pool de endereços back-end do gateway do aplicativo armazenado no $AppGw usando FQDNs.</span><span class="sxs-lookup"><span data-stu-id="18823-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="18823-111">Exemplo 2: adicionar um pool de endereços back-end usando endereços IP do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="18823-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzureApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="18823-112">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando adiciona o pool de endereços back-end do gateway do aplicativo armazenado no $AppGw usando endereços IP.</span><span class="sxs-lookup"><span data-stu-id="18823-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="18823-113">Exemplo 3: pool de endereços back-end seta usando a ID do endereço IP do servidor back-end</span><span class="sxs-lookup"><span data-stu-id="18823-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="18823-114">O primeiro comando obtém um objeto de interface de rede chamado Nic01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável de 01 $Nic. O segundo comando obtém um objeto de interface de rede chamado Nic02 que pertence ao grupo de recursos chamado ResourceGroup02 e o armazena na variável $Nic 02. O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O comando avançar usa as IDs de configuração de IP back-end de $Nic 01 e $Nic 02 para adicionar o pool de endereços back-end do gateway do aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="18823-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="18823-115">OS</span><span class="sxs-lookup"><span data-stu-id="18823-115">PARAMETERS</span></span>

### <span data-ttu-id="18823-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18823-116">-ApplicationGateway</span></span>
<span data-ttu-id="18823-117">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona um pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="18823-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="18823-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="18823-118">-BackendFqdns</span></span>
<span data-ttu-id="18823-119">Especifica uma lista de FQDNs de back-end que esse cmdlet adiciona como um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="18823-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="18823-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="18823-120">-BackendIPAddresses</span></span>
<span data-ttu-id="18823-121">Especifica uma lista de endereços IP back-end que esse cmdlet adiciona como um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="18823-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="18823-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="18823-122">-Name</span></span>
<span data-ttu-id="18823-123">Especifica o nome do pool de servidores back-end que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="18823-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="18823-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18823-124">-Confirm</span></span>
<span data-ttu-id="18823-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18823-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18823-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18823-126">-WhatIf</span></span>
<span data-ttu-id="18823-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18823-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18823-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18823-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18823-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18823-129">-DefaultProfile</span></span>
<span data-ttu-id="18823-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18823-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18823-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18823-131">CommonParameters</span></span>
<span data-ttu-id="18823-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18823-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18823-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18823-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18823-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18823-134">INPUTS</span></span>

###  
<span data-ttu-id="18823-135">System. String</span><span class="sxs-lookup"><span data-stu-id="18823-135">System.String</span></span>

## <span data-ttu-id="18823-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18823-136">OUTPUTS</span></span>

### <span data-ttu-id="18823-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18823-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="18823-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18823-138">NOTES</span></span>

## <span data-ttu-id="18823-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18823-139">RELATED LINKS</span></span>

[<span data-ttu-id="18823-140">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18823-140">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="18823-141">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18823-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="18823-142">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18823-142">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="18823-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18823-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="18823-144">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18823-144">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)

