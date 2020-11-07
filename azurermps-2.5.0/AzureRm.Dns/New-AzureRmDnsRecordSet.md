---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce82a1bae63fafcf0d221d0c2ce6d8e82e8e8e12
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785531"
---
# <span data-ttu-id="0a037-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a037-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="0a037-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a037-102">SYNOPSIS</span></span>
<span data-ttu-id="0a037-103">Cria um conjunto de registros DNS.</span><span class="sxs-lookup"><span data-stu-id="0a037-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a037-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a037-104">SYNTAX</span></span>

### <span data-ttu-id="0a037-105">Campos</span><span class="sxs-lookup"><span data-stu-id="0a037-105">Fields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a037-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="0a037-106">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a037-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a037-107">DESCRIPTION</span></span>
<span data-ttu-id="0a037-108">O cmdlet **New-AzureRmDnsRecordSet** cria um novo conjunto de registros DNS (sistema de nomes de domínio) com o nome e o tipo especificados na zona especificada.</span><span class="sxs-lookup"><span data-stu-id="0a037-108">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="0a037-109">Um objeto **Recordset** é um conjunto de registros DNS com o mesmo nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="0a037-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="0a037-110">Observe que o nome é relativo à zona e não o nome totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="0a037-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="0a037-111">O parâmetro *DnsRecords* especifica os registros no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="0a037-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="0a037-112">Esse parâmetro usa uma matriz de registros DNS, construídos usando New-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="0a037-112">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>

<span data-ttu-id="0a037-113">Você pode usar o operador de pipeline para passar um objeto **dnsZone** para esse cmdlet, ou pode passar um objeto **dnsZone** como o parâmetro de *zona* ou, como alternativa, pode especificar a zona por nome.</span><span class="sxs-lookup"><span data-stu-id="0a037-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="0a037-114">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="0a037-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="0a037-115">Se um **conjunto de registros** correspondente já existir (mesmo nome e tipo de registro), você deverá especificar o parâmetro *overwrite* , caso contrário, o cmdlet não criará um novo **conjunto de registros** .</span><span class="sxs-lookup"><span data-stu-id="0a037-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="0a037-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a037-116">EXAMPLES</span></span>

### <span data-ttu-id="0a037-117">Exemplo 1: criar um conjunto de registros do tipo A</span><span class="sxs-lookup"><span data-stu-id="0a037-117">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0a037-118">Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0a037-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0a037-119">O conjunto de registros é do tipo A e tem uma TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0a037-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0a037-120">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0a037-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="0a037-121">Exemplo 2: criar um conjunto de registros do tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="0a037-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0a037-122">Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0a037-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0a037-123">O conjunto de registros é do tipo AAAA e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0a037-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0a037-124">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0a037-124">It contains a single DNS record.</span></span>

<span data-ttu-id="0a037-125">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0a037-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a037-126">Exemplo 3: criar um conjunto de registros do tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="0a037-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0a037-127">Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0a037-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0a037-128">O conjunto de registros é do tipo CNAME e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0a037-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0a037-129">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0a037-129">It contains a single DNS record.</span></span>

<span data-ttu-id="0a037-130">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0a037-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a037-131">Exemplo 4: criar um conjunto de registros do tipo MX</span><span class="sxs-lookup"><span data-stu-id="0a037-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0a037-132">Esse comando cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0a037-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0a037-133">O conjunto de registros é do tipo MX e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0a037-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0a037-134">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0a037-134">It contains a single DNS record.</span></span>

<span data-ttu-id="0a037-135">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0a037-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a037-136">Exemplo 5: criar um conjunto de registros do tipo NS</span><span class="sxs-lookup"><span data-stu-id="0a037-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0a037-137">Esse comando cria um **conjunto de registros** chamado ns1 na zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0a037-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="0a037-138">O conjunto de registros é do tipo NS e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0a037-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0a037-139">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0a037-139">It contains a single DNS record.</span></span>

<span data-ttu-id="0a037-140">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0a037-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a037-141">Exemplo 6: criar um conjunto de registros do tipo PTR</span><span class="sxs-lookup"><span data-stu-id="0a037-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="0a037-142">Esse comando cria um **conjunto de registros** chamado 4 na zona 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="0a037-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="0a037-143">O conjunto de registros é do tipo PTR e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0a037-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0a037-144">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0a037-144">It contains a single DNS record.</span></span>

<span data-ttu-id="0a037-145">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0a037-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a037-146">Exemplo 7: criar um conjunto de registros do tipo SRV</span><span class="sxs-lookup"><span data-stu-id="0a037-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0a037-147">Esse comando cria um **conjunto de registros** chamado _sip. _ TCP na zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0a037-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="0a037-148">O conjunto de registros é do tipo SRV e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0a037-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0a037-149">Ele contém um único registro DNS, apontando para o endereço de IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="0a037-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="0a037-150">O serviço (SIP) e o protocolo (TCP) são especificados como parte do nome do conjunto de registros, não como parte dos dados do registro.</span><span class="sxs-lookup"><span data-stu-id="0a037-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="0a037-151">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0a037-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a037-152">Exemplo 8: criar um conjunto de registros do tipo TXT</span><span class="sxs-lookup"><span data-stu-id="0a037-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0a037-153">Esse comando cria um **conjunto de registros** chamado texto na zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0a037-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="0a037-154">O conjunto de registros é do tipo TXT e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0a037-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0a037-155">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0a037-155">It contains a single DNS record.</span></span>

<span data-ttu-id="0a037-156">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0a037-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a037-157">Exemplo 9: criar um conjunto de registros na zona Apex</span><span class="sxs-lookup"><span data-stu-id="0a037-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0a037-158">Esse comando cria um **conjunto de registros** no Apex (ou raiz) da região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0a037-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="0a037-159">Para fazer isso, o nome do conjunto de registros é especificado como "@" (incluindo as aspas duplas).</span><span class="sxs-lookup"><span data-stu-id="0a037-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="0a037-160">Não é possível criar registros CNAME na Apex de uma zona.</span><span class="sxs-lookup"><span data-stu-id="0a037-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="0a037-161">Isso é uma restrição dos padrões de DNS; Ele não é uma limitação do Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="0a037-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="0a037-162">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0a037-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a037-163">Exemplo 10: criar um conjunto de registros curinga</span><span class="sxs-lookup"><span data-stu-id="0a037-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0a037-164">Esse comando cria um **conjunto de registros** chamado \* na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0a037-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="0a037-165">Este é um conjunto de registros curinga.</span><span class="sxs-lookup"><span data-stu-id="0a037-165">This is a wildcard record set.</span></span>

<span data-ttu-id="0a037-166">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0a037-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a037-167">Exemplo 11: criar um conjunto de registros vazio</span><span class="sxs-lookup"><span data-stu-id="0a037-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="0a037-168">Esse comando cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0a037-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0a037-169">O conjunto de registros é do tipo A e tem uma TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0a037-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0a037-170">Esse é um conjunto de registros vazio, que atua como um espaço reservado para o qual você pode adicionar registros mais tarde.</span><span class="sxs-lookup"><span data-stu-id="0a037-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="0a037-171">Exemplo 12: criar um conjunto de registros e suprimir todas as confirmações</span><span class="sxs-lookup"><span data-stu-id="0a037-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="0a037-172">Esse comando cria um **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="0a037-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="0a037-173">O parâmetro overwrite garante que esse registro *substitua* o conjunto de registros preexistentes com o mesmo nome e tipo (os registros existentes nesse conjunto de registros são perdidos).</span><span class="sxs-lookup"><span data-stu-id="0a037-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="0a037-174">O parâmetro *Confirm* com um valor de $false suprime o prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="0a037-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="0a037-175">OS</span><span class="sxs-lookup"><span data-stu-id="0a037-175">PARAMETERS</span></span>

### <span data-ttu-id="0a037-176">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="0a037-176">-DnsRecords</span></span>
<span data-ttu-id="0a037-177">Especifica a matriz de registros DNS a serem incluídos no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="0a037-177">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="0a037-178">Você pode usar o cmdlet New-AzureRmDnsRecordConfig para criar objetos de registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0a037-178">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="0a037-179">Consulte os exemplos para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="0a037-179">See the examples for more information.</span></span>

```yaml
Type: DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a037-180">-Force</span><span class="sxs-lookup"><span data-stu-id="0a037-180">-Force</span></span>
<span data-ttu-id="0a037-181">Esse parâmetro é preterido para esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a037-181">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="0a037-182">Ela será removida em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="0a037-182">It will be removed in a future release.</span></span>

<span data-ttu-id="0a037-183">Para controlar se esse cmdlet solicita confirmação, use o parâmetro *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="0a037-183">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="0a037-184">-Metadados</span><span class="sxs-lookup"><span data-stu-id="0a037-184">-Metadata</span></span>
<span data-ttu-id="0a037-185">Especifica uma matriz de metadados a serem associados ao conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="0a037-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="0a037-186">Os metadados são especificados usando pares de nome-valor representados como tabelas de hash, por exemplo, @ (@ {"Name" = "Dept"; "Valor" = "compra"}, @ {"nome" = "env"; "Valor" = "produção"}).</span><span class="sxs-lookup"><span data-stu-id="0a037-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

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

### <span data-ttu-id="0a037-187">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a037-187">-Name</span></span>
<span data-ttu-id="0a037-188">Especifica o nome do **conjunto de registros** a ser criado.</span><span class="sxs-lookup"><span data-stu-id="0a037-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="0a037-189">-Substituir</span><span class="sxs-lookup"><span data-stu-id="0a037-189">-Overwrite</span></span>
<span data-ttu-id="0a037-190">Indica que esse cmdlet substitui o **conjunto de registros** especificado se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="0a037-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="0a037-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="0a037-191">-RecordType</span></span>
<span data-ttu-id="0a037-192">Especifica o tipo de registro DNS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="0a037-192">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="0a037-193">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0a037-193">Valid values are:</span></span>

- <span data-ttu-id="0a037-194">Um</span><span class="sxs-lookup"><span data-stu-id="0a037-194">A</span></span>
- <span data-ttu-id="0a037-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="0a037-195">AAAA</span></span>
- <span data-ttu-id="0a037-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="0a037-196">CNAME</span></span>
- <span data-ttu-id="0a037-197">MX</span><span class="sxs-lookup"><span data-stu-id="0a037-197">MX</span></span>
- <span data-ttu-id="0a037-198">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="0a037-198">NS</span></span>
- <span data-ttu-id="0a037-199">PTR</span><span class="sxs-lookup"><span data-stu-id="0a037-199">PTR</span></span>
- <span data-ttu-id="0a037-200">SRV</span><span class="sxs-lookup"><span data-stu-id="0a037-200">SRV</span></span>
- <span data-ttu-id="0a037-201">LOCALIZADO</span><span class="sxs-lookup"><span data-stu-id="0a037-201">TXT</span></span>

<span data-ttu-id="0a037-202">Os registros SOA são criados automaticamente quando a zona é criada e não podem ser criadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="0a037-202">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a037-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a037-203">-ResourceGroupName</span></span>
<span data-ttu-id="0a037-204">Especifica o grupo de recursos que contém a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="0a037-204">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="0a037-205">Você também deve especificar o parâmetro *zonename* para especificar o nome da zona.</span><span class="sxs-lookup"><span data-stu-id="0a037-205">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="0a037-206">Você também pode especificar a zona e o grupo de recursos, passando um objeto de zona DNS usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="0a037-206">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a037-207">-TTL</span><span class="sxs-lookup"><span data-stu-id="0a037-207">-Ttl</span></span>
<span data-ttu-id="0a037-208">Especifica o tempo de vida útil (TTL) do conjunto de registros DNS.</span><span class="sxs-lookup"><span data-stu-id="0a037-208">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a037-209">-Zone</span><span class="sxs-lookup"><span data-stu-id="0a037-209">-Zone</span></span>
<span data-ttu-id="0a037-210">Especifica o DnsZone no qual criar o **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="0a037-210">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="0a037-211">Você também pode especificar a zona usando os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="0a037-211">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a037-212">-Zonename</span><span class="sxs-lookup"><span data-stu-id="0a037-212">-ZoneName</span></span>
<span data-ttu-id="0a037-213">Especifica o nome da zona na qual criar o conjunto de **registros**.</span><span class="sxs-lookup"><span data-stu-id="0a037-213">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="0a037-214">Você também deve especificar o grupo de recursos que contém a zona usando o parâmetro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="0a037-214">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="0a037-215">Você também pode especificar a zona e o grupo de recursos, passando um objeto de zona DNS usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="0a037-215">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a037-216">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0a037-216">-Confirm</span></span>
<span data-ttu-id="0a037-217">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a037-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a037-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a037-218">-WhatIf</span></span>
<span data-ttu-id="0a037-219">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0a037-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a037-220">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a037-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a037-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a037-221">CommonParameters</span></span>
<span data-ttu-id="0a037-222">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a037-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a037-223">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a037-223">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a037-224">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a037-224">INPUTS</span></span>

### <span data-ttu-id="0a037-225">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="0a037-225">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="0a037-226">Você pode canalizar um objeto DnsZone para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a037-226">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="0a037-227">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a037-227">OUTPUTS</span></span>

### <span data-ttu-id="0a037-228">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a037-228">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="0a037-229">Esse cmdlet retorna um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="0a037-229">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="0a037-230">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a037-230">NOTES</span></span>
<span data-ttu-id="0a037-231">Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="0a037-231">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="0a037-232">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.</span><span class="sxs-lookup"><span data-stu-id="0a037-232">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="0a037-233">Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="0a037-233">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="0a037-234">Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="0a037-234">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0a037-235">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a037-235">RELATED LINKS</span></span>

[<span data-ttu-id="0a037-236">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="0a037-236">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="0a037-237">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a037-237">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="0a037-238">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="0a037-238">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="0a037-239">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a037-239">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="0a037-240">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a037-240">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
