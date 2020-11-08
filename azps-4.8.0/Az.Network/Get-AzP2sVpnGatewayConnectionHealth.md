---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111062"
---
# <span data-ttu-id="7ee28-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7ee28-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="7ee28-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ee28-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee28-103">Obtém o ponto de aggregared atual para informações de integridade de conexões de site do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7ee28-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="7ee28-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ee28-104">SYNTAX</span></span>

### <span data-ttu-id="7ee28-105">ByP2SVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7ee28-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ee28-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7ee28-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ee28-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7ee28-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ee28-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ee28-108">DESCRIPTION</span></span>
<span data-ttu-id="7ee28-109">O cmdlet **Get-AzP2sVpnGatewayConnectionHealth** permite que você obtenha a integridade agregada atual do Point para o site Connections do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7ee28-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="7ee28-110">A integridade agregada mostra o número de pontos do ponto para os clientes do site conectados ao P2SVpnGateway, o total de entrada de entrada e de saída transferida por meio do P2SVpnGateway e os endereços IP atribuídos para o ponto conectado para clientes do site.</span><span class="sxs-lookup"><span data-stu-id="7ee28-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="7ee28-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ee28-111">EXAMPLES</span></span>

### <span data-ttu-id="7ee28-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ee28-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayConnectionHealth -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : { 
                  "VpnClientConnectionsCount": 2,
                      "AllocatedIpAddresses": { "192.168.2.1", "192.168.2.2" },
                      "TotalIngressBytesTransferred": 100,
                      "TotalEgressBytesTransferred": 200
                 }
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
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="7ee28-113">O cmdlet **Get-AzP2sVpnGatewayConnectionHealth** permite que você obtenha a integridade agregada atual do Point para o site Connections do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7ee28-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="7ee28-114">Comando acima deixe a integridade da saída mostrar que o número de pontos para clientes do site conectados ao P2SVpnGateway é 2.</span><span class="sxs-lookup"><span data-stu-id="7ee28-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="7ee28-115">Total de bytes de entrada e saída transferidas por meio do P2SVpnGateway são 100 e 200 respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7ee28-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="7ee28-116">Os endereços IP atribuídos para o ponto conectado para clientes do site são "192.168.2.1", "192.168.2.2".</span><span class="sxs-lookup"><span data-stu-id="7ee28-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="7ee28-117">OS</span><span class="sxs-lookup"><span data-stu-id="7ee28-117">PARAMETERS</span></span>

### <span data-ttu-id="7ee28-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee28-118">-DefaultProfile</span></span>
<span data-ttu-id="7ee28-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ee28-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ee28-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ee28-120">-InputObject</span></span>
<span data-ttu-id="7ee28-121">O objeto de gateway de VPN P2s a ser modificado</span><span class="sxs-lookup"><span data-stu-id="7ee28-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee28-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ee28-122">-Name</span></span>
<span data-ttu-id="7ee28-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="7ee28-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee28-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee28-124">-ResourceGroupName</span></span>
<span data-ttu-id="7ee28-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ee28-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee28-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ee28-126">-ResourceId</span></span>
<span data-ttu-id="7ee28-127">A ID de recurso do Azure do P2SVpnGateway a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="7ee28-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee28-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee28-128">CommonParameters</span></span>
<span data-ttu-id="7ee28-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ee28-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee28-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ee28-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee28-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ee28-131">INPUTS</span></span>

### <span data-ttu-id="7ee28-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7ee28-132">System.String</span></span>
<span data-ttu-id="7ee28-133">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7ee28-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="7ee28-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ee28-134">OUTPUTS</span></span>

### <span data-ttu-id="7ee28-135">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7ee28-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="7ee28-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ee28-136">NOTES</span></span>

## <span data-ttu-id="7ee28-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ee28-137">RELATED LINKS</span></span>
