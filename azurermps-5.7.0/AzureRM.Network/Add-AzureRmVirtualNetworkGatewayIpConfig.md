---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 4b157dfd7e7ac47a8161c9f36f9b52bbaaa61869
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428191"
---
# <span data-ttu-id="893b4-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="893b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="893b4-102">SYNOPSIS</span></span>
<span data-ttu-id="893b4-103">Adiciona uma configuração de IP a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="893b4-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="893b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="893b4-104">SYNTAX</span></span>

### <span data-ttu-id="893b4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="893b4-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="893b4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="893b4-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="893b4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="893b4-107">DESCRIPTION</span></span>
<span data-ttu-id="893b4-108">O cmdlet **Add-AzureRmVirtualNetworkGatewayIpConfig** adiciona uma configuração de IP a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="893b4-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="893b4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="893b4-109">EXAMPLES</span></span>

## <span data-ttu-id="893b4-110">OS</span><span class="sxs-lookup"><span data-stu-id="893b4-110">PARAMETERS</span></span>

### <span data-ttu-id="893b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="893b4-111">-DefaultProfile</span></span>
<span data-ttu-id="893b4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="893b4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="893b4-113">-Name</span></span>
<span data-ttu-id="893b4-114">Especifica o nome da configuração de IP do gateway a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="893b4-114">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="893b4-115">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="893b4-115">-PrivateIpAddress</span></span>
<span data-ttu-id="893b4-116">Especifica o endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="893b4-116">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="893b4-117">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="893b4-117">-PublicIpAddress</span></span>
<span data-ttu-id="893b4-118">Especifica o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="893b4-118">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="893b4-119">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="893b4-119">-PublicIpAddressId</span></span>
<span data-ttu-id="893b4-120">Especifica a ID do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="893b4-120">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="893b4-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="893b4-121">-Subnet</span></span>
<span data-ttu-id="893b4-122">Especifica um objeto **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="893b4-122">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="893b4-123">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="893b4-123">-SubnetId</span></span>
<span data-ttu-id="893b4-124">Especifica a ID da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="893b4-124">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="893b4-125">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="893b4-125">-VirtualNetworkGateway</span></span>
<span data-ttu-id="893b4-126">Especifica um objeto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="893b4-126">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="893b4-127">Esse cmdlet modifica o objeto **PSVirtualNetworkGateway** que você especificar.</span><span class="sxs-lookup"><span data-stu-id="893b4-127">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="893b4-128">Você pode usar o cmdlet Get-AzureRmVirtualNetworkGateway para recuperar um objeto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="893b4-128">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="893b4-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="893b4-129">-Confirm</span></span>
<span data-ttu-id="893b4-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="893b4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="893b4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="893b4-131">-WhatIf</span></span>
<span data-ttu-id="893b4-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="893b4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="893b4-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="893b4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="893b4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893b4-134">CommonParameters</span></span>
<span data-ttu-id="893b4-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="893b4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893b4-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="893b4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893b4-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="893b4-137">INPUTS</span></span>

### <span data-ttu-id="893b4-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="893b4-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="893b4-139">O parâmetro ' VirtualNetworkGateway ' aceita o valor do tipo ' PSVirtualNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="893b4-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="893b4-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="893b4-140">OUTPUTS</span></span>

### <span data-ttu-id="893b4-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="893b4-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="893b4-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="893b4-142">NOTES</span></span>

## <span data-ttu-id="893b4-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="893b4-143">RELATED LINKS</span></span>

[<span data-ttu-id="893b4-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="893b4-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="893b4-145">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="893b4-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


