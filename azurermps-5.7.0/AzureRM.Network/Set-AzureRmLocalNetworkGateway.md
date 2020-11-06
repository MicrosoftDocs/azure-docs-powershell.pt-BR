---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: a33fb510e351a8f1c762801947cf4bbac9a66e28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432054"
---
# <span data-ttu-id="da1a2-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da1a2-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="da1a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="da1a2-103">Modifica um gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="da1a2-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da1a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da1a2-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da1a2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da1a2-105">DESCRIPTION</span></span>
<span data-ttu-id="da1a2-106">O cmdlet **set-AzureRmLocalNetworkGateway** modifica um gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="da1a2-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="da1a2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da1a2-107">EXAMPLES</span></span>

## <span data-ttu-id="da1a2-108">OS</span><span class="sxs-lookup"><span data-stu-id="da1a2-108">PARAMETERS</span></span>

### <span data-ttu-id="da1a2-109">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="da1a2-109">-AddressPrefix</span></span>
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

### <span data-ttu-id="da1a2-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da1a2-110">-AsJob</span></span>
<span data-ttu-id="da1a2-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="da1a2-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da1a2-112">-ASN</span><span class="sxs-lookup"><span data-stu-id="da1a2-112">-Asn</span></span>
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

### <span data-ttu-id="da1a2-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="da1a2-113">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="da1a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da1a2-114">-DefaultProfile</span></span>
<span data-ttu-id="da1a2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da1a2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da1a2-116">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da1a2-116">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="da1a2-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="da1a2-117">-PeerWeight</span></span>
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

### <span data-ttu-id="da1a2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da1a2-118">CommonParameters</span></span>
<span data-ttu-id="da1a2-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da1a2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da1a2-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da1a2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da1a2-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da1a2-121">INPUTS</span></span>

### <span data-ttu-id="da1a2-122">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da1a2-122">PSLocalNetworkGateway</span></span>
<span data-ttu-id="da1a2-123">O parâmetro ' LocalNetworkGateway ' aceita o valor do tipo ' PSLocalNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="da1a2-123">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="da1a2-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da1a2-124">OUTPUTS</span></span>

### <span data-ttu-id="da1a2-125">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da1a2-125">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="da1a2-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da1a2-126">NOTES</span></span>

## <span data-ttu-id="da1a2-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da1a2-127">RELATED LINKS</span></span>

[<span data-ttu-id="da1a2-128">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da1a2-128">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="da1a2-129">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da1a2-129">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="da1a2-130">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da1a2-130">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


