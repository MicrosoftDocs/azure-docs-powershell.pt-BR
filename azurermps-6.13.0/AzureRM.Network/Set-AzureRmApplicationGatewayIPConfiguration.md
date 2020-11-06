---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 013831c6b7b05a1da520744df9823076d95ccf3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441229"
---
# <span data-ttu-id="8b0d6-101">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b0d6-101">Set-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="8b0d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0d6-103">Modifica uma configuração de IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-103">Modifies an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b0d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b0d6-104">SYNTAX</span></span>

### <span data-ttu-id="8b0d6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b0d6-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b0d6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8b0d6-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b0d6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b0d6-107">DESCRIPTION</span></span>
<span data-ttu-id="8b0d6-108">O cmdlet **set-AzureRmApplicationGatewayIPConfiguration** modifica uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-108">The **Set-AzureRmApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="8b0d6-109">Uma configuração de IP contém a sub-rede na qual um gateway de aplicativo é implantado.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="8b0d6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b0d6-110">EXAMPLES</span></span>

### <span data-ttu-id="8b0d6-111">Exemplo 1: definir o estado da meta de uma configuração de IP</span><span class="sxs-lookup"><span data-stu-id="8b0d6-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzureRmVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="8b0d6-112">O primeiro comando obtém a rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="8b0d6-113">O segundo comando obtém a configuração de sub-rede chamada Subnet01 usando $VNet e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="8b0d6-114">O terceiro comando obtém um gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8b0d6-115">O comando avançar define a configuração de IP do gateway do aplicativo armazenado no $AppGw para a configuração de sub-rede armazenada no $Subnet.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="8b0d6-116">OS</span><span class="sxs-lookup"><span data-stu-id="8b0d6-116">PARAMETERS</span></span>

### <span data-ttu-id="8b0d6-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b0d6-117">-ApplicationGateway</span></span>
<span data-ttu-id="8b0d6-118">Especifica um objeto do aplicativo gateway com o qual esse cmdlet associa uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="8b0d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0d6-119">-DefaultProfile</span></span>
<span data-ttu-id="8b0d6-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b0d6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b0d6-121">-Name</span></span>
<span data-ttu-id="8b0d6-122">Especifica o nome da configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="8b0d6-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="8b0d6-123">-Subnet</span></span>
<span data-ttu-id="8b0d6-124">Especifica a sub-rede.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-124">Specifies the subnet.</span></span>
<span data-ttu-id="8b0d6-125">Esta é a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="8b0d6-126">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="8b0d6-126">-SubnetId</span></span>
<span data-ttu-id="8b0d6-127">Especifica a identificação de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="8b0d6-128">Esta é a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="8b0d6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0d6-129">CommonParameters</span></span>
<span data-ttu-id="8b0d6-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b0d6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0d6-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b0d6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0d6-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b0d6-132">INPUTS</span></span>

### <span data-ttu-id="8b0d6-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b0d6-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="8b0d6-134">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8b0d6-134">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="8b0d6-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b0d6-135">OUTPUTS</span></span>

### <span data-ttu-id="8b0d6-136">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b0d6-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8b0d6-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b0d6-137">NOTES</span></span>

## <span data-ttu-id="8b0d6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b0d6-138">RELATED LINKS</span></span>

[<span data-ttu-id="8b0d6-139">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b0d6-139">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8b0d6-140">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b0d6-140">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8b0d6-141">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b0d6-141">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8b0d6-142">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b0d6-142">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8b0d6-143">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b0d6-143">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)


