---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8099942A-B6EB-4C01-9F57-378B0EB7B3C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c933b716095392a215543cfc61d334cd347835
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945437"
---
# <span data-ttu-id="ae984-101">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="ae984-101">Set-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="ae984-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae984-102">SYNOPSIS</span></span>
<span data-ttu-id="ae984-103">Define a chave para um gateway de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae984-103">Sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="ae984-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae984-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ae984-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae984-105">DESCRIPTION</span></span>
<span data-ttu-id="ae984-106">O cmdlet **set-AzureVirtualNetworkGatewayKey** define a chave para um gateway de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae984-106">The **Set-AzureVirtualNetworkGatewayKey** cmdlet sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="ae984-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae984-107">EXAMPLES</span></span>

## <span data-ttu-id="ae984-108">OS</span><span class="sxs-lookup"><span data-stu-id="ae984-108">PARAMETERS</span></span>

### <span data-ttu-id="ae984-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="ae984-109">-ConnectedEntityId</span></span>
<span data-ttu-id="ae984-110">Especifica a ID de uma entidade conectada.</span><span class="sxs-lookup"><span data-stu-id="ae984-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="ae984-111">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="ae984-111">-GatewayId</span></span>
<span data-ttu-id="ae984-112">Especifica a ID de um gateway.</span><span class="sxs-lookup"><span data-stu-id="ae984-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="ae984-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ae984-113">-Profile</span></span>
<span data-ttu-id="ae984-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ae984-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ae984-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ae984-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae984-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ae984-116">-SharedKey</span></span>
<span data-ttu-id="ae984-117">Especifica uma chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="ae984-117">Specifies a shared key.</span></span>

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

### <span data-ttu-id="ae984-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae984-118">CommonParameters</span></span>
<span data-ttu-id="ae984-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae984-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae984-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae984-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae984-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae984-121">INPUTS</span></span>

## <span data-ttu-id="ae984-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae984-122">OUTPUTS</span></span>

## <span data-ttu-id="ae984-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae984-123">NOTES</span></span>

## <span data-ttu-id="ae984-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae984-124">RELATED LINKS</span></span>

[<span data-ttu-id="ae984-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="ae984-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="ae984-126">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="ae984-126">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)


