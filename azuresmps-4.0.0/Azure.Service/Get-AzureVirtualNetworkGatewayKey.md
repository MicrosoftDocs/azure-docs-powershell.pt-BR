---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5F016D72-80EB-462D-9646-25EC4E33293E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 485b29130fd4b54c378f3ec19389b6c24ba86c63
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946513"
---
# <span data-ttu-id="a53c3-101">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="a53c3-101">Get-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="a53c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a53c3-102">SYNOPSIS</span></span>
<span data-ttu-id="a53c3-103">Obtém a chave para um gateway de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="a53c3-103">Gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="a53c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a53c3-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a53c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a53c3-105">DESCRIPTION</span></span>
<span data-ttu-id="a53c3-106">O cmdlet **Get-AzureVirtualNetworkGatewayKey** Obtém a chave para um gateway de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="a53c3-106">The **Get-AzureVirtualNetworkGatewayKey** cmdlet gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="a53c3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a53c3-107">EXAMPLES</span></span>

## <span data-ttu-id="a53c3-108">OS</span><span class="sxs-lookup"><span data-stu-id="a53c3-108">PARAMETERS</span></span>

### <span data-ttu-id="a53c3-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="a53c3-109">-ConnectedEntityId</span></span>
<span data-ttu-id="a53c3-110">Especifica a ID de uma entidade conectada.</span><span class="sxs-lookup"><span data-stu-id="a53c3-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="a53c3-111">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="a53c3-111">-GatewayId</span></span>
<span data-ttu-id="a53c3-112">Especifica a ID de um gateway.</span><span class="sxs-lookup"><span data-stu-id="a53c3-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="a53c3-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a53c3-113">-Profile</span></span>
<span data-ttu-id="a53c3-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a53c3-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a53c3-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a53c3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a53c3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a53c3-116">CommonParameters</span></span>
<span data-ttu-id="a53c3-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a53c3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a53c3-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a53c3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a53c3-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a53c3-119">INPUTS</span></span>

## <span data-ttu-id="a53c3-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a53c3-120">OUTPUTS</span></span>

## <span data-ttu-id="a53c3-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a53c3-121">NOTES</span></span>

## <span data-ttu-id="a53c3-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a53c3-122">RELATED LINKS</span></span>

[<span data-ttu-id="a53c3-123">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="a53c3-123">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="a53c3-124">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="a53c3-124">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)


