---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: E3C0C3AA-3941-469E-A6CC-A92ADD7377B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bf6824219879af52549d7815d65dcb502a2a752
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946185"
---
# <span data-ttu-id="5a3be-101">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5a3be-101">New-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="5a3be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a3be-102">SYNOPSIS</span></span>
<span data-ttu-id="5a3be-103">Cria uma conexão de rede de gateway virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="5a3be-103">Creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="5a3be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a3be-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGatewayConnection -ConnectedEntityId <String> -GatewayConnectionName <String>
 -GatewayConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>]
 -VirtualNetworkGatewayId <String> [-EnableBgp <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5a3be-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a3be-105">DESCRIPTION</span></span>
<span data-ttu-id="5a3be-106">O cmdlet **New-AzureVirtualNetworkGatewayConnection** cria uma conexão de rede de gateway virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="5a3be-106">The **New-AzureVirtualNetworkGatewayConnection** cmdlet creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="5a3be-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a3be-107">EXAMPLES</span></span>

## <span data-ttu-id="5a3be-108">OS</span><span class="sxs-lookup"><span data-stu-id="5a3be-108">PARAMETERS</span></span>

### <span data-ttu-id="5a3be-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="5a3be-109">-ConnectedEntityId</span></span>
<span data-ttu-id="5a3be-110">Especifica a ID de uma entidade conectada.</span><span class="sxs-lookup"><span data-stu-id="5a3be-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="5a3be-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="5a3be-111">-EnableBgp</span></span>
<span data-ttu-id="5a3be-112">Habilita o BGP (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="5a3be-112">Enables Border Gateway Protocol (BGP).</span></span>

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

### <span data-ttu-id="5a3be-113">-GatewayConnectionName</span><span class="sxs-lookup"><span data-stu-id="5a3be-113">-GatewayConnectionName</span></span>
<span data-ttu-id="5a3be-114">Especifica um nome para a conexão do gateway.</span><span class="sxs-lookup"><span data-stu-id="5a3be-114">Specifies a name for the gateway connection.</span></span>

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

### <span data-ttu-id="5a3be-115">-GatewayConnectionType</span><span class="sxs-lookup"><span data-stu-id="5a3be-115">-GatewayConnectionType</span></span>
<span data-ttu-id="5a3be-116">Especifica o tipo de conexão de gateway.</span><span class="sxs-lookup"><span data-stu-id="5a3be-116">Specifies the type of gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a3be-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="5a3be-117">-Profile</span></span>
<span data-ttu-id="5a3be-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="5a3be-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5a3be-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="5a3be-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a3be-120">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="5a3be-120">-RoutingWeight</span></span>
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

### <span data-ttu-id="5a3be-121">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="5a3be-121">-SharedKey</span></span>
<span data-ttu-id="5a3be-122">Especifica uma chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="5a3be-122">Specifies a shared key.</span></span>

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

### <span data-ttu-id="5a3be-123">-VirtualNetworkGatewayId</span><span class="sxs-lookup"><span data-stu-id="5a3be-123">-VirtualNetworkGatewayId</span></span>
<span data-ttu-id="5a3be-124">Especifica a ID de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5a3be-124">Specifies the ID of a virtual network gateway.</span></span>

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

### <span data-ttu-id="5a3be-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a3be-125">CommonParameters</span></span>
<span data-ttu-id="5a3be-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a3be-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a3be-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a3be-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a3be-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a3be-128">INPUTS</span></span>

## <span data-ttu-id="5a3be-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a3be-129">OUTPUTS</span></span>

## <span data-ttu-id="5a3be-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a3be-130">NOTES</span></span>

## <span data-ttu-id="5a3be-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a3be-131">RELATED LINKS</span></span>

[<span data-ttu-id="5a3be-132">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5a3be-132">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="5a3be-133">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5a3be-133">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="5a3be-134">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5a3be-134">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


