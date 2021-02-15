---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 8c48c7ec1f651348309c012275287bd88dd42bcc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112806"
---
# <span data-ttu-id="66cab-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="66cab-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="66cab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66cab-102">SYNOPSIS</span></span>
<span data-ttu-id="66cab-103">Cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="66cab-103">Creates a public IP address.</span></span>

## <span data-ttu-id="66cab-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66cab-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66cab-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="66cab-105">DESCRIPTION</span></span>
<span data-ttu-id="66cab-106">O **cmdlet New-AzPublicIpAddress** cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="66cab-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="66cab-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66cab-107">EXAMPLES</span></span>

### <span data-ttu-id="66cab-108">Exemplo 1: Criar um novo endereço IP público</span><span class="sxs-lookup"><span data-stu-id="66cab-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="66cab-109">Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix.$location.cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="66cab-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="66cab-110">Um endereço IP público é imediatamente alocado a esse recurso, pois o -AllocationMethod é especificado como "Estático".</span><span class="sxs-lookup"><span data-stu-id="66cab-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="66cab-111">Se for especificado como "Dinâmico", um endereço IP público será alocado somente quando você iniciar (ou criar) o recurso associado (como um VM ou balanceador de carga).</span><span class="sxs-lookup"><span data-stu-id="66cab-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="66cab-112">Exemplo 2: Criar um endereço IP público com um FQDN reverso</span><span class="sxs-lookup"><span data-stu-id="66cab-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="66cab-113">Esse comando cria um novo recurso de endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="66cab-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="66cab-114">Com o parâmetro -ReverseFqdn, o Azure cria um registro DNS PTR (busca reversa) para o endereço IP público atribuído a esse recurso, apontando para o $customFqdn especificado no comando.</span><span class="sxs-lookup"><span data-stu-id="66cab-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="66cab-115">Como um pré-requisito, o $customFqdn (digamos webapp.contoso.com) deve ter um registro CNAME DNS (forward-lookup) apontando para $dnsPrefix.$location.cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="66cab-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="66cab-116">Exemplo 3: Criar um novo endereço IP público com IpTag</span><span class="sxs-lookup"><span data-stu-id="66cab-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="66cab-117">Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix.$location.cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="66cab-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="66cab-118">Um endereço IP público é imediatamente alocado a esse recurso, pois o -AllocationMethod é especificado como "Estático".</span><span class="sxs-lookup"><span data-stu-id="66cab-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="66cab-119">Se for especificado como "Dinâmico", um endereço IP público será alocado somente quando você iniciar (ou criar) o recurso associado (como um VM ou balanceador de carga).</span><span class="sxs-lookup"><span data-stu-id="66cab-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="66cab-120">Um Iptag é usado para específicas as Marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="66cab-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="66cab-121">O Iptag pode ser especificado usando New-AzPublicIpTag e passado como entrada por -IpTags.</span><span class="sxs-lookup"><span data-stu-id="66cab-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="66cab-122">Exemplo 4: Criar um novo endereço IP público a partir de um Prefixo</span><span class="sxs-lookup"><span data-stu-id="66cab-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="66cab-123">Esse comando cria um novo recurso de endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="66cab-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="66cab-124">Um registro DNS é criado para $dnsPrefix.$location.cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="66cab-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="66cab-125">Um endereço IP público é imediatamente atribuído a esse recurso a partir do publicIpPrefix especificado.</span><span class="sxs-lookup"><span data-stu-id="66cab-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="66cab-126">Essa opção só tem suporte para a SKU 'Padrão' e a Alocação EstáticaMethod.</span><span class="sxs-lookup"><span data-stu-id="66cab-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

### <span data-ttu-id="66cab-127">Exemplo 5: Criar um novo endereço IP público global</span><span class="sxs-lookup"><span data-stu-id="66cab-127">Example 5: Create a new global public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

<span data-ttu-id="66cab-128">Esse comando cria um novo recurso de endereço IP público global. Um registro DNS é criado para $dnsPrefix.$location.cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="66cab-128">This command creates a new global public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="66cab-129">Um endereço IP público global é imediatamente atribuído a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="66cab-129">A global public IP address is immediately allocated to this resource.</span></span>
<span data-ttu-id="66cab-130">Essa opção só tem suporte para a SKU 'Padrão' e a Alocação EstáticaMethod.</span><span class="sxs-lookup"><span data-stu-id="66cab-130">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="66cab-131">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66cab-131">PARAMETERS</span></span>

### <span data-ttu-id="66cab-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="66cab-132">-AllocationMethod</span></span>
<span data-ttu-id="66cab-133">Especifica o método com o qual atribuir o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="66cab-133">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="66cab-134">Os valores aceitáveis para este parâmetro são: Estático ou Dinâmico.</span><span class="sxs-lookup"><span data-stu-id="66cab-134">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="66cab-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66cab-135">-AsJob</span></span>
<span data-ttu-id="66cab-136">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="66cab-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66cab-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66cab-137">-DefaultProfile</span></span>
<span data-ttu-id="66cab-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="66cab-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66cab-139">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="66cab-139">-DomainNameLabel</span></span>
<span data-ttu-id="66cab-140">Especifica o nome DNS relativo de um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="66cab-140">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="66cab-141">-Forçar</span><span class="sxs-lookup"><span data-stu-id="66cab-141">-Force</span></span>
<span data-ttu-id="66cab-142">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="66cab-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66cab-143">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="66cab-143">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="66cab-144">Especifica o tempo ocioso em minutos.</span><span class="sxs-lookup"><span data-stu-id="66cab-144">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="66cab-145">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="66cab-145">-IpAddressVersion</span></span>
<span data-ttu-id="66cab-146">Especifica a versão do endereço IP.</span><span class="sxs-lookup"><span data-stu-id="66cab-146">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="66cab-147">-IpTag</span><span class="sxs-lookup"><span data-stu-id="66cab-147">-IpTag</span></span>
<span data-ttu-id="66cab-148">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="66cab-148">IpTag List.</span></span>

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

### <span data-ttu-id="66cab-149">-Local</span><span class="sxs-lookup"><span data-stu-id="66cab-149">-Location</span></span>
<span data-ttu-id="66cab-150">Especifica a região na qual criar um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="66cab-150">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="66cab-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="66cab-151">-Name</span></span>
<span data-ttu-id="66cab-152">Especifica o nome do endereço IP público que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="66cab-152">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="66cab-153">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="66cab-153">-PublicIpPrefix</span></span>
<span data-ttu-id="66cab-154">Especifica a PSPublicIpPrefix a partir da qual o endereço IP público deve ser alocado.</span><span class="sxs-lookup"><span data-stu-id="66cab-154">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="66cab-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66cab-155">-ResourceGroupName</span></span>
<span data-ttu-id="66cab-156">Especifica o nome do grupo de recursos no qual se cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="66cab-156">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="66cab-157">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="66cab-157">-ReverseFqdn</span></span>
<span data-ttu-id="66cab-158">Especifica um FQDN (nome de domínio totalmente qualificado) reverso.</span><span class="sxs-lookup"><span data-stu-id="66cab-158">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="66cab-159">-SKU</span><span class="sxs-lookup"><span data-stu-id="66cab-159">-Sku</span></span>
<span data-ttu-id="66cab-160">O nome SKU do IP público.</span><span class="sxs-lookup"><span data-stu-id="66cab-160">The public IP Sku name.</span></span>

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

### <span data-ttu-id="66cab-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="66cab-161">-Tag</span></span>
<span data-ttu-id="66cab-162">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="66cab-162">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="66cab-163">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="66cab-163">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="66cab-164">-Tier</span><span class="sxs-lookup"><span data-stu-id="66cab-164">-Tier</span></span>
<span data-ttu-id="66cab-165">A camada de SKU ip pública.</span><span class="sxs-lookup"><span data-stu-id="66cab-165">The public IP Sku Tier.</span></span>

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

### <span data-ttu-id="66cab-166">-Zona</span><span class="sxs-lookup"><span data-stu-id="66cab-166">-Zone</span></span>
<span data-ttu-id="66cab-167">Uma lista de zonas de disponibilidade que denotam o IP alocado para o recurso precisa vir.</span><span class="sxs-lookup"><span data-stu-id="66cab-167">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="66cab-168">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="66cab-168">-Confirm</span></span>
<span data-ttu-id="66cab-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66cab-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66cab-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66cab-170">-WhatIf</span></span>
<span data-ttu-id="66cab-171">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="66cab-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66cab-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66cab-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66cab-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66cab-173">CommonParameters</span></span>
<span data-ttu-id="66cab-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66cab-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66cab-175">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66cab-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66cab-176">Entradas</span><span class="sxs-lookup"><span data-stu-id="66cab-176">INPUTS</span></span>

### <span data-ttu-id="66cab-177">System.String</span><span class="sxs-lookup"><span data-stu-id="66cab-177">System.String</span></span>

### <span data-ttu-id="66cab-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span><span class="sxs-lookup"><span data-stu-id="66cab-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="66cab-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="66cab-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="66cab-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="66cab-180">System.Int32</span></span>

### <span data-ttu-id="66cab-181">System.String[]</span><span class="sxs-lookup"><span data-stu-id="66cab-181">System.String[]</span></span>

### <span data-ttu-id="66cab-182">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="66cab-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="66cab-183">Saídas</span><span class="sxs-lookup"><span data-stu-id="66cab-183">OUTPUTS</span></span>

### <span data-ttu-id="66cab-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="66cab-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="66cab-185">Notas</span><span class="sxs-lookup"><span data-stu-id="66cab-185">NOTES</span></span>

## <span data-ttu-id="66cab-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66cab-186">RELATED LINKS</span></span>

[<span data-ttu-id="66cab-187">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="66cab-187">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="66cab-188">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="66cab-188">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="66cab-189">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="66cab-189">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
