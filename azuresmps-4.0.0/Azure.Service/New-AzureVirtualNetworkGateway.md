---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A40F3BBB-4DC6-452E-A939-ED610F541EB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7797c916813c985802a0a2f63a5a43e033009a06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946186"
---
# <span data-ttu-id="c15b5-101">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c15b5-101">New-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="c15b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c15b5-102">SYNOPSIS</span></span>
<span data-ttu-id="c15b5-103">Cria um gateway de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="c15b5-103">Creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="c15b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c15b5-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGateway -VNetName <String> -GatewayName <String> [-GatewayType <String>]
 [-GatewaySKU <String>] [-Location <String>] [-VnetId <String>] [-Asn <UInt32>] [-PeerWeight <Int32>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c15b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c15b5-105">DESCRIPTION</span></span>
<span data-ttu-id="c15b5-106">O cmdlet **New-AzureVirtualNetworkGateway** cria um gateway de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="c15b5-106">The **New-AzureVirtualNetworkGateway** cmdlet creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="c15b5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c15b5-107">EXAMPLES</span></span>

## <span data-ttu-id="c15b5-108">OS</span><span class="sxs-lookup"><span data-stu-id="c15b5-108">PARAMETERS</span></span>

### <span data-ttu-id="c15b5-109">-ASN</span><span class="sxs-lookup"><span data-stu-id="c15b5-109">-Asn</span></span>
<span data-ttu-id="c15b5-110">Especifica o número do sistema autônomo (ASN).</span><span class="sxs-lookup"><span data-stu-id="c15b5-110">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="c15b5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c15b5-111">-Force</span></span>
<span data-ttu-id="c15b5-112">Não confirmar a criação do gateway de rede virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="c15b5-112">Do not confirm Azure Virtual Network Gateway Creation</span></span>

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

### <span data-ttu-id="c15b5-113">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="c15b5-113">-GatewayName</span></span>
<span data-ttu-id="c15b5-114">Especifica o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="c15b5-114">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="c15b5-115">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="c15b5-115">-GatewaySKU</span></span>
<span data-ttu-id="c15b5-116">Especifica a SKU do gateway de rede virtual que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="c15b5-116">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="c15b5-117">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c15b5-117">Valid values are:</span></span>

- <span data-ttu-id="c15b5-118">Assume</span><span class="sxs-lookup"><span data-stu-id="c15b5-118">Default</span></span>
- <span data-ttu-id="c15b5-119">Oficial</span><span class="sxs-lookup"><span data-stu-id="c15b5-119">Standard</span></span>
- <span data-ttu-id="c15b5-120">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="c15b5-120">HighPerformance</span></span>

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

### <span data-ttu-id="c15b5-121">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="c15b5-121">-GatewayType</span></span>
<span data-ttu-id="c15b5-122">Especifica o tipo de gateway.</span><span class="sxs-lookup"><span data-stu-id="c15b5-122">Specifies the type of gateway.</span></span>

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

### <span data-ttu-id="c15b5-123">-Local</span><span class="sxs-lookup"><span data-stu-id="c15b5-123">-Location</span></span>
<span data-ttu-id="c15b5-124">Especifica o local.</span><span class="sxs-lookup"><span data-stu-id="c15b5-124">Specifies the location.</span></span>

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

### <span data-ttu-id="c15b5-125">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="c15b5-125">-PeerWeight</span></span>
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

### <span data-ttu-id="c15b5-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c15b5-126">-Profile</span></span>
<span data-ttu-id="c15b5-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c15b5-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c15b5-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c15b5-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c15b5-129">-VnetId</span><span class="sxs-lookup"><span data-stu-id="c15b5-129">-VnetId</span></span>
<span data-ttu-id="c15b5-130">Especifica a ID de uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c15b5-130">Specifies the ID of a virtual network.</span></span>

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

### <span data-ttu-id="c15b5-131">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c15b5-131">-VNetName</span></span>
<span data-ttu-id="c15b5-132">Especifica uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c15b5-132">Specifies a virtual network.</span></span>

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

### <span data-ttu-id="c15b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c15b5-133">CommonParameters</span></span>
<span data-ttu-id="c15b5-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c15b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c15b5-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c15b5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c15b5-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c15b5-136">INPUTS</span></span>

## <span data-ttu-id="c15b5-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c15b5-137">OUTPUTS</span></span>

## <span data-ttu-id="c15b5-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c15b5-138">NOTES</span></span>

## <span data-ttu-id="c15b5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c15b5-139">RELATED LINKS</span></span>

[<span data-ttu-id="c15b5-140">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c15b5-140">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="c15b5-141">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c15b5-141">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="c15b5-142">Redimensionar-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c15b5-142">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)
