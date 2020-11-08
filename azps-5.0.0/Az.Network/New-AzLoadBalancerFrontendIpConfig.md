---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: fa520056b9e1d098271cd726575e8d521d7c27f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118318"
---
# <span data-ttu-id="edb3b-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="edb3b-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="edb3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="edb3b-102">SYNOPSIS</span></span>
<span data-ttu-id="edb3b-103">Cria uma configuração de IP de front-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="edb3b-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="edb3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edb3b-104">SYNTAX</span></span>

### <span data-ttu-id="edb3b-105">SetByResourceSubnet (padrão)</span><span class="sxs-lookup"><span data-stu-id="edb3b-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edb3b-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="edb3b-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edb3b-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="edb3b-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edb3b-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="edb3b-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edb3b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="edb3b-109">DESCRIPTION</span></span>
<span data-ttu-id="edb3b-110">O cmdlet **New-AzLoadBalancerFrontendIpConfig** cria uma configuração de IP de front-end para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="edb3b-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="edb3b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="edb3b-111">EXAMPLES</span></span>

### <span data-ttu-id="edb3b-112">Exemplo 1: criar uma configuração de IP de front-end para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="edb3b-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="edb3b-113">O primeiro comando cria um endereço IP público dinâmico chamado MyPublicIP no grupo de recursos chamado MyResource Group e, em seguida, armazena-o na variável $publicip.</span><span class="sxs-lookup"><span data-stu-id="edb3b-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="edb3b-114">O segundo comando cria uma configuração de IP de front-end chamada FrontendIpConfig01 usando o endereço IP público em $publicip.</span><span class="sxs-lookup"><span data-stu-id="edb3b-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="edb3b-115">OS</span><span class="sxs-lookup"><span data-stu-id="edb3b-115">PARAMETERS</span></span>

### <span data-ttu-id="edb3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb3b-116">-DefaultProfile</span></span>
<span data-ttu-id="edb3b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="edb3b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edb3b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="edb3b-118">-Name</span></span>
<span data-ttu-id="edb3b-119">Especifica a configuração de IP de front-end que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="edb3b-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="edb3b-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="edb3b-120">-PrivateIpAddress</span></span>
<span data-ttu-id="edb3b-121">Especifica o endereço IP privado do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="edb3b-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="edb3b-122">Especifique esse parâmetro somente se você também especificar o parâmetro de *sub-rede* .</span><span class="sxs-lookup"><span data-stu-id="edb3b-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb3b-123">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="edb3b-123">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="edb3b-124">A versão do endereço IP privado da configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="edb3b-124">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb3b-125">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="edb3b-125">-PublicIpAddress</span></span>
<span data-ttu-id="edb3b-126">Especifica o objeto **PublicIpAddress** para associar a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="edb3b-126">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb3b-127">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="edb3b-127">-PublicIpAddressId</span></span>
<span data-ttu-id="edb3b-128">Especifica a ID do objeto **PublicIpAddress** a ser associado a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="edb3b-128">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb3b-129">-Subnet</span><span class="sxs-lookup"><span data-stu-id="edb3b-129">-Subnet</span></span>
<span data-ttu-id="edb3b-130">Especifica o objeto de **sub-rede** no qual criar uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="edb3b-130">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb3b-131">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="edb3b-131">-SubnetId</span></span>
<span data-ttu-id="edb3b-132">Especifica a ID da sub-rede na qual criar uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="edb3b-132">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb3b-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="edb3b-133">-Zone</span></span>
<span data-ttu-id="edb3b-134">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="edb3b-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb3b-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="edb3b-135">-Confirm</span></span>
<span data-ttu-id="edb3b-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edb3b-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edb3b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edb3b-137">-WhatIf</span></span>
<span data-ttu-id="edb3b-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="edb3b-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edb3b-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="edb3b-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edb3b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb3b-140">CommonParameters</span></span>
<span data-ttu-id="edb3b-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb3b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb3b-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edb3b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb3b-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="edb3b-143">INPUTS</span></span>

### <span data-ttu-id="edb3b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="edb3b-144">System.String</span></span>

### <span data-ttu-id="edb3b-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="edb3b-145">System.String[]</span></span>

### <span data-ttu-id="edb3b-146">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="edb3b-146">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="edb3b-147">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="edb3b-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="edb3b-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="edb3b-148">OUTPUTS</span></span>

### <span data-ttu-id="edb3b-149">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="edb3b-149">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="edb3b-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="edb3b-150">NOTES</span></span>

## <span data-ttu-id="edb3b-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="edb3b-151">RELATED LINKS</span></span>

[<span data-ttu-id="edb3b-152">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="edb3b-152">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="edb3b-153">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="edb3b-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="edb3b-154">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="edb3b-154">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="edb3b-155">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="edb3b-155">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="edb3b-156">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="edb3b-156">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


