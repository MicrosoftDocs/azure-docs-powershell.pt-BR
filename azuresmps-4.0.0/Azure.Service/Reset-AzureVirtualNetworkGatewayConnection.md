---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 09642B94-E888-4A22-9E8E-62109DB9394E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f42a788f29f8546e6f402f1685f4c91aa3d7e5cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946089"
---
# <span data-ttu-id="06762-101">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="06762-101">Reset-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="06762-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06762-102">SYNOPSIS</span></span>
<span data-ttu-id="06762-103">Redefine uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="06762-103">Resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="06762-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06762-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 -RoutingWeight <Int32> [-SharedKey <String>] [-EnableBgp <Boolean>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="06762-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06762-105">DESCRIPTION</span></span>
<span data-ttu-id="06762-106">O cmdlet **Reset-AzureVirtualNetworkGatewayConnection** redefine uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="06762-106">The **Reset-AzureVirtualNetworkGatewayConnection** cmdlet resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="06762-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06762-107">EXAMPLES</span></span>

## <span data-ttu-id="06762-108">OS</span><span class="sxs-lookup"><span data-stu-id="06762-108">PARAMETERS</span></span>

### <span data-ttu-id="06762-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="06762-109">-ConnectedEntityId</span></span>
<span data-ttu-id="06762-110">Especifica a ID de uma entidade conectada.</span><span class="sxs-lookup"><span data-stu-id="06762-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="06762-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="06762-111">-EnableBgp</span></span>
<span data-ttu-id="06762-112">Habilita o BGP (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="06762-112">Enables Border Gateway Protocol (BGP).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06762-113">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="06762-113">-GatewayId</span></span>
<span data-ttu-id="06762-114">Especifica a ID de um gateway.</span><span class="sxs-lookup"><span data-stu-id="06762-114">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="06762-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="06762-115">-Profile</span></span>
<span data-ttu-id="06762-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="06762-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="06762-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="06762-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06762-118">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="06762-118">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06762-119">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="06762-119">-SharedKey</span></span>
<span data-ttu-id="06762-120">Especifica uma chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="06762-120">Specifies a shared key.</span></span>

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

### <span data-ttu-id="06762-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06762-121">CommonParameters</span></span>
<span data-ttu-id="06762-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06762-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06762-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06762-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06762-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06762-124">INPUTS</span></span>

## <span data-ttu-id="06762-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06762-125">OUTPUTS</span></span>

## <span data-ttu-id="06762-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06762-126">NOTES</span></span>

## <span data-ttu-id="06762-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06762-127">RELATED LINKS</span></span>

[<span data-ttu-id="06762-128">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="06762-128">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="06762-129">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="06762-129">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="06762-130">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="06762-130">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)


