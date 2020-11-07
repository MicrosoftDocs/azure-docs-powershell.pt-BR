---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: 4c196fd8c18ff14c2d1da295b8a3ecc949734783
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771438"
---
# <span data-ttu-id="e25f9-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e25f9-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="e25f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e25f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e25f9-103">Modifica um gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="e25f9-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="e25f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e25f9-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway> [-AddressPrefix <String[]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e25f9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e25f9-105">DESCRIPTION</span></span>
<span data-ttu-id="e25f9-106">O cmdlet **set-AzLocalNetworkGateway** modifica um gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="e25f9-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="e25f9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e25f9-107">EXAMPLES</span></span>

### <span data-ttu-id="e25f9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e25f9-108">Example 1</span></span>
<span data-ttu-id="e25f9-109">Definir a configuração de um gateway existente</span><span class="sxs-lookup"><span data-stu-id="e25f9-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzLocalNetworkGateway -LocalNetworkGateway $lgw

Name                     : myLocalGW
ResourceGroupName        : TestRG1
Location                 : westus
Id                       : /subscriptions/81ab786c-56eb-4a4d-bb5f-f60329772466/resourceGroups/TestRG1/providers/Microso
                           ft.Network/localNetworkGateways/myLocalGW
Etag                     : W/"d2de6968-315e-411d-a4b8-a8c335abe61b"
ResourceGuid             : 393acf8b-dbb8-4b08-a9ea-c714570710e1
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : 1.2.3.4
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

## <span data-ttu-id="e25f9-110">OS</span><span class="sxs-lookup"><span data-stu-id="e25f9-110">PARAMETERS</span></span>

### <span data-ttu-id="e25f9-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e25f9-111">-AddressPrefix</span></span>
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

### <span data-ttu-id="e25f9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e25f9-112">-AsJob</span></span>
<span data-ttu-id="e25f9-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e25f9-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e25f9-114">-ASN</span><span class="sxs-lookup"><span data-stu-id="e25f9-114">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e25f9-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="e25f9-115">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e25f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25f9-116">-DefaultProfile</span></span>
<span data-ttu-id="e25f9-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e25f9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e25f9-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e25f9-118">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e25f9-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="e25f9-119">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e25f9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25f9-120">CommonParameters</span></span>
<span data-ttu-id="e25f9-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e25f9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25f9-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e25f9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25f9-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e25f9-123">INPUTS</span></span>

### <span data-ttu-id="e25f9-124">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e25f9-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="e25f9-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="e25f9-125">System.String[]</span></span>

### <span data-ttu-id="e25f9-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="e25f9-126">System.UInt32</span></span>

### <span data-ttu-id="e25f9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e25f9-127">System.String</span></span>

### <span data-ttu-id="e25f9-128">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e25f9-128">System.Int32</span></span>

## <span data-ttu-id="e25f9-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e25f9-129">OUTPUTS</span></span>

### <span data-ttu-id="e25f9-130">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e25f9-130">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="e25f9-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e25f9-131">NOTES</span></span>

## <span data-ttu-id="e25f9-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e25f9-132">RELATED LINKS</span></span>

[<span data-ttu-id="e25f9-133">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e25f9-133">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="e25f9-134">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e25f9-134">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="e25f9-135">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e25f9-135">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)
