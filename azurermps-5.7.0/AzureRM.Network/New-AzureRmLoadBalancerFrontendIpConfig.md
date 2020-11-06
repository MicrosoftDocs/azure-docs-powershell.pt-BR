---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b05804bb5af2513e6a54026c7b989662212ba350
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603012"
---
# <span data-ttu-id="3f722-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f722-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="3f722-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f722-102">SYNOPSIS</span></span>
<span data-ttu-id="3f722-103">Cria uma configuração de IP de front-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f722-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f722-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f722-104">SYNTAX</span></span>

### <span data-ttu-id="3f722-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="3f722-105">SetByResourceSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f722-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="3f722-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f722-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f722-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f722-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f722-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f722-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f722-109">DESCRIPTION</span></span>
<span data-ttu-id="3f722-110">O cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** cria uma configuração de IP de front-end para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f722-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="3f722-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f722-111">EXAMPLES</span></span>

### <span data-ttu-id="3f722-112">Exemplo 1: criar uma configuração de IP de front-end para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="3f722-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="3f722-113">O primeiro comando cria um endereço IP público dinâmico chamado MyPublicIP no grupo de recursos chamado MyResource Group e, em seguida, armazena-o na variável $publicip.</span><span class="sxs-lookup"><span data-stu-id="3f722-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="3f722-114">O segundo comando cria uma configuração de IP de front-end chamada FrontendIpConfig01 usando o endereço IP público em $publicip.</span><span class="sxs-lookup"><span data-stu-id="3f722-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="3f722-115">OS</span><span class="sxs-lookup"><span data-stu-id="3f722-115">PARAMETERS</span></span>

### <span data-ttu-id="3f722-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f722-116">-DefaultProfile</span></span>
<span data-ttu-id="3f722-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f722-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f722-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f722-118">-Name</span></span>
<span data-ttu-id="3f722-119">Especifica a configuração de IP de front-end que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="3f722-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3f722-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f722-120">-PrivateIpAddress</span></span>
<span data-ttu-id="3f722-121">Especifica o endereço IP privado do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f722-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="3f722-122">Especifique esse parâmetro somente se você também especificar o parâmetro de *sub-rede* .</span><span class="sxs-lookup"><span data-stu-id="3f722-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f722-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f722-123">-PublicIpAddress</span></span>
<span data-ttu-id="3f722-124">Especifica o objeto **PublicIpAddress** para associar a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="3f722-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f722-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3f722-125">-PublicIpAddressId</span></span>
<span data-ttu-id="3f722-126">Especifica a ID do objeto **PublicIpAddress** a ser associado a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="3f722-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f722-127">-Subnet</span><span class="sxs-lookup"><span data-stu-id="3f722-127">-Subnet</span></span>
<span data-ttu-id="3f722-128">Especifica o objeto de **sub-rede** no qual criar uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="3f722-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f722-129">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="3f722-129">-SubnetId</span></span>
<span data-ttu-id="3f722-130">Especifica a ID da sub-rede na qual criar uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="3f722-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f722-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="3f722-131">-Zone</span></span>
<span data-ttu-id="3f722-132">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="3f722-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f722-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f722-133">CommonParameters</span></span>
<span data-ttu-id="3f722-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f722-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f722-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f722-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f722-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f722-136">INPUTS</span></span>

### <span data-ttu-id="3f722-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3f722-137">None</span></span>
<span data-ttu-id="3f722-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3f722-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f722-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f722-139">OUTPUTS</span></span>

### <span data-ttu-id="3f722-140">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f722-140">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="3f722-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f722-141">NOTES</span></span>

## <span data-ttu-id="3f722-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f722-142">RELATED LINKS</span></span>

[<span data-ttu-id="3f722-143">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f722-143">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3f722-144">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f722-144">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3f722-145">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f722-145">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="3f722-146">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f722-146">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3f722-147">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f722-147">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


