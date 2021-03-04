---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 6399843edfc8ee806693e0ddfee77952438f2d35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890781"
---
# <span data-ttu-id="f6a6e-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6a6e-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="f6a6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a6e-103">Cria uma configuração IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="f6a6e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f6a6e-104">SYNTAX</span></span>

### <span data-ttu-id="f6a6e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f6a6e-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6a6e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f6a6e-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6a6e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f6a6e-107">DESCRIPTION</span></span>
<span data-ttu-id="f6a6e-108">O cmdlet **New-AzApplicationGatewayIPConfiguration** cria uma configuração IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="f6a6e-109">A configuração ip contém a sub-rede na qual o gateway de aplicativo é implantado.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="f6a6e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6a6e-110">EXAMPLES</span></span>

### <span data-ttu-id="f6a6e-111">Exemplo 1: Criar uma configuração IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="f6a6e-112">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="f6a6e-113">O segundo comando obtém a configuração de sub-rede da sub-rede à que a rede virtual no comando anterior pertence e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="f6a6e-114">O terceiro comando cria a configuração IP usando $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="f6a6e-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f6a6e-115">PARAMETERS</span></span>

### <span data-ttu-id="f6a6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a6e-116">-DefaultProfile</span></span>
<span data-ttu-id="f6a6e-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6a6e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f6a6e-118">-Name</span></span>
<span data-ttu-id="f6a6e-119">Especifica o nome da configuração IP a ser criado.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="f6a6e-120">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="f6a6e-120">-Subnet</span></span>
<span data-ttu-id="f6a6e-121">Especifica o objeto de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-121">Specifies the subnet object.</span></span>
<span data-ttu-id="f6a6e-122">Esta é a sub-rede na qual o gateway de aplicativo é implantado.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="f6a6e-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f6a6e-123">-SubnetId</span></span>
<span data-ttu-id="f6a6e-124">Especifica a ID da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="f6a6e-125">Esta é a sub-rede na qual o gateway de aplicativo seria implantado.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="f6a6e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a6e-126">CommonParameters</span></span>
<span data-ttu-id="f6a6e-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a6e-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a6e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a6e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6a6e-129">INPUTS</span></span>

### <span data-ttu-id="f6a6e-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f6a6e-130">None</span></span>

## <span data-ttu-id="f6a6e-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f6a6e-131">OUTPUTS</span></span>

### <span data-ttu-id="f6a6e-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6a6e-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="f6a6e-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="f6a6e-133">NOTES</span></span>

## <span data-ttu-id="f6a6e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6a6e-134">RELATED LINKS</span></span>

[<span data-ttu-id="f6a6e-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6a6e-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f6a6e-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6a6e-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f6a6e-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6a6e-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f6a6e-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6a6e-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


