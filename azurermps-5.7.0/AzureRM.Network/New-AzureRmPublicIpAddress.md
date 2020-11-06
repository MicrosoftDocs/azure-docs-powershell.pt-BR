---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 98ea4632004787626237e5845f3c573b51a91934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440445"
---
# <span data-ttu-id="078fa-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="078fa-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="078fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="078fa-102">SYNOPSIS</span></span>
<span data-ttu-id="078fa-103">Cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="078fa-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="078fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="078fa-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="078fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="078fa-105">DESCRIPTION</span></span>
<span data-ttu-id="078fa-106">O cmdlet **New-AzureRmPublicIpAddress** cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="078fa-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="078fa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="078fa-107">EXAMPLES</span></span>

### <span data-ttu-id="078fa-108">1: criar um novo endereço IP público</span><span class="sxs-lookup"><span data-stu-id="078fa-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="078fa-109">Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix. $location. cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="078fa-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="078fa-110">Um endereço IP público é imediatamente atribuído a esse recurso, pois o-AllocationMethod é especificado como ' estático '.</span><span class="sxs-lookup"><span data-stu-id="078fa-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="078fa-111">Se for especificado como ' dinâmico ', um endereço IP público será alocado somente quando você iniciar (ou criar) o recurso associado (como uma VM ou um balanceador de carga).</span><span class="sxs-lookup"><span data-stu-id="078fa-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="078fa-112">2: criar um endereço IP público com um FQDN reverso</span><span class="sxs-lookup"><span data-stu-id="078fa-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="078fa-113">Esse comando cria um novo recurso de endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="078fa-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="078fa-114">Com o parâmetro-ReverseFqdn, o Azure cria um registro de DNS PTR (pesquisa inversa) para o endereço IP público atribuído a esse recurso, apontando para o $customFqdn especificado no comando.</span><span class="sxs-lookup"><span data-stu-id="078fa-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="078fa-115">Como pré-requisito, o $customFqdn (Diga webapp.contoso.com) deve ter um registro CNAME DNS (pesquisa avançada) apontando para $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="078fa-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="078fa-116">3: criar um novo endereço IP público com IpTag</span><span class="sxs-lookup"><span data-stu-id="078fa-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="078fa-117">Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix. $location. cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="078fa-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="078fa-118">Um endereço IP público é imediatamente atribuído a esse recurso, pois o-AllocationMethod é especificado como ' estático '.</span><span class="sxs-lookup"><span data-stu-id="078fa-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="078fa-119">Se for especificado como ' dinâmico ', um endereço IP público será alocado somente quando você iniciar (ou criar) o recurso associado (como uma VM ou um balanceador de carga).</span><span class="sxs-lookup"><span data-stu-id="078fa-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="078fa-120">Um Iptag é usado para especificar as marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="078fa-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="078fa-121">Iptag pode ser especificado usando New-AzureRmPublicIpTag e passado como Input through-IpTags.</span><span class="sxs-lookup"><span data-stu-id="078fa-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

## <span data-ttu-id="078fa-122">OS</span><span class="sxs-lookup"><span data-stu-id="078fa-122">PARAMETERS</span></span>

### <span data-ttu-id="078fa-123">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="078fa-123">-AllocationMethod</span></span>
<span data-ttu-id="078fa-124">Especifica o método com o qual atribuir o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="078fa-124">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="078fa-125">Os valores aceitáveis para esse parâmetro são: estático ou dinâmico.</span><span class="sxs-lookup"><span data-stu-id="078fa-125">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fa-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="078fa-126">-AsJob</span></span>
<span data-ttu-id="078fa-127">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="078fa-127">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="078fa-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="078fa-128">-DefaultProfile</span></span>
<span data-ttu-id="078fa-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="078fa-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="078fa-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="078fa-130">-DomainNameLabel</span></span>
<span data-ttu-id="078fa-131">Especifica o nome DNS relativo para um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="078fa-131">Specifies the relative DNS name for a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fa-132">-Force</span><span class="sxs-lookup"><span data-stu-id="078fa-132">-Force</span></span>
<span data-ttu-id="078fa-133">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="078fa-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="078fa-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="078fa-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="078fa-135">Especifica o tempo limite ocioso, em minutos.</span><span class="sxs-lookup"><span data-stu-id="078fa-135">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fa-136">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="078fa-136">-IpAddressVersion</span></span>
<span data-ttu-id="078fa-137">Especifica a versão do endereço IP.</span><span class="sxs-lookup"><span data-stu-id="078fa-137">Specifies the version of the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fa-138">-IpTag</span><span class="sxs-lookup"><span data-stu-id="078fa-138">-IpTag</span></span>
<span data-ttu-id="078fa-139">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="078fa-139">IpTag List.</span></span>

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

### <span data-ttu-id="078fa-140">-Local</span><span class="sxs-lookup"><span data-stu-id="078fa-140">-Location</span></span>
<span data-ttu-id="078fa-141">Especifica a região na qual criar um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="078fa-141">Specifies the region in which to create a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fa-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="078fa-142">-Name</span></span>
<span data-ttu-id="078fa-143">Especifica o nome do endereço IP público que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="078fa-143">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fa-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="078fa-144">-ResourceGroupName</span></span>
<span data-ttu-id="078fa-145">Especifica o nome do grupo de recursos no qual você deseja criar um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="078fa-145">Specifies the name of the resource group in which to create a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fa-146">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="078fa-146">-ReverseFqdn</span></span>
<span data-ttu-id="078fa-147">Especifica um nome de domínio totalmente qualificado (FQDN) reverso.</span><span class="sxs-lookup"><span data-stu-id="078fa-147">Specifies a reverse fully qualified domain name (FQDN).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fa-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="078fa-148">-Sku</span></span>
<span data-ttu-id="078fa-149">O nome da SKU de IP público.</span><span class="sxs-lookup"><span data-stu-id="078fa-149">The public IP Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fa-150">-Marca</span><span class="sxs-lookup"><span data-stu-id="078fa-150">-Tag</span></span>
<span data-ttu-id="078fa-151">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="078fa-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="078fa-152">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="078fa-152">For example:</span></span>

<span data-ttu-id="078fa-153">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="078fa-153">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fa-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="078fa-154">-Zone</span></span>
<span data-ttu-id="078fa-155">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="078fa-155">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="078fa-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="078fa-156">-Confirm</span></span>
<span data-ttu-id="078fa-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="078fa-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="078fa-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="078fa-158">-WhatIf</span></span>
<span data-ttu-id="078fa-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="078fa-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="078fa-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="078fa-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="078fa-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="078fa-161">CommonParameters</span></span>
<span data-ttu-id="078fa-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="078fa-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="078fa-163">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="078fa-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="078fa-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="078fa-164">INPUTS</span></span>

### <span data-ttu-id="078fa-165">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="078fa-165">None</span></span>
<span data-ttu-id="078fa-166">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="078fa-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="078fa-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="078fa-167">OUTPUTS</span></span>

### <span data-ttu-id="078fa-168">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="078fa-168">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="078fa-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="078fa-169">NOTES</span></span>

## <span data-ttu-id="078fa-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="078fa-170">RELATED LINKS</span></span>

[<span data-ttu-id="078fa-171">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="078fa-171">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="078fa-172">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="078fa-172">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="078fa-173">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="078fa-173">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
