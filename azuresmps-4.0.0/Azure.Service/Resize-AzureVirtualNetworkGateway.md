---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AD5F4D69-45AF-46FB-ADF0-59CEF9908EF7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d63ac418d2dcee97afef9ae5f351fb2c1eebece0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946086"
---
# <span data-ttu-id="6d3f1-101">Resize-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6d3f1-101">Resize-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="6d3f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3f1-103">Redimensiona um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6d3f1-103">Resizes a virtual network gateway.</span></span>

## <span data-ttu-id="6d3f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d3f1-104">SYNTAX</span></span>

```
Resize-AzureVirtualNetworkGateway -GatewayId <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d3f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d3f1-105">DESCRIPTION</span></span>
<span data-ttu-id="6d3f1-106">O cmdlet Resize-AzureVirtualNetworkGateway redimensiona um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6d3f1-106">The Resize-AzureVirtualNetworkGateway cmdlet resizes a virtual network gateway.</span></span>

## <span data-ttu-id="6d3f1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d3f1-107">EXAMPLES</span></span>

## <span data-ttu-id="6d3f1-108">OS</span><span class="sxs-lookup"><span data-stu-id="6d3f1-108">PARAMETERS</span></span>

### <span data-ttu-id="6d3f1-109">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="6d3f1-109">-GatewayId</span></span>
<span data-ttu-id="6d3f1-110">Especifica a ID de um gateway.</span><span class="sxs-lookup"><span data-stu-id="6d3f1-110">Specifies the ID of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3f1-111">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="6d3f1-111">-GatewaySKU</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3f1-112">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6d3f1-112">-Profile</span></span>
<span data-ttu-id="6d3f1-113">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6d3f1-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6d3f1-114">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6d3f1-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3f1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3f1-115">CommonParameters</span></span>
<span data-ttu-id="6d3f1-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d3f1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3f1-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d3f1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3f1-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d3f1-118">INPUTS</span></span>

## <span data-ttu-id="6d3f1-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d3f1-119">OUTPUTS</span></span>

## <span data-ttu-id="6d3f1-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d3f1-120">NOTES</span></span>

## <span data-ttu-id="6d3f1-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d3f1-121">RELATED LINKS</span></span>

[<span data-ttu-id="6d3f1-122">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6d3f1-122">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="6d3f1-123">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6d3f1-123">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="6d3f1-124">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6d3f1-124">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="6d3f1-125">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6d3f1-125">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)


