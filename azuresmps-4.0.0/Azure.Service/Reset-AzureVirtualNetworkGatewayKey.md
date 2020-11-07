---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4F1E69B8-15FB-495F-B910-04E450D3215F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a5b53f909b840a761d40f79a311fb61b7e2337b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946088"
---
# <span data-ttu-id="d7fcf-101">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d7fcf-101">Reset-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="d7fcf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="d7fcf-103">Redefine uma chave do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d7fcf-103">Resets a virtual network gateway key.</span></span>

## <span data-ttu-id="d7fcf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7fcf-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -keyLength <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d7fcf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="d7fcf-106">O cmdlet **Reset-AzureVirtualNetworkGatewayKey** redefine uma chave do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d7fcf-106">The **Reset-AzureVirtualNetworkGatewayKey** cmdlet resets a virtual network gateway key.</span></span>

## <span data-ttu-id="d7fcf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7fcf-107">EXAMPLES</span></span>

## <span data-ttu-id="d7fcf-108">OS</span><span class="sxs-lookup"><span data-stu-id="d7fcf-108">PARAMETERS</span></span>

### <span data-ttu-id="d7fcf-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="d7fcf-109">-ConnectedEntityId</span></span>
<span data-ttu-id="d7fcf-110">Especifica a ID de uma entidade conectada.</span><span class="sxs-lookup"><span data-stu-id="d7fcf-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="d7fcf-111">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="d7fcf-111">-GatewayId</span></span>
<span data-ttu-id="d7fcf-112">Especifica a ID de um gateway.</span><span class="sxs-lookup"><span data-stu-id="d7fcf-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="d7fcf-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="d7fcf-113">-keyLength</span></span>
<span data-ttu-id="d7fcf-114">Especifica o comprimento da chave.</span><span class="sxs-lookup"><span data-stu-id="d7fcf-114">Specifies the key length.</span></span>

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

### <span data-ttu-id="d7fcf-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d7fcf-115">-Profile</span></span>
<span data-ttu-id="d7fcf-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d7fcf-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d7fcf-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d7fcf-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d7fcf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7fcf-118">CommonParameters</span></span>
<span data-ttu-id="d7fcf-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7fcf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7fcf-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7fcf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7fcf-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7fcf-121">INPUTS</span></span>

## <span data-ttu-id="d7fcf-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7fcf-122">OUTPUTS</span></span>

## <span data-ttu-id="d7fcf-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7fcf-123">NOTES</span></span>

## <span data-ttu-id="d7fcf-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7fcf-124">RELATED LINKS</span></span>

[<span data-ttu-id="d7fcf-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d7fcf-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="d7fcf-126">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d7fcf-126">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)
