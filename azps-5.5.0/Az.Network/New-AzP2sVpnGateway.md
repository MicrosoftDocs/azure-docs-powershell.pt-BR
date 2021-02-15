---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 401fa91682e68b74e950d5010b22ce140436b06a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112823"
---
# <span data-ttu-id="455ea-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="455ea-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="455ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="455ea-102">SYNOPSIS</span></span>
<span data-ttu-id="455ea-103">Crie um novo P2SVpnGateway no VirtualHub para apontar para a conectividade do site.</span><span class="sxs-lookup"><span data-stu-id="455ea-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="455ea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="455ea-104">SYNTAX</span></span>

### <span data-ttu-id="455ea-105">ByVirtualHubNameByVpnServerConfigurationObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="455ea-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="455ea-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="455ea-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="455ea-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="455ea-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="455ea-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="455ea-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="455ea-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="455ea-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="455ea-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="455ea-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="455ea-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="455ea-111">DESCRIPTION</span></span>
<span data-ttu-id="455ea-112">O cmdlet New-AzP2sVpnGateway permite que você crie um novo P2SVpnGateway no VirtualHub para apontar para a conectividade do site de clientes ponto a site para o Azure VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="455ea-112">The New-AzP2sVpnGateway cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="455ea-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="455ea-113">EXAMPLES</span></span>

### <span data-ttu-id="455ea-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="455ea-114">Example 1</span></span>
```
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1 -EnableInternetSecurityFlag -EnableRoutingPreferenceInternetFlag

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "EnableInternetSecurity": True,
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="455ea-115">O New-AzP2sVpnGateway cmdlet permite que você crie um novo P2SVpnGateway no VirtualHub para conectividade ponto a site.</span><span class="sxs-lookup"><span data-stu-id="455ea-115">The New-AzP2sVpnGateway cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="455ea-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="455ea-116">PARAMETERS</span></span>

### <span data-ttu-id="455ea-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="455ea-117">-AsJob</span></span>
<span data-ttu-id="455ea-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="455ea-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-119">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="455ea-119">-CustomDnsServer</span></span>
<span data-ttu-id="455ea-120">A lista de Servidores DNS Personalizados.</span><span class="sxs-lookup"><span data-stu-id="455ea-120">The list of Custom Dns Servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="455ea-121">-DefaultProfile</span></span>
<span data-ttu-id="455ea-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="455ea-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="455ea-123">-Name</span></span>
<span data-ttu-id="455ea-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="455ea-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="455ea-125">-ResourceGroupName</span></span>
<span data-ttu-id="455ea-126">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="455ea-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="455ea-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="455ea-128">Habilitar o sinalizador de segurança da Internet para as conexões P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="455ea-128">Enable internet security flag for this P2SVpnGateway connections</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-129">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="455ea-129">-RoutingConfiguration</span></span>
<span data-ttu-id="455ea-130">Configuração de roteamento para esta conexão</span><span class="sxs-lookup"><span data-stu-id="455ea-130">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="455ea-131">-Tag</span></span>
<span data-ttu-id="455ea-132">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="455ea-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="455ea-133">-VirtualHub</span></span>
<span data-ttu-id="455ea-134">O VirtualHub com o P2SVpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="455ea-134">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-135">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="455ea-135">-VirtualHubId</span></span>
<span data-ttu-id="455ea-136">A ID do VirtualHub a que este P2SVpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="455ea-136">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-137">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="455ea-137">-VirtualHubName</span></span>
<span data-ttu-id="455ea-138">A ID do VirtualHub a que este P2SVpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="455ea-138">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-139">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="455ea-139">-VpnClientAddressPool</span></span>
<span data-ttu-id="455ea-140">P2S VpnClient AddressPool para este P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="455ea-140">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-141">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="455ea-141">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="455ea-142">A unidade de escala deste P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="455ea-142">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-143">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="455ea-143">-VpnServerConfiguration</span></span>
<span data-ttu-id="455ea-144">O VpnServerConfiguration a ser anexado a este P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="455ea-144">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-145">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="455ea-145">-VpnServerConfigurationId</span></span>
<span data-ttu-id="455ea-146">A id do objeto de configuração do servidor Vpn ao que o P2SVpnGateway será anexado.</span><span class="sxs-lookup"><span data-stu-id="455ea-146">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-147">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="455ea-147">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="455ea-148">Sinalizar para habilitar a Internet de Preferências de Roteamento neste P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="455ea-148">Flag to enable Routing Preference Internet on this P2SVpnGateway.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-149">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="455ea-149">-Confirm</span></span>
<span data-ttu-id="455ea-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="455ea-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="455ea-151">-WhatIf</span></span>
<span data-ttu-id="455ea-152">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="455ea-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="455ea-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="455ea-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455ea-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="455ea-154">CommonParameters</span></span>
<span data-ttu-id="455ea-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="455ea-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="455ea-156">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="455ea-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="455ea-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="455ea-157">INPUTS</span></span>

### <span data-ttu-id="455ea-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="455ea-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="455ea-159">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="455ea-159">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="455ea-160">Saídas</span><span class="sxs-lookup"><span data-stu-id="455ea-160">OUTPUTS</span></span>

### <span data-ttu-id="455ea-161">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="455ea-161">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
## <span data-ttu-id="455ea-162">Notas</span><span class="sxs-lookup"><span data-stu-id="455ea-162">NOTES</span></span>

## <span data-ttu-id="455ea-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="455ea-163">RELATED LINKS</span></span>

[<span data-ttu-id="455ea-164">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="455ea-164">New-AzRoutingConfiguration</span></span>]()

