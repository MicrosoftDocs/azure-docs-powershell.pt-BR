---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: e00b31783554b8ea70760809c36f23a6a62575ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776727"
---
# <span data-ttu-id="5931a-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="5931a-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="5931a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5931a-102">SYNOPSIS</span></span>
<span data-ttu-id="5931a-103">Remove um registro DNS de um objeto de conjunto de registros local.</span><span class="sxs-lookup"><span data-stu-id="5931a-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="5931a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5931a-104">SYNTAX</span></span>

### <span data-ttu-id="5931a-105">Um</span><span class="sxs-lookup"><span data-stu-id="5931a-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="5931a-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="5931a-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="5931a-107">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="5931a-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="5931a-108">MX</span><span class="sxs-lookup"><span data-stu-id="5931a-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="5931a-109">PTR</span><span class="sxs-lookup"><span data-stu-id="5931a-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="5931a-110">LOCALIZADO</span><span class="sxs-lookup"><span data-stu-id="5931a-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="5931a-111">SRV</span><span class="sxs-lookup"><span data-stu-id="5931a-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="5931a-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="5931a-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="5931a-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5931a-113">DESCRIPTION</span></span>
<span data-ttu-id="5931a-114">O cmdlet **Remove-AzDnsRecordConfig** remove um registro de DNS (sistema de nomes de domínio) de um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="5931a-114">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="5931a-115">O objeto **Recordset** é um objeto offline, e as alterações feitas a ele não alteram as respostas de DNS até que você execute o cmdlet Set-AzDnsRecordSet para persistir a alteração no serviço DNS do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5931a-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="5931a-116">Para remover um registro, todos os campos desse tipo de registro devem corresponder exatamente.</span><span class="sxs-lookup"><span data-stu-id="5931a-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="5931a-117">Não é possível adicionar ou remover registros SOA.</span><span class="sxs-lookup"><span data-stu-id="5931a-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="5931a-118">Os registros SOA são automaticamente criados quando uma zona DNS é criada e excluída automaticamente quando a zona DNS é excluída.</span><span class="sxs-lookup"><span data-stu-id="5931a-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="5931a-119">Você pode passar o objeto **Recordset** para esse cmdlet como um parâmetro ou usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="5931a-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="5931a-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5931a-120">EXAMPLES</span></span>

### <span data-ttu-id="5931a-121">Exemplo 1: remover um registro A de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="5931a-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="5931a-122">Este exemplo remove um registro A de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="5931a-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="5931a-123">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="5931a-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="5931a-124">Para remover completamente um conjunto de registros, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5931a-124">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="5931a-125">Exemplo 2: remover um registro AAAA de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="5931a-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="5931a-126">Este exemplo remove um registro AAAA de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="5931a-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="5931a-127">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="5931a-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="5931a-128">Para remover completamente um conjunto de registros, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5931a-128">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="5931a-129">Exemplo 3: remover um registro CNAME de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="5931a-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="5931a-130">Este exemplo remove um registro CNAME de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="5931a-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="5931a-131">Como um conjunto de registros CNAME pode conter no máximo um registro, o resultado é um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="5931a-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="5931a-132">Exemplo 4: remover um registro MX de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="5931a-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="5931a-133">Este exemplo remove um registro MX de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="5931a-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="5931a-134">O nome do registro "@" indica um conjunto de registros na zona Apex.</span><span class="sxs-lookup"><span data-stu-id="5931a-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="5931a-135">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="5931a-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="5931a-136">Para remover completamente um conjunto de registros, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5931a-136">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="5931a-137">Exemplo 5: remover um registro NS de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="5931a-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="5931a-138">Este exemplo remove um registro NS de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="5931a-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="5931a-139">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="5931a-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="5931a-140">Para remover completamente um conjunto de registros, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5931a-140">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="5931a-141">Exemplo 6: remover um registro PTR de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="5931a-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="5931a-142">Este exemplo remove um registro PTR de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="5931a-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="5931a-143">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="5931a-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="5931a-144">Para remover completamente um conjunto de registros, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5931a-144">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="5931a-145">Exemplo 7: remover um registro SRV de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="5931a-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="5931a-146">Este exemplo remove um registro SRV de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="5931a-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="5931a-147">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="5931a-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="5931a-148">Para remover completamente um conjunto de registros, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5931a-148">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="5931a-149">Exemplo 8: remover um registro TXT de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="5931a-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="5931a-150">Este exemplo remove um registro TXT de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="5931a-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="5931a-151">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="5931a-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="5931a-152">Para remover completamente um conjunto de registros, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5931a-152">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="5931a-153">OS</span><span class="sxs-lookup"><span data-stu-id="5931a-153">PARAMETERS</span></span>

### <span data-ttu-id="5931a-154">-CNAME</span><span class="sxs-lookup"><span data-stu-id="5931a-154">-Cname</span></span>
<span data-ttu-id="5931a-155">Especifica o nome de domínio para um registro de nome canônico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="5931a-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="5931a-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="5931a-156">-Exchange</span></span>
<span data-ttu-id="5931a-157">Especifica o nome do servidor do servidor de mensagens para um registro de troca de email (MX).</span><span class="sxs-lookup"><span data-stu-id="5931a-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="5931a-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="5931a-158">-Ipv4Address</span></span>
<span data-ttu-id="5931a-159">Especifica um endereço IPv4 para um registro A.</span><span class="sxs-lookup"><span data-stu-id="5931a-159">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="5931a-160">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="5931a-160">-Ipv6Address</span></span>
<span data-ttu-id="5931a-161">Especifica um endereço IPv6 para um registro AAAA.</span><span class="sxs-lookup"><span data-stu-id="5931a-161">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="5931a-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="5931a-162">-Nsdname</span></span>
<span data-ttu-id="5931a-163">Especifica o servidor de nomes para um registro de servidor de nomes (NS).</span><span class="sxs-lookup"><span data-stu-id="5931a-163">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="5931a-164">-Porta</span><span class="sxs-lookup"><span data-stu-id="5931a-164">-Port</span></span>
<span data-ttu-id="5931a-165">Especifica a porta para um registro de serviço (SRV).</span><span class="sxs-lookup"><span data-stu-id="5931a-165">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="5931a-166">-Preferência</span><span class="sxs-lookup"><span data-stu-id="5931a-166">-Preference</span></span>
<span data-ttu-id="5931a-167">Especifica a preferência para um registro MX.</span><span class="sxs-lookup"><span data-stu-id="5931a-167">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="5931a-168">-Priority</span><span class="sxs-lookup"><span data-stu-id="5931a-168">-Priority</span></span>
<span data-ttu-id="5931a-169">Especifica a prioridade para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="5931a-169">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="5931a-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="5931a-170">-Ptrdname</span></span>
<span data-ttu-id="5931a-171">Especifica o nome de domínio de destino de um registro de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="5931a-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="5931a-172">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="5931a-172">-RecordSet</span></span>
<span data-ttu-id="5931a-173">Especifica o objeto **Recordset** que contém o registro a remover.</span><span class="sxs-lookup"><span data-stu-id="5931a-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="5931a-174">-Destino</span><span class="sxs-lookup"><span data-stu-id="5931a-174">-Target</span></span>
<span data-ttu-id="5931a-175">Especifica o destino para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="5931a-175">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="5931a-176">-Valor</span><span class="sxs-lookup"><span data-stu-id="5931a-176">-Value</span></span>
<span data-ttu-id="5931a-177">Especifica o valor de um registro TXT.</span><span class="sxs-lookup"><span data-stu-id="5931a-177">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="5931a-178">-Weight</span><span class="sxs-lookup"><span data-stu-id="5931a-178">-Weight</span></span>
<span data-ttu-id="5931a-179">Especifica o peso para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="5931a-179">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="5931a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5931a-180">CommonParameters</span></span>
<span data-ttu-id="5931a-181">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5931a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5931a-182">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5931a-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5931a-183">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5931a-183">INPUTS</span></span>

### <span data-ttu-id="5931a-184">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5931a-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="5931a-185">Você pode canalizar um objeto **DnsRecordSet** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5931a-185">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="5931a-186">Esta é uma representação offline do conjunto de registros e as atualizações dele não alteram as respostas de DNS até que você execute Set-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5931a-186">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzDnsRecordSet.</span></span>

## <span data-ttu-id="5931a-187">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5931a-187">OUTPUTS</span></span>

### <span data-ttu-id="5931a-188">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5931a-188">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="5931a-189">Esse cmdlet retorna o objeto **Recordset** modificado.</span><span class="sxs-lookup"><span data-stu-id="5931a-189">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="5931a-190">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5931a-190">NOTES</span></span>

## <span data-ttu-id="5931a-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5931a-191">RELATED LINKS</span></span>

[<span data-ttu-id="5931a-192">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="5931a-192">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="5931a-193">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5931a-193">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="5931a-194">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5931a-194">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
