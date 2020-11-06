---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 97d87464f49d9f43d6ab6fb08d0cd8034560a108
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433135"
---
# <span data-ttu-id="c5d7a-101">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c5d7a-101">Remove-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="c5d7a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d7a-103">Remove um registro DNS de um objeto de conjunto de registros local.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-103">Removes a DNS record from a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5d7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5d7a-104">SYNTAX</span></span>

### <span data-ttu-id="c5d7a-105">Um</span><span class="sxs-lookup"><span data-stu-id="c5d7a-105">A</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5d7a-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="c5d7a-106">AAAA</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5d7a-107">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="c5d7a-107">NS</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5d7a-108">MX</span><span class="sxs-lookup"><span data-stu-id="c5d7a-108">MX</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5d7a-109">PTR</span><span class="sxs-lookup"><span data-stu-id="c5d7a-109">PTR</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5d7a-110">LOCALIZADO</span><span class="sxs-lookup"><span data-stu-id="c5d7a-110">TXT</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5d7a-111">SRV</span><span class="sxs-lookup"><span data-stu-id="c5d7a-111">SRV</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5d7a-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="c5d7a-112">CNAME</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5d7a-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5d7a-113">DESCRIPTION</span></span>
<span data-ttu-id="c5d7a-114">O cmdlet **Remove-AzureRmDnsRecordConfig** remove um registro de DNS (sistema de nomes de domínio) de um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-114">The **Remove-AzureRmDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="c5d7a-115">O objeto **Recordset** é um objeto offline, e as alterações feitas a ele não alteram as respostas de DNS até que você execute o cmdlet Set-AzureRmDnsRecordSet para persistir a alteração no serviço DNS do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="c5d7a-116">Para remover um registro, todos os campos desse tipo de registro devem corresponder exatamente.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="c5d7a-117">Não é possível adicionar ou remover registros SOA.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="c5d7a-118">Os registros SOA são automaticamente criados quando uma zona DNS é criada e excluída automaticamente quando a zona DNS é excluída.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="c5d7a-119">Você pode passar o objeto **Recordset** para esse cmdlet como um parâmetro ou usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="c5d7a-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5d7a-120">EXAMPLES</span></span>

### <span data-ttu-id="c5d7a-121">Exemplo 1: remover um registro A de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c5d7a-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5d7a-122">Este exemplo remove um registro A de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="c5d7a-123">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="c5d7a-124">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-124">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="c5d7a-125">Exemplo 2: remover um registro AAAA de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c5d7a-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5d7a-126">Este exemplo remove um registro AAAA de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="c5d7a-127">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="c5d7a-128">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-128">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="c5d7a-129">Exemplo 3: remover um registro CNAME de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c5d7a-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5d7a-130">Este exemplo remove um registro CNAME de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="c5d7a-131">Como um conjunto de registros CNAME pode conter no máximo um registro, o resultado é um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="c5d7a-132">Exemplo 4: remover um registro MX de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c5d7a-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5d7a-133">Este exemplo remove um registro MX de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="c5d7a-134">O nome do registro "@" indica um conjunto de registros na zona Apex.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="c5d7a-135">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="c5d7a-136">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-136">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="c5d7a-137">Exemplo 5: remover um registro NS de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c5d7a-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5d7a-138">Este exemplo remove um registro NS de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="c5d7a-139">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="c5d7a-140">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-140">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="c5d7a-141">Exemplo 6: remover um registro PTR de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c5d7a-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5d7a-142">Este exemplo remove um registro PTR de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="c5d7a-143">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="c5d7a-144">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-144">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="c5d7a-145">Exemplo 7: remover um registro SRV de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c5d7a-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5d7a-146">Este exemplo remove um registro SRV de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="c5d7a-147">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="c5d7a-148">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-148">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="c5d7a-149">Exemplo 8: remover um registro TXT de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c5d7a-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5d7a-150">Este exemplo remove um registro TXT de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="c5d7a-151">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="c5d7a-152">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-152">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="c5d7a-153">OS</span><span class="sxs-lookup"><span data-stu-id="c5d7a-153">PARAMETERS</span></span>

### <span data-ttu-id="c5d7a-154">-CNAME</span><span class="sxs-lookup"><span data-stu-id="c5d7a-154">-Cname</span></span>
<span data-ttu-id="c5d7a-155">Especifica o nome de domínio para um registro de nome canônico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="c5d7a-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="c5d7a-156">-Exchange</span></span>
<span data-ttu-id="c5d7a-157">Especifica o nome do servidor do servidor de mensagens para um registro de troca de email (MX).</span><span class="sxs-lookup"><span data-stu-id="c5d7a-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="c5d7a-158">-Ipv4Address</span></span>
<span data-ttu-id="c5d7a-159">Especifica um endereço IPv4 para um registro A.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-159">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-160">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="c5d7a-160">-Ipv6Address</span></span>
<span data-ttu-id="c5d7a-161">Especifica um endereço IPv6 para um registro AAAA.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-161">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="c5d7a-162">-Nsdname</span></span>
<span data-ttu-id="c5d7a-163">Especifica o servidor de nomes para um registro de servidor de nomes (NS).</span><span class="sxs-lookup"><span data-stu-id="c5d7a-163">Specifies the name server for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-164">-Porta</span><span class="sxs-lookup"><span data-stu-id="c5d7a-164">-Port</span></span>
<span data-ttu-id="c5d7a-165">Especifica a porta para um registro de serviço (SRV).</span><span class="sxs-lookup"><span data-stu-id="c5d7a-165">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-166">-Preferência</span><span class="sxs-lookup"><span data-stu-id="c5d7a-166">-Preference</span></span>
<span data-ttu-id="c5d7a-167">Especifica a preferência para um registro MX.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-167">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-168">-Priority</span><span class="sxs-lookup"><span data-stu-id="c5d7a-168">-Priority</span></span>
<span data-ttu-id="c5d7a-169">Especifica a prioridade para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-169">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="c5d7a-170">-Ptrdname</span></span>
<span data-ttu-id="c5d7a-171">Especifica o nome de domínio de destino de um registro de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="c5d7a-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-172">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="c5d7a-172">-RecordSet</span></span>
<span data-ttu-id="c5d7a-173">Especifica o objeto **Recordset** que contém o registro a remover.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-174">-Destino</span><span class="sxs-lookup"><span data-stu-id="c5d7a-174">-Target</span></span>
<span data-ttu-id="c5d7a-175">Especifica o destino para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-175">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-176">-Valor</span><span class="sxs-lookup"><span data-stu-id="c5d7a-176">-Value</span></span>
<span data-ttu-id="c5d7a-177">Especifica o valor de um registro TXT.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-177">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-178">-Weight</span><span class="sxs-lookup"><span data-stu-id="c5d7a-178">-Weight</span></span>
<span data-ttu-id="c5d7a-179">Especifica o peso para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-179">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d7a-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d7a-180">-DefaultProfile</span></span>
<span data-ttu-id="c5d7a-181">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-181">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5d7a-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d7a-182">CommonParameters</span></span>
<span data-ttu-id="c5d7a-183">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d7a-184">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5d7a-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d7a-185">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5d7a-185">INPUTS</span></span>

### <span data-ttu-id="c5d7a-186">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c5d7a-186">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="c5d7a-187">Você pode canalizar um objeto **DnsRecordSet** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-187">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="c5d7a-188">Esta é uma representação offline do conjunto de registros e as atualizações dele não alteram as respostas de DNS até que você execute Set-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-188">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="c5d7a-189">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5d7a-189">OUTPUTS</span></span>

### <span data-ttu-id="c5d7a-190">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c5d7a-190">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="c5d7a-191">Esse cmdlet retorna o objeto **Recordset** modificado.</span><span class="sxs-lookup"><span data-stu-id="c5d7a-191">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="c5d7a-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5d7a-192">NOTES</span></span>

## <span data-ttu-id="c5d7a-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5d7a-193">RELATED LINKS</span></span>

[<span data-ttu-id="c5d7a-194">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c5d7a-194">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="c5d7a-195">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c5d7a-195">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="c5d7a-196">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c5d7a-196">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
