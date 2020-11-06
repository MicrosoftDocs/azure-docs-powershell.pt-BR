---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: b88fff9775665f5b20f403d46f11bba89dc61220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429425"
---
# <span data-ttu-id="e0187-101">Remove-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e0187-101">Remove-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="e0187-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0187-102">SYNOPSIS</span></span>
<span data-ttu-id="e0187-103">Remove a política IPSec personalizada de VPN definida no recurso de gateway virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="e0187-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0187-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0187-104">SYNTAX</span></span>

### <span data-ttu-id="e0187-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e0187-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0187-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e0187-106">ByFactoryObject</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0187-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0187-107">ByResourceId</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0187-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0187-108">DESCRIPTION</span></span>
<span data-ttu-id="e0187-109">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="e0187-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="e0187-110">O cmdlet **Remove-AzureRmVpnClientIpsecParameter** remove os parâmetros IPSec personalizados de VPN definidos em seu gateway de rede virtual, que, por sua vez, define a política padrão IPSec de VPN no gateway VPN com base no nome do VirtualNetworkGateway e no nome do grupo de recursos aprovado.</span><span class="sxs-lookup"><span data-stu-id="e0187-110">The **Remove-AzureRmVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="e0187-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0187-111">EXAMPLES</span></span>

### <span data-ttu-id="e0187-112">1: exclui os parâmetros Set VPN IPSec definidos no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e0187-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="e0187-113">Exclui os parâmetros IPSec personalizados de VPN definidos em seu gateway de rede virtual com o nome "mygateway" no grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="e0187-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="e0187-114">Esse comando retorna o objeto bool mostrando se a remoção foi bem-sucedida ou falhou.</span><span class="sxs-lookup"><span data-stu-id="e0187-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="e0187-115">Observação: isso resultará na definição da política IPSec de VPN padrão em seu gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e0187-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="e0187-116">OS</span><span class="sxs-lookup"><span data-stu-id="e0187-116">PARAMETERS</span></span>

### <span data-ttu-id="e0187-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0187-117">-DefaultProfile</span></span>
<span data-ttu-id="e0187-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0187-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0187-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0187-119">-InputObject</span></span>
<span data-ttu-id="e0187-120">O objeto Gateaway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e0187-120">The virtual network gateaway object</span></span>

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

### <span data-ttu-id="e0187-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0187-121">-ResourceGroupName</span></span>
<span data-ttu-id="e0187-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0187-122">The resource group name.</span></span>

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

### <span data-ttu-id="e0187-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0187-123">-ResourceId</span></span>
<span data-ttu-id="e0187-124">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0187-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e0187-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="e0187-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="e0187-126">O nome do gateway da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e0187-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="e0187-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0187-127">-Confirm</span></span>
<span data-ttu-id="e0187-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0187-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0187-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0187-129">-WhatIf</span></span>
<span data-ttu-id="e0187-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0187-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0187-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0187-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0187-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0187-132">CommonParameters</span></span>
<span data-ttu-id="e0187-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0187-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0187-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0187-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0187-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0187-135">INPUTS</span></span>

### <span data-ttu-id="e0187-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0187-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="e0187-137">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e0187-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e0187-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e0187-138">System.String</span></span>

## <span data-ttu-id="e0187-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0187-139">OUTPUTS</span></span>

### <span data-ttu-id="e0187-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0187-140">System.Boolean</span></span>

## <span data-ttu-id="e0187-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0187-141">NOTES</span></span>

## <span data-ttu-id="e0187-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0187-142">RELATED LINKS</span></span>
