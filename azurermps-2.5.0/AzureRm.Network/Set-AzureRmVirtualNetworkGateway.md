---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 622fb5278f7e0a78fb6163954829b1a2aaa6bba7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785146"
---
# <span data-ttu-id="5b11a-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5b11a-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="5b11a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b11a-102">SYNOPSIS</span></span>
<span data-ttu-id="5b11a-103">Atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5b11a-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b11a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b11a-104">SYNTAX</span></span>

### <span data-ttu-id="5b11a-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="5b11a-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b11a-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b11a-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b11a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b11a-107">DESCRIPTION</span></span>
<span data-ttu-id="5b11a-108">O cmdlet **set-AzureRmVirtualNetworkGateway** atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5b11a-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="5b11a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b11a-109">EXAMPLES</span></span>

### <span data-ttu-id="5b11a-110">Exemplo 1: definir o estado da meta em um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="5b11a-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="5b11a-111">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway</span><span class="sxs-lookup"><span data-stu-id="5b11a-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="5b11a-112">O segundo comando define o estado da meta do gateway de rede virtual armazenado em variável $Gateway.</span><span class="sxs-lookup"><span data-stu-id="5b11a-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="5b11a-113">O comando também define o ASN para o 1337.</span><span class="sxs-lookup"><span data-stu-id="5b11a-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="5b11a-114">OS</span><span class="sxs-lookup"><span data-stu-id="5b11a-114">PARAMETERS</span></span>

### <span data-ttu-id="5b11a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b11a-115">-AsJob</span></span>
<span data-ttu-id="5b11a-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5b11a-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="5b11a-117">-Asn</span></span>
<span data-ttu-id="5b11a-118">Especifica o número de sistema autônomo do gateway de rede virtual (ASN) que é usado para configurar sessões do BGP (Border Gateway Protocol) dentro de túneis IPsec.</span><span class="sxs-lookup"><span data-stu-id="5b11a-118">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b11a-119">-DefaultProfile</span></span>
<span data-ttu-id="5b11a-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b11a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="5b11a-121">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="5b11a-121">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="5b11a-122">Desabilita o recurso ativo-ativo.</span><span class="sxs-lookup"><span data-stu-id="5b11a-122">Disables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-123">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="5b11a-123">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="5b11a-124">Habilita o recurso ativo-ativo.</span><span class="sxs-lookup"><span data-stu-id="5b11a-124">Enables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-125">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5b11a-125">-GatewayDefaultSite</span></span>
<span data-ttu-id="5b11a-126">Especifica o site padrão a ser usado para o tunelamento forçado.</span><span class="sxs-lookup"><span data-stu-id="5b11a-126">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="5b11a-127">Se um site padrão for especificado, todo o tráfego da Internet da VPN (rede virtual privada) do gateway será roteado para esse site.</span><span class="sxs-lookup"><span data-stu-id="5b11a-127">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-128">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="5b11a-128">-GatewaySku</span></span>
<span data-ttu-id="5b11a-129">Especifica a SKU (unidade de manutenção de estoque) do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5b11a-129">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="5b11a-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5b11a-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5b11a-131">Basic</span><span class="sxs-lookup"><span data-stu-id="5b11a-131">Basic</span></span>
- <span data-ttu-id="5b11a-132">Oficial</span><span class="sxs-lookup"><span data-stu-id="5b11a-132">Standard</span></span>
- <span data-ttu-id="5b11a-133">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="5b11a-133">HighPerformance</span></span>
- <span data-ttu-id="5b11a-134">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="5b11a-134">VpnGw1</span></span>
- <span data-ttu-id="5b11a-135">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="5b11a-135">VpnGw2</span></span>
- <span data-ttu-id="5b11a-136">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="5b11a-136">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="5b11a-137">-PeerWeight</span></span>
<span data-ttu-id="5b11a-138">Especifica a espessura adicionada às rotas aprendidas em BGP deste gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="5b11a-138">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-139">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="5b11a-139">-RadiusServerAddress</span></span>
<span data-ttu-id="5b11a-140">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="5b11a-140">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-141">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="5b11a-141">-RadiusServerSecret</span></span>
<span data-ttu-id="5b11a-142">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="5b11a-142">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-143">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5b11a-143">-VirtualNetworkGateway</span></span>
<span data-ttu-id="5b11a-144">Especifica o objeto de gateway de rede virtual para basear as modificações de.</span><span class="sxs-lookup"><span data-stu-id="5b11a-144">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="5b11a-145">Você pode usar o cmdlet Get-AzureRmVirtualNetworkGateway para obter o objeto do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5b11a-145">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="5b11a-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="5b11a-147">Especifica o espaço de endereço que esse cmdlet usa para atribuir endereços IP do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="5b11a-147">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="5b11a-148">Isso não deve sobrepor a rede virtual ou intervalos locais.</span><span class="sxs-lookup"><span data-stu-id="5b11a-148">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="5b11a-149">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="5b11a-149">-VpnClientProtocol</span></span>
<span data-ttu-id="5b11a-150">Uma lista de protocolos de encapsulamento de cliente VPN P2S</span><span class="sxs-lookup"><span data-stu-id="5b11a-150">A list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-151">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="5b11a-151">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="5b11a-152">Especifica uma lista de certificados de cliente VPN revogados.</span><span class="sxs-lookup"><span data-stu-id="5b11a-152">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="5b11a-153">Um cliente VPN apresentando um certificado que corresponda a um deles é removido.</span><span class="sxs-lookup"><span data-stu-id="5b11a-153">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="5b11a-154">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="5b11a-154">-VpnClientRootCertificates</span></span>
<span data-ttu-id="5b11a-155">Especifica uma lista de certificados raiz de cliente VPN a serem usados para autenticação de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="5b11a-155">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="5b11a-156">A conexão de clientes VPN deve apresentar certificados gerados a partir de um desses certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="5b11a-156">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="5b11a-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5b11a-157">-Confirm</span></span>
<span data-ttu-id="5b11a-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b11a-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b11a-159">-WhatIf</span></span>
<span data-ttu-id="5b11a-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5b11a-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b11a-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b11a-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b11a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b11a-162">CommonParameters</span></span>
<span data-ttu-id="5b11a-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b11a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b11a-164">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b11a-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b11a-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b11a-165">INPUTS</span></span>

### <span data-ttu-id="5b11a-166">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5b11a-166">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="5b11a-167">O parâmetro ' VirtualNetworkGateway ' aceita o valor do tipo ' PSVirtualNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="5b11a-167">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="5b11a-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b11a-168">OUTPUTS</span></span>

### <span data-ttu-id="5b11a-169">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5b11a-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="5b11a-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b11a-170">NOTES</span></span>
* <span data-ttu-id="5b11a-171">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="5b11a-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5b11a-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b11a-172">RELATED LINKS</span></span>

[<span data-ttu-id="5b11a-173">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5b11a-173">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="5b11a-174">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5b11a-174">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="5b11a-175">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5b11a-175">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="5b11a-176">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5b11a-176">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="5b11a-177">Redimensionar-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5b11a-177">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


