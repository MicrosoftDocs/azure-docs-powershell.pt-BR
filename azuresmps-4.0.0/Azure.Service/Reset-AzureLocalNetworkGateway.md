---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0E4D44EE-BF28-46FE-B2FA-D35C1651016F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3940a5e6fc69ebee02f3e0de963bc87f790f8860
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945472"
---
# <span data-ttu-id="3087c-101">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3087c-101">Reset-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="3087c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3087c-102">SYNOPSIS</span></span>
<span data-ttu-id="3087c-103">Redefine um gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="3087c-103">Resets a local network gateway.</span></span>

## <span data-ttu-id="3087c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3087c-104">SYNTAX</span></span>

```
Reset-AzureLocalNetworkGateway -GatewayId <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3087c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3087c-105">DESCRIPTION</span></span>
<span data-ttu-id="3087c-106">O cmdlet **Reset-AzureLocalNetworkGateway** redefine um gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="3087c-106">The **Reset-AzureLocalNetworkGateway** cmdlet resets a local network gateway.</span></span>

## <span data-ttu-id="3087c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3087c-107">EXAMPLES</span></span>

## <span data-ttu-id="3087c-108">OS</span><span class="sxs-lookup"><span data-stu-id="3087c-108">PARAMETERS</span></span>

### <span data-ttu-id="3087c-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="3087c-109">-AddressSpace</span></span>
<span data-ttu-id="3087c-110">Especifica o espaço de endereço.</span><span class="sxs-lookup"><span data-stu-id="3087c-110">Specifies the address space.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3087c-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="3087c-111">-Asn</span></span>
<span data-ttu-id="3087c-112">Especifica o número do sistema autônomo (ASN).</span><span class="sxs-lookup"><span data-stu-id="3087c-112">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3087c-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="3087c-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="3087c-114">Especifica o endereço de emparelhamento do BGP (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="3087c-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3087c-115">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="3087c-115">-GatewayId</span></span>
<span data-ttu-id="3087c-116">Especifica a ID do gateway.</span><span class="sxs-lookup"><span data-stu-id="3087c-116">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="3087c-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="3087c-117">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3087c-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3087c-118">-Profile</span></span>
<span data-ttu-id="3087c-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="3087c-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3087c-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="3087c-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3087c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3087c-121">CommonParameters</span></span>
<span data-ttu-id="3087c-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3087c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3087c-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3087c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3087c-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3087c-124">INPUTS</span></span>

## <span data-ttu-id="3087c-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3087c-125">OUTPUTS</span></span>

## <span data-ttu-id="3087c-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3087c-126">NOTES</span></span>

## <span data-ttu-id="3087c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3087c-127">RELATED LINKS</span></span>

[<span data-ttu-id="3087c-128">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3087c-128">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="3087c-129">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3087c-129">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="3087c-130">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3087c-130">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)


