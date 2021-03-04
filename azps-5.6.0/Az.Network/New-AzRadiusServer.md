---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: d739741333f0c50da237fc29d96ac2dd02435280
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886162"
---
# <span data-ttu-id="d77c2-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="d77c2-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="d77c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d77c2-102">SYNOPSIS</span></span>
<span data-ttu-id="d77c2-103">Cria uma configuração de servidor de raio externo</span><span class="sxs-lookup"><span data-stu-id="d77c2-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="d77c2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d77c2-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d77c2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d77c2-105">DESCRIPTION</span></span>
<span data-ttu-id="d77c2-106">O New-AzRadiusServer cmdlet cria uma configuração de servidor de raio externo a ser usada no gateway de rede virtual e na configuração do servidor VPN.</span><span class="sxs-lookup"><span data-stu-id="d77c2-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="d77c2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d77c2-107">EXAMPLES</span></span>

### <span data-ttu-id="d77c2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d77c2-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="d77c2-109">Criando várias configurações de servidor de raio externo a serem usadas para configurar o P2S em um novo gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d77c2-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="d77c2-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d77c2-110">PARAMETERS</span></span>

### <span data-ttu-id="d77c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d77c2-111">-DefaultProfile</span></span>
<span data-ttu-id="d77c2-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d77c2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d77c2-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d77c2-113">-RadiusServerAddress</span></span>
<span data-ttu-id="d77c2-114">Endereço do servidor de raio externo</span><span class="sxs-lookup"><span data-stu-id="d77c2-114">External radius server address</span></span>

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

### <span data-ttu-id="d77c2-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="d77c2-115">-RadiusServerScore</span></span>
<span data-ttu-id="d77c2-116">Pontuação do servidor de raio externo</span><span class="sxs-lookup"><span data-stu-id="d77c2-116">External radius server score</span></span>

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

### <span data-ttu-id="d77c2-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d77c2-117">-RadiusServerSecret</span></span>
<span data-ttu-id="d77c2-118">Segredo do servidor de raio externo</span><span class="sxs-lookup"><span data-stu-id="d77c2-118">External radius server secret</span></span>

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

### <span data-ttu-id="d77c2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d77c2-119">CommonParameters</span></span>
<span data-ttu-id="d77c2-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d77c2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d77c2-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d77c2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d77c2-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d77c2-122">INPUTS</span></span>

### <span data-ttu-id="d77c2-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d77c2-123">System.String</span></span>

### <span data-ttu-id="d77c2-124">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="d77c2-124">System.Security.SecureString</span></span>

### <span data-ttu-id="d77c2-125">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d77c2-125">System.Int32</span></span>

## <span data-ttu-id="d77c2-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d77c2-126">OUTPUTS</span></span>

### <span data-ttu-id="d77c2-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="d77c2-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="d77c2-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="d77c2-128">NOTES</span></span>

## <span data-ttu-id="d77c2-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d77c2-129">RELATED LINKS</span></span>
