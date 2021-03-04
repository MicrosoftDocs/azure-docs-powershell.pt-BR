---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 513fbe1d973a75dbc1c967610d95882202bab147
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886420"
---
# <span data-ttu-id="dffa6-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="dffa6-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="dffa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dffa6-102">SYNOPSIS</span></span>
<span data-ttu-id="dffa6-103">Remove o conjunto de política ipsec personalizada vpn no recurso Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="dffa6-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="dffa6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dffa6-104">SYNTAX</span></span>

### <span data-ttu-id="dffa6-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dffa6-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dffa6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dffa6-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dffa6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dffa6-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dffa6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dffa6-108">DESCRIPTION</span></span>
<span data-ttu-id="dffa6-109">O Gateway de Rede Virtual é o objeto que representa seu gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="dffa6-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="dffa6-110">O cmdlet **Remove-AzVpnClientIpsecParameter** remove os parâmetros ipsec personalizados vpn definidos em seu Gateway de Rede Virtual, que, por sua vez, define a política padrão de ipsec vpn no gateway VPN com base no Nome virtualNetworkGateway e no Nome do Grupo de Recursos passado.</span><span class="sxs-lookup"><span data-stu-id="dffa6-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="dffa6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dffa6-111">EXAMPLES</span></span>

### <span data-ttu-id="dffa6-112">Exemplo 1: exclui os parâmetros ipsec de vpn definidos no Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="dffa6-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="dffa6-113">Exclui os parâmetros ipsec personalizados vpn definidos em seu Gateway de Rede Virtual com o nome "myGateway" dentro do grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="dffa6-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="dffa6-114">Este comando retorna o objeto bool mostrando se a remoção foi bem-sucedida ou falhou.</span><span class="sxs-lookup"><span data-stu-id="dffa6-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="dffa6-115">Observação: isso resultará na definição da política padrão de ipsec vpn no Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="dffa6-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="dffa6-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dffa6-116">PARAMETERS</span></span>

### <span data-ttu-id="dffa6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dffa6-117">-DefaultProfile</span></span>
<span data-ttu-id="dffa6-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dffa6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dffa6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dffa6-119">-InputObject</span></span>
<span data-ttu-id="dffa6-120">O objeto gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="dffa6-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="dffa6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dffa6-121">-ResourceGroupName</span></span>
<span data-ttu-id="dffa6-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dffa6-122">The resource group name.</span></span>

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

### <span data-ttu-id="dffa6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dffa6-123">-ResourceId</span></span>
<span data-ttu-id="dffa6-124">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="dffa6-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="dffa6-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="dffa6-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="dffa6-126">O nome do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="dffa6-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="dffa6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dffa6-127">-Confirm</span></span>
<span data-ttu-id="dffa6-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dffa6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dffa6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dffa6-129">-WhatIf</span></span>
<span data-ttu-id="dffa6-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dffa6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dffa6-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dffa6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dffa6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dffa6-132">CommonParameters</span></span>
<span data-ttu-id="dffa6-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dffa6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dffa6-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dffa6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dffa6-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dffa6-135">INPUTS</span></span>

### <span data-ttu-id="dffa6-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dffa6-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="dffa6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="dffa6-137">System.String</span></span>

## <span data-ttu-id="dffa6-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dffa6-138">OUTPUTS</span></span>

### <span data-ttu-id="dffa6-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dffa6-139">System.Boolean</span></span>

## <span data-ttu-id="dffa6-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="dffa6-140">NOTES</span></span>

## <span data-ttu-id="dffa6-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dffa6-141">RELATED LINKS</span></span>

[<span data-ttu-id="dffa6-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="dffa6-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="dffa6-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="dffa6-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="dffa6-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="dffa6-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
