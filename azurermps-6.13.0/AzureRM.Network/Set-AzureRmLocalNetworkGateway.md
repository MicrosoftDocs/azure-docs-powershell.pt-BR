---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: a37cb732aed95a2c31c970d83558a3eff8ab31c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426330"
---
# <span data-ttu-id="79de3-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79de3-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="79de3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79de3-102">SYNOPSIS</span></span>
<span data-ttu-id="79de3-103">Modifica um gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="79de3-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79de3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79de3-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79de3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79de3-105">DESCRIPTION</span></span>
<span data-ttu-id="79de3-106">O cmdlet **set-AzureRmLocalNetworkGateway** modifica um gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="79de3-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="79de3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79de3-107">EXAMPLES</span></span>

### <span data-ttu-id="79de3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="79de3-108">Example 1</span></span>
<span data-ttu-id="79de3-109">Definir a configuração de um gateway existente</span><span class="sxs-lookup"><span data-stu-id="79de3-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway $lgw

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

## <span data-ttu-id="79de3-110">OS</span><span class="sxs-lookup"><span data-stu-id="79de3-110">PARAMETERS</span></span>

### <span data-ttu-id="79de3-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="79de3-111">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79de3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79de3-112">-AsJob</span></span>
<span data-ttu-id="79de3-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="79de3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79de3-114">-ASN</span><span class="sxs-lookup"><span data-stu-id="79de3-114">-Asn</span></span>
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

### <span data-ttu-id="79de3-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="79de3-115">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="79de3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79de3-116">-DefaultProfile</span></span>
<span data-ttu-id="79de3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79de3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79de3-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79de3-118">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="79de3-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="79de3-119">-PeerWeight</span></span>
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

### <span data-ttu-id="79de3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79de3-120">CommonParameters</span></span>
<span data-ttu-id="79de3-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79de3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79de3-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79de3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79de3-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79de3-123">INPUTS</span></span>

### <span data-ttu-id="79de3-124">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79de3-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>
<span data-ttu-id="79de3-125">Parâmetros: LocalNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79de3-125">Parameters: LocalNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="79de3-126">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="79de3-126">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="79de3-127">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="79de3-127">System.UInt32</span></span>

### <span data-ttu-id="79de3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="79de3-128">System.String</span></span>

### <span data-ttu-id="79de3-129">System. Int32</span><span class="sxs-lookup"><span data-stu-id="79de3-129">System.Int32</span></span>

## <span data-ttu-id="79de3-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79de3-130">OUTPUTS</span></span>

### <span data-ttu-id="79de3-131">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79de3-131">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="79de3-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79de3-132">NOTES</span></span>

## <span data-ttu-id="79de3-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79de3-133">RELATED LINKS</span></span>

[<span data-ttu-id="79de3-134">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79de3-134">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="79de3-135">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79de3-135">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="79de3-136">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79de3-136">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


