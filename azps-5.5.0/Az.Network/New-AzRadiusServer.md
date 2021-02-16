---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113471"
---
# <span data-ttu-id="183d7-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="183d7-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="183d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="183d7-102">SYNOPSIS</span></span>
<span data-ttu-id="183d7-103">Cria uma configuração de servidor de raio externo</span><span class="sxs-lookup"><span data-stu-id="183d7-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="183d7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="183d7-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="183d7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="183d7-105">DESCRIPTION</span></span>
<span data-ttu-id="183d7-106">O New-AzRadiusServer cmdlet cria uma configuração de servidor de raio externo a ser usada no gateway de rede virtual e na configuração do servidor VPN.</span><span class="sxs-lookup"><span data-stu-id="183d7-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="183d7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="183d7-107">EXAMPLES</span></span>

### <span data-ttu-id="183d7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="183d7-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="183d7-109">Criar várias configurações de servidor de raio externo a serem usadas para configurar o P2S em um novo gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="183d7-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="183d7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="183d7-110">PARAMETERS</span></span>

### <span data-ttu-id="183d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="183d7-111">-DefaultProfile</span></span>
<span data-ttu-id="183d7-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="183d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="183d7-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="183d7-113">-RadiusServerAddress</span></span>
<span data-ttu-id="183d7-114">Endereço do servidor de raio externo</span><span class="sxs-lookup"><span data-stu-id="183d7-114">External radius server address</span></span>

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

### <span data-ttu-id="183d7-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="183d7-115">-RadiusServerScore</span></span>
<span data-ttu-id="183d7-116">Pontuação do servidor de raio externo</span><span class="sxs-lookup"><span data-stu-id="183d7-116">External radius server score</span></span>

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

### <span data-ttu-id="183d7-117">-RadiusServerSecsec</span><span class="sxs-lookup"><span data-stu-id="183d7-117">-RadiusServerSecret</span></span>
<span data-ttu-id="183d7-118">Segredo do servidor de raio externo</span><span class="sxs-lookup"><span data-stu-id="183d7-118">External radius server secret</span></span>

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

### <span data-ttu-id="183d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="183d7-119">CommonParameters</span></span>
<span data-ttu-id="183d7-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="183d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="183d7-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="183d7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="183d7-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="183d7-122">INPUTS</span></span>

### <span data-ttu-id="183d7-123">System.String</span><span class="sxs-lookup"><span data-stu-id="183d7-123">System.String</span></span>

### <span data-ttu-id="183d7-124">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="183d7-124">System.Security.SecureString</span></span>

### <span data-ttu-id="183d7-125">System.Int32</span><span class="sxs-lookup"><span data-stu-id="183d7-125">System.Int32</span></span>

## <span data-ttu-id="183d7-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="183d7-126">OUTPUTS</span></span>

### <span data-ttu-id="183d7-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="183d7-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="183d7-128">Notas</span><span class="sxs-lookup"><span data-stu-id="183d7-128">NOTES</span></span>

## <span data-ttu-id="183d7-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="183d7-129">RELATED LINKS</span></span>
