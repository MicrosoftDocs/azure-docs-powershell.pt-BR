---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: f1731cb0eceb4474c233db859c3f4edb10461fe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889493"
---
# <span data-ttu-id="c0b0f-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c0b0f-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="c0b0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b0f-103">Cria um conjunto de registros DNS.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="c0b0f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c0b0f-104">SYNTAX</span></span>

### <span data-ttu-id="c0b0f-105">Campos (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c0b0f-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0b0f-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="c0b0f-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0b0f-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="c0b0f-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0b0f-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="c0b0f-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0b0f-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c0b0f-109">DESCRIPTION</span></span>
<span data-ttu-id="c0b0f-110">O cmdlet **New-AzDnsRecordSet** cria um novo registro DNS (Sistema de Nomes de Domínio) definido com o nome especificado e digite na zona especificada.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="c0b0f-111">Um **objeto RecordSet** é um conjunto de registros DNS com o mesmo nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="c0b0f-112">Observe que o nome é relativo à zona e não ao nome totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="c0b0f-113">O *parâmetro DnsRecords* especifica os registros no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="c0b0f-114">Esse parâmetro usa uma matriz de registros DNS, construída usando New-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="c0b0f-115">Você pode usar o operador de pipeline para passar um objeto **DnsZone** para esse cmdlet, ou pode passar um **objeto DnsZone** como o parâmetro *Zone* ou, como alternativa, pode especificar a zona pelo nome.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="c0b0f-116">Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c0b0f-117">Se um **RecordSet** correspondente já existir (mesmo nome e tipo de registro), você deverá especificar o parâmetro *Overwrite,* caso contrário, o cmdlet não criará um **novo RecordSet** .</span><span class="sxs-lookup"><span data-stu-id="c0b0f-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="c0b0f-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0b0f-118">EXAMPLES</span></span>

### <span data-ttu-id="c0b0f-119">Exemplo 1: Criar um RecordSet do tipo A</span><span class="sxs-lookup"><span data-stu-id="c0b0f-119">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="c0b0f-120">Este exemplo cria um **RecordSet** denominado www na zona myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c0b0f-121">O conjunto de registros é do tipo A e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="c0b0f-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c0b0f-122">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="c0b0f-123">Exemplo 2: Criar um RecordSet do tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="c0b0f-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c0b0f-124">Este exemplo cria um **RecordSet** denominado www na zona myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c0b0f-125">O conjunto de registros é do tipo AAAA e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="c0b0f-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c0b0f-126">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-126">It contains a single DNS record.</span></span>
<span data-ttu-id="c0b0f-127">Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c0b0f-128">Exemplo 3: Criar um RecordSet do tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="c0b0f-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c0b0f-129">Este exemplo cria um **RecordSet** denominado www na zona myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c0b0f-130">O conjunto de registros é do tipo CNAME e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="c0b0f-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c0b0f-131">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-131">It contains a single DNS record.</span></span>
<span data-ttu-id="c0b0f-132">Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c0b0f-133">Exemplo 4: Criar um RecordSet do tipo MX</span><span class="sxs-lookup"><span data-stu-id="c0b0f-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c0b0f-134">Este comando cria um **RecordSet** denominado www na zona myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c0b0f-135">O conjunto de registros é do tipo MX e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="c0b0f-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c0b0f-136">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-136">It contains a single DNS record.</span></span>
<span data-ttu-id="c0b0f-137">Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c0b0f-138">Exemplo 5: Criar um RecordSet do tipo NS</span><span class="sxs-lookup"><span data-stu-id="c0b0f-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c0b0f-139">Este comando cria um **RecordSet** chamado ns1 na zona myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="c0b0f-140">O conjunto de registros é do tipo NS e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="c0b0f-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c0b0f-141">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-141">It contains a single DNS record.</span></span>
<span data-ttu-id="c0b0f-142">Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c0b0f-143">Exemplo 6: Criar um RecordSet do tipo PTR</span><span class="sxs-lookup"><span data-stu-id="c0b0f-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="c0b0f-144">Este comando cria um **RecordSet** chamado 4 na zona 3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="c0b0f-145">O conjunto de registros é do tipo PTR e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="c0b0f-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c0b0f-146">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-146">It contains a single DNS record.</span></span>
<span data-ttu-id="c0b0f-147">Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c0b0f-148">Exemplo 7: Criar um RecordSet do tipo SRV</span><span class="sxs-lookup"><span data-stu-id="c0b0f-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c0b0f-149">Este comando cria um **RecordSet** chamado _sip._tcp na zona myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="c0b0f-150">O conjunto de registros é do tipo SRV e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="c0b0f-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c0b0f-151">Ele contém um único registro DNS, apontando para o endereço IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="c0b0f-152">O serviço (sip) e o protocolo (tcp) são especificados como parte do nome do conjunto de registros, não como parte dos dados do registro.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="c0b0f-153">Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c0b0f-154">Exemplo 8: Criar um RecordSet do tipo TXT</span><span class="sxs-lookup"><span data-stu-id="c0b0f-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c0b0f-155">Este comando cria um **texto chamado RecordSet** na zona myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="c0b0f-156">O conjunto de registros é do tipo TXT e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="c0b0f-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c0b0f-157">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-157">It contains a single DNS record.</span></span>
<span data-ttu-id="c0b0f-158">Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c0b0f-159">Exemplo 9: Criar um RecordSet no véreo de zona</span><span class="sxs-lookup"><span data-stu-id="c0b0f-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c0b0f-160">Este comando cria um **RecordSet** no véreo (ou raiz) da zona myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="c0b0f-161">Para fazer isso, o nome do conjunto de registros é especificado como "@" (incluindo aspas duplas).</span><span class="sxs-lookup"><span data-stu-id="c0b0f-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="c0b0f-162">Não é possível criar registros CNAME no vérme de uma zona.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="c0b0f-163">Essa é uma restrição dos padrões DNS; não é uma limitação do DNS do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="c0b0f-164">Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c0b0f-165">Exemplo 10: Criar um conjunto de registros curinga</span><span class="sxs-lookup"><span data-stu-id="c0b0f-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c0b0f-166">Este comando cria um **RecordSet** chamado \* na zona myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="c0b0f-167">Este é um conjunto de registros curinga.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-167">This is a wildcard record set.</span></span>
<span data-ttu-id="c0b0f-168">Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c0b0f-169">Exemplo 11: Criar um conjunto de registros vazio</span><span class="sxs-lookup"><span data-stu-id="c0b0f-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="c0b0f-170">Este comando cria um **RecordSet** denominado www na zona myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c0b0f-171">O conjunto de registros é do tipo A e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="c0b0f-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c0b0f-172">Este é um conjunto de registros vazio, que atua como um espaço reservado para o qual você pode adicionar registros posteriormente.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="c0b0f-173">Exemplo 12: Criar um conjunto de registros e suprimir toda a confirmação</span><span class="sxs-lookup"><span data-stu-id="c0b0f-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="c0b0f-174">Este comando cria um **RecordSet**.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="c0b0f-175">O *parâmetro Overwrite* garante que esse conjunto de registros sobrescreva qualquer conjunto de registros pré-existentes com o mesmo nome e tipo (os registros existentes nesse conjunto de registros são perdidos).</span><span class="sxs-lookup"><span data-stu-id="c0b0f-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="c0b0f-176">O *parâmetro Confirm* com um valor de $False suprime o prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="c0b0f-177">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c0b0f-177">PARAMETERS</span></span>

### <span data-ttu-id="c0b0f-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b0f-178">-DefaultProfile</span></span>
<span data-ttu-id="c0b0f-179">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c0b0f-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0b0f-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="c0b0f-180">-DnsRecords</span></span>
<span data-ttu-id="c0b0f-181">Especifica a matriz de registros DNS a incluir no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="c0b0f-182">Você pode usar o cmdlet New-AzDnsRecordConfig para criar objetos de registro DNS.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="c0b0f-183">Confira os exemplos para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-183">See the examples for more information.</span></span>

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

### <span data-ttu-id="c0b0f-184">-Metadados</span><span class="sxs-lookup"><span data-stu-id="c0b0f-184">-Metadata</span></span>
<span data-ttu-id="c0b0f-185">Especifica uma matriz de metadados a ser associada ao RecordSet.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="c0b0f-186">Os metadados são especificados usando pares de valores de nome representados como tabelas de hash, por exemplo @{"dept"="shopping";" env"="production"}.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

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

### <span data-ttu-id="c0b0f-187">-Name</span><span class="sxs-lookup"><span data-stu-id="c0b0f-187">-Name</span></span>
<span data-ttu-id="c0b0f-188">Especifica o nome do **RecordSet** a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="c0b0f-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="c0b0f-189">-Overwrite</span></span>
<span data-ttu-id="c0b0f-190">Indica que esse cmdlet substitui o **RecordSet** especificado se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="c0b0f-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="c0b0f-191">-RecordType</span></span>
<span data-ttu-id="c0b0f-192">Especifica o tipo de registro DNS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="c0b0f-193">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c0b0f-193">Valid values are:</span></span>
- <span data-ttu-id="c0b0f-194">A</span><span class="sxs-lookup"><span data-stu-id="c0b0f-194">A</span></span>
- <span data-ttu-id="c0b0f-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="c0b0f-195">AAAA</span></span>
- <span data-ttu-id="c0b0f-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="c0b0f-196">CNAME</span></span>
- <span data-ttu-id="c0b0f-197">MX</span><span class="sxs-lookup"><span data-stu-id="c0b0f-197">MX</span></span>
- <span data-ttu-id="c0b0f-198">NS</span><span class="sxs-lookup"><span data-stu-id="c0b0f-198">NS</span></span>
- <span data-ttu-id="c0b0f-199">PTR</span><span class="sxs-lookup"><span data-stu-id="c0b0f-199">PTR</span></span>
- <span data-ttu-id="c0b0f-200">SRV</span><span class="sxs-lookup"><span data-stu-id="c0b0f-200">SRV</span></span>
- <span data-ttu-id="c0b0f-201">Os registros SOA TXT são criados automaticamente quando a zona é criada e não podem ser criados manualmente.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="c0b0f-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0b0f-202">-ResourceGroupName</span></span>
<span data-ttu-id="c0b0f-203">Especifica o grupo de recursos que contém a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="c0b0f-204">Você também deve especificar o parâmetro *ZoneName* para especificar o nome da zona.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="c0b0f-205">Como alternativa, você pode especificar a zona e o grupo de recursos passando um objeto Zona DNS usando o *parâmetro Zone.*</span><span class="sxs-lookup"><span data-stu-id="c0b0f-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="c0b0f-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c0b0f-206">-TargetResourceId</span></span>
<span data-ttu-id="c0b0f-207">ID do Recurso de Destino de Alias.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-207">Alias Target Resource Id.</span></span>

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

### <span data-ttu-id="c0b0f-208">-Ttl</span><span class="sxs-lookup"><span data-stu-id="c0b0f-208">-Ttl</span></span>
<span data-ttu-id="c0b0f-209">Especifica o TTL (Time to Live) para o DNS RecordSet.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="c0b0f-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="c0b0f-210">-Zone</span></span>
<span data-ttu-id="c0b0f-211">Especifica o DnsZone no qual criar o **RecordSet**.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="c0b0f-212">Como alternativa, você pode especificar a zona usando os *parâmetros ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="c0b0f-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="c0b0f-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="c0b0f-213">-ZoneName</span></span>
<span data-ttu-id="c0b0f-214">Especifica o nome da zona na qual criar o **RecordSet**.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="c0b0f-215">Você também deve especificar o grupo de recursos que contém a zona usando o *parâmetro ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="c0b0f-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="c0b0f-216">Como alternativa, você pode especificar a zona e o grupo de recursos passando um objeto Zona DNS usando o *parâmetro Zone.*</span><span class="sxs-lookup"><span data-stu-id="c0b0f-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="c0b0f-217">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0b0f-217">-Confirm</span></span>
<span data-ttu-id="c0b0f-218">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0b0f-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0b0f-219">-WhatIf</span></span>
<span data-ttu-id="c0b0f-220">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0b0f-221">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0b0f-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b0f-222">CommonParameters</span></span>
<span data-ttu-id="c0b0f-223">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b0f-224">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0b0f-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b0f-225">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0b0f-225">INPUTS</span></span>

### <span data-ttu-id="c0b0f-226">System.String</span><span class="sxs-lookup"><span data-stu-id="c0b0f-226">System.String</span></span>

### <span data-ttu-id="c0b0f-227">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="c0b0f-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="c0b0f-228">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="c0b0f-228">System.UInt32</span></span>

### <span data-ttu-id="c0b0f-229">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="c0b0f-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="c0b0f-230">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c0b0f-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c0b0f-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span><span class="sxs-lookup"><span data-stu-id="c0b0f-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="c0b0f-232">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c0b0f-232">OUTPUTS</span></span>

### <span data-ttu-id="c0b0f-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c0b0f-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="c0b0f-234">NOTES</span><span class="sxs-lookup"><span data-stu-id="c0b0f-234">NOTES</span></span>
<span data-ttu-id="c0b0f-235">Você pode usar o *parâmetro Confirm* para controlar se esse cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c0b0f-236">Por padrão, o cmdlet solicita que você confirme se a variável $ConfirmPreference Windows PowerShell tem um valor médio ou inferior.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="c0b0f-237">Se você especificar *Confirm* ou *Confirm:$True*, este cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-237">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="c0b0f-238">Se você especificar *Confirm:$False*, o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="c0b0f-238">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c0b0f-239">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0b0f-239">RELATED LINKS</span></span>

[<span data-ttu-id="c0b0f-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c0b0f-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="c0b0f-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c0b0f-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="c0b0f-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c0b0f-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="c0b0f-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c0b0f-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="c0b0f-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c0b0f-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
