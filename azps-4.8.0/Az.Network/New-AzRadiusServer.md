---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955401"
---
# <span data-ttu-id="53eed-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="53eed-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="53eed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53eed-102">SYNOPSIS</span></span>
<span data-ttu-id="53eed-103">Cria uma configuração de servidor RADIUS externo</span><span class="sxs-lookup"><span data-stu-id="53eed-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="53eed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53eed-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53eed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53eed-105">DESCRIPTION</span></span>
<span data-ttu-id="53eed-106">O cmdlet New-AzRadiusServer cria uma configuração de servidor RADIUS externo para ser usada no gateway de rede virtual e na configuração do servidor VPN.</span><span class="sxs-lookup"><span data-stu-id="53eed-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="53eed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53eed-107">EXAMPLES</span></span>

### <span data-ttu-id="53eed-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="53eed-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="53eed-109">Criar várias configurações de servidor RADIUS externo a serem usadas para configurar o P2S em um novo gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="53eed-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="53eed-110">OS</span><span class="sxs-lookup"><span data-stu-id="53eed-110">PARAMETERS</span></span>

### <span data-ttu-id="53eed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53eed-111">-DefaultProfile</span></span>
<span data-ttu-id="53eed-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53eed-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53eed-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="53eed-113">-RadiusServerAddress</span></span>
<span data-ttu-id="53eed-114">Endereço do servidor RADIUS externo</span><span class="sxs-lookup"><span data-stu-id="53eed-114">External radius server address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eed-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="53eed-115">-RadiusServerScore</span></span>
<span data-ttu-id="53eed-116">Pontuação do servidor RADIUS externo</span><span class="sxs-lookup"><span data-stu-id="53eed-116">External radius server score</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eed-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="53eed-117">-RadiusServerSecret</span></span>
<span data-ttu-id="53eed-118">Segredo do servidor RADIUS externo</span><span class="sxs-lookup"><span data-stu-id="53eed-118">External radius server secret</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53eed-119">CommonParameters</span></span>
<span data-ttu-id="53eed-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53eed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53eed-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53eed-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53eed-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53eed-122">INPUTS</span></span>

### <span data-ttu-id="53eed-123">System. String</span><span class="sxs-lookup"><span data-stu-id="53eed-123">System.String</span></span>

### <span data-ttu-id="53eed-124">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="53eed-124">System.Security.SecureString</span></span>

### <span data-ttu-id="53eed-125">System. Int32</span><span class="sxs-lookup"><span data-stu-id="53eed-125">System.Int32</span></span>

## <span data-ttu-id="53eed-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53eed-126">OUTPUTS</span></span>

### <span data-ttu-id="53eed-127">Microsoft. Azure. Commands. Network. Models. PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="53eed-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="53eed-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53eed-128">NOTES</span></span>

## <span data-ttu-id="53eed-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53eed-129">RELATED LINKS</span></span>
