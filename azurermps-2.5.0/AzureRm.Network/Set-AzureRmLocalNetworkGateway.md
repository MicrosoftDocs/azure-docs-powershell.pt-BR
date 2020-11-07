---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f01fd5c1c6694c8d16ab34e6aad9f6a52463c726
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786263"
---
# <span data-ttu-id="86ced-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86ced-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="86ced-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86ced-102">SYNOPSIS</span></span>
<span data-ttu-id="86ced-103">Modifica um gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="86ced-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86ced-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86ced-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86ced-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86ced-105">DESCRIPTION</span></span>
<span data-ttu-id="86ced-106">O cmdlet **set-AzureRmLocalNetworkGateway** modifica um gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="86ced-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="86ced-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86ced-107">EXAMPLES</span></span>

### <span data-ttu-id="86ced-108">1:</span><span class="sxs-lookup"><span data-stu-id="86ced-108">1:</span></span>
```

```

## <span data-ttu-id="86ced-109">OS</span><span class="sxs-lookup"><span data-stu-id="86ced-109">PARAMETERS</span></span>

### <span data-ttu-id="86ced-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="86ced-110">-AddressPrefix</span></span>
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

### <span data-ttu-id="86ced-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86ced-111">-AsJob</span></span>
<span data-ttu-id="86ced-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="86ced-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86ced-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="86ced-113">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ced-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="86ced-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="86ced-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ced-115">-DefaultProfile</span></span>
<span data-ttu-id="86ced-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86ced-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ced-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86ced-117">-LocalNetworkGateway</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86ced-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="86ced-118">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ced-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ced-119">CommonParameters</span></span>
<span data-ttu-id="86ced-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ced-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ced-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ced-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ced-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86ced-122">INPUTS</span></span>

### <span data-ttu-id="86ced-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86ced-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="86ced-124">O parâmetro ' LocalNetworkGateway ' aceita o valor do tipo ' PSLocalNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="86ced-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="86ced-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86ced-125">OUTPUTS</span></span>

### <span data-ttu-id="86ced-126">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86ced-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="86ced-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86ced-127">NOTES</span></span>

## <span data-ttu-id="86ced-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86ced-128">RELATED LINKS</span></span>

[<span data-ttu-id="86ced-129">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86ced-129">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="86ced-130">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86ced-130">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="86ced-131">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86ced-131">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


