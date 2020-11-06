---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 98e2249c3577d49a140d31b4287507e0e46185f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433085"
---
# <span data-ttu-id="23742-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="23742-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="23742-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23742-102">SYNOPSIS</span></span>
<span data-ttu-id="23742-103">Adiciona uma configuração de IP a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="23742-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23742-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23742-104">SYNTAX</span></span>

### <span data-ttu-id="23742-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="23742-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23742-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="23742-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23742-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23742-107">DESCRIPTION</span></span>
<span data-ttu-id="23742-108">O cmdlet **Add-AzureRmApplicationGatewayIPConfiguration** adiciona uma configuração de IP a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="23742-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="23742-109">As configurações de IP contêm a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="23742-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="23742-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23742-110">EXAMPLES</span></span>

### <span data-ttu-id="23742-111">Exemplo 1: adicionar uma configuração de rede virtual a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="23742-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="23742-112">O primeiro comando cria uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="23742-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="23742-113">O segundo comando cria uma sub-rede usando a rede virtual previamente criada.</span><span class="sxs-lookup"><span data-stu-id="23742-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="23742-114">O terceiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="23742-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="23742-115">O comando Fouth adiciona a configuração de IP ao gateway do aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="23742-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="23742-116">OS</span><span class="sxs-lookup"><span data-stu-id="23742-116">PARAMETERS</span></span>

### <span data-ttu-id="23742-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23742-117">-ApplicationGateway</span></span>
<span data-ttu-id="23742-118">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="23742-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="23742-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="23742-119">-Name</span></span>
<span data-ttu-id="23742-120">Especifica o nome da configuração de IP a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="23742-120">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="23742-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="23742-121">-Subnet</span></span>
<span data-ttu-id="23742-122">Especifica uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="23742-122">Specifies a subnet.</span></span>
<span data-ttu-id="23742-123">Esta é a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="23742-123">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="23742-124">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="23742-124">-SubnetId</span></span>
<span data-ttu-id="23742-125">Especifica uma ID de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="23742-125">Specifies a subnet ID.</span></span>
<span data-ttu-id="23742-126">Esta é a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="23742-126">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="23742-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23742-127">-DefaultProfile</span></span>
<span data-ttu-id="23742-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23742-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23742-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23742-129">CommonParameters</span></span>
<span data-ttu-id="23742-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23742-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23742-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23742-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23742-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23742-132">INPUTS</span></span>

### <span data-ttu-id="23742-133">System. String</span><span class="sxs-lookup"><span data-stu-id="23742-133">System.String</span></span>

## <span data-ttu-id="23742-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23742-134">OUTPUTS</span></span>

### <span data-ttu-id="23742-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23742-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="23742-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23742-136">NOTES</span></span>

## <span data-ttu-id="23742-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23742-137">RELATED LINKS</span></span>

[<span data-ttu-id="23742-138">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="23742-138">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="23742-139">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="23742-139">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="23742-140">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="23742-140">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="23742-141">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="23742-141">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


