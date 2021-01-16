---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
ms.openlocfilehash: 682f6bdb8eb0ce80d4b81dc12b9ed8d09de4713a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261179"
---
# <span data-ttu-id="a540d-101">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a540d-101">Update-AzP2sVpnGateway</span></span>

## <span data-ttu-id="a540d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a540d-102">SYNOPSIS</span></span>
<span data-ttu-id="a540d-103">Atualize um P2SVpnGateway existente em VirtualHub para conectividade com o ponto para o site.</span><span class="sxs-lookup"><span data-stu-id="a540d-103">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="a540d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a540d-104">SYNTAX</span></span>

### <span data-ttu-id="a540d-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (padrão)</span><span class="sxs-lookup"><span data-stu-id="a540d-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Default)</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a540d-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="a540d-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a540d-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a540d-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a540d-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="a540d-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a540d-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="a540d-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>]
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a540d-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a540d-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a540d-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="a540d-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a540d-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="a540d-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a540d-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a540d-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a540d-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a540d-114">DESCRIPTION</span></span>
<span data-ttu-id="a540d-115">O cmdlet **Update-AzP2sVpnGateway** permite que você atualize um P2SVpnGateway existente em VirtualHub com novos VpnClientAddressPool ou novo VpnServerConfiguration ou alterar VpnGatewayScaleUnit.</span><span class="sxs-lookup"><span data-stu-id="a540d-115">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool or new VpnServerConfiguration or change of VpnGatewayScaleUnit.</span></span>

## <span data-ttu-id="a540d-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a540d-116">EXAMPLES</span></span>

### <span data-ttu-id="a540d-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a540d-117">Example 1</span></span>
```powershell
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1 
PS C:\> $vpnClientAddressSpaces[0] = "101.10.0.0/16"
PS C:\> Update-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VpnClientAddressPool $vpnClientAddressSpaces -EnableInternetSecurityFlag                                

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/NilamdWestUsVirtualH
                                 ub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/NilamdWe
                                 stUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "101.10.0.0/16"
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
                                     "Etag": "W/\"d7debc2f-ccbb-4f00-bddc-42c99b52fda3\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="a540d-118">O cmdlet **Update-AzP2sVpnGateway** permite que você atualize um P2SVpnGateway existente em VirtualHub com novo VpnClientAddressPool.</span><span class="sxs-lookup"><span data-stu-id="a540d-118">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool.</span></span> <span data-ttu-id="a540d-119">Quando o ponto para o cliente do site se conecta a este P2SVpnGateway, um dos endereços IP desse VpnClientAddressPool é atribuído a esse cliente.</span><span class="sxs-lookup"><span data-stu-id="a540d-119">When Point to site client connects with this P2SVpnGateway, one of the ip address from this VpnClientAddressPool gets allocated to that client.</span></span>

### <span data-ttu-id="a540d-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a540d-120">Example 2</span></span>

<span data-ttu-id="a540d-121">Atualize um P2SVpnGateway existente em VirtualHub para conectividade com o ponto para o site.</span><span class="sxs-lookup"><span data-stu-id="a540d-121">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span> <span data-ttu-id="a540d-122">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="a540d-122">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzP2sVpnGateway -AsJob -Name 00000000-0000-0000-0000-00000000000000000-westus-gw -ResourceGroupName P2SCortexGATesting -VpnClientAddressPool <String[]> -VpnGatewayScaleUnit 1 -VpnServerConfiguration <PSVpnServerConfiguration>
```

## <span data-ttu-id="a540d-123">OS</span><span class="sxs-lookup"><span data-stu-id="a540d-123">PARAMETERS</span></span>

### <span data-ttu-id="a540d-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a540d-124">-AsJob</span></span>
<span data-ttu-id="a540d-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a540d-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a540d-126">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="a540d-126">-CustomDnsServer</span></span>
<span data-ttu-id="a540d-127">A lista de servidores DNS personalizados.</span><span class="sxs-lookup"><span data-stu-id="a540d-127">The list of Custom Dns Servers.</span></span>

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

### <span data-ttu-id="a540d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a540d-128">-DefaultProfile</span></span>
<span data-ttu-id="a540d-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a540d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a540d-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a540d-130">-InputObject</span></span>
<span data-ttu-id="a540d-131">O objeto de gateway de VPN P2s a ser modificado</span><span class="sxs-lookup"><span data-stu-id="a540d-131">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a540d-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="a540d-132">-Name</span></span>
<span data-ttu-id="a540d-133">O nome do gateway de VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="a540d-133">The P2S vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases: ResourceName, P2SVpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a540d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a540d-134">-ResourceGroupName</span></span>
<span data-ttu-id="a540d-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a540d-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a540d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a540d-136">-ResourceId</span></span>
<span data-ttu-id="a540d-137">A ID de recurso do Azure do P2SVpnGateway a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="a540d-137">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a540d-138">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="a540d-138">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="a540d-139">Habilitar o sinalizador de segurança da Internet para esta P2SVpnGateway conexões</span><span class="sxs-lookup"><span data-stu-id="a540d-139">Enable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="a540d-140">-DisableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="a540d-140">-DisableInternetSecurityFlag</span></span>
<span data-ttu-id="a540d-141">Desabilitar o sinalizador de segurança da Internet para esta P2SVpnGateway conexões</span><span class="sxs-lookup"><span data-stu-id="a540d-141">Disable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="a540d-142">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a540d-142">-RoutingConfiguration</span></span>
<span data-ttu-id="a540d-143">Configuração de roteamento para esta conexão</span><span class="sxs-lookup"><span data-stu-id="a540d-143">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="a540d-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="a540d-144">-Tag</span></span>
<span data-ttu-id="a540d-145">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="a540d-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a540d-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="a540d-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="a540d-147">P2S VpnClient AddressPool para este P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a540d-147">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

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

### <span data-ttu-id="a540d-148">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a540d-148">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="a540d-149">A unidade de escala para este P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a540d-149">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a540d-150">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a540d-150">-VpnServerConfiguration</span></span>
<span data-ttu-id="a540d-151">O VpnServerConfiguration a ser anexado a este P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a540d-151">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a540d-152">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a540d-152">-VpnServerConfigurationId</span></span>
<span data-ttu-id="a540d-153">A ID do objeto de configuração do servidor VPN a qual esta P2SVpnGateway será anexada.</span><span class="sxs-lookup"><span data-stu-id="a540d-153">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationResourceId, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a540d-154">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a540d-154">-Confirm</span></span>
<span data-ttu-id="a540d-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a540d-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a540d-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a540d-156">-WhatIf</span></span>
<span data-ttu-id="a540d-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a540d-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a540d-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a540d-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a540d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a540d-159">CommonParameters</span></span>
<span data-ttu-id="a540d-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a540d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a540d-161">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a540d-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a540d-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a540d-162">INPUTS</span></span>

### <span data-ttu-id="a540d-163">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a540d-163">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="a540d-164">System. String Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a540d-164">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="a540d-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a540d-165">OUTPUTS</span></span>

### <span data-ttu-id="a540d-166">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a540d-166">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="a540d-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a540d-167">NOTES</span></span>

## <span data-ttu-id="a540d-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a540d-168">RELATED LINKS</span></span>

[<span data-ttu-id="a540d-169">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a540d-169">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
