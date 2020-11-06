---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 1884dd461c0433c4f6a68bf906f56653ca960e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431933"
---
# <span data-ttu-id="03547-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03547-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="03547-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03547-102">SYNOPSIS</span></span>
<span data-ttu-id="03547-103">Atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="03547-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03547-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03547-104">SYNTAX</span></span>

### <span data-ttu-id="03547-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="03547-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03547-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="03547-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03547-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03547-107">DESCRIPTION</span></span>
<span data-ttu-id="03547-108">O cmdlet **set-AzureRmVirtualNetworkGateway** atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="03547-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="03547-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03547-109">EXAMPLES</span></span>

### <span data-ttu-id="03547-110">Exemplo 1: definir o estado da meta em um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="03547-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="03547-111">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando define o estado da meta do gateway de rede virtual armazenado no $Gateway variável.</span><span class="sxs-lookup"><span data-stu-id="03547-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="03547-112">O comando também define o ASN para o 1337.</span><span class="sxs-lookup"><span data-stu-id="03547-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="03547-113">Exemplo 2: definir o estado da meta em um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="03547-113">Example 2: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="03547-114">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando cria o objeto da política IPSec de VPN de acordo com os parâmetros de IPSec especificados.</span><span class="sxs-lookup"><span data-stu-id="03547-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="03547-115">O terceiro comando define o estado da meta do gateway de rede virtual armazenado em variável $Gateway.</span><span class="sxs-lookup"><span data-stu-id="03547-115">The third command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="03547-116">O comando também define a política IPSec VPN personalizada especificada no objeto $vpnclientipsecpolicy no gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="03547-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="03547-117">OS</span><span class="sxs-lookup"><span data-stu-id="03547-117">PARAMETERS</span></span>

### <span data-ttu-id="03547-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03547-118">-AsJob</span></span>
<span data-ttu-id="03547-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="03547-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03547-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="03547-120">-Asn</span></span>
<span data-ttu-id="03547-121">Especifica o número de sistema autônomo do gateway de rede virtual (ASN) que é usado para configurar sessões do BGP (Border Gateway Protocol) dentro de túneis IPsec.</span><span class="sxs-lookup"><span data-stu-id="03547-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="03547-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03547-122">-DefaultProfile</span></span>
<span data-ttu-id="03547-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03547-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03547-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="03547-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="03547-125">Desabilita o recurso ativo-ativo.</span><span class="sxs-lookup"><span data-stu-id="03547-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="03547-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="03547-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="03547-127">Habilita o recurso ativo-ativo.</span><span class="sxs-lookup"><span data-stu-id="03547-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="03547-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="03547-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="03547-129">Especifica o site padrão a ser usado para o tunelamento forçado.</span><span class="sxs-lookup"><span data-stu-id="03547-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="03547-130">Se um site padrão for especificado, todo o tráfego da Internet da VPN (rede virtual privada) do gateway será roteado para esse site.</span><span class="sxs-lookup"><span data-stu-id="03547-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="03547-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="03547-131">-GatewaySku</span></span>
<span data-ttu-id="03547-132">Especifica a SKU (unidade de manutenção de estoque) do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="03547-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="03547-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="03547-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03547-134">Basic</span><span class="sxs-lookup"><span data-stu-id="03547-134">Basic</span></span>
- <span data-ttu-id="03547-135">Oficial</span><span class="sxs-lookup"><span data-stu-id="03547-135">Standard</span></span>
- <span data-ttu-id="03547-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="03547-136">HighPerformance</span></span>
- <span data-ttu-id="03547-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="03547-137">VpnGw1</span></span>
- <span data-ttu-id="03547-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="03547-138">VpnGw2</span></span>
- <span data-ttu-id="03547-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="03547-139">VpnGw3</span></span>
- <span data-ttu-id="03547-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="03547-140">VpnGw1AZ</span></span>
- <span data-ttu-id="03547-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="03547-141">VpnGw2AZ</span></span>
- <span data-ttu-id="03547-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="03547-142">VpnGw3AZ</span></span>
- <span data-ttu-id="03547-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="03547-143">ErGw1AZ</span></span>
- <span data-ttu-id="03547-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="03547-144">ErGw2AZ</span></span>
- <span data-ttu-id="03547-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="03547-145">ErGw3AZ</span></span>

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

### <span data-ttu-id="03547-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="03547-146">-PeerWeight</span></span>
<span data-ttu-id="03547-147">Especifica a espessura adicionada às rotas aprendidas em BGP deste gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="03547-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="03547-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="03547-148">-RadiusServerAddress</span></span>
<span data-ttu-id="03547-149">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="03547-149">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="03547-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="03547-150">-RadiusServerSecret</span></span>
<span data-ttu-id="03547-151">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="03547-151">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="03547-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03547-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="03547-153">Especifica o objeto de gateway de rede virtual para basear as modificações de.</span><span class="sxs-lookup"><span data-stu-id="03547-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="03547-154">Você pode usar o cmdlet Get-AzureRmVirtualNetworkGateway para obter o objeto do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="03547-154">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="03547-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="03547-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="03547-156">Especifica o espaço de endereço que esse cmdlet usa para atribuir endereços IP do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="03547-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="03547-157">Isso não deve sobrepor a rede virtual ou intervalos locais.</span><span class="sxs-lookup"><span data-stu-id="03547-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03547-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="03547-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="03547-159">Uma lista de diretivas IPSec para protocolos de encapsulamento de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="03547-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03547-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="03547-160">-VpnClientProtocol</span></span>
<span data-ttu-id="03547-161">Uma lista de protocolos de encapsulamento de cliente VPN P2S</span><span class="sxs-lookup"><span data-stu-id="03547-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03547-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="03547-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="03547-163">Especifica uma lista de certificados de cliente VPN revogados.</span><span class="sxs-lookup"><span data-stu-id="03547-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="03547-164">Um cliente VPN apresentando um certificado que corresponda a um deles é removido.</span><span class="sxs-lookup"><span data-stu-id="03547-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03547-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="03547-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="03547-166">Especifica uma lista de certificados raiz de cliente VPN a serem usados para autenticação de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="03547-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="03547-167">A conexão de clientes VPN deve apresentar certificados gerados a partir de um desses certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="03547-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03547-168">-Confirme</span><span class="sxs-lookup"><span data-stu-id="03547-168">-Confirm</span></span>
<span data-ttu-id="03547-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03547-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03547-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03547-170">-WhatIf</span></span>
<span data-ttu-id="03547-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03547-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03547-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03547-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03547-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03547-173">CommonParameters</span></span>
<span data-ttu-id="03547-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03547-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03547-175">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03547-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03547-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03547-176">INPUTS</span></span>

### <span data-ttu-id="03547-177">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03547-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="03547-178">Parâmetros: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="03547-178">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="03547-179">System. String</span><span class="sxs-lookup"><span data-stu-id="03547-179">System.String</span></span>

### <span data-ttu-id="03547-180">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03547-180">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="03547-181">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="03547-181">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="03547-182">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="03547-182">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="03547-183">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="03547-183">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="03547-184">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="03547-184">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="03547-185">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="03547-185">System.UInt32</span></span>

### <span data-ttu-id="03547-186">System. Int32</span><span class="sxs-lookup"><span data-stu-id="03547-186">System.Int32</span></span>

### <span data-ttu-id="03547-187">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="03547-187">System.Security.SecureString</span></span>

## <span data-ttu-id="03547-188">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03547-188">OUTPUTS</span></span>

### <span data-ttu-id="03547-189">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03547-189">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="03547-190">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03547-190">NOTES</span></span>
* <span data-ttu-id="03547-191">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="03547-191">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="03547-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03547-192">RELATED LINKS</span></span>

[<span data-ttu-id="03547-193">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03547-193">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="03547-194">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03547-194">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="03547-195">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03547-195">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="03547-196">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03547-196">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="03547-197">Redimensionar-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03547-197">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


