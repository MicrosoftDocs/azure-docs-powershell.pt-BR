---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111649"
---
# <span data-ttu-id="6277c-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6277c-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="6277c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6277c-102">SYNOPSIS</span></span>
<span data-ttu-id="6277c-103">Cria uma configuração IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6277c-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="6277c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6277c-104">SYNTAX</span></span>

### <span data-ttu-id="6277c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6277c-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6277c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6277c-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6277c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6277c-107">DESCRIPTION</span></span>
<span data-ttu-id="6277c-108">O **cmdlet New-AzApplicationGatewayIPConfiguration** cria uma configuração IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6277c-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="6277c-109">A configuração IP contém a sub-rede na qual o gateway de aplicativos é implantado.</span><span class="sxs-lookup"><span data-stu-id="6277c-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="6277c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6277c-110">EXAMPLES</span></span>

### <span data-ttu-id="6277c-111">Exemplo 1: Criar uma configuração IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6277c-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="6277c-112">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6277c-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="6277c-113">O segundo comando obtém a configuração de sub-rede da sub-rede à que a rede virtual no comando anterior pertence e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="6277c-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="6277c-114">O terceiro comando cria a configuração IP usando $Subnet.</span><span class="sxs-lookup"><span data-stu-id="6277c-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="6277c-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6277c-115">PARAMETERS</span></span>

### <span data-ttu-id="6277c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6277c-116">-DefaultProfile</span></span>
<span data-ttu-id="6277c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6277c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6277c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6277c-118">-Name</span></span>
<span data-ttu-id="6277c-119">Especifica o nome da configuração IP a ser criado.</span><span class="sxs-lookup"><span data-stu-id="6277c-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="6277c-120">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="6277c-120">-Subnet</span></span>
<span data-ttu-id="6277c-121">Especifica o objeto da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6277c-121">Specifies the subnet object.</span></span>
<span data-ttu-id="6277c-122">Esta é a sub-rede na qual o gateway de aplicativos é implantado.</span><span class="sxs-lookup"><span data-stu-id="6277c-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="6277c-123">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="6277c-123">-SubnetId</span></span>
<span data-ttu-id="6277c-124">Especifica a ID da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6277c-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="6277c-125">Esta é a sub-rede na qual o gateway de aplicativos seria implantado.</span><span class="sxs-lookup"><span data-stu-id="6277c-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="6277c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6277c-126">CommonParameters</span></span>
<span data-ttu-id="6277c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6277c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6277c-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6277c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6277c-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="6277c-129">INPUTS</span></span>

### <span data-ttu-id="6277c-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6277c-130">None</span></span>

## <span data-ttu-id="6277c-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="6277c-131">OUTPUTS</span></span>

### <span data-ttu-id="6277c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6277c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="6277c-133">Notas</span><span class="sxs-lookup"><span data-stu-id="6277c-133">NOTES</span></span>

## <span data-ttu-id="6277c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6277c-134">RELATED LINKS</span></span>

[<span data-ttu-id="6277c-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6277c-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="6277c-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6277c-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="6277c-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6277c-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="6277c-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6277c-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


