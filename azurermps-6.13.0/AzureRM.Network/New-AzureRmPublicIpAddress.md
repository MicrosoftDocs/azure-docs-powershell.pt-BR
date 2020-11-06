---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 7ef0d3ce20868c4240abc43278cdc38a33efa5b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441240"
---
# <span data-ttu-id="efb4c-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="efb4c-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="efb4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efb4c-102">SYNOPSIS</span></span>
<span data-ttu-id="efb4c-103">Cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="efb4c-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efb4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efb4c-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-PublicIpPrefix <Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix>]
 [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efb4c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="efb4c-105">DESCRIPTION</span></span>
<span data-ttu-id="efb4c-106">O cmdlet **New-AzureRmPublicIpAddress** cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="efb4c-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="efb4c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="efb4c-107">EXAMPLES</span></span>

### <span data-ttu-id="efb4c-108">1: criar um novo endereço IP público</span><span class="sxs-lookup"><span data-stu-id="efb4c-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="efb4c-109">Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix. $location. cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="efb4c-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="efb4c-110">Um endereço IP público é imediatamente atribuído a esse recurso, pois o-AllocationMethod é especificado como ' estático '.</span><span class="sxs-lookup"><span data-stu-id="efb4c-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="efb4c-111">Se for especificado como ' dinâmico ', um endereço IP público será alocado somente quando você iniciar (ou criar) o recurso associado (como uma VM ou um balanceador de carga).</span><span class="sxs-lookup"><span data-stu-id="efb4c-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="efb4c-112">2: criar um endereço IP público com um FQDN reverso</span><span class="sxs-lookup"><span data-stu-id="efb4c-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="efb4c-113">Esse comando cria um novo recurso de endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="efb4c-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="efb4c-114">Com o parâmetro-ReverseFqdn, o Azure cria um registro de DNS PTR (pesquisa inversa) para o endereço IP público atribuído a esse recurso, apontando para o $customFqdn especificado no comando.</span><span class="sxs-lookup"><span data-stu-id="efb4c-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="efb4c-115">Como pré-requisito, o $customFqdn (Diga webapp.contoso.com) deve ter um registro CNAME DNS (pesquisa avançada) apontando para $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="efb4c-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="efb4c-116">3: criar um novo endereço IP público com IpTag</span><span class="sxs-lookup"><span data-stu-id="efb4c-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="efb4c-117">Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix. $location. cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="efb4c-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="efb4c-118">Um endereço IP público é imediatamente atribuído a esse recurso, pois o-AllocationMethod é especificado como ' estático '.</span><span class="sxs-lookup"><span data-stu-id="efb4c-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="efb4c-119">Se for especificado como ' dinâmico ', um endereço IP público será alocado somente quando você iniciar (ou criar) o recurso associado (como uma VM ou um balanceador de carga).</span><span class="sxs-lookup"><span data-stu-id="efb4c-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="efb4c-120">Um Iptag é usado para especificar as marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="efb4c-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="efb4c-121">Iptag pode ser especificado usando New-AzureRmPublicIpTag e passado como Input through-IpTags.</span><span class="sxs-lookup"><span data-stu-id="efb4c-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="efb4c-122">4: criar um novo endereço IP público a partir de um prefixo</span><span class="sxs-lookup"><span data-stu-id="efb4c-122">4: Create a new public IP address from a Prefix</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="efb4c-123">Esse comando cria um novo recurso de endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="efb4c-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="efb4c-124">Um registro DNS é criado para $dnsPrefix. $location. cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="efb4c-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="efb4c-125">Um endereço IP público é imediatamente atribuído a esse recurso da publicIpPrefix especificada.</span><span class="sxs-lookup"><span data-stu-id="efb4c-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="efb4c-126">Essa opção só tem suporte para o ' padrão ' SKU e ' static ' AllocationMethod.</span><span class="sxs-lookup"><span data-stu-id="efb4c-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="efb4c-127">OS</span><span class="sxs-lookup"><span data-stu-id="efb4c-127">PARAMETERS</span></span>

### <span data-ttu-id="efb4c-128">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="efb4c-128">-AllocationMethod</span></span>
<span data-ttu-id="efb4c-129">Especifica o método com o qual atribuir o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="efb4c-129">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="efb4c-130">Os valores aceitáveis para esse parâmetro são: estático ou dinâmico.</span><span class="sxs-lookup"><span data-stu-id="efb4c-130">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efb4c-131">-AsJob</span></span>
<span data-ttu-id="efb4c-132">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="efb4c-132">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb4c-133">-DefaultProfile</span></span>
<span data-ttu-id="efb4c-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="efb4c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efb4c-135">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="efb4c-135">-DomainNameLabel</span></span>
<span data-ttu-id="efb4c-136">Especifica o nome DNS relativo para um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="efb4c-136">Specifies the relative DNS name for a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-137">-Force</span><span class="sxs-lookup"><span data-stu-id="efb4c-137">-Force</span></span>
<span data-ttu-id="efb4c-138">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="efb4c-138">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="efb4c-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="efb4c-140">Especifica o tempo limite ocioso, em minutos.</span><span class="sxs-lookup"><span data-stu-id="efb4c-140">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-141">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="efb4c-141">-IpAddressVersion</span></span>
<span data-ttu-id="efb4c-142">Especifica a versão do endereço IP.</span><span class="sxs-lookup"><span data-stu-id="efb4c-142">Specifies the version of the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-143">-IpTag</span><span class="sxs-lookup"><span data-stu-id="efb4c-143">-IpTag</span></span>
<span data-ttu-id="efb4c-144">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="efb4c-144">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-145">-Local</span><span class="sxs-lookup"><span data-stu-id="efb4c-145">-Location</span></span>
<span data-ttu-id="efb4c-146">Especifica a região na qual criar um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="efb4c-146">Specifies the region in which to create a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-147">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="efb4c-147">-PublicIpPrefix</span></span>
<span data-ttu-id="efb4c-148">Especifica o PSPublicIpPrefix do qual atribuir o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="efb4c-148">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="efb4c-149">-Name</span></span>
<span data-ttu-id="efb4c-150">Especifica o nome do endereço IP público que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="efb4c-150">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efb4c-151">-ResourceGroupName</span></span>
<span data-ttu-id="efb4c-152">Especifica o nome do grupo de recursos no qual você deseja criar um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="efb4c-152">Specifies the name of the resource group in which to create a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-153">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="efb4c-153">-ReverseFqdn</span></span>
<span data-ttu-id="efb4c-154">Especifica um nome de domínio totalmente qualificado (FQDN) reverso.</span><span class="sxs-lookup"><span data-stu-id="efb4c-154">Specifies a reverse fully qualified domain name (FQDN).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="efb4c-155">-Sku</span></span>
<span data-ttu-id="efb4c-156">O nome da SKU de IP público.</span><span class="sxs-lookup"><span data-stu-id="efb4c-156">The public IP Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-157">-Marca</span><span class="sxs-lookup"><span data-stu-id="efb4c-157">-Tag</span></span>
<span data-ttu-id="efb4c-158">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="efb4c-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="efb4c-159">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="efb4c-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4c-160">-Zone</span><span class="sxs-lookup"><span data-stu-id="efb4c-160">-Zone</span></span>
<span data-ttu-id="efb4c-161">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="efb4c-161">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="efb4c-162">-Confirme</span><span class="sxs-lookup"><span data-stu-id="efb4c-162">-Confirm</span></span>
<span data-ttu-id="efb4c-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efb4c-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efb4c-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efb4c-164">-WhatIf</span></span>
<span data-ttu-id="efb4c-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="efb4c-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efb4c-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="efb4c-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efb4c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb4c-167">CommonParameters</span></span>
<span data-ttu-id="efb4c-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efb4c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb4c-169">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efb4c-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb4c-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="efb4c-170">INPUTS</span></span>

### <span data-ttu-id="efb4c-171">System. String</span><span class="sxs-lookup"><span data-stu-id="efb4c-171">System.String</span></span>

### <span data-ttu-id="efb4c-172">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSPublicIpTag, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="efb4c-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="efb4c-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="efb4c-173">System.Int32</span></span>

### <span data-ttu-id="efb4c-174">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="efb4c-174">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="efb4c-175">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="efb4c-175">System.Collections.Hashtable</span></span>

## <span data-ttu-id="efb4c-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="efb4c-176">OUTPUTS</span></span>

### <span data-ttu-id="efb4c-177">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="efb4c-177">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="efb4c-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="efb4c-178">NOTES</span></span>

## <span data-ttu-id="efb4c-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efb4c-179">RELATED LINKS</span></span>

[<span data-ttu-id="efb4c-180">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="efb4c-180">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="efb4c-181">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="efb4c-181">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="efb4c-182">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="efb4c-182">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
