---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 505f9eb3b2402756b14fa8b8f49cb1a9ea2a3745
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943952"
---
# <span data-ttu-id="fd47d-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fd47d-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="fd47d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd47d-102">SYNOPSIS</span></span>
<span data-ttu-id="fd47d-103">Remove a política IPSec personalizada de VPN definida no recurso de gateway virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="fd47d-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="fd47d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd47d-104">SYNTAX</span></span>

### <span data-ttu-id="fd47d-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fd47d-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd47d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fd47d-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd47d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd47d-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd47d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd47d-108">DESCRIPTION</span></span>
<span data-ttu-id="fd47d-109">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="fd47d-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="fd47d-110">O cmdlet **Remove-AzVpnClientIpsecParameter** remove os parâmetros IPSec personalizados de VPN definidos em seu gateway de rede virtual, que, por sua vez, define a política padrão IPSec de VPN no gateway VPN com base no nome do VirtualNetworkGateway e no nome do grupo de recursos aprovado.</span><span class="sxs-lookup"><span data-stu-id="fd47d-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="fd47d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd47d-111">EXAMPLES</span></span>

### <span data-ttu-id="fd47d-112">1: exclui os parâmetros Set VPN IPSec definidos no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="fd47d-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="fd47d-113">Exclui os parâmetros IPSec personalizados de VPN definidos em seu gateway de rede virtual com o nome "mygateway" no grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="fd47d-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="fd47d-114">Esse comando retorna o objeto bool mostrando se a remoção foi bem-sucedida ou falhou.</span><span class="sxs-lookup"><span data-stu-id="fd47d-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="fd47d-115">Observação: isso resultará na definição da política IPSec de VPN padrão em seu gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fd47d-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="fd47d-116">OS</span><span class="sxs-lookup"><span data-stu-id="fd47d-116">PARAMETERS</span></span>

### <span data-ttu-id="fd47d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd47d-117">-DefaultProfile</span></span>
<span data-ttu-id="fd47d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd47d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd47d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd47d-119">-InputObject</span></span>
<span data-ttu-id="fd47d-120">O objeto de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="fd47d-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="fd47d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd47d-121">-ResourceGroupName</span></span>
<span data-ttu-id="fd47d-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fd47d-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd47d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd47d-123">-ResourceId</span></span>
<span data-ttu-id="fd47d-124">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="fd47d-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fd47d-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="fd47d-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="fd47d-126">O nome do gateway da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fd47d-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd47d-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fd47d-127">-Confirm</span></span>
<span data-ttu-id="fd47d-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd47d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd47d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd47d-129">-WhatIf</span></span>
<span data-ttu-id="fd47d-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd47d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd47d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd47d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd47d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd47d-132">CommonParameters</span></span>
<span data-ttu-id="fd47d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd47d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd47d-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd47d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd47d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd47d-135">INPUTS</span></span>

### <span data-ttu-id="fd47d-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd47d-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="fd47d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fd47d-137">System.String</span></span>

## <span data-ttu-id="fd47d-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd47d-138">OUTPUTS</span></span>

### <span data-ttu-id="fd47d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd47d-139">System.Boolean</span></span>

## <span data-ttu-id="fd47d-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd47d-140">NOTES</span></span>

## <span data-ttu-id="fd47d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd47d-141">RELATED LINKS</span></span>

[<span data-ttu-id="fd47d-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fd47d-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="fd47d-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fd47d-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="fd47d-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fd47d-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
