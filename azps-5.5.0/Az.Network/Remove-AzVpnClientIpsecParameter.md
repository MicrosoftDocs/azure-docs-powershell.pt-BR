---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: cee8d5d1ca76fbf206b4695661cc8f452052e62c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114641"
---
# <span data-ttu-id="aaefd-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="aaefd-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="aaefd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aaefd-102">SYNOPSIS</span></span>
<span data-ttu-id="aaefd-103">Remove a política ipsec personalizada vpn definida no recurso Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="aaefd-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="aaefd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aaefd-104">SYNTAX</span></span>

### <span data-ttu-id="aaefd-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="aaefd-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaefd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="aaefd-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaefd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aaefd-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaefd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="aaefd-108">DESCRIPTION</span></span>
<span data-ttu-id="aaefd-109">O Gateway de Rede Virtual é o objeto que representa seu gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="aaefd-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="aaefd-110">O cmdlet **Remove-AzVpnClientIpsecParameter** remove os parâmetros ipsec personalizados vpn definidos em seu Gateway de Rede Virtual, que, por sua vez, define a política ipsec de vpn padrão no gateway VPN com base no Nome virtualNetworkGateway e no Nome do Grupo de Recursos passado.</span><span class="sxs-lookup"><span data-stu-id="aaefd-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="aaefd-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aaefd-111">EXAMPLES</span></span>

### <span data-ttu-id="aaefd-112">Exemplo 1: exclui os parâmetros ipsec de vpn definidos no Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="aaefd-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="aaefd-113">Exclui os parâmetros ipsec personalizados vpn definidos em seu Gateway de Rede Virtual com o nome "myGateway" dentro do grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="aaefd-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="aaefd-114">Esse comando retorna um objeto bool mostrando se a remoção foi bem-sucedida ou falhou.</span><span class="sxs-lookup"><span data-stu-id="aaefd-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="aaefd-115">Observação: isso resultará na configuração da política ipsec de vpn padrão em seu Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="aaefd-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="aaefd-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aaefd-116">PARAMETERS</span></span>

### <span data-ttu-id="aaefd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaefd-117">-DefaultProfile</span></span>
<span data-ttu-id="aaefd-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aaefd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaefd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaefd-119">-InputObject</span></span>
<span data-ttu-id="aaefd-120">O objeto de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="aaefd-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="aaefd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaefd-121">-ResourceGroupName</span></span>
<span data-ttu-id="aaefd-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aaefd-122">The resource group name.</span></span>

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

### <span data-ttu-id="aaefd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaefd-123">-ResourceId</span></span>
<span data-ttu-id="aaefd-124">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="aaefd-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="aaefd-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="aaefd-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="aaefd-126">O nome do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="aaefd-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="aaefd-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="aaefd-127">-Confirm</span></span>
<span data-ttu-id="aaefd-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaefd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaefd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaefd-129">-WhatIf</span></span>
<span data-ttu-id="aaefd-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="aaefd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaefd-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aaefd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaefd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaefd-132">CommonParameters</span></span>
<span data-ttu-id="aaefd-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaefd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaefd-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaefd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaefd-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="aaefd-135">INPUTS</span></span>

### <span data-ttu-id="aaefd-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="aaefd-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="aaefd-137">System.String</span><span class="sxs-lookup"><span data-stu-id="aaefd-137">System.String</span></span>

## <span data-ttu-id="aaefd-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="aaefd-138">OUTPUTS</span></span>

### <span data-ttu-id="aaefd-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aaefd-139">System.Boolean</span></span>

## <span data-ttu-id="aaefd-140">Notas</span><span class="sxs-lookup"><span data-stu-id="aaefd-140">NOTES</span></span>

## <span data-ttu-id="aaefd-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aaefd-141">RELATED LINKS</span></span>

[<span data-ttu-id="aaefd-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="aaefd-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="aaefd-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="aaefd-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="aaefd-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="aaefd-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
