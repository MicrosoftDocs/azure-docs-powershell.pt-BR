---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 41c94d0dd8401399f360af89f1744cc10e900e1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430718"
---
# <span data-ttu-id="6abef-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6abef-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="6abef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6abef-102">SYNOPSIS</span></span>
<span data-ttu-id="6abef-103">Atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6abef-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6abef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6abef-104">SYNTAX</span></span>

### <span data-ttu-id="6abef-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="6abef-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6abef-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6abef-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6abef-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6abef-107">DESCRIPTION</span></span>
<span data-ttu-id="6abef-108">O cmdlet **set-AzureRmVirtualNetworkGateway** atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6abef-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="6abef-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6abef-109">EXAMPLES</span></span>

### <span data-ttu-id="6abef-110">Exemplo 1: definir o estado da meta em um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="6abef-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="6abef-111">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway</span><span class="sxs-lookup"><span data-stu-id="6abef-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="6abef-112">O segundo comando define o estado da meta do gateway de rede virtual armazenado em variável $Gateway.</span><span class="sxs-lookup"><span data-stu-id="6abef-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="6abef-113">O comando também define o ASN para o 1337.</span><span class="sxs-lookup"><span data-stu-id="6abef-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="6abef-114">OS</span><span class="sxs-lookup"><span data-stu-id="6abef-114">PARAMETERS</span></span>

### <span data-ttu-id="6abef-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="6abef-115">-Asn</span></span>
<span data-ttu-id="6abef-116">Especifica o número de sistema autônomo do gateway de rede virtual (ASN) que é usado para configurar sessões do BGP (Border Gateway Protocol) dentro de túneis IPsec.</span><span class="sxs-lookup"><span data-stu-id="6abef-116">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="6abef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6abef-117">-DefaultProfile</span></span>
<span data-ttu-id="6abef-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6abef-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="6abef-119">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="6abef-119">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="6abef-120">Desabilita o recurso ativo-ativo.</span><span class="sxs-lookup"><span data-stu-id="6abef-120">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="6abef-121">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="6abef-121">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="6abef-122">Habilita o recurso ativo-ativo.</span><span class="sxs-lookup"><span data-stu-id="6abef-122">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="6abef-123">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="6abef-123">-GatewayDefaultSite</span></span>
<span data-ttu-id="6abef-124">Especifica o site padrão a ser usado para o tunelamento forçado.</span><span class="sxs-lookup"><span data-stu-id="6abef-124">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="6abef-125">Se um site padrão for especificado, todo o tráfego da Internet da VPN (rede virtual privada) do gateway será roteado para esse site.</span><span class="sxs-lookup"><span data-stu-id="6abef-125">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="6abef-126">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="6abef-126">-GatewaySku</span></span>
<span data-ttu-id="6abef-127">Especifica a SKU (unidade de manutenção de estoque) do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6abef-127">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="6abef-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6abef-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6abef-129">Basic</span><span class="sxs-lookup"><span data-stu-id="6abef-129">Basic</span></span>
- <span data-ttu-id="6abef-130">Oficial</span><span class="sxs-lookup"><span data-stu-id="6abef-130">Standard</span></span>
- <span data-ttu-id="6abef-131">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="6abef-131">HighPerformance</span></span>
- <span data-ttu-id="6abef-132">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="6abef-132">VpnGw1</span></span>
- <span data-ttu-id="6abef-133">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="6abef-133">VpnGw2</span></span>
- <span data-ttu-id="6abef-134">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="6abef-134">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6abef-135">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="6abef-135">-PeerWeight</span></span>
<span data-ttu-id="6abef-136">Especifica a espessura adicionada às rotas aprendidas em BGP deste gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="6abef-136">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="6abef-137">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="6abef-137">-RadiusServerAddress</span></span>
<span data-ttu-id="6abef-138">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="6abef-138">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="6abef-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="6abef-139">-RadiusServerSecret</span></span>
<span data-ttu-id="6abef-140">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="6abef-140">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="6abef-141">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6abef-141">-VirtualNetworkGateway</span></span>
<span data-ttu-id="6abef-142">Especifica o objeto de gateway de rede virtual para basear as modificações de.</span><span class="sxs-lookup"><span data-stu-id="6abef-142">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="6abef-143">Você pode usar o cmdlet Get-AzureRmVirtualNetworkGateway para obter o objeto do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6abef-143">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="6abef-144">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="6abef-144">-VpnClientAddressPool</span></span>
<span data-ttu-id="6abef-145">Especifica o espaço de endereço que esse cmdlet usa para atribuir endereços IP do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="6abef-145">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="6abef-146">Isso não deve sobrepor a rede virtual ou intervalos locais.</span><span class="sxs-lookup"><span data-stu-id="6abef-146">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="6abef-147">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="6abef-147">-VpnClientProtocol</span></span>
<span data-ttu-id="6abef-148">Uma lista de protocolos de encapsulamento de cliente VPN P2S</span><span class="sxs-lookup"><span data-stu-id="6abef-148">A list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="6abef-149">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="6abef-149">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="6abef-150">Especifica uma lista de certificados de cliente VPN revogados.</span><span class="sxs-lookup"><span data-stu-id="6abef-150">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="6abef-151">Um cliente VPN apresentando um certificado que corresponda a um deles é removido.</span><span class="sxs-lookup"><span data-stu-id="6abef-151">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="6abef-152">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="6abef-152">-VpnClientRootCertificates</span></span>
<span data-ttu-id="6abef-153">Especifica uma lista de certificados raiz de cliente VPN a serem usados para autenticação de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="6abef-153">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="6abef-154">A conexão de clientes VPN deve apresentar certificados gerados a partir de um desses certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="6abef-154">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="6abef-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6abef-155">-Confirm</span></span>
<span data-ttu-id="6abef-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6abef-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6abef-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6abef-157">-WhatIf</span></span>
<span data-ttu-id="6abef-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6abef-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6abef-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6abef-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6abef-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6abef-160">CommonParameters</span></span>
<span data-ttu-id="6abef-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6abef-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6abef-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6abef-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6abef-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6abef-163">INPUTS</span></span>

### <span data-ttu-id="6abef-164">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6abef-164">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="6abef-165">O parâmetro ' VirtualNetworkGateway ' aceita o valor do tipo ' PSVirtualNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6abef-165">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="6abef-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6abef-166">OUTPUTS</span></span>

### <span data-ttu-id="6abef-167">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6abef-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="6abef-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6abef-168">NOTES</span></span>
* <span data-ttu-id="6abef-169">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="6abef-169">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6abef-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6abef-170">RELATED LINKS</span></span>

[<span data-ttu-id="6abef-171">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6abef-171">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="6abef-172">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6abef-172">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="6abef-173">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6abef-173">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="6abef-174">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6abef-174">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="6abef-175">Redimensionar-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6abef-175">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


