---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9F9E4639-A557-4BD8-88C2-894F6C848C4A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa54a7bd236bb561b3de4b9c2a3c0a2710deb61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946007"
---
# <span data-ttu-id="dd760-101">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dd760-101">New-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="dd760-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd760-102">SYNOPSIS</span></span>
<span data-ttu-id="dd760-103">Cria um gateway de rede local do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd760-103">creates an Azure local network gateway.</span></span>

## <span data-ttu-id="dd760-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd760-104">SYNTAX</span></span>

```
New-AzureLocalNetworkGateway -GatewayName <String> -IpAddress <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dd760-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd760-105">DESCRIPTION</span></span>
<span data-ttu-id="dd760-106">O cmdlet **New-AzureLocalNetworkGateway** cria um gateway de rede local do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd760-106">The **New-AzureLocalNetworkGateway** cmdlet creates an Azure local network gateway.</span></span>

## <span data-ttu-id="dd760-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd760-107">EXAMPLES</span></span>

## <span data-ttu-id="dd760-108">OS</span><span class="sxs-lookup"><span data-stu-id="dd760-108">PARAMETERS</span></span>

### <span data-ttu-id="dd760-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="dd760-109">-AddressSpace</span></span>
<span data-ttu-id="dd760-110">Especifica o espaço de endereço.</span><span class="sxs-lookup"><span data-stu-id="dd760-110">Specifies the address space.</span></span>

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

### <span data-ttu-id="dd760-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="dd760-111">-Asn</span></span>
<span data-ttu-id="dd760-112">Especifica o número do sistema autônomo (ASN).</span><span class="sxs-lookup"><span data-stu-id="dd760-112">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="dd760-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="dd760-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="dd760-114">Especifica o endereço de emparelhamento do BGP (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="dd760-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="dd760-115">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="dd760-115">-GatewayName</span></span>
<span data-ttu-id="dd760-116">Especifica o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="dd760-116">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="dd760-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="dd760-117">-IpAddress</span></span>
<span data-ttu-id="dd760-118">Especifica o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="dd760-118">Specifies the IP address.</span></span>

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

### <span data-ttu-id="dd760-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="dd760-119">-PeerWeight</span></span>
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

### <span data-ttu-id="dd760-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="dd760-120">-Profile</span></span>
<span data-ttu-id="dd760-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="dd760-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="dd760-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="dd760-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dd760-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd760-123">CommonParameters</span></span>
<span data-ttu-id="dd760-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd760-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd760-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd760-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd760-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd760-126">INPUTS</span></span>

## <span data-ttu-id="dd760-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd760-127">OUTPUTS</span></span>

## <span data-ttu-id="dd760-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd760-128">NOTES</span></span>

## <span data-ttu-id="dd760-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd760-129">RELATED LINKS</span></span>

[<span data-ttu-id="dd760-130">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dd760-130">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="dd760-131">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dd760-131">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)

[<span data-ttu-id="dd760-132">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dd760-132">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)


