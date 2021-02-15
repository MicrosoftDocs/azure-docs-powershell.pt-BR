---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117373"
---
# <span data-ttu-id="fb752-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb752-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="fb752-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb752-102">SYNOPSIS</span></span>
<span data-ttu-id="fb752-103">Cria uma Configuração IP para um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="fb752-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="fb752-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb752-104">SYNTAX</span></span>

### <span data-ttu-id="fb752-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb752-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb752-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fb752-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb752-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb752-107">DESCRIPTION</span></span>
<span data-ttu-id="fb752-108">O cmdlet **New-AzVirtualNetworkGatewayIpConfig** cria uma configuração atribuída a um Gateway de Rede Virtual com um Endereço IP Público (criado anteriormente) com base na ID da Sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fb752-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="fb752-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fb752-109">EXAMPLES</span></span>

### <span data-ttu-id="fb752-110">1: Criar uma Configuração IP para um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="fb752-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="fb752-111">Configura um Gateway de Rede Virtual com um Endereço IP Público.</span><span class="sxs-lookup"><span data-stu-id="fb752-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="fb752-112">A variável $myGWsubnet é obtida usando o cmdlet **Get-AzVirtualNetworkSubnetConfig** na "GatewaySubnet" na Rede Virtual que você pretende criar um Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="fb752-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="fb752-113">A variável $myGWpip é obtida usando o cmdlet **New-AzPublicIpAddress.**</span><span class="sxs-lookup"><span data-stu-id="fb752-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="fb752-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb752-114">PARAMETERS</span></span>

### <span data-ttu-id="fb752-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb752-115">-DefaultProfile</span></span>
<span data-ttu-id="fb752-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fb752-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb752-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb752-117">-Name</span></span>
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

### <span data-ttu-id="fb752-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="fb752-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="fb752-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fb752-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="fb752-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="fb752-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="fb752-121">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="fb752-121">-Subnet</span></span>
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

### <span data-ttu-id="fb752-122">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="fb752-122">-SubnetId</span></span>
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

### <span data-ttu-id="fb752-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb752-123">CommonParameters</span></span>
<span data-ttu-id="fb752-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb752-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb752-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb752-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb752-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="fb752-126">INPUTS</span></span>

### <span data-ttu-id="fb752-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fb752-127">None</span></span>

## <span data-ttu-id="fb752-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="fb752-128">OUTPUTS</span></span>

### <span data-ttu-id="fb752-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb752-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="fb752-130">Notas</span><span class="sxs-lookup"><span data-stu-id="fb752-130">NOTES</span></span>

## <span data-ttu-id="fb752-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb752-131">RELATED LINKS</span></span>

[<span data-ttu-id="fb752-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb752-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="fb752-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb752-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
