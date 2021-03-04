---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 55a4f3c143355bf40672a1c3151d509b69062490
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885387"
---
# <span data-ttu-id="ebc5b-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ebc5b-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="ebc5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebc5b-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc5b-103">Define os parâmetros ipsec vpn para gateway de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="ebc5b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ebc5b-104">SYNTAX</span></span>

### <span data-ttu-id="ebc5b-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ebc5b-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc5b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ebc5b-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc5b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ebc5b-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebc5b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ebc5b-108">DESCRIPTION</span></span>
<span data-ttu-id="ebc5b-109">O cmdlet **Set-AzVpnClientIpsecParameter** define os parâmetros ipsec vpn para gateway de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="ebc5b-110">Quando o gateway de rede virtual é criado, ele define o conjunto de políticas ipsec de vpn padrão no Gateway.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="ebc5b-111">Caso o usuário aponte para o site queira usar determinada política ipsec personalizada para se conectar ao Gateway VPN, o usuário precisa definir essa política ipsec primeiro no VPN Gateway.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="ebc5b-112">**Set-AzVpnClientIpsecParameter** fornece uma maneira de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="ebc5b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ebc5b-113">EXAMPLES</span></span>

### <span data-ttu-id="ebc5b-114">Exemplo 1: define uma política ipsec de vpn personalizada como gateway de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="ebc5b-115">Este exemplo define a política de ipsec vpn personalizada como gateway de rede virtual existente chamado ContosoVirtualGateway do grupo resource chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="ebc5b-116">New-AzVpnClientIpsecParameter cmdlet é usado para criar o objeto de parâmetros ipsec vpn de usar os valores de um ou todos os parâmetros passados que o usuário pode definir para qualquer gateway de rede virtual existente no ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="ebc5b-117">Este objeto VpnClientIPsecParameters criado é passado para o comando Set-AzVpnClientIpsecParameter para definir a política personalizada ipsec vpn especificada no gateway de rede virtual, conforme mostrado no exemplo acima.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="ebc5b-118">Este comando retorna o objeto VpnClientIPsecParameters que mostra parâmetros definidos.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="ebc5b-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ebc5b-119">PARAMETERS</span></span>

### <span data-ttu-id="ebc5b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc5b-120">-DefaultProfile</span></span>
<span data-ttu-id="ebc5b-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebc5b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebc5b-122">-InputObject</span></span>
<span data-ttu-id="ebc5b-123">O objeto gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="ebc5b-123">The virtual network gateway object</span></span>

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

### <span data-ttu-id="ebc5b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc5b-124">-ResourceGroupName</span></span>
<span data-ttu-id="ebc5b-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-125">The resource group name.</span></span>

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

### <span data-ttu-id="ebc5b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebc5b-126">-ResourceId</span></span>
<span data-ttu-id="ebc5b-127">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ebc5b-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ebc5b-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ebc5b-129">O nome do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="ebc5b-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="ebc5b-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="ebc5b-131">Parâmetros ipsec de cliente vpn.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="ebc5b-132">Esse valor de parâmetro pode ser construído usando o comando PS let:New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ebc5b-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="ebc5b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebc5b-133">-Confirm</span></span>
<span data-ttu-id="ebc5b-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebc5b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebc5b-135">-WhatIf</span></span>
<span data-ttu-id="ebc5b-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebc5b-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebc5b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc5b-138">CommonParameters</span></span>
<span data-ttu-id="ebc5b-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc5b-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebc5b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc5b-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebc5b-141">INPUTS</span></span>

### <span data-ttu-id="ebc5b-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="ebc5b-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="ebc5b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ebc5b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="ebc5b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ebc5b-144">System.String</span></span>

## <span data-ttu-id="ebc5b-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ebc5b-145">OUTPUTS</span></span>

### <span data-ttu-id="ebc5b-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="ebc5b-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="ebc5b-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="ebc5b-147">NOTES</span></span>

## <span data-ttu-id="ebc5b-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ebc5b-148">RELATED LINKS</span></span>

[<span data-ttu-id="ebc5b-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ebc5b-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="ebc5b-150">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ebc5b-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="ebc5b-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ebc5b-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
