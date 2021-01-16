---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 8c48c7ec1f651348309c012275287bd88dd42bcc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257823"
---
# <span data-ttu-id="2b4f2-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b4f2-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="2b4f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="2b4f2-103">Cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-103">Creates a public IP address.</span></span>

## <span data-ttu-id="2b4f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b4f2-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b4f2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b4f2-105">DESCRIPTION</span></span>
<span data-ttu-id="2b4f2-106">O cmdlet **New-AzPublicIpAddress** cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="2b4f2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b4f2-107">EXAMPLES</span></span>

### <span data-ttu-id="2b4f2-108">Exemplo 1: criar um novo endereço IP público</span><span class="sxs-lookup"><span data-stu-id="2b4f2-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="2b4f2-109">Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix. $location. cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="2b4f2-110">Um endereço IP público é imediatamente atribuído a esse recurso, pois o-AllocationMethod é especificado como ' estático '.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="2b4f2-111">Se for especificado como ' dinâmico ', um endereço IP público será alocado somente quando você iniciar (ou criar) o recurso associado (como uma VM ou um balanceador de carga).</span><span class="sxs-lookup"><span data-stu-id="2b4f2-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="2b4f2-112">Exemplo 2: criar um endereço IP público com um FQDN reverso</span><span class="sxs-lookup"><span data-stu-id="2b4f2-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="2b4f2-113">Esse comando cria um novo recurso de endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="2b4f2-114">Com o parâmetro-ReverseFqdn, o Azure cria um registro de DNS PTR (pesquisa inversa) para o endereço IP público atribuído a esse recurso, apontando para o $customFqdn especificado no comando.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="2b4f2-115">Como pré-requisito, o $customFqdn (Diga webapp.contoso.com) deve ter um registro CNAME DNS (pesquisa avançada) apontando para $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="2b4f2-116">Exemplo 3: criar um novo endereço IP público com IpTag</span><span class="sxs-lookup"><span data-stu-id="2b4f2-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="2b4f2-117">Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix. $location. cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="2b4f2-118">Um endereço IP público é imediatamente atribuído a esse recurso, pois o-AllocationMethod é especificado como ' estático '.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="2b4f2-119">Se for especificado como ' dinâmico ', um endereço IP público será alocado somente quando você iniciar (ou criar) o recurso associado (como uma VM ou um balanceador de carga).</span><span class="sxs-lookup"><span data-stu-id="2b4f2-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="2b4f2-120">Um Iptag é usado para especificar as marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="2b4f2-121">Iptag pode ser especificado usando New-AzPublicIpTag e passado como Input through-IpTags.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="2b4f2-122">Exemplo 4: criar um novo endereço IP público a partir de um prefixo</span><span class="sxs-lookup"><span data-stu-id="2b4f2-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="2b4f2-123">Esse comando cria um novo recurso de endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="2b4f2-124">Um registro DNS é criado para $dnsPrefix. $location. cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="2b4f2-125">Um endereço IP público é imediatamente atribuído a esse recurso da publicIpPrefix especificada.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="2b4f2-126">Essa opção só tem suporte para o ' padrão ' SKU e ' static ' AllocationMethod.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

### <span data-ttu-id="2b4f2-127">Exemplo 5: criar um novo endereço IP público global</span><span class="sxs-lookup"><span data-stu-id="2b4f2-127">Example 5: Create a new global public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

<span data-ttu-id="2b4f2-128">Esse comando cria um novo recurso global de endereço IP público. Um registro DNS é criado para $dnsPrefix. $location. cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-128">This command creates a new global public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="2b4f2-129">Um endereço IP público global é imediatamente atribuído a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-129">A global public IP address is immediately allocated to this resource.</span></span>
<span data-ttu-id="2b4f2-130">Essa opção só tem suporte para o ' padrão ' SKU e ' static ' AllocationMethod.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-130">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="2b4f2-131">OS</span><span class="sxs-lookup"><span data-stu-id="2b4f2-131">PARAMETERS</span></span>

### <span data-ttu-id="2b4f2-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="2b4f2-132">-AllocationMethod</span></span>
<span data-ttu-id="2b4f2-133">Especifica o método com o qual atribuir o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-133">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="2b4f2-134">Os valores aceitáveis para esse parâmetro são: estático ou dinâmico.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-134">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="2b4f2-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b4f2-135">-AsJob</span></span>
<span data-ttu-id="2b4f2-136">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2b4f2-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b4f2-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b4f2-137">-DefaultProfile</span></span>
<span data-ttu-id="2b4f2-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b4f2-139">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="2b4f2-139">-DomainNameLabel</span></span>
<span data-ttu-id="2b4f2-140">Especifica o nome DNS relativo para um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-140">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="2b4f2-141">-Force</span><span class="sxs-lookup"><span data-stu-id="2b4f2-141">-Force</span></span>
<span data-ttu-id="2b4f2-142">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b4f2-143">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2b4f2-143">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2b4f2-144">Especifica o tempo limite ocioso, em minutos.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-144">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="2b4f2-145">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="2b4f2-145">-IpAddressVersion</span></span>
<span data-ttu-id="2b4f2-146">Especifica a versão do endereço IP.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-146">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="2b4f2-147">-IpTag</span><span class="sxs-lookup"><span data-stu-id="2b4f2-147">-IpTag</span></span>
<span data-ttu-id="2b4f2-148">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-148">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b4f2-149">-Local</span><span class="sxs-lookup"><span data-stu-id="2b4f2-149">-Location</span></span>
<span data-ttu-id="2b4f2-150">Especifica a região na qual criar um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-150">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="2b4f2-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b4f2-151">-Name</span></span>
<span data-ttu-id="2b4f2-152">Especifica o nome do endereço IP público que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-152">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2b4f2-153">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2b4f2-153">-PublicIpPrefix</span></span>
<span data-ttu-id="2b4f2-154">Especifica o PSPublicIpPrefix do qual atribuir o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-154">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="2b4f2-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b4f2-155">-ResourceGroupName</span></span>
<span data-ttu-id="2b4f2-156">Especifica o nome do grupo de recursos no qual você deseja criar um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-156">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="2b4f2-157">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="2b4f2-157">-ReverseFqdn</span></span>
<span data-ttu-id="2b4f2-158">Especifica um nome de domínio totalmente qualificado (FQDN) reverso.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-158">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="2b4f2-159">-SKU</span><span class="sxs-lookup"><span data-stu-id="2b4f2-159">-Sku</span></span>
<span data-ttu-id="2b4f2-160">O nome da SKU de IP público.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-160">The public IP Sku name.</span></span>

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

### <span data-ttu-id="2b4f2-161">-Marca</span><span class="sxs-lookup"><span data-stu-id="2b4f2-161">-Tag</span></span>
<span data-ttu-id="2b4f2-162">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-162">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2b4f2-163">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2b4f2-163">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2b4f2-164">-Tier</span><span class="sxs-lookup"><span data-stu-id="2b4f2-164">-Tier</span></span>
<span data-ttu-id="2b4f2-165">A camada de SKU de IP público.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-165">The public IP Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b4f2-166">-Zone</span><span class="sxs-lookup"><span data-stu-id="2b4f2-166">-Zone</span></span>
<span data-ttu-id="2b4f2-167">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-167">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="2b4f2-168">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2b4f2-168">-Confirm</span></span>
<span data-ttu-id="2b4f2-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b4f2-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b4f2-170">-WhatIf</span></span>
<span data-ttu-id="2b4f2-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b4f2-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b4f2-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b4f2-173">CommonParameters</span></span>
<span data-ttu-id="2b4f2-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b4f2-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b4f2-175">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b4f2-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b4f2-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b4f2-176">INPUTS</span></span>

### <span data-ttu-id="2b4f2-177">System. String</span><span class="sxs-lookup"><span data-stu-id="2b4f2-177">System.String</span></span>

### <span data-ttu-id="2b4f2-178">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag []</span><span class="sxs-lookup"><span data-stu-id="2b4f2-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="2b4f2-179">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2b4f2-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="2b4f2-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2b4f2-180">System.Int32</span></span>

### <span data-ttu-id="2b4f2-181">System. String []</span><span class="sxs-lookup"><span data-stu-id="2b4f2-181">System.String[]</span></span>

### <span data-ttu-id="2b4f2-182">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2b4f2-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2b4f2-183">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b4f2-183">OUTPUTS</span></span>

### <span data-ttu-id="2b4f2-184">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b4f2-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="2b4f2-185">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b4f2-185">NOTES</span></span>

## <span data-ttu-id="2b4f2-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b4f2-186">RELATED LINKS</span></span>

[<span data-ttu-id="2b4f2-187">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b4f2-187">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="2b4f2-188">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b4f2-188">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="2b4f2-189">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b4f2-189">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
