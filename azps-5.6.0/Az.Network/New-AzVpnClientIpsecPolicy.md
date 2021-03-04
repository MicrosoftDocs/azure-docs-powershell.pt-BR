---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 7556a2d23d4c4969c3037d6b49dbd482bcdea207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886900"
---
# <span data-ttu-id="19cca-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="19cca-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="19cca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19cca-102">SYNOPSIS</span></span>
<span data-ttu-id="19cca-103">Este comando permite que os usuários criem o objeto de política ipsec vpn especificando um ou todos os valores, como IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup para definir no gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="19cca-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="19cca-104">Este comando permite que o objeto de saída seja usado para definir a política ipsec vpn para o gateway novo/existente.</span><span class="sxs-lookup"><span data-stu-id="19cca-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="19cca-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="19cca-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19cca-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="19cca-106">DESCRIPTION</span></span>
<span data-ttu-id="19cca-107">Este comando permite que os usuários criem o objeto de política ipsec vpn especificando um ou todos os valores, como IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup para definir no gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="19cca-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="19cca-108">Este comando permite que o objeto de saída seja usado para definir a política ipsec vpn para o gateway novo/existente.</span><span class="sxs-lookup"><span data-stu-id="19cca-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="19cca-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19cca-109">EXAMPLES</span></span>

### <span data-ttu-id="19cca-110">Exemplo 1: Definir o objeto de política ipsec vpn:</span><span class="sxs-lookup"><span data-stu-id="19cca-110">Example 1: Define vpn ipsec policy object:</span></span>
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="19cca-111">Este cmdlet é usado para criar o objeto de política ipsec vpn usando os valores passados de um ou todos os parâmetros que o usuário pode passar para param:VpnClientIpsecPolicy do comando PS permite: New-AzVirtualNetworkGateway (Criação do Novo Gateway VPN) / Set-AzVirtualNetworkGateway (atualização existente do Gateway VPN) em ResourceGroup :</span><span class="sxs-lookup"><span data-stu-id="19cca-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="19cca-112">Exemplo 2: Criar novo gateway de rede virtual com a configuração da política de ipsec personalizada vpn:</span><span class="sxs-lookup"><span data-stu-id="19cca-112">Example 2: Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="19cca-113">Este cmdlet retorna o objeto gateway de rede virtual após a criação.</span><span class="sxs-lookup"><span data-stu-id="19cca-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="19cca-114">Exemplo 3: Definir política ipsec personalizada vpn no gateway de rede virtual existente:</span><span class="sxs-lookup"><span data-stu-id="19cca-114">Example 3: Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="19cca-115">Este cmdlet retorna o objeto gateway de rede virtual após a configuração da política de ipsec personalizada vpn.</span><span class="sxs-lookup"><span data-stu-id="19cca-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="19cca-116">Exemplo 4: Obter gateway de rede virtual para ver se a política personalizada vpn está definida corretamente:</span><span class="sxs-lookup"><span data-stu-id="19cca-116">Example 4: Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="19cca-117">Este cmdlet retorna o objeto gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="19cca-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="19cca-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="19cca-118">PARAMETERS</span></span>

### <span data-ttu-id="19cca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19cca-119">-DefaultProfile</span></span>
<span data-ttu-id="19cca-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19cca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19cca-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="19cca-121">-DhGroup</span></span>
<span data-ttu-id="19cca-122">Os Grupos DH VpnClient usados na Fase 1 do IKE para SA inicial</span><span class="sxs-lookup"><span data-stu-id="19cca-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cca-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="19cca-123">-IkeEncryption</span></span>
<span data-ttu-id="19cca-124">O algoritmo de criptografia IKE VpnClient (Fase 2 do IKE)</span><span class="sxs-lookup"><span data-stu-id="19cca-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cca-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="19cca-125">-IkeIntegrity</span></span>
<span data-ttu-id="19cca-126">O algoritmo de integridade IKE VpnClient (Fase 2 do IKE)</span><span class="sxs-lookup"><span data-stu-id="19cca-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cca-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="19cca-127">-IpsecEncryption</span></span>
<span data-ttu-id="19cca-128">O algoritmo de criptografia IPSec VpnClient (Fase 1 do IKE)</span><span class="sxs-lookup"><span data-stu-id="19cca-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cca-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="19cca-129">-IpsecIntegrity</span></span>
<span data-ttu-id="19cca-130">O algoritmo de integridade IPSec VpnClient (Fase 1 do IKE)</span><span class="sxs-lookup"><span data-stu-id="19cca-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cca-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="19cca-131">-PfsGroup</span></span>
<span data-ttu-id="19cca-132">Os Grupos PFS vpnClient usados na Fase 2 do IKE para o novo SA filho</span><span class="sxs-lookup"><span data-stu-id="19cca-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cca-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="19cca-133">-SADataSize</span></span>
<span data-ttu-id="19cca-134">O tamanho da carga vpnClient IPSec Security Association (também chamado de Modo Rápido ou Fase 2 SA) no KB</span><span class="sxs-lookup"><span data-stu-id="19cca-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cca-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="19cca-135">-SALifeTime</span></span>
<span data-ttu-id="19cca-136">A vida útil da VpnClient IPSec Security Association (também chamada de Modo Rápido ou Fase 2 SA) em segundos</span><span class="sxs-lookup"><span data-stu-id="19cca-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19cca-137">CommonParameters</span></span>
<span data-ttu-id="19cca-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19cca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19cca-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19cca-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19cca-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19cca-140">INPUTS</span></span>

### <span data-ttu-id="19cca-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="19cca-141">None</span></span>

## <span data-ttu-id="19cca-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="19cca-142">OUTPUTS</span></span>

### <span data-ttu-id="19cca-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="19cca-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="19cca-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="19cca-144">NOTES</span></span>

## <span data-ttu-id="19cca-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19cca-145">RELATED LINKS</span></span>
