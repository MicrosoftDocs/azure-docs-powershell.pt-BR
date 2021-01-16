---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256770"
---
# <span data-ttu-id="442ab-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="442ab-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="442ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="442ab-102">SYNOPSIS</span></span>
<span data-ttu-id="442ab-103">Cria uma configuração de IP para um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="442ab-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="442ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="442ab-104">SYNTAX</span></span>

### <span data-ttu-id="442ab-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="442ab-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="442ab-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="442ab-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="442ab-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="442ab-107">DESCRIPTION</span></span>
<span data-ttu-id="442ab-108">O cmdlet **New-AzVirtualNetworkGatewayIpConfig** cria uma configuração atribuída a um gateway de rede virtual com um endereço IP público (criado anteriormente) com base na ID de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="442ab-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="442ab-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="442ab-109">EXAMPLES</span></span>

### <span data-ttu-id="442ab-110">1: criar uma configuração de IP para um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="442ab-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="442ab-111">Configura um gateway de rede virtual com um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="442ab-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="442ab-112">A variável $myGWsubnet é obtida usando o cmdlet **Get-AzVirtualNetworkSubnetConfig** em "GatewaySubnet" na rede virtual para a qual você pretende criar um gateway virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="442ab-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="442ab-113">A variável $myGWpip é obtida usando o cmdlet **New-AzPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="442ab-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="442ab-114">OS</span><span class="sxs-lookup"><span data-stu-id="442ab-114">PARAMETERS</span></span>

### <span data-ttu-id="442ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442ab-115">-DefaultProfile</span></span>
<span data-ttu-id="442ab-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="442ab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="442ab-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="442ab-117">-Name</span></span>
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

### <span data-ttu-id="442ab-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="442ab-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="442ab-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="442ab-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="442ab-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="442ab-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="442ab-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="442ab-121">-Subnet</span></span>
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

### <span data-ttu-id="442ab-122">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="442ab-122">-SubnetId</span></span>
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

### <span data-ttu-id="442ab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442ab-123">CommonParameters</span></span>
<span data-ttu-id="442ab-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="442ab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442ab-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="442ab-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442ab-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="442ab-126">INPUTS</span></span>

### <span data-ttu-id="442ab-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="442ab-127">None</span></span>

## <span data-ttu-id="442ab-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="442ab-128">OUTPUTS</span></span>

### <span data-ttu-id="442ab-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="442ab-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="442ab-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="442ab-130">NOTES</span></span>

## <span data-ttu-id="442ab-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="442ab-131">RELATED LINKS</span></span>

[<span data-ttu-id="442ab-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="442ab-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="442ab-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="442ab-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
