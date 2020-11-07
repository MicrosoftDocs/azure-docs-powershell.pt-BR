---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 150EE0DC-07CD-4E24-AF70-0C1A7BB61433
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b663ced66318335afb1fe4c3bf0e6a1520ede7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946412"
---
# <span data-ttu-id="8da8d-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="8da8d-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="8da8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8da8d-102">SYNOPSIS</span></span>
<span data-ttu-id="8da8d-103">Define os parâmetros IPsec para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8da8d-103">Sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="8da8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8da8d-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8da8d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8da8d-105">DESCRIPTION</span></span>
<span data-ttu-id="8da8d-106">O cmdlet **set-AzureVirtualNetworkGatewayIPsecParameters** define parâmetros IPSec para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8da8d-106">The **Set-AzureVirtualNetworkGatewayIPsecParameters** cmdlet sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="8da8d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8da8d-107">EXAMPLES</span></span>

## <span data-ttu-id="8da8d-108">OS</span><span class="sxs-lookup"><span data-stu-id="8da8d-108">PARAMETERS</span></span>

### <span data-ttu-id="8da8d-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="8da8d-109">-ConnectedEntityId</span></span>
<span data-ttu-id="8da8d-110">Especifica a ID de uma entidade conectada.</span><span class="sxs-lookup"><span data-stu-id="8da8d-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="8da8d-111">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="8da8d-111">-EncryptionType</span></span>
<span data-ttu-id="8da8d-112">Especifica o tipo de criptografia do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8da8d-112">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="8da8d-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8da8d-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8da8d-114">Descriptografia</span><span class="sxs-lookup"><span data-stu-id="8da8d-114">NoEncryption</span></span>
- <span data-ttu-id="8da8d-115">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="8da8d-115">RequireEncryption</span></span>

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

### <span data-ttu-id="8da8d-116">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="8da8d-116">-GatewayId</span></span>
<span data-ttu-id="8da8d-117">Especifica a ID de um gateway.</span><span class="sxs-lookup"><span data-stu-id="8da8d-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="8da8d-118">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="8da8d-118">-PfsGroup</span></span>
<span data-ttu-id="8da8d-119">Especifica o grupo sigilo total na transferência (PFS).</span><span class="sxs-lookup"><span data-stu-id="8da8d-119">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="8da8d-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8da8d-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8da8d-121">PFS1</span><span class="sxs-lookup"><span data-stu-id="8da8d-121">PFS1</span></span>
- <span data-ttu-id="8da8d-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8da8d-122">None</span></span>

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

### <span data-ttu-id="8da8d-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8da8d-123">-Profile</span></span>
<span data-ttu-id="8da8d-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="8da8d-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8da8d-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="8da8d-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8da8d-126">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="8da8d-126">-SADataSizeKilobytes</span></span>
<span data-ttu-id="8da8d-127">Especifica o tamanho, em kilobytes, da Associação de segurança (SA).</span><span class="sxs-lookup"><span data-stu-id="8da8d-127">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="8da8d-128">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="8da8d-128">-SALifetimeSeconds</span></span>
<span data-ttu-id="8da8d-129">Especifica o período, em segundos, da Associação de segurança.</span><span class="sxs-lookup"><span data-stu-id="8da8d-129">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="8da8d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da8d-130">CommonParameters</span></span>
<span data-ttu-id="8da8d-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da8d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da8d-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da8d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da8d-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8da8d-133">INPUTS</span></span>

## <span data-ttu-id="8da8d-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8da8d-134">OUTPUTS</span></span>

## <span data-ttu-id="8da8d-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8da8d-135">NOTES</span></span>

## <span data-ttu-id="8da8d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8da8d-136">RELATED LINKS</span></span>

[<span data-ttu-id="8da8d-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="8da8d-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Get-AzureVirtualNetworkGatewayIPsecParameters.md)


