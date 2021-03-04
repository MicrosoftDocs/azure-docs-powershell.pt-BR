---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
ms.openlocfilehash: d4f0b908a229ee47472d40eefe60c5771c0147d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889432"
---
# <span data-ttu-id="194a7-101">New-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="194a7-101">New-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="194a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="194a7-102">SYNOPSIS</span></span>
<span data-ttu-id="194a7-103">Cria uma regra NAT em uma VpnGateway que pode ser associada a VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="194a7-103">Creates a NAT rule on a VpnGateway which can be associated with VpnSiteLinkConnection.</span></span>

## <span data-ttu-id="194a7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="194a7-104">SYNTAX</span></span>

### <span data-ttu-id="194a7-105">ByVpnGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="194a7-105">ByVpnGatewayName (Default)</span></span>
```
New-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] -InternalMapping <String[]> -ExternalMapping <String[]>
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="194a7-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="194a7-106">ByVpnGatewayObject</span></span>
```
New-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="194a7-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="194a7-107">ByVpnGatewayResourceId</span></span>
```
New-AzVpnGatewayNatRule -ParentResourceId <String> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="194a7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="194a7-108">DESCRIPTION</span></span>
<span data-ttu-id="194a7-109">Cria uma regra NAT em uma VpnGateway que pode ser associada a VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="194a7-109">Creates a NAT rule on a VpnGateway which can be associated with VpnGateway.</span></span>

## <span data-ttu-id="194a7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="194a7-110">EXAMPLES</span></span>

### <span data-ttu-id="194a7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="194a7-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"

Type                      : Static
Mode                      : EgressSnat
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

<span data-ttu-id="194a7-112">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="194a7-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="194a7-113">Em seguida, criaremos VpnGateway sob esse Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="194a7-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="194a7-114">Em seguida, usando este comando: New-AzVpnGatewayNatRule, a regra NAT pode ser criada e associada ao VpnGateway criado.</span><span class="sxs-lookup"><span data-stu-id="194a7-114">Then, using this command: New-AzVpnGatewayNatRule, NAT rule can be createdand associated with created VpnGateway.</span></span>

## <span data-ttu-id="194a7-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="194a7-115">PARAMETERS</span></span>

### <span data-ttu-id="194a7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="194a7-116">-AsJob</span></span>
<span data-ttu-id="194a7-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="194a7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="194a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="194a7-118">-DefaultProfile</span></span>
<span data-ttu-id="194a7-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="194a7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="194a7-120">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="194a7-120">-ExternalMapping</span></span>
<span data-ttu-id="194a7-121">A lista de mapeamentos externos de sub-rede de endereço IP privados para NAT</span><span class="sxs-lookup"><span data-stu-id="194a7-121">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="194a7-122">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="194a7-122">-InternalMapping</span></span>
<span data-ttu-id="194a7-123">A lista de mapeamentos internos de sub-rede de endereço IP privados para NAT</span><span class="sxs-lookup"><span data-stu-id="194a7-123">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="194a7-124">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="194a7-124">-IpConfigurationId</span></span>
<span data-ttu-id="194a7-125">A ID de Configuração IP a que esta regra NAT se aplica</span><span class="sxs-lookup"><span data-stu-id="194a7-125">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="194a7-126">-Mode</span><span class="sxs-lookup"><span data-stu-id="194a7-126">-Mode</span></span>
<span data-ttu-id="194a7-127">A direção NAT de origem de um NAT VPN</span><span class="sxs-lookup"><span data-stu-id="194a7-127">The Source NAT direction of a VPN NAT</span></span>

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

### <span data-ttu-id="194a7-128">-Name</span><span class="sxs-lookup"><span data-stu-id="194a7-128">-Name</span></span>
<span data-ttu-id="194a7-129">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="194a7-129">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="194a7-130">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="194a7-130">-ParentObject</span></span>
<span data-ttu-id="194a7-131">O VpnGateway pai para esta regra NAT.</span><span class="sxs-lookup"><span data-stu-id="194a7-131">The parent VpnGateway for this NAT Rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="194a7-132">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="194a7-132">-ParentResourceId</span></span>
<span data-ttu-id="194a7-133">A id de recurso do VpnGateway pai para esta Regra NAT.</span><span class="sxs-lookup"><span data-stu-id="194a7-133">The resource id of the parent VpnGateway for this NAT Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="194a7-134">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="194a7-134">-ParentResourceName</span></span>
<span data-ttu-id="194a7-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="194a7-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="194a7-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="194a7-136">-ResourceGroupName</span></span>
<span data-ttu-id="194a7-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="194a7-137">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="194a7-138">-Type</span><span class="sxs-lookup"><span data-stu-id="194a7-138">-Type</span></span>
<span data-ttu-id="194a7-139">O tipo de regra NAT para NAT VPN</span><span class="sxs-lookup"><span data-stu-id="194a7-139">The type of NAT rule for VPN NAT</span></span>

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

### <span data-ttu-id="194a7-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="194a7-140">-Confirm</span></span>
<span data-ttu-id="194a7-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="194a7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="194a7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="194a7-142">-WhatIf</span></span>
<span data-ttu-id="194a7-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="194a7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="194a7-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="194a7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="194a7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="194a7-145">CommonParameters</span></span>
<span data-ttu-id="194a7-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="194a7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="194a7-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="194a7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="194a7-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="194a7-148">INPUTS</span></span>

### <span data-ttu-id="194a7-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="194a7-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="194a7-150">System.String</span><span class="sxs-lookup"><span data-stu-id="194a7-150">System.String</span></span>

## <span data-ttu-id="194a7-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="194a7-151">OUTPUTS</span></span>

### <span data-ttu-id="194a7-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="194a7-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="194a7-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="194a7-153">NOTES</span></span>

## <span data-ttu-id="194a7-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="194a7-154">RELATED LINKS</span></span>
