---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 31790ead292c9146aa73f41c56e79f3bdf51c715
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775621"
---
# <span data-ttu-id="c84c6-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c84c6-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="c84c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c84c6-102">SYNOPSIS</span></span>
<span data-ttu-id="c84c6-103">Adiciona uma configuração de IP a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c84c6-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="c84c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c84c6-104">SYNTAX</span></span>

### <span data-ttu-id="c84c6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c84c6-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c84c6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c84c6-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c84c6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c84c6-107">DESCRIPTION</span></span>
<span data-ttu-id="c84c6-108">O cmdlet **Add-AzVirtualNetworkGatewayIpConfig** adiciona uma configuração de IP a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c84c6-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="c84c6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c84c6-109">EXAMPLES</span></span>

### <span data-ttu-id="c84c6-110">1:</span><span class="sxs-lookup"><span data-stu-id="c84c6-110">1:</span></span>
```

```

## <span data-ttu-id="c84c6-111">OS</span><span class="sxs-lookup"><span data-stu-id="c84c6-111">PARAMETERS</span></span>

### <span data-ttu-id="c84c6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c84c6-112">-DefaultProfile</span></span>
<span data-ttu-id="c84c6-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c84c6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c84c6-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c84c6-114">-Name</span></span>
<span data-ttu-id="c84c6-115">Especifica o nome da configuração de IP do gateway a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="c84c6-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="c84c6-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="c84c6-116">-PrivateIpAddress</span></span>
<span data-ttu-id="c84c6-117">Especifica o endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="c84c6-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="c84c6-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c84c6-118">-PublicIpAddress</span></span>
<span data-ttu-id="c84c6-119">Especifica o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="c84c6-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="c84c6-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="c84c6-120">-PublicIpAddressId</span></span>
<span data-ttu-id="c84c6-121">Especifica a ID do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="c84c6-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="c84c6-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="c84c6-122">-Subnet</span></span>
<span data-ttu-id="c84c6-123">Especifica um objeto **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="c84c6-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="c84c6-124">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="c84c6-124">-SubnetId</span></span>
<span data-ttu-id="c84c6-125">Especifica a ID da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="c84c6-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="c84c6-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c84c6-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="c84c6-127">Especifica um objeto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="c84c6-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="c84c6-128">Esse cmdlet modifica o objeto **PSVirtualNetworkGateway** que você especificar.</span><span class="sxs-lookup"><span data-stu-id="c84c6-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="c84c6-129">Você pode usar o cmdlet Get-AzVirtualNetworkGateway para recuperar um objeto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="c84c6-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="c84c6-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c84c6-130">-Confirm</span></span>
<span data-ttu-id="c84c6-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c84c6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c84c6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c84c6-132">-WhatIf</span></span>
<span data-ttu-id="c84c6-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c84c6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c84c6-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c84c6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c84c6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c84c6-135">CommonParameters</span></span>
<span data-ttu-id="c84c6-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c84c6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c84c6-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c84c6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c84c6-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c84c6-138">INPUTS</span></span>

### <span data-ttu-id="c84c6-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c84c6-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="c84c6-140">O parâmetro ' VirtualNetworkGateway ' aceita o valor do tipo ' PSVirtualNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c84c6-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="c84c6-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c84c6-141">OUTPUTS</span></span>

### <span data-ttu-id="c84c6-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c84c6-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c84c6-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c84c6-143">NOTES</span></span>

## <span data-ttu-id="c84c6-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c84c6-144">RELATED LINKS</span></span>

[<span data-ttu-id="c84c6-145">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c84c6-145">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c84c6-146">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c84c6-146">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="c84c6-147">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c84c6-147">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)


