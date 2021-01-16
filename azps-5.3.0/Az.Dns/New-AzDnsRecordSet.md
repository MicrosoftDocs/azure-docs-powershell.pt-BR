---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428336"
---
# <span data-ttu-id="5d5f4-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5d5f4-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="5d5f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5f4-103">Cria um conjunto de registros DNS.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="5d5f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d5f4-104">SYNTAX</span></span>

### <span data-ttu-id="5d5f4-105">Campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="5d5f4-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d5f4-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="5d5f4-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d5f4-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="5d5f4-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d5f4-108">Aliasobject</span><span class="sxs-lookup"><span data-stu-id="5d5f4-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d5f4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d5f4-109">DESCRIPTION</span></span>
<span data-ttu-id="5d5f4-110">O cmdlet **New-AzDnsRecordSet** cria um novo conjunto de registros DNS (sistema de nomes de domínio) com o nome e o tipo especificados na zona especificada.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="5d5f4-111">Um objeto **Recordset** é um conjunto de registros DNS com o mesmo nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="5d5f4-112">Observe que o nome é relativo à zona e não o nome totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="5d5f4-113">O parâmetro *DnsRecords* especifica os registros no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="5d5f4-114">Esse parâmetro usa uma matriz de registros DNS, construídos usando New-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="5d5f4-115">Você pode usar o operador de pipeline para passar um objeto **dnsZone** para esse cmdlet, ou pode passar um objeto **dnsZone** como o parâmetro de *zona* ou, como alternativa, pode especificar a zona por nome.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="5d5f4-116">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5d5f4-117">Se um **conjunto de registros** correspondente já existir (mesmo nome e tipo de registro), você deverá especificar o parâmetro *overwrite* , caso contrário, o cmdlet não criará um novo **conjunto de registros** .</span><span class="sxs-lookup"><span data-stu-id="5d5f4-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="5d5f4-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d5f4-118">EXAMPLES</span></span>

### <span data-ttu-id="5d5f4-119">Exemplo 1: criar um conjunto de registros do tipo A</span><span class="sxs-lookup"><span data-stu-id="5d5f4-119">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5d5f4-120">Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="5d5f4-121">O conjunto de registros é do tipo A e tem uma TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="5d5f4-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5d5f4-122">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="5d5f4-123">Exemplo 2: criar um conjunto de registros do tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="5d5f4-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5d5f4-124">Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="5d5f4-125">O conjunto de registros é do tipo AAAA e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="5d5f4-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5d5f4-126">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-126">It contains a single DNS record.</span></span>
<span data-ttu-id="5d5f4-127">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5d5f4-128">Exemplo 3: criar um conjunto de registros do tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="5d5f4-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5d5f4-129">Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="5d5f4-130">O conjunto de registros é do tipo CNAME e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="5d5f4-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5d5f4-131">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-131">It contains a single DNS record.</span></span>
<span data-ttu-id="5d5f4-132">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5d5f4-133">Exemplo 4: criar um conjunto de registros do tipo MX</span><span class="sxs-lookup"><span data-stu-id="5d5f4-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5d5f4-134">Esse comando cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="5d5f4-135">O conjunto de registros é do tipo MX e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="5d5f4-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5d5f4-136">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-136">It contains a single DNS record.</span></span>
<span data-ttu-id="5d5f4-137">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5d5f4-138">Exemplo 5: criar um conjunto de registros do tipo NS</span><span class="sxs-lookup"><span data-stu-id="5d5f4-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5d5f4-139">Esse comando cria um **conjunto de registros** chamado ns1 na zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="5d5f4-140">O conjunto de registros é do tipo NS e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="5d5f4-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5d5f4-141">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-141">It contains a single DNS record.</span></span>
<span data-ttu-id="5d5f4-142">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5d5f4-143">Exemplo 6: criar um conjunto de registros do tipo PTR</span><span class="sxs-lookup"><span data-stu-id="5d5f4-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="5d5f4-144">Esse comando cria um **conjunto de registros** chamado 4 na zona 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="5d5f4-145">O conjunto de registros é do tipo PTR e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="5d5f4-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5d5f4-146">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-146">It contains a single DNS record.</span></span>
<span data-ttu-id="5d5f4-147">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5d5f4-148">Exemplo 7: criar um conjunto de registros do tipo SRV</span><span class="sxs-lookup"><span data-stu-id="5d5f4-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5d5f4-149">Esse comando cria um **conjunto de registros** chamado _sip. _ TCP na zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="5d5f4-150">O conjunto de registros é do tipo SRV e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="5d5f4-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5d5f4-151">Ele contém um único registro DNS, apontando para o endereço de IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="5d5f4-152">O serviço (SIP) e o protocolo (TCP) são especificados como parte do nome do conjunto de registros, não como parte dos dados do registro.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="5d5f4-153">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5d5f4-154">Exemplo 8: criar um conjunto de registros do tipo TXT</span><span class="sxs-lookup"><span data-stu-id="5d5f4-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5d5f4-155">Esse comando cria um **conjunto de registros** chamado texto na zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="5d5f4-156">O conjunto de registros é do tipo TXT e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="5d5f4-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5d5f4-157">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-157">It contains a single DNS record.</span></span>
<span data-ttu-id="5d5f4-158">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5d5f4-159">Exemplo 9: criar um conjunto de registros na zona Apex</span><span class="sxs-lookup"><span data-stu-id="5d5f4-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5d5f4-160">Esse comando cria um **conjunto de registros** no Apex (ou raiz) da região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="5d5f4-161">Para fazer isso, o nome do conjunto de registros é especificado como "@" (incluindo as aspas duplas).</span><span class="sxs-lookup"><span data-stu-id="5d5f4-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="5d5f4-162">Não é possível criar registros CNAME na Apex de uma zona.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="5d5f4-163">Isso é uma restrição dos padrões de DNS; Ele não é uma limitação do Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="5d5f4-164">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5d5f4-165">Exemplo 10: criar um conjunto de registros curinga</span><span class="sxs-lookup"><span data-stu-id="5d5f4-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5d5f4-166">Esse comando cria um **conjunto de registros** chamado \* na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="5d5f4-167">Este é um conjunto de registros curinga.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-167">This is a wildcard record set.</span></span>
<span data-ttu-id="5d5f4-168">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5d5f4-169">Exemplo 11: criar um conjunto de registros vazio</span><span class="sxs-lookup"><span data-stu-id="5d5f4-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="5d5f4-170">Esse comando cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="5d5f4-171">O conjunto de registros é do tipo A e tem uma TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="5d5f4-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5d5f4-172">Esse é um conjunto de registros vazio, que atua como um espaço reservado para o qual você pode adicionar registros mais tarde.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="5d5f4-173">Exemplo 12: criar um conjunto de registros e suprimir todas as confirmações</span><span class="sxs-lookup"><span data-stu-id="5d5f4-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="5d5f4-174">Esse comando cria um **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="5d5f4-175">O parâmetro overwrite garante que esse registro *substitua* o conjunto de registros preexistentes com o mesmo nome e tipo (os registros existentes nesse conjunto de registros são perdidos).</span><span class="sxs-lookup"><span data-stu-id="5d5f4-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="5d5f4-176">O parâmetro *Confirm* com um valor de $false suprime o prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="5d5f4-177">OS</span><span class="sxs-lookup"><span data-stu-id="5d5f4-177">PARAMETERS</span></span>

### <span data-ttu-id="5d5f4-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5f4-178">-DefaultProfile</span></span>
<span data-ttu-id="5d5f4-179">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5d5f4-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d5f4-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="5d5f4-180">-DnsRecords</span></span>
<span data-ttu-id="5d5f4-181">Especifica a matriz de registros DNS a serem incluídos no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="5d5f4-182">Você pode usar o cmdlet New-AzDnsRecordConfig para criar objetos de registro DNS.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="5d5f4-183">Consulte os exemplos para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-183">See the examples for more information.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d5f4-184">-Metadados</span><span class="sxs-lookup"><span data-stu-id="5d5f4-184">-Metadata</span></span>
<span data-ttu-id="5d5f4-185">Especifica uma matriz de metadados a serem associados ao conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="5d5f4-186">Os metadados são especificados usando pares de nome-valor representados como tabelas de hash, por exemplo, @ {"Dept" = "shopping"; " env "=" Production "}.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

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

### <span data-ttu-id="5d5f4-187">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d5f4-187">-Name</span></span>
<span data-ttu-id="5d5f4-188">Especifica o nome do **conjunto de registros** a ser criado.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="5d5f4-189">-Substituir</span><span class="sxs-lookup"><span data-stu-id="5d5f4-189">-Overwrite</span></span>
<span data-ttu-id="5d5f4-190">Indica que esse cmdlet substitui o **conjunto de registros** especificado se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="5d5f4-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="5d5f4-191">-RecordType</span></span>
<span data-ttu-id="5d5f4-192">Especifica o tipo de registro DNS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="5d5f4-193">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="5d5f4-193">Valid values are:</span></span>
- <span data-ttu-id="5d5f4-194">Um</span><span class="sxs-lookup"><span data-stu-id="5d5f4-194">A</span></span>
- <span data-ttu-id="5d5f4-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="5d5f4-195">AAAA</span></span>
- <span data-ttu-id="5d5f4-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="5d5f4-196">CNAME</span></span>
- <span data-ttu-id="5d5f4-197">MX</span><span class="sxs-lookup"><span data-stu-id="5d5f4-197">MX</span></span>
- <span data-ttu-id="5d5f4-198">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="5d5f4-198">NS</span></span>
- <span data-ttu-id="5d5f4-199">PTR</span><span class="sxs-lookup"><span data-stu-id="5d5f4-199">PTR</span></span>
- <span data-ttu-id="5d5f4-200">SRV</span><span class="sxs-lookup"><span data-stu-id="5d5f4-200">SRV</span></span>
- <span data-ttu-id="5d5f4-201">Os registros TXT SOA são criados automaticamente quando a zona é criada e não podem ser criadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d5f4-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d5f4-202">-ResourceGroupName</span></span>
<span data-ttu-id="5d5f4-203">Especifica o grupo de recursos que contém a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="5d5f4-204">Você também deve especificar o parâmetro *zonename* para especificar o nome da zona.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="5d5f4-205">Você também pode especificar a zona e o grupo de recursos, passando um objeto de zona DNS usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="5d5f4-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d5f4-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="5d5f4-206">-TargetResourceId</span></span>
<span data-ttu-id="5d5f4-207">ID do recurso de destino do alias.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-207">Alias Target Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5f4-208">-TTL</span><span class="sxs-lookup"><span data-stu-id="5d5f4-208">-Ttl</span></span>
<span data-ttu-id="5d5f4-209">Especifica o tempo de vida útil (TTL) do conjunto de registros DNS.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d5f4-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="5d5f4-210">-Zone</span></span>
<span data-ttu-id="5d5f4-211">Especifica o DnsZone no qual criar o **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="5d5f4-212">Você também pode especificar a zona usando os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="5d5f4-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d5f4-213">-Zonename</span><span class="sxs-lookup"><span data-stu-id="5d5f4-213">-ZoneName</span></span>
<span data-ttu-id="5d5f4-214">Especifica o nome da zona na qual criar o conjunto de **registros**.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="5d5f4-215">Você também deve especificar o grupo de recursos que contém a zona usando o parâmetro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="5d5f4-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="5d5f4-216">Você também pode especificar a zona e o grupo de recursos, passando um objeto de zona DNS usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="5d5f4-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d5f4-217">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5d5f4-217">-Confirm</span></span>
<span data-ttu-id="5d5f4-218">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d5f4-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d5f4-219">-WhatIf</span></span>
<span data-ttu-id="5d5f4-220">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d5f4-221">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d5f4-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5f4-222">CommonParameters</span></span>
<span data-ttu-id="5d5f4-223">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5f4-224">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d5f4-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5f4-225">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d5f4-225">INPUTS</span></span>

### <span data-ttu-id="5d5f4-226">System. String</span><span class="sxs-lookup"><span data-stu-id="5d5f4-226">System.String</span></span>

### <span data-ttu-id="5d5f4-227">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="5d5f4-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="5d5f4-228">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="5d5f4-228">System.UInt32</span></span>

### <span data-ttu-id="5d5f4-229">Microsoft. Azure. Management. DNS. Models. RecordType</span><span class="sxs-lookup"><span data-stu-id="5d5f4-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="5d5f4-230">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5d5f4-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5d5f4-231">Microsoft. Azure. Commands. DNS. DnsRecordBase []</span><span class="sxs-lookup"><span data-stu-id="5d5f4-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="5d5f4-232">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d5f4-232">OUTPUTS</span></span>

### <span data-ttu-id="5d5f4-233">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5d5f4-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="5d5f4-234">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d5f4-234">NOTES</span></span>
<span data-ttu-id="5d5f4-235">Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5d5f4-236">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="5d5f4-237">Se você especificar *Confirm* ou *Confirm: $true*, esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-237">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="5d5f4-238">Se você especificar *Confirm: $false*, o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-238">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5d5f4-239">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d5f4-239">RELATED LINKS</span></span>

[<span data-ttu-id="5d5f4-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="5d5f4-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="5d5f4-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5d5f4-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="5d5f4-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="5d5f4-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="5d5f4-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5d5f4-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="5d5f4-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5d5f4-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
