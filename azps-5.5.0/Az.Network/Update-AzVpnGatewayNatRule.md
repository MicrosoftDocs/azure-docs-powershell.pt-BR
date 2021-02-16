---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
ms.openlocfilehash: 60f68795e79e751dda75ae4d549d2b25a43392e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113416"
---
# <span data-ttu-id="16541-101">Update-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="16541-101">Update-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="16541-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16541-102">SYNOPSIS</span></span>
<span data-ttu-id="16541-103">Atualiza uma regra NAT associada ao VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="16541-103">Updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="16541-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16541-104">SYNTAX</span></span>

### <span data-ttu-id="16541-105">ByVpnGatewayNatRuleName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="16541-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Update-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>] [-ExternalMapping <String[]>]
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16541-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="16541-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Update-AzVpnGatewayNatRule -ResourceId <String> [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>]
 [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16541-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="16541-107">ByVpnGatewayNatRuleObject</span></span>
```
Update-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Type <String>] [-Mode <String>]
 [-InternalMapping <String[]>] [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16541-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="16541-108">DESCRIPTION</span></span>
<span data-ttu-id="16541-109">O cmdlet **Update-AzVpnGatewayNatRule** atualiza uma regra NAT associada ao VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="16541-109">The **Update-AzVpnGatewayNatRule** cmdlet updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="16541-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="16541-110">EXAMPLES</span></span>

### <span data-ttu-id="16541-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="16541-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> $natRule = Update-AzVpnGatewayNatRule -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy
PS C:\> Update-AzVpnGatewayNatRule -InputObject $natRule -Type Dynamic -Mode IngressSnat

Type                      : Dynamic
Mode                      : IngressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule
```

<span data-ttu-id="16541-112">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="16541-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="16541-113">Em seguida, criaremos o VpnGateway nesse Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="16541-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="16541-114">Em seguida, crie uma nova regra NAT associada ao VpnGateway criado.</span><span class="sxs-lookup"><span data-stu-id="16541-114">Then, create new NAT rule associated with created VpnGateway.</span></span>
<span data-ttu-id="16541-115">Usando este comando: Update-AzVpnGatewayNatRule, atualize a regra NAT.</span><span class="sxs-lookup"><span data-stu-id="16541-115">Using this command: Update-AzVpnGatewayNatRule, update NAT rule.</span></span>

## <span data-ttu-id="16541-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16541-116">PARAMETERS</span></span>

### <span data-ttu-id="16541-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16541-117">-AsJob</span></span>
<span data-ttu-id="16541-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="16541-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16541-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16541-119">-DefaultProfile</span></span>
<span data-ttu-id="16541-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16541-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16541-121">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="16541-121">-ExternalMapping</span></span>
<span data-ttu-id="16541-122">A lista de mapeamentos externos da sub-rede de endereço IP particular para NAT</span><span class="sxs-lookup"><span data-stu-id="16541-122">The list of private IP address subnet external mappings for NAT</span></span>

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

### <span data-ttu-id="16541-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16541-123">-InputObject</span></span>
<span data-ttu-id="16541-124">O objeto VpnGatewayNatRule a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="16541-124">The VpnGatewayNatRule object to update.</span></span>

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

### <span data-ttu-id="16541-125">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="16541-125">-InternalMapping</span></span>
<span data-ttu-id="16541-126">A lista de mapeamentos internos da sub-rede de endereços IP particulares para NAT</span><span class="sxs-lookup"><span data-stu-id="16541-126">The list of private IP address subnet internal mappings for NAT</span></span>

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

### <span data-ttu-id="16541-127">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="16541-127">-IpConfigurationId</span></span>
<span data-ttu-id="16541-128">A ID de Configuração IP a que esta regra NAT se aplica</span><span class="sxs-lookup"><span data-stu-id="16541-128">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="16541-129">-Modo</span><span class="sxs-lookup"><span data-stu-id="16541-129">-Mode</span></span>
<span data-ttu-id="16541-130">A direção NAT de origem de uma NAT VPN</span><span class="sxs-lookup"><span data-stu-id="16541-130">The Source NAT direction of a VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EgressSnat, IngressSnat

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16541-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="16541-131">-Name</span></span>
<span data-ttu-id="16541-132">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="16541-132">The resource name.</span></span>

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

### <span data-ttu-id="16541-133">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="16541-133">-ParentResourceName</span></span>
<span data-ttu-id="16541-134">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="16541-134">The parent resource name.</span></span>

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

### <span data-ttu-id="16541-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16541-135">-ResourceGroupName</span></span>
<span data-ttu-id="16541-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16541-136">The resource group name.</span></span>

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

### <span data-ttu-id="16541-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16541-137">-ResourceId</span></span>
<span data-ttu-id="16541-138">A ID do recurso do objeto VpnGatewayNatRule a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="16541-138">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16541-139">-Tipo</span><span class="sxs-lookup"><span data-stu-id="16541-139">-Type</span></span>
<span data-ttu-id="16541-140">O tipo de regra NAT para NAT VPN</span><span class="sxs-lookup"><span data-stu-id="16541-140">The type of NAT rule for VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16541-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="16541-141">-Confirm</span></span>
<span data-ttu-id="16541-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16541-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16541-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16541-143">-WhatIf</span></span>
<span data-ttu-id="16541-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="16541-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16541-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16541-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16541-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16541-146">CommonParameters</span></span>
<span data-ttu-id="16541-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16541-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16541-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16541-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16541-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="16541-149">INPUTS</span></span>

### <span data-ttu-id="16541-150">System.String</span><span class="sxs-lookup"><span data-stu-id="16541-150">System.String</span></span>

### <span data-ttu-id="16541-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="16541-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="16541-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="16541-152">OUTPUTS</span></span>

### <span data-ttu-id="16541-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="16541-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="16541-154">Notas</span><span class="sxs-lookup"><span data-stu-id="16541-154">NOTES</span></span>

## <span data-ttu-id="16541-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16541-155">RELATED LINKS</span></span>
