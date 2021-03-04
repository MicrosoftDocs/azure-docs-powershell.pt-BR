---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 961edb46c71b60f0c3c43523d8d88486f1414d3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892452"
---
# <span data-ttu-id="c9e68-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c9e68-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="c9e68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9e68-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e68-103">Obtém um Gateway de Rede Local</span><span class="sxs-lookup"><span data-stu-id="c9e68-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="c9e68-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c9e68-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9e68-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c9e68-105">DESCRIPTION</span></span>
<span data-ttu-id="c9e68-106">O Gateway de Rede Local é o objeto que representa seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="c9e68-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="c9e68-107">O cmdlet **Get-AzLocalNetworkGateway** retorna o objeto que representa seu gateway local com base em Nome e Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="c9e68-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="c9e68-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9e68-108">EXAMPLES</span></span>

### <span data-ttu-id="c9e68-109">Exemplo 1: Obter um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="c9e68-109">Example 1: Get a Local Network Gateway</span></span>
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

<span data-ttu-id="c9e68-110">Retorna o objeto do Gateway de Rede Local com o nome "myLocalGW1" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="c9e68-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="c9e68-111">Exemplo 2: Obter gateways de rede locais usando filtragem</span><span class="sxs-lookup"><span data-stu-id="c9e68-111">Example 2: Get Local Network Gateways using filtering</span></span>
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

<span data-ttu-id="c9e68-112">Retorna o objeto do Gateway de Rede Local com nome começando com "myLocalGW" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="c9e68-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="c9e68-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c9e68-113">PARAMETERS</span></span>

### <span data-ttu-id="c9e68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e68-114">-DefaultProfile</span></span>
<span data-ttu-id="c9e68-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c9e68-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9e68-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c9e68-116">-Name</span></span>
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

### <span data-ttu-id="c9e68-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9e68-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c9e68-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e68-118">CommonParameters</span></span>
<span data-ttu-id="c9e68-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9e68-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e68-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9e68-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e68-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9e68-121">INPUTS</span></span>

### <span data-ttu-id="c9e68-122">System.String</span><span class="sxs-lookup"><span data-stu-id="c9e68-122">System.String</span></span>

## <span data-ttu-id="c9e68-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c9e68-123">OUTPUTS</span></span>

### <span data-ttu-id="c9e68-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c9e68-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="c9e68-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="c9e68-125">NOTES</span></span>

## <span data-ttu-id="c9e68-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9e68-126">RELATED LINKS</span></span>

[<span data-ttu-id="c9e68-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c9e68-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="c9e68-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c9e68-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="c9e68-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c9e68-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
