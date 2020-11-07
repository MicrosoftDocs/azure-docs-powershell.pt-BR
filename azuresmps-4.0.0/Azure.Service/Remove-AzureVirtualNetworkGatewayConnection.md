---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F3D44471-50F0-4737-9AF5-3DE7222EAF9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9aa386b47c02ed945cad63c00425534d68e66f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945485"
---
# <span data-ttu-id="7ff86-101">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7ff86-101">Remove-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7ff86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ff86-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff86-103">Remove uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7ff86-103">Removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="7ff86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ff86-104">SYNTAX</span></span>

```
Remove-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7ff86-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ff86-105">DESCRIPTION</span></span>
<span data-ttu-id="7ff86-106">O cmdlet **Remove-AzureVirtualNetworkGatewayConnection** remove uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7ff86-106">The **Remove-AzureVirtualNetworkGatewayConnection** cmdlet removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="7ff86-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ff86-107">EXAMPLES</span></span>

## <span data-ttu-id="7ff86-108">OS</span><span class="sxs-lookup"><span data-stu-id="7ff86-108">PARAMETERS</span></span>

### <span data-ttu-id="7ff86-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="7ff86-109">-ConnectedEntityId</span></span>
<span data-ttu-id="7ff86-110">Especifica a ID de uma entidade conectada.</span><span class="sxs-lookup"><span data-stu-id="7ff86-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="7ff86-111">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="7ff86-111">-GatewayId</span></span>
<span data-ttu-id="7ff86-112">Especifica a ID de um gateway.</span><span class="sxs-lookup"><span data-stu-id="7ff86-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="7ff86-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7ff86-113">-Profile</span></span>
<span data-ttu-id="7ff86-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7ff86-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7ff86-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7ff86-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7ff86-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff86-116">CommonParameters</span></span>
<span data-ttu-id="7ff86-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ff86-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff86-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ff86-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff86-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ff86-119">INPUTS</span></span>

## <span data-ttu-id="7ff86-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ff86-120">OUTPUTS</span></span>

## <span data-ttu-id="7ff86-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ff86-121">NOTES</span></span>

## <span data-ttu-id="7ff86-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ff86-122">RELATED LINKS</span></span>

[<span data-ttu-id="7ff86-123">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7ff86-123">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7ff86-124">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7ff86-124">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7ff86-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7ff86-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


