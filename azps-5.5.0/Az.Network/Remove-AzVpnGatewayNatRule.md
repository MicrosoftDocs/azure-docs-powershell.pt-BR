---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
ms.openlocfilehash: 35a59b24297efe3fd94a66d19a778913f488b800
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111567"
---
# <span data-ttu-id="da261-101">Remove-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="da261-101">Remove-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="da261-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da261-102">SYNOPSIS</span></span>
<span data-ttu-id="da261-103">Remove uma regra NAT associada ao VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="da261-103">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="da261-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da261-104">SYNTAX</span></span>

### <span data-ttu-id="da261-105">ByVpnGatewayNatRuleName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="da261-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da261-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="da261-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da261-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="da261-107">ByVpnGatewayNatRuleObject</span></span>
```
Remove-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da261-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="da261-108">DESCRIPTION</span></span>
<span data-ttu-id="da261-109">Remove uma regra NAT associada ao VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="da261-109">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="da261-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="da261-110">EXAMPLES</span></span>

### <span data-ttu-id="da261-111">Exemplo1</span><span class="sxs-lookup"><span data-stu-id="da261-111">Example1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Remove-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"
```

<span data-ttu-id="da261-112">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual, VpnGateway e regra NAT associada a essa VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="da261-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub,VpnGateway and NAT rule associated with that VpnGateway.</span></span>
<span data-ttu-id="da261-113">Em seguida, ela remove a regra NAT usando o nome da regra NAT.</span><span class="sxs-lookup"><span data-stu-id="da261-113">Then it removes the NAT rule using the NAT rule name.</span></span>


## <span data-ttu-id="da261-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da261-114">PARAMETERS</span></span>

### <span data-ttu-id="da261-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da261-115">-DefaultProfile</span></span>
<span data-ttu-id="da261-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da261-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da261-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="da261-117">-Force</span></span>
<span data-ttu-id="da261-118">Não peça confirmação se quiser excluir um recurso</span><span class="sxs-lookup"><span data-stu-id="da261-118">Do not ask for confirmation if you want to delete a resource</span></span>

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

### <span data-ttu-id="da261-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da261-119">-InputObject</span></span>
<span data-ttu-id="da261-120">O objeto VpnGatewayNatRule a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="da261-120">The VpnGatewayNatRule object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule
Parameter Sets: ByVpnGatewayNatRuleObject
Aliases: VpnGatewayNatRule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da261-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="da261-121">-Name</span></span>
<span data-ttu-id="da261-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="da261-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da261-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="da261-123">-ParentResourceName</span></span>
<span data-ttu-id="da261-124">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="da261-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da261-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da261-125">-PassThru</span></span>
<span data-ttu-id="da261-126">Retorna um objeto que representa o item no qual esta operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="da261-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="da261-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da261-127">-ResourceGroupName</span></span>
<span data-ttu-id="da261-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="da261-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da261-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da261-129">-ResourceId</span></span>
<span data-ttu-id="da261-130">A ID do recurso do objeto VpnGatewayNatRule a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="da261-130">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da261-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="da261-131">-Confirm</span></span>
<span data-ttu-id="da261-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da261-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da261-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da261-133">-WhatIf</span></span>
<span data-ttu-id="da261-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="da261-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da261-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da261-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da261-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da261-136">CommonParameters</span></span>
<span data-ttu-id="da261-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da261-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da261-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da261-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da261-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="da261-139">INPUTS</span></span>

### <span data-ttu-id="da261-140">System.String</span><span class="sxs-lookup"><span data-stu-id="da261-140">System.String</span></span>

### <span data-ttu-id="da261-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="da261-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="da261-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="da261-142">OUTPUTS</span></span>

### <span data-ttu-id="da261-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da261-143">System.Boolean</span></span>

## <span data-ttu-id="da261-144">Notas</span><span class="sxs-lookup"><span data-stu-id="da261-144">NOTES</span></span>

## <span data-ttu-id="da261-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da261-145">RELATED LINKS</span></span>
