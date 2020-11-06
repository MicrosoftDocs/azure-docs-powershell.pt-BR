---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 8437c6037b52fd274415a59bea6ee66a2f9c0588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429263"
---
# <span data-ttu-id="9d02c-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9d02c-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="9d02c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d02c-102">SYNOPSIS</span></span>
<span data-ttu-id="9d02c-103">Cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="9d02c-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d02c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d02c-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d02c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d02c-105">DESCRIPTION</span></span>
<span data-ttu-id="9d02c-106">O cmdlet **New-AzureRmPublicIpAddress** cria um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="9d02c-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="9d02c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d02c-107">EXAMPLES</span></span>

### <span data-ttu-id="9d02c-108">1: criar um novo endereço IP público</span><span class="sxs-lookup"><span data-stu-id="9d02c-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="9d02c-109">Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix. $location. cloudapp.azure.com apontando para o endereço IP público desse recurso.</span><span class="sxs-lookup"><span data-stu-id="9d02c-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="9d02c-110">Um endereço IP público é imediatamente atribuído a esse recurso, pois o-AllocationMethod é especificado como ' estático '.</span><span class="sxs-lookup"><span data-stu-id="9d02c-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="9d02c-111">Se for especificado como ' dinâmico ', um endereço IP público será alocado somente quando você iniciar (ou criar) o recurso associado (como uma VM ou um balanceador de carga).</span><span class="sxs-lookup"><span data-stu-id="9d02c-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="9d02c-112">2: criar um endereço IP público com um FQDN reverso</span><span class="sxs-lookup"><span data-stu-id="9d02c-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="9d02c-113">Esse comando cria um novo recurso de endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="9d02c-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="9d02c-114">Com o parâmetro-ReverseFqdn, o Azure cria um registro de DNS PTR (pesquisa inversa) para o endereço IP público atribuído a esse recurso, apontando para o $customFqdn especificado no comando.</span><span class="sxs-lookup"><span data-stu-id="9d02c-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="9d02c-115">Como pré-requisito, o $customFqdn (Diga webapp.contoso.com) deve ter um registro CNAME DNS (pesquisa avançada) apontando para $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="9d02c-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="9d02c-116">OS</span><span class="sxs-lookup"><span data-stu-id="9d02c-116">PARAMETERS</span></span>

### <span data-ttu-id="9d02c-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="9d02c-117">-AllocationMethod</span></span>
<span data-ttu-id="9d02c-118">Especifica o método com o qual atribuir o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="9d02c-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="9d02c-119">Os valores aceitáveis para esse parâmetro são: estático ou dinâmico.</span><span class="sxs-lookup"><span data-stu-id="9d02c-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="9d02c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d02c-120">-DefaultProfile</span></span>
<span data-ttu-id="9d02c-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d02c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d02c-122">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="9d02c-122">-DomainNameLabel</span></span>
<span data-ttu-id="9d02c-123">Especifica o nome DNS relativo para um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="9d02c-123">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="9d02c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9d02c-124">-Force</span></span>
<span data-ttu-id="9d02c-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9d02c-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9d02c-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9d02c-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9d02c-127">Especifica o tempo limite ocioso, em minutos.</span><span class="sxs-lookup"><span data-stu-id="9d02c-127">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="9d02c-128">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="9d02c-128">-IpAddressVersion</span></span>
<span data-ttu-id="9d02c-129">Especifica a versão do endereço IP.</span><span class="sxs-lookup"><span data-stu-id="9d02c-129">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="9d02c-130">-Local</span><span class="sxs-lookup"><span data-stu-id="9d02c-130">-Location</span></span>
<span data-ttu-id="9d02c-131">Especifica a região na qual criar um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="9d02c-131">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="9d02c-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d02c-132">-Name</span></span>
<span data-ttu-id="9d02c-133">Especifica o nome do endereço IP público que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="9d02c-133">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9d02c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d02c-134">-ResourceGroupName</span></span>
<span data-ttu-id="9d02c-135">Especifica o nome do grupo de recursos no qual você deseja criar um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="9d02c-135">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="9d02c-136">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="9d02c-136">-ReverseFqdn</span></span>
<span data-ttu-id="9d02c-137">Especifica um nome de domínio totalmente qualificado (FQDN) reverso.</span><span class="sxs-lookup"><span data-stu-id="9d02c-137">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="9d02c-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="9d02c-138">-Sku</span></span>
<span data-ttu-id="9d02c-139">O nome da SKU de IP público.</span><span class="sxs-lookup"><span data-stu-id="9d02c-139">The public IP Sku name.</span></span>

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

### <span data-ttu-id="9d02c-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="9d02c-140">-Tag</span></span>
<span data-ttu-id="9d02c-141">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9d02c-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9d02c-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9d02c-142">For example:</span></span>

<span data-ttu-id="9d02c-143">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9d02c-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9d02c-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="9d02c-144">-Zone</span></span>
<span data-ttu-id="9d02c-145">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="9d02c-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="9d02c-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d02c-146">-Confirm</span></span>
<span data-ttu-id="9d02c-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d02c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d02c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d02c-148">-WhatIf</span></span>
<span data-ttu-id="9d02c-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d02c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d02c-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d02c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d02c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d02c-151">CommonParameters</span></span>
<span data-ttu-id="9d02c-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d02c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d02c-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d02c-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d02c-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d02c-154">INPUTS</span></span>

## <span data-ttu-id="9d02c-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d02c-155">OUTPUTS</span></span>

### <span data-ttu-id="9d02c-156">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9d02c-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="9d02c-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d02c-157">NOTES</span></span>

## <span data-ttu-id="9d02c-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d02c-158">RELATED LINKS</span></span>

[<span data-ttu-id="9d02c-159">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9d02c-159">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="9d02c-160">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9d02c-160">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="9d02c-161">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9d02c-161">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
