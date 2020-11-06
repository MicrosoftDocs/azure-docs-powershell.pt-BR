---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: a97379fb3cf59658c3f0822fc08fa65c0614021d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600245"
---
# <span data-ttu-id="3c7cb-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="3c7cb-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="3c7cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7cb-103">Esse comando permite que os usuários criem o objeto da política IPSec VPN especificando um ou todos os valores, como IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup para definir no gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="3c7cb-104">Esse comando permite que o objeto output seja usado para definir a política IPSec de VPN para o gateway novo/sistema.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-104">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="3c7cb-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c7cb-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c7cb-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c7cb-106">DESCRIPTION</span></span>
<span data-ttu-id="3c7cb-107">Esse comando permite que os usuários criem o objeto da política IPSec VPN especificando um ou todos os valores, como IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup para definir no gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="3c7cb-108">Esse comando permite que o objeto output seja usado para definir a política IPSec de VPN para o gateway novo/sistema.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-108">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="3c7cb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c7cb-109">EXAMPLES</span></span>

### <span data-ttu-id="3c7cb-110">Defina o objeto da política IPSec da VPN:</span><span class="sxs-lookup"><span data-stu-id="3c7cb-110">Define vpn ipsec policy object:</span></span>
```
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="3c7cb-111">Esse cmdlet é usado para criar o objeto da política IPSec de VPN usando os valores passados um ou todos os parâmetros que o usuário pode transmitir para o parâmetro: VpnClientIpsecPolicy do comando PS Let: New-AzVirtualNetworkGateway (nova criação do gateway VPN)/Set-AzVirtualNetworkGateway (atualização do gateway VPN existente) no objeto Resource:</span><span class="sxs-lookup"><span data-stu-id="3c7cb-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="3c7cb-112">Criar novo gateway de rede virtual com a configuração de política IPSec personalizada VPN:</span><span class="sxs-lookup"><span data-stu-id="3c7cb-112">Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="3c7cb-113">Esse cmdlet retorna o objeto do gateway de rede virtual após a criação.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="3c7cb-114">Definir a política IPSec personalizada de VPN no gateway de rede virtual existente:</span><span class="sxs-lookup"><span data-stu-id="3c7cb-114">Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="3c7cb-115">Esse cmdlet retorna o objeto do gateway de rede virtual após a configuração da política IPSec personalizada de VPN.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="3c7cb-116">Obtenha o gateway de rede virtual para ver se a política personalizada de VPN está definida corretamente:</span><span class="sxs-lookup"><span data-stu-id="3c7cb-116">Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="3c7cb-117">Esse cmdlet retorna o objeto do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="3c7cb-118">OS</span><span class="sxs-lookup"><span data-stu-id="3c7cb-118">PARAMETERS</span></span>

### <span data-ttu-id="3c7cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7cb-119">-DefaultProfile</span></span>
<span data-ttu-id="3c7cb-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c7cb-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="3c7cb-121">-DhGroup</span></span>
<span data-ttu-id="3c7cb-122">Os grupos DH do vpnclient usados na fase 1 do IKE para SA inicial</span><span class="sxs-lookup"><span data-stu-id="3c7cb-122">The Vpnclient DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="3c7cb-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="3c7cb-123">-IkeEncryption</span></span>
<span data-ttu-id="3c7cb-124">O algoritmo de criptografia IKE do vpnclient (fase 2 da IKE)</span><span class="sxs-lookup"><span data-stu-id="3c7cb-124">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="3c7cb-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="3c7cb-125">-IkeIntegrity</span></span>
<span data-ttu-id="3c7cb-126">O algoritmo de integridade IKE do vpnclient (fase 2 da IKE)</span><span class="sxs-lookup"><span data-stu-id="3c7cb-126">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="3c7cb-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="3c7cb-127">-IpsecEncryption</span></span>
<span data-ttu-id="3c7cb-128">O algoritmo de criptografia IPSec do vpnclient (fase 1 da IKE)</span><span class="sxs-lookup"><span data-stu-id="3c7cb-128">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="3c7cb-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="3c7cb-129">-IpsecIntegrity</span></span>
<span data-ttu-id="3c7cb-130">O algoritmo de integridade IPSec do vpnclient (fase 1 da IKE)</span><span class="sxs-lookup"><span data-stu-id="3c7cb-130">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="3c7cb-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="3c7cb-131">-PfsGroup</span></span>
<span data-ttu-id="3c7cb-132">Os grupos de PFS do vpnclient usados na fase 2 do IKE para novas associações de SA filho</span><span class="sxs-lookup"><span data-stu-id="3c7cb-132">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="3c7cb-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="3c7cb-133">-SADataSize</span></span>
<span data-ttu-id="3c7cb-134">O tamanho da carga de segurança IPSec do vpnclient (também chamado de modo rápido ou da fase 2 do SA) em KB</span><span class="sxs-lookup"><span data-stu-id="3c7cb-134">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="3c7cb-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="3c7cb-135">-SALifeTime</span></span>
<span data-ttu-id="3c7cb-136">O tempo de vida da Associação de segurança IPSec do vpnclient (também chamado de modo rápido ou da fase 2 SA) em segundos</span><span class="sxs-lookup"><span data-stu-id="3c7cb-136">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="3c7cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7cb-137">CommonParameters</span></span>
<span data-ttu-id="3c7cb-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c7cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7cb-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c7cb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7cb-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c7cb-140">INPUTS</span></span>

### <span data-ttu-id="3c7cb-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3c7cb-141">None</span></span>

## <span data-ttu-id="3c7cb-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c7cb-142">OUTPUTS</span></span>

### <span data-ttu-id="3c7cb-143">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="3c7cb-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="3c7cb-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c7cb-144">NOTES</span></span>

## <span data-ttu-id="3c7cb-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c7cb-145">RELATED LINKS</span></span>
