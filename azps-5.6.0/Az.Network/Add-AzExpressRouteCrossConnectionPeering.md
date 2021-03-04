---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: b16206fdcaf775315947ca9fe71f487d1f9d8df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893141"
---
# <span data-ttu-id="645d8-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="645d8-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="645d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="645d8-102">SYNOPSIS</span></span>
<span data-ttu-id="645d8-103">Adiciona uma configuração de peering a uma conexão cruzada ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="645d8-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="645d8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="645d8-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="645d8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="645d8-105">DESCRIPTION</span></span>
<span data-ttu-id="645d8-106">O cmdlet **Add-AzExpressRouteCrossConnectionPeering** adiciona uma configuração de peering a uma conexão cruzada expressRoute.</span><span class="sxs-lookup"><span data-stu-id="645d8-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="645d8-107">Observe que, depois de executar **Add-AzExpressRouteCrossConnectionPeering,** você deve chamar o cmdlet Set-AzExpressRouteCrossConnection para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="645d8-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering**, you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="645d8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="645d8-108">EXAMPLES</span></span>

### <span data-ttu-id="645d8-109">Exemplo 1: Adicionar um par a uma conexão cruzada ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="645d8-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    CrossConnection = $cc
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCrossConnectionPeering @parameters
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="645d8-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="645d8-110">PARAMETERS</span></span>

### <span data-ttu-id="645d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="645d8-111">-DefaultProfile</span></span>
<span data-ttu-id="645d8-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="645d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="645d8-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="645d8-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="645d8-114">A conexão cruzada ExpressRoute sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="645d8-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="645d8-115">Este é o objeto Azure retornado pelo cmdlet **Get-AzExpressRouteCrossConnection.**</span><span class="sxs-lookup"><span data-stu-id="645d8-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="645d8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="645d8-116">-Force</span></span>
<span data-ttu-id="645d8-117">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="645d8-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="645d8-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="645d8-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="645d8-119">Para um PeeringType do MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que você planeja anunciar durante a sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="645d8-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="645d8-120">Somente prefixos de endereço IP públicos são aceitos.</span><span class="sxs-lookup"><span data-stu-id="645d8-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="645d8-121">Você pode enviar uma lista separada por vírgulas se planeja enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="645d8-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="645d8-122">Esses prefixos devem ser registrados em um Nome de Registro de Roteamento (RIR/RIR).</span><span class="sxs-lookup"><span data-stu-id="645d8-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645d8-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="645d8-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="645d8-124">Se você estiver anunciando prefixos que não estão registrados no número AS de paração, você poderá especificar o número AS ao qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="645d8-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="645d8-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="645d8-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="645d8-126">O Nome do Registro de Roteamento (RIR/RIR) ao qual o número AS e os prefixos estão registrados.</span><span class="sxs-lookup"><span data-stu-id="645d8-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645d8-127">-Name</span><span class="sxs-lookup"><span data-stu-id="645d8-127">-Name</span></span>
<span data-ttu-id="645d8-128">O nome da relação de paração a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="645d8-128">The name of the peering relationship to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645d8-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="645d8-129">-PeerAddressType</span></span>
<span data-ttu-id="645d8-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="645d8-130">PeerAddressType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="645d8-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="645d8-131">-PeerASN</span></span>
<span data-ttu-id="645d8-132">O número AS de sua conexão cruzada ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="645d8-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="645d8-133">Deve ser uma ASN Pública quando PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="645d8-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645d8-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="645d8-134">-PeeringType</span></span>
<span data-ttu-id="645d8-135">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="645d8-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645d8-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="645d8-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="645d8-137">Este é o intervalo de Endereços IP para o caminho de roteamento principal dessa relação de paridade.</span><span class="sxs-lookup"><span data-stu-id="645d8-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="645d8-138">Deve ser uma sub-rede CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="645d8-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="645d8-139">O primeiro endereço numerado ímpar nesta sub-rede deve ser atribuído à interface do roteador.</span><span class="sxs-lookup"><span data-stu-id="645d8-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="645d8-140">O Azure configurará o próximo endereço numerado para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="645d8-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645d8-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="645d8-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="645d8-142">Este é o intervalo de Endereços IP para o caminho de roteamento secundário dessa relação de paridade.</span><span class="sxs-lookup"><span data-stu-id="645d8-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="645d8-143">Deve ser uma sub-rede CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="645d8-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="645d8-144">O primeiro endereço numerado ímpar nesta sub-rede deve ser atribuído à interface do roteador.</span><span class="sxs-lookup"><span data-stu-id="645d8-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="645d8-145">O Azure configurará o próximo endereço numerado para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="645d8-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645d8-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="645d8-146">-SharedKey</span></span>
<span data-ttu-id="645d8-147">Este é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de peering.</span><span class="sxs-lookup"><span data-stu-id="645d8-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645d8-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="645d8-148">-VlanId</span></span>
<span data-ttu-id="645d8-149">Esse é o número de Id da VLAN atribuída a esse paring.</span><span class="sxs-lookup"><span data-stu-id="645d8-149">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645d8-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="645d8-150">-Confirm</span></span>
<span data-ttu-id="645d8-151">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="645d8-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="645d8-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="645d8-152">-WhatIf</span></span>
<span data-ttu-id="645d8-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="645d8-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="645d8-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="645d8-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="645d8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645d8-155">CommonParameters</span></span>
<span data-ttu-id="645d8-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="645d8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645d8-157">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="645d8-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645d8-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="645d8-158">INPUTS</span></span>

### <span data-ttu-id="645d8-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="645d8-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="645d8-160">Parâmetro 'ExpressRouteCrossConnection' aceita o valor do tipo 'PSExpressRouteCrossConnection' do pipeline</span><span class="sxs-lookup"><span data-stu-id="645d8-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="645d8-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="645d8-161">OUTPUTS</span></span>

### <span data-ttu-id="645d8-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="645d8-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="645d8-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="645d8-163">NOTES</span></span>

## <span data-ttu-id="645d8-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="645d8-164">RELATED LINKS</span></span>

[<span data-ttu-id="645d8-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="645d8-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="645d8-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="645d8-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="645d8-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="645d8-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="645d8-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="645d8-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
