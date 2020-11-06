---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 6576cedfa49d2ba2215d72b7f31ea85288f5cbda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599962"
---
# <span data-ttu-id="b1f3d-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f3d-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="b1f3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f3d-103">Atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="b1f3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1f3d-104">SYNTAX</span></span>

### <span data-ttu-id="b1f3d-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="b1f3d-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1f3d-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1f3d-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1f3d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1f3d-107">DESCRIPTION</span></span>
<span data-ttu-id="b1f3d-108">O cmdlet **set-AzVirtualNetworkGateway** atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="b1f3d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1f3d-109">EXAMPLES</span></span>

### <span data-ttu-id="b1f3d-110">Exemplo 1: atualizar uma ASN do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="b1f3d-110">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="b1f3d-111">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando atualiza o gateway de rede virtual armazenado no $Gateway variável.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="b1f3d-112">O comando também define o ASN para o 1337.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="b1f3d-113">Exemplo 2: adicionar a política IPsec a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="b1f3d-113">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="b1f3d-114">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando cria o objeto da política IPSec de VPN de acordo com os parâmetros de IPSec especificados.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="b1f3d-115">O terceiro comando atualiza o gateway de rede virtual armazenado em variável $Gateway.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-115">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="b1f3d-116">O comando também define a política IPSec VPN personalizada especificada no objeto $vpnclientipsecpolicy no gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="b1f3d-117">OS</span><span class="sxs-lookup"><span data-stu-id="b1f3d-117">PARAMETERS</span></span>

### <span data-ttu-id="b1f3d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1f3d-118">-AsJob</span></span>
<span data-ttu-id="b1f3d-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b1f3d-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="b1f3d-120">-Asn</span></span>
<span data-ttu-id="b1f3d-121">Especifica o número de sistema autônomo do gateway de rede virtual (ASN) que é usado para configurar sessões do BGP (Border Gateway Protocol) dentro de túneis IPsec.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f3d-122">-DefaultProfile</span></span>
<span data-ttu-id="b1f3d-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1f3d-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="b1f3d-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="b1f3d-125">Desabilita o recurso ativo-ativo.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-125">Disables the active-active feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="b1f3d-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="b1f3d-127">Habilita o recurso ativo-ativo.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-127">Enables the active-active feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b1f3d-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="b1f3d-129">Especifica o site padrão a ser usado para o tunelamento forçado.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="b1f3d-130">Se um site padrão for especificado, todo o tráfego da Internet da VPN (rede virtual privada) do gateway será roteado para esse site.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="b1f3d-131">-GatewaySku</span></span>
<span data-ttu-id="b1f3d-132">Especifica a SKU (unidade de manutenção de estoque) do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="b1f3d-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b1f3d-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b1f3d-134">Basic</span><span class="sxs-lookup"><span data-stu-id="b1f3d-134">Basic</span></span>
- <span data-ttu-id="b1f3d-135">Oficial</span><span class="sxs-lookup"><span data-stu-id="b1f3d-135">Standard</span></span>
- <span data-ttu-id="b1f3d-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="b1f3d-136">HighPerformance</span></span>
- <span data-ttu-id="b1f3d-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="b1f3d-137">VpnGw1</span></span>
- <span data-ttu-id="b1f3d-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="b1f3d-138">VpnGw2</span></span>
- <span data-ttu-id="b1f3d-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="b1f3d-139">VpnGw3</span></span>
- <span data-ttu-id="b1f3d-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="b1f3d-140">VpnGw1AZ</span></span>
- <span data-ttu-id="b1f3d-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="b1f3d-141">VpnGw2AZ</span></span>
- <span data-ttu-id="b1f3d-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="b1f3d-142">VpnGw3AZ</span></span>
- <span data-ttu-id="b1f3d-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="b1f3d-143">ErGw1AZ</span></span>
- <span data-ttu-id="b1f3d-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="b1f3d-144">ErGw2AZ</span></span>
- <span data-ttu-id="b1f3d-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="b1f3d-145">ErGw3AZ</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="b1f3d-146">-PeerWeight</span></span>
<span data-ttu-id="b1f3d-147">Especifica a espessura adicionada às rotas aprendidas em BGP deste gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="b1f3d-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="b1f3d-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="b1f3d-148">-RadiusServerAddress</span></span>
<span data-ttu-id="b1f3d-149">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-149">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="b1f3d-150">-RadiusServerSecret</span></span>
<span data-ttu-id="b1f3d-151">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-151">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f3d-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="b1f3d-153">Especifica o objeto de gateway de rede virtual para basear as modificações de.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="b1f3d-154">Você pode usar o cmdlet Get-AzVirtualNetworkGateway para obter o objeto do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-154">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="b1f3d-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="b1f3d-156">Especifica o espaço de endereço que esse cmdlet usa para atribuir endereços IP do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="b1f3d-157">Isso não deve sobrepor a rede virtual ou intervalos locais.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="b1f3d-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="b1f3d-159">Uma lista de diretivas IPSec para protocolos de encapsulamento de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="b1f3d-160">-VpnClientProtocol</span></span>
<span data-ttu-id="b1f3d-161">Uma lista de protocolos de encapsulamento de cliente VPN P2S</span><span class="sxs-lookup"><span data-stu-id="b1f3d-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="b1f3d-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="b1f3d-163">Especifica uma lista de certificados de cliente VPN revogados.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="b1f3d-164">Um cliente VPN apresentando um certificado que corresponda a um deles é removido.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="b1f3d-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="b1f3d-166">Especifica uma lista de certificados raiz de cliente VPN a serem usados para autenticação de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="b1f3d-167">A conexão de clientes VPN deve apresentar certificados gerados a partir de um desses certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-168">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b1f3d-168">-Confirm</span></span>
<span data-ttu-id="b1f3d-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f3d-170">-WhatIf</span></span>
<span data-ttu-id="b1f3d-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1f3d-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-172">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f3d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f3d-173">CommonParameters</span></span>
<span data-ttu-id="b1f3d-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f3d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f3d-175">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1f3d-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f3d-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1f3d-176">INPUTS</span></span>

### <span data-ttu-id="b1f3d-177">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f3d-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="b1f3d-178">System. String</span><span class="sxs-lookup"><span data-stu-id="b1f3d-178">System.String</span></span>

### <span data-ttu-id="b1f3d-179">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f3d-179">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="b1f3d-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="b1f3d-180">System.String[]</span></span>

### <span data-ttu-id="b1f3d-181">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="b1f3d-181">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="b1f3d-182">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="b1f3d-182">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="b1f3d-183">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="b1f3d-183">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="b1f3d-184">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="b1f3d-184">System.UInt32</span></span>

### <span data-ttu-id="b1f3d-185">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b1f3d-185">System.Int32</span></span>

### <span data-ttu-id="b1f3d-186">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="b1f3d-186">System.Security.SecureString</span></span>

## <span data-ttu-id="b1f3d-187">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1f3d-187">OUTPUTS</span></span>

### <span data-ttu-id="b1f3d-188">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f3d-188">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b1f3d-189">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1f3d-189">NOTES</span></span>
* <span data-ttu-id="b1f3d-190">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="b1f3d-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b1f3d-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1f3d-191">RELATED LINKS</span></span>

[<span data-ttu-id="b1f3d-192">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f3d-192">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b1f3d-193">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f3d-193">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b1f3d-194">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f3d-194">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b1f3d-195">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f3d-195">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b1f3d-196">Redimensionar-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f3d-196">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
