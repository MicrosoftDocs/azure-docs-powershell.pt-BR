---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 1ffa87d60426bc7b012dd003cf8a52b215502f59
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940651"
---
# <span data-ttu-id="8bdb0-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8bdb0-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="8bdb0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bdb0-102">SYNOPSIS</span></span>
<span data-ttu-id="8bdb0-103">Define os parâmetros de VPN IPsec do gateway de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="8bdb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bdb0-104">SYNTAX</span></span>

### <span data-ttu-id="8bdb0-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8bdb0-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bdb0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8bdb0-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bdb0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8bdb0-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bdb0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bdb0-108">DESCRIPTION</span></span>
<span data-ttu-id="8bdb0-109">O cmdlet **set-AzVpnClientIpsecParameter** define os parâmetros de VPN IPsec do gateway de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="8bdb0-110">Quando o gateway de rede virtual é criado, ele define o conjunto de diretivas IPSec de VPN padrão no gateway.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="8bdb0-111">Em caso afirmativo, o usuário do site quer usar determinada política IPSec personalizada para se conectar ao gateway VPN, o usuário tem que definir essa política IPSec em um gateway VPN primeiro.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="8bdb0-112">**Set-AzVpnClientIpsecParameter** fornece uma maneira de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="8bdb0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bdb0-113">EXAMPLES</span></span>

### <span data-ttu-id="8bdb0-114">Exemplo 1: define uma política IPSec VPN personalizada como um gateway de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-114">Example 1 : Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="8bdb0-115">Este exemplo define a política IPSec de VPN personalizada como o gateway de rede virtual existente chamado ContosoVirtualGateway do grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="8bdb0-116">New-AzVpnClientIpsecParameter cmdlet é usado para criar o objeto de parâmetros de IPSec VPN do uso dos valores passados um ou todos os parâmetros que o usuário pode definir para qualquer gateway de rede virtual existente no grupo de Resource.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="8bdb0-117">Esse objeto VpnClientIPsecParameters criado é passado para o comando Set-AzVpnClientIpsecParameter para definir a política personalizada IPSec IPSec especificada no gateway de rede virtual, conforme mostrado no exemplo acima.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="8bdb0-118">Esse comando retorna o objeto do VpnClientIPsecParameters que mostra Set Parameters.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="8bdb0-119">OS</span><span class="sxs-lookup"><span data-stu-id="8bdb0-119">PARAMETERS</span></span>

### <span data-ttu-id="8bdb0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bdb0-120">-DefaultProfile</span></span>
<span data-ttu-id="8bdb0-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bdb0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bdb0-122">-InputObject</span></span>
<span data-ttu-id="8bdb0-123">O objeto de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="8bdb0-123">The virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdb0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bdb0-124">-ResourceGroupName</span></span>
<span data-ttu-id="8bdb0-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-125">The resource group name.</span></span>

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

### <span data-ttu-id="8bdb0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bdb0-126">-ResourceId</span></span>
<span data-ttu-id="8bdb0-127">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdb0-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8bdb0-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8bdb0-129">O nome do gateway da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="8bdb0-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="8bdb0-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="8bdb0-131">Parâmetros de IPsec do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="8bdb0-132">Esse valor de parâmetro pode ser construído usando o comando PS Let: New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8bdb0-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdb0-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8bdb0-133">-Confirm</span></span>
<span data-ttu-id="8bdb0-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bdb0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bdb0-135">-WhatIf</span></span>
<span data-ttu-id="8bdb0-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bdb0-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bdb0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bdb0-138">CommonParameters</span></span>
<span data-ttu-id="8bdb0-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bdb0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bdb0-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bdb0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bdb0-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bdb0-141">INPUTS</span></span>

### <span data-ttu-id="8bdb0-142">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="8bdb0-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="8bdb0-143">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8bdb0-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="8bdb0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8bdb0-144">System.String</span></span>

## <span data-ttu-id="8bdb0-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bdb0-145">OUTPUTS</span></span>

### <span data-ttu-id="8bdb0-146">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="8bdb0-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="8bdb0-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bdb0-147">NOTES</span></span>

## <span data-ttu-id="8bdb0-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bdb0-148">RELATED LINKS</span></span>

[<span data-ttu-id="8bdb0-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8bdb0-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8bdb0-150">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8bdb0-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8bdb0-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8bdb0-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
