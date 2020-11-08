---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 516cd38257a8742f1bc23b3207b7e3c982d9eb36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114814"
---
# <span data-ttu-id="319e0-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="319e0-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="319e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="319e0-102">SYNOPSIS</span></span>
<span data-ttu-id="319e0-103">Crie um novo P2SVpnGateway em VirtualHub para obter a conectividade do site.</span><span class="sxs-lookup"><span data-stu-id="319e0-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="319e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="319e0-104">SYNTAX</span></span>

### <span data-ttu-id="319e0-105">ByVirtualHubNameByVpnServerConfigurationObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="319e0-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="319e0-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="319e0-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="319e0-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="319e0-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="319e0-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="319e0-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="319e0-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="319e0-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="319e0-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="319e0-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="319e0-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="319e0-111">DESCRIPTION</span></span>
<span data-ttu-id="319e0-112">O cmdlet **New-AzP2sVpnGateway** permite que você crie um novo P2SVpnGateway em VirtualHub para obter a conectividade do ponto para o site do Point para os clientes do site para o Azure VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="319e0-112">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="319e0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="319e0-113">EXAMPLES</span></span>

### <span data-ttu-id="319e0-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="319e0-114">Example 1</span></span>
```powershell
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1 -EnableInternetSecurityFlag

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

<span data-ttu-id="319e0-115">O cmdlet **New-AzP2sVpnGateway** permite que você crie um novo P2SVpnGateway em VirtualHub para obter a conectividade do ponto para o site.</span><span class="sxs-lookup"><span data-stu-id="319e0-115">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="319e0-116">OS</span><span class="sxs-lookup"><span data-stu-id="319e0-116">PARAMETERS</span></span>

### <span data-ttu-id="319e0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="319e0-117">-AsJob</span></span>
<span data-ttu-id="319e0-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="319e0-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="319e0-119">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="319e0-119">-CustomDnsServer</span></span>
<span data-ttu-id="319e0-120">A lista de servidores DNS personalizados.</span><span class="sxs-lookup"><span data-stu-id="319e0-120">The list of Custom Dns Servers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319e0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="319e0-121">-DefaultProfile</span></span>
<span data-ttu-id="319e0-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="319e0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="319e0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="319e0-123">-Name</span></span>
<span data-ttu-id="319e0-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="319e0-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319e0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="319e0-125">-ResourceGroupName</span></span>
<span data-ttu-id="319e0-126">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="319e0-126">The resource name.</span></span>

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

### <span data-ttu-id="319e0-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="319e0-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="319e0-128">Habilitar o sinalizador de segurança da Internet para esta P2SVpnGateway conexões</span><span class="sxs-lookup"><span data-stu-id="319e0-128">Enable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="319e0-129">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="319e0-129">-RoutingConfiguration</span></span>
<span data-ttu-id="319e0-130">Configuração de roteamento para esta conexão</span><span class="sxs-lookup"><span data-stu-id="319e0-130">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="319e0-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="319e0-131">-Tag</span></span>
<span data-ttu-id="319e0-132">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="319e0-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319e0-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="319e0-133">-VirtualHub</span></span>
<span data-ttu-id="319e0-134">O VirtualHub para o qual este P2SVpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="319e0-134">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="319e0-135">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="319e0-135">-VirtualHubId</span></span>
<span data-ttu-id="319e0-136">A ID do VirtualHub para o qual este P2SVpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="319e0-136">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319e0-137">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="319e0-137">-VirtualHubName</span></span>
<span data-ttu-id="319e0-138">A ID do VirtualHub para o qual este P2SVpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="319e0-138">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319e0-139">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="319e0-139">-VpnClientAddressPool</span></span>
<span data-ttu-id="319e0-140">P2S VpnClient AddressPool para este P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="319e0-140">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

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

### <span data-ttu-id="319e0-141">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="319e0-141">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="319e0-142">A unidade de escala para este P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="319e0-142">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319e0-143">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="319e0-143">-VpnServerConfiguration</span></span>
<span data-ttu-id="319e0-144">O VpnServerConfiguration a ser anexado a este P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="319e0-144">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="319e0-145">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="319e0-145">-VpnServerConfigurationId</span></span>
<span data-ttu-id="319e0-146">A ID do objeto de configuração do servidor VPN a qual esta P2SVpnGateway será anexada.</span><span class="sxs-lookup"><span data-stu-id="319e0-146">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319e0-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="319e0-147">-Confirm</span></span>
<span data-ttu-id="319e0-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="319e0-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="319e0-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="319e0-149">-WhatIf</span></span>
<span data-ttu-id="319e0-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="319e0-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="319e0-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="319e0-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="319e0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="319e0-152">CommonParameters</span></span>
<span data-ttu-id="319e0-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="319e0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="319e0-154">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="319e0-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="319e0-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="319e0-155">INPUTS</span></span>

### <span data-ttu-id="319e0-156">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="319e0-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="319e0-157">System. String Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="319e0-157">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="319e0-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="319e0-158">OUTPUTS</span></span>

### <span data-ttu-id="319e0-159">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="319e0-159">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="319e0-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="319e0-160">NOTES</span></span>

## <span data-ttu-id="319e0-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="319e0-161">RELATED LINKS</span></span>

[<span data-ttu-id="319e0-162">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="319e0-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
