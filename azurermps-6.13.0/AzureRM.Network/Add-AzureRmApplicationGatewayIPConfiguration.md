---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 2ce0cb130e6c4d25d4b076d06224364011ced2b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440370"
---
# <span data-ttu-id="53110-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53110-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="53110-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53110-102">SYNOPSIS</span></span>
<span data-ttu-id="53110-103">Adiciona uma configuração de IP a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53110-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53110-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53110-104">SYNTAX</span></span>

### <span data-ttu-id="53110-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="53110-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53110-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="53110-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53110-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53110-107">DESCRIPTION</span></span>
<span data-ttu-id="53110-108">O cmdlet **Add-AzureRmApplicationGatewayIPConfiguration** adiciona uma configuração de IP a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53110-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="53110-109">As configurações de IP contêm a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="53110-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="53110-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53110-110">EXAMPLES</span></span>

### <span data-ttu-id="53110-111">Exemplo 1: adicionar uma configuração de rede virtual a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="53110-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="53110-112">O primeiro comando cria uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="53110-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="53110-113">O segundo comando cria uma sub-rede usando a rede virtual previamente criada.</span><span class="sxs-lookup"><span data-stu-id="53110-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="53110-114">O terceiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="53110-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="53110-115">O comando Fouth adiciona a configuração de IP ao gateway do aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="53110-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="53110-116">OS</span><span class="sxs-lookup"><span data-stu-id="53110-116">PARAMETERS</span></span>

### <span data-ttu-id="53110-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53110-117">-ApplicationGateway</span></span>
<span data-ttu-id="53110-118">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="53110-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="53110-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53110-119">-DefaultProfile</span></span>
<span data-ttu-id="53110-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53110-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53110-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="53110-121">-Name</span></span>
<span data-ttu-id="53110-122">Especifica o nome da configuração de IP a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="53110-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="53110-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="53110-123">-Subnet</span></span>
<span data-ttu-id="53110-124">Especifica uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="53110-124">Specifies a subnet.</span></span>
<span data-ttu-id="53110-125">Esta é a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="53110-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="53110-126">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="53110-126">-SubnetId</span></span>
<span data-ttu-id="53110-127">Especifica uma ID de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="53110-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="53110-128">Esta é a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="53110-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="53110-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53110-129">CommonParameters</span></span>
<span data-ttu-id="53110-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53110-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53110-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53110-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53110-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53110-132">INPUTS</span></span>

### <span data-ttu-id="53110-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53110-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="53110-134">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="53110-134">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="53110-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53110-135">OUTPUTS</span></span>

### <span data-ttu-id="53110-136">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53110-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="53110-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53110-137">NOTES</span></span>

## <span data-ttu-id="53110-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53110-138">RELATED LINKS</span></span>

[<span data-ttu-id="53110-139">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53110-139">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="53110-140">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53110-140">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="53110-141">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53110-141">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="53110-142">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53110-142">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


