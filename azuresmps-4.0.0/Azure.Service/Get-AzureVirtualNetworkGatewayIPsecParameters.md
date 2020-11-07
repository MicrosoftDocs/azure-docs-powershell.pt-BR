---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 425008DB-9761-42F1-8D6D-F35757A3CA6C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37aa0718c4faa637b16ccde61f5e5b241bb9aa92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946515"
---
# <span data-ttu-id="fb8e1-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="fb8e1-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="fb8e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8e1-103">Obtém os parâmetros IPsec para um gateway de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb8e1-103">Gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="fb8e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb8e1-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fb8e1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb8e1-105">DESCRIPTION</span></span>
<span data-ttu-id="fb8e1-106">O cmdlet **Get-AzureVirtualNetworkGatewayIPsecParameters** Obtém os parâmetros IPSec para um gateway de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb8e1-106">The **Get-AzureVirtualNetworkGatewayIPsecParameters** cmdlet gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="fb8e1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb8e1-107">EXAMPLES</span></span>

## <span data-ttu-id="fb8e1-108">OS</span><span class="sxs-lookup"><span data-stu-id="fb8e1-108">PARAMETERS</span></span>

### <span data-ttu-id="fb8e1-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="fb8e1-109">-ConnectedEntityId</span></span>
<span data-ttu-id="fb8e1-110">Especifica a ID de um entitiy conectado.</span><span class="sxs-lookup"><span data-stu-id="fb8e1-110">Specifies the ID of a connected entitiy.</span></span>

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

### <span data-ttu-id="fb8e1-111">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="fb8e1-111">-GatewayId</span></span>
<span data-ttu-id="fb8e1-112">Especifica a ID de um gateway.</span><span class="sxs-lookup"><span data-stu-id="fb8e1-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="fb8e1-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="fb8e1-113">-Profile</span></span>
<span data-ttu-id="fb8e1-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="fb8e1-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="fb8e1-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="fb8e1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fb8e1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8e1-116">CommonParameters</span></span>
<span data-ttu-id="fb8e1-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb8e1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8e1-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb8e1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8e1-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb8e1-119">INPUTS</span></span>

## <span data-ttu-id="fb8e1-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb8e1-120">OUTPUTS</span></span>

## <span data-ttu-id="fb8e1-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb8e1-121">NOTES</span></span>

## <span data-ttu-id="fb8e1-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb8e1-122">RELATED LINKS</span></span>

[<span data-ttu-id="fb8e1-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="fb8e1-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Set-AzureVirtualNetworkGatewayIPsecParameters.md)


