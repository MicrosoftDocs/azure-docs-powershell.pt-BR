---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 88AB3621-7C80-41BA-BE49-4F8F9C46BCF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fb0fa13cb5ea155b945505fd3f99c28494c5dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946523"
---
# <span data-ttu-id="f02bb-101">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f02bb-101">Get-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f02bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f02bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f02bb-103">Obtém uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f02bb-103">Gets a virtual network gateway connection.</span></span>

## <span data-ttu-id="f02bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f02bb-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayConnection [-GatewayId <String>] [-ConnectedEntityId <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f02bb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f02bb-105">DESCRIPTION</span></span>
<span data-ttu-id="f02bb-106">O cmdlet **Get-AzureVirtualNetworkGatewayConnection** Obtém uma conexão de gateway de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f02bb-106">The **Get-AzureVirtualNetworkGatewayConnection** cmdlet gets an Azure virtual network gateway connection.</span></span>

## <span data-ttu-id="f02bb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f02bb-107">EXAMPLES</span></span>

## <span data-ttu-id="f02bb-108">OS</span><span class="sxs-lookup"><span data-stu-id="f02bb-108">PARAMETERS</span></span>

### <span data-ttu-id="f02bb-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="f02bb-109">-ConnectedEntityId</span></span>
<span data-ttu-id="f02bb-110">Especifica a ID de uma entidade conectada.</span><span class="sxs-lookup"><span data-stu-id="f02bb-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="f02bb-111">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="f02bb-111">-GatewayId</span></span>
<span data-ttu-id="f02bb-112">Especifica a ID do gateway.</span><span class="sxs-lookup"><span data-stu-id="f02bb-112">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="f02bb-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f02bb-113">-Profile</span></span>
<span data-ttu-id="f02bb-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f02bb-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f02bb-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f02bb-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f02bb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f02bb-116">CommonParameters</span></span>
<span data-ttu-id="f02bb-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f02bb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f02bb-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f02bb-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f02bb-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f02bb-119">INPUTS</span></span>

## <span data-ttu-id="f02bb-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f02bb-120">OUTPUTS</span></span>

## <span data-ttu-id="f02bb-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f02bb-121">NOTES</span></span>

## <span data-ttu-id="f02bb-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f02bb-122">RELATED LINKS</span></span>

[<span data-ttu-id="f02bb-123">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f02bb-123">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f02bb-124">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f02bb-124">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f02bb-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f02bb-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)
