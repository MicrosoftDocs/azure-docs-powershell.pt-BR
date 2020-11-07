---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 2c14c8c903f892ac5fe822e96fc463528d32f39d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776566"
---
# <span data-ttu-id="804d4-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="804d4-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="804d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="804d4-102">SYNOPSIS</span></span>
<span data-ttu-id="804d4-103">Modifica uma configuração de IP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="804d4-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="804d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="804d4-104">SYNTAX</span></span>

### <span data-ttu-id="804d4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="804d4-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="804d4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="804d4-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="804d4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="804d4-107">DESCRIPTION</span></span>
<span data-ttu-id="804d4-108">O cmdlet **set-AzApplicationGatewayIPConfiguration** modifica uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="804d4-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="804d4-109">Uma configuração de IP contém a sub-rede na qual um gateway de aplicativo é implantado.</span><span class="sxs-lookup"><span data-stu-id="804d4-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="804d4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="804d4-110">EXAMPLES</span></span>

### <span data-ttu-id="804d4-111">Exemplo 1: definir o estado da meta de uma configuração de IP</span><span class="sxs-lookup"><span data-stu-id="804d4-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="804d4-112">O primeiro comando obtém a rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="804d4-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>

<span data-ttu-id="804d4-113">O segundo comando obtém a configuração de sub-rede chamada Subnet01 usando $VNet e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="804d4-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="804d4-114">O terceiro comando obtém um gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="804d4-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="804d4-115">O comando avançar define a configuração de IP do gateway do aplicativo armazenado no $AppGw para a configuração de sub-rede armazenada no $Subnet.</span><span class="sxs-lookup"><span data-stu-id="804d4-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="804d4-116">OS</span><span class="sxs-lookup"><span data-stu-id="804d4-116">PARAMETERS</span></span>

### <span data-ttu-id="804d4-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="804d4-117">-ApplicationGateway</span></span>
<span data-ttu-id="804d4-118">Especifica um objeto do aplicativo gateway com o qual esse cmdlet associa uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="804d4-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="804d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="804d4-119">-DefaultProfile</span></span>
<span data-ttu-id="804d4-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="804d4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="804d4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="804d4-121">-Name</span></span>
<span data-ttu-id="804d4-122">Especifica o nome da configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="804d4-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="804d4-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="804d4-123">-Subnet</span></span>
<span data-ttu-id="804d4-124">Especifica a sub-rede.</span><span class="sxs-lookup"><span data-stu-id="804d4-124">Specifies the subnet.</span></span>
<span data-ttu-id="804d4-125">Esta é a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="804d4-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="804d4-126">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="804d4-126">-SubnetId</span></span>
<span data-ttu-id="804d4-127">Especifica a identificação de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="804d4-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="804d4-128">Esta é a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="804d4-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="804d4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="804d4-129">CommonParameters</span></span>
<span data-ttu-id="804d4-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="804d4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="804d4-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="804d4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="804d4-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="804d4-132">INPUTS</span></span>

### <span data-ttu-id="804d4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="804d4-133">System.String</span></span>

## <span data-ttu-id="804d4-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="804d4-134">OUTPUTS</span></span>

### <span data-ttu-id="804d4-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="804d4-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="804d4-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="804d4-136">NOTES</span></span>

## <span data-ttu-id="804d4-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="804d4-137">RELATED LINKS</span></span>

[<span data-ttu-id="804d4-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="804d4-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="804d4-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="804d4-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="804d4-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="804d4-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="804d4-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="804d4-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="804d4-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="804d4-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


