---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e06d91fe55d8288b4f123202e2e32d90c51af3eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432306"
---
# <span data-ttu-id="677d1-101">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="677d1-101">New-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="677d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="677d1-102">SYNOPSIS</span></span>
<span data-ttu-id="677d1-103">Cria uma configuração de IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="677d1-103">Creates an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="677d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="677d1-104">SYNTAX</span></span>

### <span data-ttu-id="677d1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="677d1-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="677d1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="677d1-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="677d1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="677d1-107">DESCRIPTION</span></span>
<span data-ttu-id="677d1-108">O cmdlet **New-AzureRmApplicationGatewayIPConfiguration** cria uma configuração de IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="677d1-108">The **New-AzureRmApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="677d1-109">A configuração de IP contém a sub-rede na qual o gateway do aplicativo é implantado.</span><span class="sxs-lookup"><span data-stu-id="677d1-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="677d1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="677d1-110">EXAMPLES</span></span>

### <span data-ttu-id="677d1-111">Exemplo 1: criar uma configuração de IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="677d1-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="677d1-112">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="677d1-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="677d1-113">O segundo comando obtém a configuração de sub-rede para a sub-rede à qual a rede virtual no comando anterior pertence e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="677d1-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="677d1-114">O terceiro comando cria a configuração de IP usando $Subnet.</span><span class="sxs-lookup"><span data-stu-id="677d1-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="677d1-115">OS</span><span class="sxs-lookup"><span data-stu-id="677d1-115">PARAMETERS</span></span>

### <span data-ttu-id="677d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677d1-116">-DefaultProfile</span></span>
<span data-ttu-id="677d1-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="677d1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="677d1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="677d1-118">-Name</span></span>
<span data-ttu-id="677d1-119">Especifica o nome da configuração de IP a ser criada.</span><span class="sxs-lookup"><span data-stu-id="677d1-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="677d1-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="677d1-120">-Subnet</span></span>
<span data-ttu-id="677d1-121">Especifica o objeto de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="677d1-121">Specifies the subnet object.</span></span>
<span data-ttu-id="677d1-122">Esta é a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="677d1-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="677d1-123">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="677d1-123">-SubnetId</span></span>
<span data-ttu-id="677d1-124">Especifica a identificação de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="677d1-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="677d1-125">Esta é a sub-rede na qual o gateway do aplicativo seria implantado.</span><span class="sxs-lookup"><span data-stu-id="677d1-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="677d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677d1-126">CommonParameters</span></span>
<span data-ttu-id="677d1-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677d1-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="677d1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677d1-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="677d1-129">INPUTS</span></span>

### <span data-ttu-id="677d1-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="677d1-130">None</span></span>

## <span data-ttu-id="677d1-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="677d1-131">OUTPUTS</span></span>

### <span data-ttu-id="677d1-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="677d1-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="677d1-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="677d1-133">NOTES</span></span>

## <span data-ttu-id="677d1-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="677d1-134">RELATED LINKS</span></span>

[<span data-ttu-id="677d1-135">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="677d1-135">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="677d1-136">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="677d1-136">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="677d1-137">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="677d1-137">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="677d1-138">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="677d1-138">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


