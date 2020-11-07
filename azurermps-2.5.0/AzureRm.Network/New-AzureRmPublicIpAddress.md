---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: 032090bb494718a6420f54960106fe9c5fa9871c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785890"
---
# <span data-ttu-id="86d15-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="86d15-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="86d15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86d15-102">SYNOPSIS</span></span>
<span data-ttu-id="86d15-103">Cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="86d15-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86d15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86d15-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86d15-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86d15-105">DESCRIPTION</span></span>
<span data-ttu-id="86d15-106">O cmdlet **New-AzureRmPublicIpAddress** cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="86d15-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="86d15-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86d15-107">EXAMPLES</span></span>

### <span data-ttu-id="86d15-108">1: criar um novo endereço IP público</span><span class="sxs-lookup"><span data-stu-id="86d15-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="86d15-109">Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix. $location. cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="86d15-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="86d15-110">Um endereço IP público é imediatamente atribuído a esse recurso, pois o-AllocationMethod é especificado como ' estático '.</span><span class="sxs-lookup"><span data-stu-id="86d15-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="86d15-111">Se for especificado como ' dinâmico ', um endereço IP público será alocado somente quando você iniciar (ou criar) o recurso associado (como uma VM ou um balanceador de carga).</span><span class="sxs-lookup"><span data-stu-id="86d15-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="86d15-112">2: criar um endereço IP público com um FQDN reverso</span><span class="sxs-lookup"><span data-stu-id="86d15-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="86d15-113">Esse comando cria um novo recurso de endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="86d15-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="86d15-114">Com o parâmetro-ReverseFqdn, o Azure cria um registro de DNS PTR (pesquisa inversa) para o endereço IP público atribuído a esse recurso, apontando para o $customFqdn especificado no comando.</span><span class="sxs-lookup"><span data-stu-id="86d15-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="86d15-115">Como pré-requisito, o $customFqdn (Diga webapp.contoso.com) deve ter um registro CNAME DNS (pesquisa avançada) apontando para $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="86d15-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="86d15-116">OS</span><span class="sxs-lookup"><span data-stu-id="86d15-116">PARAMETERS</span></span>

### <span data-ttu-id="86d15-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="86d15-117">-AllocationMethod</span></span>
<span data-ttu-id="86d15-118">Especifica o método com o qual atribuir o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="86d15-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="86d15-119">Os valores aceitáveis para esse parâmetro são: estático ou dinâmico.</span><span class="sxs-lookup"><span data-stu-id="86d15-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="86d15-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86d15-120">-AsJob</span></span>
<span data-ttu-id="86d15-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="86d15-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86d15-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d15-122">-DefaultProfile</span></span>
<span data-ttu-id="86d15-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86d15-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86d15-124">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="86d15-124">-DomainNameLabel</span></span>
<span data-ttu-id="86d15-125">Especifica o nome DNS relativo para um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="86d15-125">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="86d15-126">-Force</span><span class="sxs-lookup"><span data-stu-id="86d15-126">-Force</span></span>
<span data-ttu-id="86d15-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="86d15-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="86d15-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="86d15-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="86d15-129">Especifica o tempo limite ocioso, em minutos.</span><span class="sxs-lookup"><span data-stu-id="86d15-129">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="86d15-130">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="86d15-130">-IpAddressVersion</span></span>
<span data-ttu-id="86d15-131">Especifica a versão do endereço IP.</span><span class="sxs-lookup"><span data-stu-id="86d15-131">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="86d15-132">-Local</span><span class="sxs-lookup"><span data-stu-id="86d15-132">-Location</span></span>
<span data-ttu-id="86d15-133">Especifica a região na qual criar um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="86d15-133">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="86d15-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="86d15-134">-Name</span></span>
<span data-ttu-id="86d15-135">Especifica o nome do endereço IP público que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="86d15-135">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="86d15-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d15-136">-ResourceGroupName</span></span>
<span data-ttu-id="86d15-137">Especifica o nome do grupo de recursos no qual você deseja criar um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="86d15-137">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="86d15-138">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="86d15-138">-ReverseFqdn</span></span>
<span data-ttu-id="86d15-139">Especifica um nome de domínio totalmente qualificado (FQDN) reverso.</span><span class="sxs-lookup"><span data-stu-id="86d15-139">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="86d15-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="86d15-140">-Sku</span></span>
<span data-ttu-id="86d15-141">O nome da SKU de IP público.</span><span class="sxs-lookup"><span data-stu-id="86d15-141">The public IP Sku name.</span></span>

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

### <span data-ttu-id="86d15-142">-Marca</span><span class="sxs-lookup"><span data-stu-id="86d15-142">-Tag</span></span>
<span data-ttu-id="86d15-143">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="86d15-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="86d15-144">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="86d15-144">For example:</span></span>

<span data-ttu-id="86d15-145">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="86d15-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="86d15-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="86d15-146">-Zone</span></span>
<span data-ttu-id="86d15-147">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="86d15-147">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="86d15-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="86d15-148">-Confirm</span></span>
<span data-ttu-id="86d15-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86d15-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86d15-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d15-150">-WhatIf</span></span>
<span data-ttu-id="86d15-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="86d15-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86d15-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="86d15-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86d15-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d15-153">CommonParameters</span></span>
<span data-ttu-id="86d15-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d15-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d15-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d15-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d15-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86d15-156">INPUTS</span></span>

## <span data-ttu-id="86d15-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86d15-157">OUTPUTS</span></span>

### <span data-ttu-id="86d15-158">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="86d15-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="86d15-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86d15-159">NOTES</span></span>

## <span data-ttu-id="86d15-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86d15-160">RELATED LINKS</span></span>

[<span data-ttu-id="86d15-161">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="86d15-161">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="86d15-162">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="86d15-162">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="86d15-163">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="86d15-163">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
