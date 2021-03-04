---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: b8a38bd16fcd08104f678752d03dbc4a6d1f054b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892087"
---
# <span data-ttu-id="3e66a-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e66a-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="3e66a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e66a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e66a-103">Modifica uma configuração IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3e66a-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="3e66a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3e66a-104">SYNTAX</span></span>

### <span data-ttu-id="3e66a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e66a-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e66a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3e66a-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e66a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3e66a-107">DESCRIPTION</span></span>
<span data-ttu-id="3e66a-108">O cmdlet **Set-AzApplicationGatewayIPConfiguration** modifica uma configuração IP.</span><span class="sxs-lookup"><span data-stu-id="3e66a-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="3e66a-109">Uma configuração IP contém a sub-rede na qual um gateway de aplicativo é implantado.</span><span class="sxs-lookup"><span data-stu-id="3e66a-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="3e66a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e66a-110">EXAMPLES</span></span>

### <span data-ttu-id="3e66a-111">Exemplo 1: atualizar uma configuração IP para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="3e66a-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="3e66a-112">O primeiro comando obtém a rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="3e66a-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="3e66a-113">O segundo comando obtém a configuração de sub-rede chamada Subnet01 usando $VNet e armazena-a na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="3e66a-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="3e66a-114">O terceiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3e66a-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3e66a-115">O comando forth define a configuração IP do gateway de aplicativo armazenado no $AppGw para a configuração de sub-rede armazenada em $Subnet.</span><span class="sxs-lookup"><span data-stu-id="3e66a-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="3e66a-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3e66a-116">PARAMETERS</span></span>

### <span data-ttu-id="3e66a-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e66a-117">-ApplicationGateway</span></span>
<span data-ttu-id="3e66a-118">Especifica um objeto gateway de aplicativo com o qual esse cmdlet associa uma configuração IP.</span><span class="sxs-lookup"><span data-stu-id="3e66a-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="3e66a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e66a-119">-DefaultProfile</span></span>
<span data-ttu-id="3e66a-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3e66a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e66a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3e66a-121">-Name</span></span>
<span data-ttu-id="3e66a-122">Especifica o nome da configuração IP.</span><span class="sxs-lookup"><span data-stu-id="3e66a-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="3e66a-123">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="3e66a-123">-Subnet</span></span>
<span data-ttu-id="3e66a-124">Especifica a sub-rede.</span><span class="sxs-lookup"><span data-stu-id="3e66a-124">Specifies the subnet.</span></span>
<span data-ttu-id="3e66a-125">Esta é a sub-rede na qual o gateway de aplicativo é implantado.</span><span class="sxs-lookup"><span data-stu-id="3e66a-125">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e66a-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3e66a-126">-SubnetId</span></span>
<span data-ttu-id="3e66a-127">Especifica a ID da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="3e66a-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="3e66a-128">Esta é a sub-rede na qual o gateway de aplicativo é implantado.</span><span class="sxs-lookup"><span data-stu-id="3e66a-128">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e66a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e66a-129">CommonParameters</span></span>
<span data-ttu-id="3e66a-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e66a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e66a-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e66a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e66a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e66a-132">INPUTS</span></span>

### <span data-ttu-id="3e66a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e66a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e66a-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3e66a-134">OUTPUTS</span></span>

### <span data-ttu-id="3e66a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e66a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e66a-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="3e66a-136">NOTES</span></span>

## <span data-ttu-id="3e66a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e66a-137">RELATED LINKS</span></span>

[<span data-ttu-id="3e66a-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e66a-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="3e66a-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e66a-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="3e66a-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e66a-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="3e66a-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e66a-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="3e66a-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e66a-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


