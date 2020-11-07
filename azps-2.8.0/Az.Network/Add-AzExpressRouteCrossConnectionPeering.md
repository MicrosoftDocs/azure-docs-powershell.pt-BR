---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: dac01839a5a646e8fe75f4b47cda2650ac5ad280
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772105"
---
# <span data-ttu-id="f3337-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f3337-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="f3337-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3337-102">SYNOPSIS</span></span>
<span data-ttu-id="f3337-103">Adiciona uma configuração de emparelhamento a uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f3337-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="f3337-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3337-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3337-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3337-105">DESCRIPTION</span></span>
<span data-ttu-id="f3337-106">O cmdlet **Add-AzExpressRouteCrossConnectionPeering** adiciona uma configuração de emparelhamento a uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f3337-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="f3337-107">Observe que, depois de executar **Add-AzExpressRouteCrossConnectionPeering** , você deve chamar o cmdlet Set-AzExpressRouteCrossConnection para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="f3337-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering** , you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="f3337-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3337-108">EXAMPLES</span></span>

### <span data-ttu-id="f3337-109">Exemplo 1: adicionar um par a uma conexão cruzada do ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="f3337-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
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

## <span data-ttu-id="f3337-110">OS</span><span class="sxs-lookup"><span data-stu-id="f3337-110">PARAMETERS</span></span>

### <span data-ttu-id="f3337-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3337-111">-DefaultProfile</span></span>
<span data-ttu-id="f3337-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3337-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3337-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f3337-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="f3337-114">A conexão cruzada do ExpressRoute está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="f3337-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="f3337-115">Esse é o objeto do Azure retornado pelo cmdlet **Get-AzExpressRouteCrossConnection** .</span><span class="sxs-lookup"><span data-stu-id="f3337-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

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

### <span data-ttu-id="f3337-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f3337-116">-Force</span></span>
<span data-ttu-id="f3337-117">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="f3337-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f3337-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="f3337-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="f3337-119">Para obter um PeeringType de MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que pretende anunciar pela sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="f3337-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="f3337-120">Somente prefixos de endereço IP público são aceitos.</span><span class="sxs-lookup"><span data-stu-id="f3337-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="f3337-121">Você pode enviar uma lista separada por vírgulas, caso pretenda enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="f3337-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="f3337-122">Esses prefixos devem ser registrados para você em um nome de registro de roteamento (RIR/TIR).</span><span class="sxs-lookup"><span data-stu-id="f3337-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="f3337-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="f3337-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="f3337-124">Se você for anunciar prefixos que não são registrados para o número de emparelhamento como número, você pode especificar o número as para o qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="f3337-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="f3337-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="f3337-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="f3337-126">O nome do registro de roteamento (RIR/TIR) para o qual o número como e os prefixos são registrados.</span><span class="sxs-lookup"><span data-stu-id="f3337-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="f3337-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3337-127">-Name</span></span>
<span data-ttu-id="f3337-128">O nome da relação de emparelhamento a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="f3337-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="f3337-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="f3337-129">-PeerAddressType</span></span>
<span data-ttu-id="f3337-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="f3337-130">PeerAddressType</span></span>

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

### <span data-ttu-id="f3337-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="f3337-131">-PeerASN</span></span>
<span data-ttu-id="f3337-132">O número as de sua conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f3337-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="f3337-133">Isso deve ser um ASN público quando o PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="f3337-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="f3337-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f3337-134">-PeeringType</span></span>
<span data-ttu-id="f3337-135">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f3337-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="f3337-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f3337-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="f3337-137">Esse é o intervalo de endereços IP para o caminho de roteamento principal dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="f3337-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="f3337-138">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="f3337-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="f3337-139">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="f3337-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="f3337-140">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="f3337-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="f3337-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f3337-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="f3337-142">Esse é o intervalo de endereços IP para o caminho de roteamento secundário dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="f3337-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="f3337-143">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="f3337-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="f3337-144">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="f3337-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="f3337-145">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="f3337-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="f3337-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="f3337-146">-SharedKey</span></span>
<span data-ttu-id="f3337-147">Esse é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="f3337-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="f3337-148">-Vlanid</span><span class="sxs-lookup"><span data-stu-id="f3337-148">-VlanId</span></span>
<span data-ttu-id="f3337-149">Este é o número de identificação da VLAN atribuída a essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="f3337-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="f3337-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f3337-150">-Confirm</span></span>
<span data-ttu-id="f3337-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3337-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3337-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3337-152">-WhatIf</span></span>
<span data-ttu-id="f3337-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f3337-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3337-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3337-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3337-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3337-155">CommonParameters</span></span>
<span data-ttu-id="f3337-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3337-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3337-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3337-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3337-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3337-158">INPUTS</span></span>

### <span data-ttu-id="f3337-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f3337-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="f3337-160">O parâmetro ' ExpressRouteCrossConnection ' aceita o valor do tipo ' PSExpressRouteCrossConnection ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f3337-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="f3337-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3337-161">OUTPUTS</span></span>

### <span data-ttu-id="f3337-162">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f3337-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="f3337-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3337-163">NOTES</span></span>

## <span data-ttu-id="f3337-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3337-164">RELATED LINKS</span></span>

[<span data-ttu-id="f3337-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f3337-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="f3337-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f3337-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="f3337-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f3337-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="f3337-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f3337-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
