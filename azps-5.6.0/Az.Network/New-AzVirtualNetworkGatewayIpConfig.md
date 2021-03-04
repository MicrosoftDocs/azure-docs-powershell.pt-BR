---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: cfbfd8df28cf4f0d9c11e654694172b86a549141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886903"
---
# <span data-ttu-id="b235e-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b235e-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="b235e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b235e-102">SYNOPSIS</span></span>
<span data-ttu-id="b235e-103">Cria uma configuração IP para um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="b235e-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="b235e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b235e-104">SYNTAX</span></span>

### <span data-ttu-id="b235e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b235e-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b235e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b235e-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b235e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b235e-107">DESCRIPTION</span></span>
<span data-ttu-id="b235e-108">O cmdlet **New-AzVirtualNetworkGatewayIpConfig** cria uma configuração atribuída a um Gateway de Rede Virtual com um Endereço IP Público (criado anteriormente) com base na ID da Sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b235e-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="b235e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b235e-109">EXAMPLES</span></span>

### <span data-ttu-id="b235e-110">1: Criar uma Configuração IP para um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="b235e-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="b235e-111">Configura um Gateway de Rede Virtual com um Endereço IP Público.</span><span class="sxs-lookup"><span data-stu-id="b235e-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="b235e-112">A variável $myGWsubnet é obtida usando o cmdlet **Get-AzVirtualNetworkSubnetConfig** no "GatewaySubnet" na Rede Virtual que você pretende criar um Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="b235e-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="b235e-113">A variável $myGWpip é obtida usando o cmdlet **New-AzPublicIpAddress.**</span><span class="sxs-lookup"><span data-stu-id="b235e-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="b235e-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b235e-114">PARAMETERS</span></span>

### <span data-ttu-id="b235e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b235e-115">-DefaultProfile</span></span>
<span data-ttu-id="b235e-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b235e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b235e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b235e-117">-Name</span></span>
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

### <span data-ttu-id="b235e-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b235e-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="b235e-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b235e-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="b235e-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b235e-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="b235e-121">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="b235e-121">-Subnet</span></span>
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

### <span data-ttu-id="b235e-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b235e-122">-SubnetId</span></span>
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

### <span data-ttu-id="b235e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b235e-123">CommonParameters</span></span>
<span data-ttu-id="b235e-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b235e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b235e-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b235e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b235e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b235e-126">INPUTS</span></span>

### <span data-ttu-id="b235e-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b235e-127">None</span></span>

## <span data-ttu-id="b235e-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b235e-128">OUTPUTS</span></span>

### <span data-ttu-id="b235e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b235e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="b235e-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="b235e-130">NOTES</span></span>

## <span data-ttu-id="b235e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b235e-131">RELATED LINKS</span></span>

[<span data-ttu-id="b235e-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b235e-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="b235e-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b235e-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
