---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9c8730c1a6430d98567f880e101497ecc1be432d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114217"
---
# <span data-ttu-id="807fe-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="807fe-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="807fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="807fe-102">SYNOPSIS</span></span>
<span data-ttu-id="807fe-103">Adiciona uma configuração IP a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="807fe-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="807fe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="807fe-104">SYNTAX</span></span>

### <span data-ttu-id="807fe-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="807fe-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="807fe-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="807fe-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="807fe-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="807fe-107">DESCRIPTION</span></span>
<span data-ttu-id="807fe-108">O **cmdlet Add-AzApplicationGatewayIPConfiguration** adiciona uma configuração IP a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="807fe-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="807fe-109">As configurações de IP contêm a sub-rede na qual o gateway de aplicativo é implantado.</span><span class="sxs-lookup"><span data-stu-id="807fe-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="807fe-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="807fe-110">EXAMPLES</span></span>

### <span data-ttu-id="807fe-111">Exemplo 1: Adicionar uma configuração de rede virtual a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="807fe-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="807fe-112">O primeiro comando obtém uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="807fe-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="807fe-113">O segundo comando obtém uma sub-rede usando a rede virtual criada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="807fe-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="807fe-114">O terceiro comando obtém o gateway do aplicativo e o armazena na $AppGw variável.</span><span class="sxs-lookup"><span data-stu-id="807fe-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="807fe-115">O quarto comando adiciona a configuração ip ao gateway de aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="807fe-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="807fe-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="807fe-116">PARAMETERS</span></span>

### <span data-ttu-id="807fe-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="807fe-117">-ApplicationGateway</span></span>
<span data-ttu-id="807fe-118">Especifica o gateway do aplicativo ao qual este cmdlet adiciona uma configuração IP.</span><span class="sxs-lookup"><span data-stu-id="807fe-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="807fe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="807fe-119">-DefaultProfile</span></span>
<span data-ttu-id="807fe-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="807fe-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="807fe-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="807fe-121">-Name</span></span>
<span data-ttu-id="807fe-122">Especifica o nome da configuração IP a ser acrescentada.</span><span class="sxs-lookup"><span data-stu-id="807fe-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="807fe-123">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="807fe-123">-Subnet</span></span>
<span data-ttu-id="807fe-124">Especifica uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="807fe-124">Specifies a subnet.</span></span>
<span data-ttu-id="807fe-125">Esta é a sub-rede na qual o gateway de aplicativos é implantado.</span><span class="sxs-lookup"><span data-stu-id="807fe-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="807fe-126">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="807fe-126">-SubnetId</span></span>
<span data-ttu-id="807fe-127">Especifica uma ID de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="807fe-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="807fe-128">Esta é a sub-rede na qual o gateway de aplicativos é implantado.</span><span class="sxs-lookup"><span data-stu-id="807fe-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="807fe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="807fe-129">CommonParameters</span></span>
<span data-ttu-id="807fe-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="807fe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="807fe-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="807fe-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="807fe-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="807fe-132">INPUTS</span></span>

### <span data-ttu-id="807fe-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="807fe-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="807fe-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="807fe-134">OUTPUTS</span></span>

### <span data-ttu-id="807fe-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="807fe-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="807fe-136">Notas</span><span class="sxs-lookup"><span data-stu-id="807fe-136">NOTES</span></span>

## <span data-ttu-id="807fe-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="807fe-137">RELATED LINKS</span></span>

[<span data-ttu-id="807fe-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="807fe-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="807fe-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="807fe-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="807fe-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="807fe-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="807fe-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="807fe-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


