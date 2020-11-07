---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b0e8642feb208c9ed7ab0a91a31ebe7bd0f7cf8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786114"
---
# <span data-ttu-id="4ecd7-101">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="4ecd7-101">Remove-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="4ecd7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ecd7-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecd7-103">Remove um registro DNS de um objeto de conjunto de registros local.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-103">Removes a DNS record from a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ecd7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ecd7-104">SYNTAX</span></span>

### <span data-ttu-id="4ecd7-105">Um</span><span class="sxs-lookup"><span data-stu-id="4ecd7-105">A</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="4ecd7-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="4ecd7-106">AAAA</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="4ecd7-107">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="4ecd7-107">NS</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="4ecd7-108">MX</span><span class="sxs-lookup"><span data-stu-id="4ecd7-108">MX</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="4ecd7-109">PTR</span><span class="sxs-lookup"><span data-stu-id="4ecd7-109">PTR</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="4ecd7-110">LOCALIZADO</span><span class="sxs-lookup"><span data-stu-id="4ecd7-110">TXT</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="4ecd7-111">SRV</span><span class="sxs-lookup"><span data-stu-id="4ecd7-111">SRV</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="4ecd7-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="4ecd7-112">CNAME</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="4ecd7-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ecd7-113">DESCRIPTION</span></span>
<span data-ttu-id="4ecd7-114">O cmdlet **Remove-AzureRmDnsRecordConfig** remove um registro de DNS (sistema de nomes de domínio) de um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-114">The **Remove-AzureRmDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="4ecd7-115">O objeto **Recordset** é um objeto offline, e as alterações feitas a ele não alteram as respostas de DNS até que você execute o cmdlet Set-AzureRmDnsRecordSet para persistir a alteração no serviço DNS do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="4ecd7-116">Para remover um registro, todos os campos desse tipo de registro devem corresponder exatamente.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="4ecd7-117">Não é possível adicionar ou remover registros SOA.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="4ecd7-118">Os registros SOA são automaticamente criados quando uma zona DNS é criada e excluída automaticamente quando a zona DNS é excluída.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="4ecd7-119">Você pode passar o objeto **Recordset** para esse cmdlet como um parâmetro ou usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="4ecd7-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ecd7-120">EXAMPLES</span></span>

### <span data-ttu-id="4ecd7-121">Exemplo 1: remover um registro A de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ecd7-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="4ecd7-122">Este exemplo remove um registro A de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="4ecd7-123">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="4ecd7-124">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-124">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="4ecd7-125">Exemplo 2: remover um registro AAAA de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ecd7-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="4ecd7-126">Este exemplo remove um registro AAAA de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="4ecd7-127">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="4ecd7-128">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-128">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="4ecd7-129">Exemplo 3: remover um registro CNAME de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ecd7-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="4ecd7-130">Este exemplo remove um registro CNAME de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="4ecd7-131">Como um conjunto de registros CNAME pode conter no máximo um registro, o resultado é um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="4ecd7-132">Exemplo 4: remover um registro MX de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ecd7-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="4ecd7-133">Este exemplo remove um registro MX de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="4ecd7-134">O nome do registro "@" indica um conjunto de registros na zona Apex.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="4ecd7-135">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="4ecd7-136">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-136">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="4ecd7-137">Exemplo 5: remover um registro NS de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ecd7-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="4ecd7-138">Este exemplo remove um registro NS de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="4ecd7-139">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="4ecd7-140">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-140">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="4ecd7-141">Exemplo 6: remover um registro PTR de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ecd7-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="4ecd7-142">Este exemplo remove um registro PTR de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="4ecd7-143">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="4ecd7-144">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-144">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="4ecd7-145">Exemplo 7: remover um registro SRV de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ecd7-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="4ecd7-146">Este exemplo remove um registro SRV de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="4ecd7-147">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="4ecd7-148">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-148">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="4ecd7-149">Exemplo 8: remover um registro TXT de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4ecd7-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="4ecd7-150">Este exemplo remove um registro TXT de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="4ecd7-151">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="4ecd7-152">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-152">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="4ecd7-153">OS</span><span class="sxs-lookup"><span data-stu-id="4ecd7-153">PARAMETERS</span></span>

### <span data-ttu-id="4ecd7-154">-CNAME</span><span class="sxs-lookup"><span data-stu-id="4ecd7-154">-Cname</span></span>
<span data-ttu-id="4ecd7-155">Especifica o nome de domínio para um registro de nome canônico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="4ecd7-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="4ecd7-156">-Exchange</span></span>
<span data-ttu-id="4ecd7-157">Especifica o nome do servidor do servidor de mensagens para um registro de troca de email (MX).</span><span class="sxs-lookup"><span data-stu-id="4ecd7-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="4ecd7-158">-Ipv4Address</span></span>
<span data-ttu-id="4ecd7-159">Especifica um endereço IPv4 para um registro A.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-159">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-160">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="4ecd7-160">-Ipv6Address</span></span>
<span data-ttu-id="4ecd7-161">Especifica um endereço IPv6 para um registro AAAA.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-161">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="4ecd7-162">-Nsdname</span></span>
<span data-ttu-id="4ecd7-163">Especifica o servidor de nomes para um registro de servidor de nomes (NS).</span><span class="sxs-lookup"><span data-stu-id="4ecd7-163">Specifies the name server for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-164">-Porta</span><span class="sxs-lookup"><span data-stu-id="4ecd7-164">-Port</span></span>
<span data-ttu-id="4ecd7-165">Especifica a porta para um registro de serviço (SRV).</span><span class="sxs-lookup"><span data-stu-id="4ecd7-165">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-166">-Preferência</span><span class="sxs-lookup"><span data-stu-id="4ecd7-166">-Preference</span></span>
<span data-ttu-id="4ecd7-167">Especifica a preferência para um registro MX.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-167">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-168">-Priority</span><span class="sxs-lookup"><span data-stu-id="4ecd7-168">-Priority</span></span>
<span data-ttu-id="4ecd7-169">Especifica a prioridade para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-169">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="4ecd7-170">-Ptrdname</span></span>
<span data-ttu-id="4ecd7-171">Especifica o nome de domínio de destino de um registro de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="4ecd7-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-172">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="4ecd7-172">-RecordSet</span></span>
<span data-ttu-id="4ecd7-173">Especifica o objeto **Recordset** que contém o registro a remover.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-174">-Destino</span><span class="sxs-lookup"><span data-stu-id="4ecd7-174">-Target</span></span>
<span data-ttu-id="4ecd7-175">Especifica o destino para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-175">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-176">-Valor</span><span class="sxs-lookup"><span data-stu-id="4ecd7-176">-Value</span></span>
<span data-ttu-id="4ecd7-177">Especifica o valor de um registro TXT.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-177">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-178">-Weight</span><span class="sxs-lookup"><span data-stu-id="4ecd7-178">-Weight</span></span>
<span data-ttu-id="4ecd7-179">Especifica o peso para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-179">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd7-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecd7-180">CommonParameters</span></span>
<span data-ttu-id="4ecd7-181">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecd7-182">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ecd7-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecd7-183">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ecd7-183">INPUTS</span></span>

### <span data-ttu-id="4ecd7-184">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4ecd7-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="4ecd7-185">Você pode canalizar um objeto **DnsRecordSet** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-185">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="4ecd7-186">Esta é uma representação offline do conjunto de registros e as atualizações dele não alteram as respostas de DNS até que você execute Set-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-186">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="4ecd7-187">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ecd7-187">OUTPUTS</span></span>

### <span data-ttu-id="4ecd7-188">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4ecd7-188">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="4ecd7-189">Esse cmdlet retorna o objeto **Recordset** modificado.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-189">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="4ecd7-190">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ecd7-190">NOTES</span></span>

## <span data-ttu-id="4ecd7-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ecd7-191">RELATED LINKS</span></span>

[<span data-ttu-id="4ecd7-192">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="4ecd7-192">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="4ecd7-193">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4ecd7-193">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="4ecd7-194">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4ecd7-194">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
