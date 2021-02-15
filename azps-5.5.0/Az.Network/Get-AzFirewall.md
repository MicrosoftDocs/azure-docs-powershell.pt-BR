---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: 71fff2d475c5cf3045be8aa4c628776b0dd42dc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115187"
---
# <span data-ttu-id="22663-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="22663-101">Get-AzFirewall</span></span>

## <span data-ttu-id="22663-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22663-102">SYNOPSIS</span></span>
<span data-ttu-id="22663-103">Obtém um Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="22663-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="22663-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22663-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22663-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="22663-105">DESCRIPTION</span></span>
<span data-ttu-id="22663-106">O **cmdlet Get-AzFirewall** obtém um ou mais Firewalls em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22663-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="22663-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="22663-107">EXAMPLES</span></span>

### <span data-ttu-id="22663-108">1: Recuperar todos os Firewalls em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="22663-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzFirewall -ResourceGroupName rgName

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="22663-109">Este exemplo recupera todos os Firewalls no grupo de recursos "rgName".</span><span class="sxs-lookup"><span data-stu-id="22663-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="22663-110">2: Recuperar um Firewall por nome</span><span class="sxs-lookup"><span data-stu-id="22663-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzFirewall -ResourceGroupName rgName -Name azFw

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="22663-111">Este exemplo recupera o Firewall chamado "azFw" no grupo de recursos "rgName".</span><span class="sxs-lookup"><span data-stu-id="22663-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="22663-112">3: Recuperar todos os Firewalls com filtragem</span><span class="sxs-lookup"><span data-stu-id="22663-112">3:  Retrieve all Firewalls with filtering</span></span>
```
Get-AzFirewall -Name azFw*

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="22663-113">Este exemplo recupera todos os Firewalls que começam com "azFw"</span><span class="sxs-lookup"><span data-stu-id="22663-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="22663-114">4: Recuperar um firewall e adicionar uma coleção de regras de aplicativo ao Firewall</span><span class="sxs-lookup"><span data-stu-id="22663-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="22663-115">Este exemplo recupera um firewall e adiciona uma coleção de regras de aplicativo ao firewall por meio do método de chamada AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="22663-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="22663-116">5: Recuperar um firewall e adicionar uma coleção de regras de rede ao Firewall</span><span class="sxs-lookup"><span data-stu-id="22663-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "UDP" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="22663-117">Este exemplo recupera um firewall e adiciona uma coleção de regras de rede ao firewall por meio do método de chamada AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="22663-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="22663-118">6: Recuperar um firewall e recuperar uma coleção de regras de aplicativo por nome do Firewall</span><span class="sxs-lookup"><span data-stu-id="22663-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="22663-119">Este exemplo recupera um firewall e obtém uma coleção de regras por nome, método de chamada GetApplicationRuleCollectionByName no objeto de firewall.</span><span class="sxs-lookup"><span data-stu-id="22663-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="22663-120">O nome da coleção de regras para o método GetApplicationRuleCollectionByName não tem maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="22663-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="22663-121">7: Recuperar um firewall e recuperar uma coleção de regras de rede por nome do Firewall</span><span class="sxs-lookup"><span data-stu-id="22663-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="22663-122">Este exemplo recupera um firewall e obtém uma coleção de regras por nome, método de chamada GetNetworkRuleCollectionByName no objeto de firewall.</span><span class="sxs-lookup"><span data-stu-id="22663-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="22663-123">O nome da coleção de regras para o método GetNetworkRuleCollectionByName não tem maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="22663-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="22663-124">8: Recuperar um firewall e remover uma coleção de regras de aplicativo por nome do Firewall</span><span class="sxs-lookup"><span data-stu-id="22663-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="22663-125">Este exemplo recupera um firewall e remove um conjunto de regras por nome, método de chamada RemoveApplicationRuleCollectionByName no objeto de firewall.</span><span class="sxs-lookup"><span data-stu-id="22663-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="22663-126">O nome da coleção de regras para o método RemoveApplicationRuleCollectionByName não tem maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="22663-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="22663-127">9: Recuperar um firewall e remover uma coleção de regras de rede por nome do Firewall</span><span class="sxs-lookup"><span data-stu-id="22663-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="22663-128">Este exemplo recupera um firewall e remove uma coleção de regras por nome, método de chamada RemoveNetworkRuleCollectionByName no objeto de firewall.</span><span class="sxs-lookup"><span data-stu-id="22663-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="22663-129">O nome da coleção de regras para o método RemoveNetworkRuleCollectionByName não tem maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="22663-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="22663-130">10: Recuperar um firewall e, em seguida, atribuir o firewall</span><span class="sxs-lookup"><span data-stu-id="22663-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="22663-131">Este exemplo recupera um firewall e chamadas Alocar no firewall para iniciar o serviço de firewall usando a configuração (coleções de regras de rede e aplicativo) associadas ao firewall.</span><span class="sxs-lookup"><span data-stu-id="22663-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="22663-132">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22663-132">PARAMETERS</span></span>

### <span data-ttu-id="22663-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22663-133">-DefaultProfile</span></span>
<span data-ttu-id="22663-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="22663-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22663-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="22663-135">-Name</span></span>
<span data-ttu-id="22663-136">Especifica o nome do Firewall que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="22663-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22663-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22663-137">-ResourceGroupName</span></span>
<span data-ttu-id="22663-138">Especifica o nome do grupo de recursos ao que o Firewall pertence.</span><span class="sxs-lookup"><span data-stu-id="22663-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22663-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22663-139">CommonParameters</span></span>
<span data-ttu-id="22663-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22663-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22663-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22663-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22663-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="22663-142">INPUTS</span></span>

### <span data-ttu-id="22663-143">System.String</span><span class="sxs-lookup"><span data-stu-id="22663-143">System.String</span></span>

## <span data-ttu-id="22663-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="22663-144">OUTPUTS</span></span>

### <span data-ttu-id="22663-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="22663-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="22663-146">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="22663-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="22663-147">Notas</span><span class="sxs-lookup"><span data-stu-id="22663-147">NOTES</span></span>

## <span data-ttu-id="22663-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22663-148">RELATED LINKS</span></span>

[<span data-ttu-id="22663-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="22663-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="22663-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="22663-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="22663-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="22663-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
