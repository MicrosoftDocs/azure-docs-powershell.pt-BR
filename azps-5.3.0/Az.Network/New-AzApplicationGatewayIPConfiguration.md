---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271783"
---
# <span data-ttu-id="b2302-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2302-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b2302-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2302-102">SYNOPSIS</span></span>
<span data-ttu-id="b2302-103">Cria uma configuração de IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b2302-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="b2302-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2302-104">SYNTAX</span></span>

### <span data-ttu-id="b2302-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2302-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2302-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b2302-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2302-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2302-107">DESCRIPTION</span></span>
<span data-ttu-id="b2302-108">O cmdlet **New-AzApplicationGatewayIPConfiguration** cria uma configuração de IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b2302-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="b2302-109">A configuração de IP contém a sub-rede na qual o gateway do aplicativo é implantado.</span><span class="sxs-lookup"><span data-stu-id="b2302-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="b2302-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2302-110">EXAMPLES</span></span>

### <span data-ttu-id="b2302-111">Exemplo 1: criar uma configuração de IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b2302-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="b2302-112">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b2302-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="b2302-113">O segundo comando obtém a configuração de sub-rede para a sub-rede à qual a rede virtual no comando anterior pertence e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="b2302-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="b2302-114">O terceiro comando cria a configuração de IP usando $Subnet.</span><span class="sxs-lookup"><span data-stu-id="b2302-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="b2302-115">OS</span><span class="sxs-lookup"><span data-stu-id="b2302-115">PARAMETERS</span></span>

### <span data-ttu-id="b2302-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2302-116">-DefaultProfile</span></span>
<span data-ttu-id="b2302-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2302-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2302-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2302-118">-Name</span></span>
<span data-ttu-id="b2302-119">Especifica o nome da configuração de IP a ser criada.</span><span class="sxs-lookup"><span data-stu-id="b2302-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="b2302-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b2302-120">-Subnet</span></span>
<span data-ttu-id="b2302-121">Especifica o objeto de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b2302-121">Specifies the subnet object.</span></span>
<span data-ttu-id="b2302-122">Esta é a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="b2302-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="b2302-123">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="b2302-123">-SubnetId</span></span>
<span data-ttu-id="b2302-124">Especifica a identificação de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b2302-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="b2302-125">Esta é a sub-rede na qual o gateway do aplicativo seria implantado.</span><span class="sxs-lookup"><span data-stu-id="b2302-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="b2302-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2302-126">CommonParameters</span></span>
<span data-ttu-id="b2302-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2302-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2302-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2302-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2302-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2302-129">INPUTS</span></span>

### <span data-ttu-id="b2302-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b2302-130">None</span></span>

## <span data-ttu-id="b2302-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2302-131">OUTPUTS</span></span>

### <span data-ttu-id="b2302-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2302-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b2302-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2302-133">NOTES</span></span>

## <span data-ttu-id="b2302-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2302-134">RELATED LINKS</span></span>

[<span data-ttu-id="b2302-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2302-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b2302-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2302-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b2302-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2302-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b2302-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2302-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


