---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
ms.openlocfilehash: 61dbb86c7eaa574abfcb3fad4bd37d6dbb242260
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114144"
---
# <span data-ttu-id="ee65d-101">Get-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="ee65d-101">Get-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="ee65d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee65d-102">SYNOPSIS</span></span>
<span data-ttu-id="ee65d-103">Obtém uma regra NAT associada ao VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="ee65d-103">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="ee65d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee65d-104">SYNTAX</span></span>

### <span data-ttu-id="ee65d-105">ByVpnGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ee65d-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee65d-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ee65d-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee65d-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ee65d-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnGatewayNatRule -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee65d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee65d-108">DESCRIPTION</span></span>
<span data-ttu-id="ee65d-109">Obtém uma regra NAT associada ao VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="ee65d-109">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="ee65d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ee65d-110">EXAMPLES</span></span>

### <span data-ttu-id="ee65d-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ee65d-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Get-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"

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

<span data-ttu-id="ee65d-112">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual e VpnGateway & uma regra NAT associada ao Vpngateway.</span><span class="sxs-lookup"><span data-stu-id="ee65d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and VpnGateway & a NAT rule associated with Vpngateway.</span></span>
<span data-ttu-id="ee65d-113">Em seguida, ela obtém a regra NAT usando o nome da regra NAT.</span><span class="sxs-lookup"><span data-stu-id="ee65d-113">Then it gets the NAT rule using the NAT rule name.</span></span>

## <span data-ttu-id="ee65d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee65d-114">PARAMETERS</span></span>

### <span data-ttu-id="ee65d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee65d-115">-DefaultProfile</span></span>
<span data-ttu-id="ee65d-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee65d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee65d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee65d-117">-Name</span></span>
<span data-ttu-id="ee65d-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ee65d-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee65d-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ee65d-119">-ParentObject</span></span>
<span data-ttu-id="ee65d-120">O VpnGateway pai desta VpnGatewayNatRule.</span><span class="sxs-lookup"><span data-stu-id="ee65d-120">The parent VpnGateway for this VpnGatewayNatRule.</span></span>

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

### <span data-ttu-id="ee65d-121">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ee65d-121">-ParentResourceId</span></span>
<span data-ttu-id="ee65d-122">A ID do recurso do VpnGateway pai para esta VpnGatewayNatRule.</span><span class="sxs-lookup"><span data-stu-id="ee65d-122">The resource id of the parent VpnGateway for this VpnGatewayNatRule.</span></span>

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

### <span data-ttu-id="ee65d-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="ee65d-123">-ParentResourceName</span></span>
<span data-ttu-id="ee65d-124">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="ee65d-124">The parent resource name.</span></span>

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

### <span data-ttu-id="ee65d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee65d-125">-ResourceGroupName</span></span>
<span data-ttu-id="ee65d-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee65d-126">The resource group name.</span></span>

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

### <span data-ttu-id="ee65d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee65d-127">CommonParameters</span></span>
<span data-ttu-id="ee65d-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee65d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee65d-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee65d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee65d-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="ee65d-130">INPUTS</span></span>

### <span data-ttu-id="ee65d-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ee65d-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="ee65d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ee65d-132">System.String</span></span>

## <span data-ttu-id="ee65d-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="ee65d-133">OUTPUTS</span></span>

### <span data-ttu-id="ee65d-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="ee65d-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="ee65d-135">Notas</span><span class="sxs-lookup"><span data-stu-id="ee65d-135">NOTES</span></span>

## <span data-ttu-id="ee65d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee65d-136">RELATED LINKS</span></span>
