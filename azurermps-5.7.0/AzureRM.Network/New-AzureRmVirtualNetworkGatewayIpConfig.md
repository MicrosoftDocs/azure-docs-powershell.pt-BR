---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: eba8cd39c621cd2e7b959e54cf20a26ec3434af0
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93611149"
---
# <span data-ttu-id="3b909-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3b909-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="3b909-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b909-102">SYNOPSIS</span></span>
<span data-ttu-id="3b909-103">Cria uma configuração de IP para um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="3b909-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b909-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b909-104">SYNTAX</span></span>

### <span data-ttu-id="3b909-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b909-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b909-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3b909-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b909-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b909-107">DESCRIPTION</span></span>
<span data-ttu-id="3b909-108">O cmdlet **New-AzureRmVirtualNetworkGatewayIpConfig** cria uma configuração atribuída a um gateway de rede virtual com um endereço IP público (criado anteriormente) com base na ID de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="3b909-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="3b909-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b909-109">EXAMPLES</span></span>

### <span data-ttu-id="3b909-110">1: criar uma configuração de IP para um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="3b909-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="3b909-111">Configura um gateway de rede virtual com um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="3b909-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="3b909-112">A variável $myGWsubnet é obtida usando o cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** em "GatewaySubnet" na rede virtual para a qual você pretende criar um gateway virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="3b909-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="3b909-113">A variável $myGWpip é obtida usando o cmdlet **New-AzureRmPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="3b909-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="3b909-114">OS</span><span class="sxs-lookup"><span data-stu-id="3b909-114">PARAMETERS</span></span>

### <span data-ttu-id="3b909-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b909-115">-DefaultProfile</span></span>
<span data-ttu-id="3b909-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b909-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b909-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b909-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b909-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3b909-118">-PrivateIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b909-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3b909-119">-PublicIpAddress</span></span>
```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b909-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3b909-120">-PublicIpAddressId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b909-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="3b909-121">-Subnet</span></span>
```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b909-122">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="3b909-122">-SubnetId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b909-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b909-123">CommonParameters</span></span>
<span data-ttu-id="3b909-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b909-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b909-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b909-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b909-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b909-126">INPUTS</span></span>

### <span data-ttu-id="3b909-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3b909-127">None</span></span>
<span data-ttu-id="3b909-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3b909-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b909-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b909-129">OUTPUTS</span></span>

### <span data-ttu-id="3b909-130">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b909-130">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="3b909-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b909-131">NOTES</span></span>

## <span data-ttu-id="3b909-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b909-132">RELATED LINKS</span></span>

