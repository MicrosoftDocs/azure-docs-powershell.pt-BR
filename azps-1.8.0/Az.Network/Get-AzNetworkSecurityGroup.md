---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: 46106379160ee593748a95489c2641d43114d863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600537"
---
# <span data-ttu-id="e4938-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e4938-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="e4938-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4938-102">SYNOPSIS</span></span>
<span data-ttu-id="e4938-103">Obtém um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="e4938-103">Gets a network security group.</span></span>

## <span data-ttu-id="e4938-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4938-104">SYNTAX</span></span>

### <span data-ttu-id="e4938-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="e4938-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4938-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="e4938-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4938-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4938-107">DESCRIPTION</span></span>
<span data-ttu-id="e4938-108">O cmdlet **Get-AzNetworkSecurityGroup** Obtém um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4938-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="e4938-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4938-109">EXAMPLES</span></span>

### <span data-ttu-id="e4938-110">1: recuperar um grupo de segurança de rede existente</span><span class="sxs-lookup"><span data-stu-id="e4938-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName "rg1"

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="e4938-111">Esse comando retorna o conteúdo do grupo de segurança de rede do Azure "nsg1" no grupo de recursos "Rg1"</span><span class="sxs-lookup"><span data-stu-id="e4938-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="e4938-112">2: listar grupos de segurança de rede existentes usando filtragem</span><span class="sxs-lookup"><span data-stu-id="e4938-112">2: List existing network security groups using filtering</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg*

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="e4938-113">Esse comando retorna o conteúdo dos grupos de segurança de rede do Azure que começam com "NSG"</span><span class="sxs-lookup"><span data-stu-id="e4938-113">This command returns contents of Azure network security groups that start with "nsg"</span></span>

## <span data-ttu-id="e4938-114">OS</span><span class="sxs-lookup"><span data-stu-id="e4938-114">PARAMETERS</span></span>

### <span data-ttu-id="e4938-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4938-115">-DefaultProfile</span></span>
<span data-ttu-id="e4938-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4938-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4938-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="e4938-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4938-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4938-118">-Name</span></span>
<span data-ttu-id="e4938-119">Especifica o nome do grupo de segurança de rede que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e4938-119">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e4938-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4938-120">-ResourceGroupName</span></span>
<span data-ttu-id="e4938-121">Especifica o nome do grupo de recursos ao qual o grupo de segurança de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="e4938-121">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e4938-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4938-122">CommonParameters</span></span>
<span data-ttu-id="e4938-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4938-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4938-124">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4938-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4938-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4938-125">INPUTS</span></span>

### <span data-ttu-id="e4938-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e4938-126">System.String</span></span>

## <span data-ttu-id="e4938-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4938-127">OUTPUTS</span></span>

### <span data-ttu-id="e4938-128">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e4938-128">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e4938-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4938-129">NOTES</span></span>

## <span data-ttu-id="e4938-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4938-130">RELATED LINKS</span></span>

[<span data-ttu-id="e4938-131">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e4938-131">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e4938-132">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e4938-132">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e4938-133">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e4938-133">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


