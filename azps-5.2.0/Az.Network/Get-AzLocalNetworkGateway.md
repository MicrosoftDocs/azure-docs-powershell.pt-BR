---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 14c0ec31f10a6405fb2a3f412f004d53dbdeb9a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262066"
---
# <span data-ttu-id="9e17f-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e17f-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="9e17f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e17f-102">SYNOPSIS</span></span>
<span data-ttu-id="9e17f-103">Obtém um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="9e17f-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="9e17f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e17f-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e17f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e17f-105">DESCRIPTION</span></span>
<span data-ttu-id="9e17f-106">O gateway de rede local é o objeto que representa o seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="9e17f-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="9e17f-107">O cmdlet **Get-AzLocalNetworkGateway** retorna o objeto que representa o gateway local com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9e17f-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="9e17f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e17f-108">EXAMPLES</span></span>

### <span data-ttu-id="9e17f-109">Exemplo 1: obter um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="9e17f-109">Example 1: Get a Local Network Gateway</span></span>
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="9e17f-110">Retorna o objeto do gateway de rede local com o nome "myLocalGW1" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="9e17f-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="9e17f-111">Exemplo 2: obter gateways de rede locais usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="9e17f-111">Example 2: Get Local Network Gateways using filtering</span></span>
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="9e17f-112">Retorna o objeto do gateway de rede local com o nome que começa com "myLocalGW" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="9e17f-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="9e17f-113">OS</span><span class="sxs-lookup"><span data-stu-id="9e17f-113">PARAMETERS</span></span>

### <span data-ttu-id="9e17f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e17f-114">-DefaultProfile</span></span>
<span data-ttu-id="9e17f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e17f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e17f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e17f-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9e17f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e17f-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9e17f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e17f-118">CommonParameters</span></span>
<span data-ttu-id="9e17f-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e17f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e17f-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e17f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e17f-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e17f-121">INPUTS</span></span>

### <span data-ttu-id="9e17f-122">System. String</span><span class="sxs-lookup"><span data-stu-id="9e17f-122">System.String</span></span>

## <span data-ttu-id="9e17f-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e17f-123">OUTPUTS</span></span>

### <span data-ttu-id="9e17f-124">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e17f-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="9e17f-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e17f-125">NOTES</span></span>

## <span data-ttu-id="9e17f-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e17f-126">RELATED LINKS</span></span>

[<span data-ttu-id="9e17f-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e17f-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="9e17f-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e17f-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="9e17f-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e17f-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
