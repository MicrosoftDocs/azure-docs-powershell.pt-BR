---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 340baa4b7a7d0afaf0e0523cb8c2f14f8270bf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786497"
---
# <span data-ttu-id="dad4b-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="dad4b-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="dad4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dad4b-102">SYNOPSIS</span></span>
<span data-ttu-id="dad4b-103">Adiciona uma configuração de IP a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="dad4b-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dad4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dad4b-104">SYNTAX</span></span>

### <span data-ttu-id="dad4b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dad4b-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad4b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dad4b-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dad4b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dad4b-107">DESCRIPTION</span></span>
<span data-ttu-id="dad4b-108">O cmdlet **Add-AzureRmVirtualNetworkGatewayIpConfig** adiciona uma configuração de IP a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="dad4b-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="dad4b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dad4b-109">EXAMPLES</span></span>

### <span data-ttu-id="dad4b-110">1:</span><span class="sxs-lookup"><span data-stu-id="dad4b-110">1:</span></span>
```

```

## <span data-ttu-id="dad4b-111">OS</span><span class="sxs-lookup"><span data-stu-id="dad4b-111">PARAMETERS</span></span>

### <span data-ttu-id="dad4b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad4b-112">-DefaultProfile</span></span>
<span data-ttu-id="dad4b-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dad4b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad4b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="dad4b-114">-Name</span></span>
<span data-ttu-id="dad4b-115">Especifica o nome da configuração de IP do gateway a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="dad4b-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="dad4b-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="dad4b-116">-PrivateIpAddress</span></span>
<span data-ttu-id="dad4b-117">Especifica o endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="dad4b-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="dad4b-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dad4b-118">-PublicIpAddress</span></span>
<span data-ttu-id="dad4b-119">Especifica o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="dad4b-119">Specifies the public IP address.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad4b-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="dad4b-120">-PublicIpAddressId</span></span>
<span data-ttu-id="dad4b-121">Especifica a ID do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="dad4b-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad4b-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="dad4b-122">-Subnet</span></span>
<span data-ttu-id="dad4b-123">Especifica um objeto **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="dad4b-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad4b-124">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="dad4b-124">-SubnetId</span></span>
<span data-ttu-id="dad4b-125">Especifica a ID da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="dad4b-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad4b-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad4b-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="dad4b-127">Especifica um objeto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="dad4b-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="dad4b-128">Esse cmdlet modifica o objeto **PSVirtualNetworkGateway** que você especificar.</span><span class="sxs-lookup"><span data-stu-id="dad4b-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="dad4b-129">Você pode usar o cmdlet Get-AzureRmVirtualNetworkGateway para recuperar um objeto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="dad4b-129">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dad4b-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dad4b-130">-Confirm</span></span>
<span data-ttu-id="dad4b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dad4b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad4b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad4b-132">-WhatIf</span></span>
<span data-ttu-id="dad4b-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dad4b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dad4b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dad4b-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad4b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad4b-135">CommonParameters</span></span>
<span data-ttu-id="dad4b-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad4b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad4b-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad4b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad4b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dad4b-138">INPUTS</span></span>

### <span data-ttu-id="dad4b-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad4b-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="dad4b-140">O parâmetro ' VirtualNetworkGateway ' aceita o valor do tipo ' PSVirtualNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="dad4b-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="dad4b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dad4b-141">OUTPUTS</span></span>

### <span data-ttu-id="dad4b-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad4b-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="dad4b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dad4b-143">NOTES</span></span>

## <span data-ttu-id="dad4b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dad4b-144">RELATED LINKS</span></span>

[<span data-ttu-id="dad4b-145">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad4b-145">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="dad4b-146">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="dad4b-146">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="dad4b-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="dad4b-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


