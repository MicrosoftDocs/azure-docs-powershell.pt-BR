---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943230"
---
# <span data-ttu-id="083f9-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="083f9-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="083f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="083f9-102">SYNOPSIS</span></span>
<span data-ttu-id="083f9-103">Cria uma configuração de IP para um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="083f9-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="083f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="083f9-104">SYNTAX</span></span>

### <span data-ttu-id="083f9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="083f9-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="083f9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="083f9-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="083f9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="083f9-107">DESCRIPTION</span></span>
<span data-ttu-id="083f9-108">O cmdlet **New-AzVirtualNetworkGatewayIpConfig** cria uma configuração atribuída a um gateway de rede virtual com um endereço IP público (criado anteriormente) com base na ID de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="083f9-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="083f9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="083f9-109">EXAMPLES</span></span>

### <span data-ttu-id="083f9-110">1: criar uma configuração de IP para um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="083f9-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="083f9-111">Configura um gateway de rede virtual com um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="083f9-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="083f9-112">A variável $myGWsubnet é obtida usando o cmdlet **Get-AzVirtualNetworkSubnetConfig** em "GatewaySubnet" na rede virtual para a qual você pretende criar um gateway virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="083f9-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="083f9-113">A variável $myGWpip é obtida usando o cmdlet **New-AzPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="083f9-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="083f9-114">OS</span><span class="sxs-lookup"><span data-stu-id="083f9-114">PARAMETERS</span></span>

### <span data-ttu-id="083f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083f9-115">-DefaultProfile</span></span>
<span data-ttu-id="083f9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="083f9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="083f9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="083f9-117">-Name</span></span>
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

### <span data-ttu-id="083f9-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="083f9-118">-PrivateIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083f9-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="083f9-119">-PublicIpAddress</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083f9-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="083f9-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="083f9-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="083f9-121">-Subnet</span></span>
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

### <span data-ttu-id="083f9-122">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="083f9-122">-SubnetId</span></span>
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

### <span data-ttu-id="083f9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083f9-123">CommonParameters</span></span>
<span data-ttu-id="083f9-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083f9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083f9-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083f9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083f9-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="083f9-126">INPUTS</span></span>

### <span data-ttu-id="083f9-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="083f9-127">None</span></span>

## <span data-ttu-id="083f9-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="083f9-128">OUTPUTS</span></span>

### <span data-ttu-id="083f9-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="083f9-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="083f9-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="083f9-130">NOTES</span></span>

## <span data-ttu-id="083f9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="083f9-131">RELATED LINKS</span></span>

[<span data-ttu-id="083f9-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="083f9-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="083f9-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="083f9-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
