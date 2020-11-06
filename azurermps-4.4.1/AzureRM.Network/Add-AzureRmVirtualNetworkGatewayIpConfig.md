---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 08dc5728e13423fdd9e05c5d5b5d843b963c4aa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433075"
---
# <span data-ttu-id="58416-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="58416-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="58416-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58416-102">SYNOPSIS</span></span>
<span data-ttu-id="58416-103">Adiciona uma configuração de IP a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="58416-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58416-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58416-104">SYNTAX</span></span>

### <span data-ttu-id="58416-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="58416-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58416-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="58416-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58416-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58416-107">DESCRIPTION</span></span>
<span data-ttu-id="58416-108">O cmdlet **Add-AzureRmVirtualNetworkGatewayIpConfig** adiciona uma configuração de IP a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="58416-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="58416-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58416-109">EXAMPLES</span></span>

## <span data-ttu-id="58416-110">OS</span><span class="sxs-lookup"><span data-stu-id="58416-110">PARAMETERS</span></span>

### <span data-ttu-id="58416-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="58416-111">-Name</span></span>
<span data-ttu-id="58416-112">Especifica o nome da configuração de IP do gateway a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="58416-112">Specifies the name of the gateway IP configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58416-113">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="58416-113">-PrivateIpAddress</span></span>
<span data-ttu-id="58416-114">Especifica o endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="58416-114">Specifies the private IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58416-115">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="58416-115">-PublicIpAddress</span></span>
<span data-ttu-id="58416-116">Especifica o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="58416-116">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58416-117">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="58416-117">-PublicIpAddressId</span></span>
<span data-ttu-id="58416-118">Especifica a ID do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="58416-118">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58416-119">-Subnet</span><span class="sxs-lookup"><span data-stu-id="58416-119">-Subnet</span></span>
<span data-ttu-id="58416-120">Especifica um objeto **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="58416-120">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58416-121">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="58416-121">-SubnetId</span></span>
<span data-ttu-id="58416-122">Especifica a ID da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="58416-122">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58416-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="58416-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="58416-124">Especifica um objeto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="58416-124">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="58416-125">Esse cmdlet modifica o objeto **PSVirtualNetworkGateway** que você especificar.</span><span class="sxs-lookup"><span data-stu-id="58416-125">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="58416-126">Você pode usar o cmdlet Get-AzureRmVirtualNetworkGateway para recuperar um objeto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="58416-126">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58416-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58416-127">-Confirm</span></span>
<span data-ttu-id="58416-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58416-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58416-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58416-129">-WhatIf</span></span>
<span data-ttu-id="58416-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58416-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58416-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58416-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58416-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58416-132">-DefaultProfile</span></span>
<span data-ttu-id="58416-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58416-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58416-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58416-134">CommonParameters</span></span>
<span data-ttu-id="58416-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58416-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58416-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58416-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58416-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58416-137">INPUTS</span></span>

### <span data-ttu-id="58416-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="58416-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="58416-139">O parâmetro ' VirtualNetworkGateway ' aceita o valor do tipo ' PSVirtualNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="58416-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="58416-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58416-140">OUTPUTS</span></span>

### <span data-ttu-id="58416-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="58416-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="58416-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58416-142">NOTES</span></span>

## <span data-ttu-id="58416-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58416-143">RELATED LINKS</span></span>

[<span data-ttu-id="58416-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="58416-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="58416-145">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="58416-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="58416-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="58416-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


