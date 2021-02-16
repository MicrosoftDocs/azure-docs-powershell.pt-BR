---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126986"
---
# <span data-ttu-id="92fbf-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="92fbf-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="92fbf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="92fbf-103">Cria um conjunto de registros DNS.</span><span class="sxs-lookup"><span data-stu-id="92fbf-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="92fbf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92fbf-104">SYNTAX</span></span>

### <span data-ttu-id="92fbf-105">Campos (Padrão)</span><span class="sxs-lookup"><span data-stu-id="92fbf-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92fbf-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="92fbf-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92fbf-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="92fbf-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92fbf-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="92fbf-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92fbf-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="92fbf-109">DESCRIPTION</span></span>
<span data-ttu-id="92fbf-110">O cmdlet **New-AzDnsRecordSet** cria um novo registro DNS (Sistema de Nomes de Domínio) definido com o nome especificado e o tipo na zona especificada.</span><span class="sxs-lookup"><span data-stu-id="92fbf-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="92fbf-111">Um **objeto RecordSet** é um conjunto de registros DNS com o mesmo nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="92fbf-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="92fbf-112">Observe que o nome é relativo à zona e não ao nome totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="92fbf-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="92fbf-113">O *parâmetro DnsRecords* especifica os registros no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="92fbf-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="92fbf-114">Esse parâmetro usa uma matriz de registros DNS, construída usando o New-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="92fbf-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="92fbf-115">Você pode usar o operador de pipeline para passar um objeto **DnsZone** para esse cmdlet, ou pode passar um objeto **DnsZone** como o parâmetro *Zona* ou, alternativamente, pode especificar a zona por nome.</span><span class="sxs-lookup"><span data-stu-id="92fbf-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="92fbf-116">Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="92fbf-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="92fbf-117">Se um **RecordSet** correspondente já existir (mesmo nome  e tipo de registro), você deverá especificar o parâmetro Substituir, caso contrário, o cmdlet não criará um novo **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="92fbf-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="92fbf-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="92fbf-118">EXAMPLES</span></span>

### <span data-ttu-id="92fbf-119">Exemplo 1: Criar um RecordSet do tipo A</span><span class="sxs-lookup"><span data-stu-id="92fbf-119">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="92fbf-120">Este exemplo cria um **RecordSet** denominado www na área myzone.com.</span><span class="sxs-lookup"><span data-stu-id="92fbf-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="92fbf-121">O conjunto de registros é do tipo A e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="92fbf-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="92fbf-122">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="92fbf-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="92fbf-123">Exemplo 2: Criar um RecordSet do tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="92fbf-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="92fbf-124">Este exemplo cria um **RecordSet** denominado www na área myzone.com.</span><span class="sxs-lookup"><span data-stu-id="92fbf-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="92fbf-125">O conjunto de registros é do tipo AAAA e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="92fbf-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="92fbf-126">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="92fbf-126">It contains a single DNS record.</span></span>
<span data-ttu-id="92fbf-127">Para criar um **Conjunto de Registros** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="92fbf-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="92fbf-128">Exemplo 3: Criar um RecordSet do tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="92fbf-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="92fbf-129">Este exemplo cria um **RecordSet** denominado www na área myzone.com.</span><span class="sxs-lookup"><span data-stu-id="92fbf-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="92fbf-130">O conjunto de registros é do tipo CNAME e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="92fbf-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="92fbf-131">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="92fbf-131">It contains a single DNS record.</span></span>
<span data-ttu-id="92fbf-132">Para criar um **Conjunto de Registros** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="92fbf-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="92fbf-133">Exemplo 4: Criar um RecordSet do tipo MX</span><span class="sxs-lookup"><span data-stu-id="92fbf-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="92fbf-134">Esse comando cria um **RecordSet** denominado www na área myzone.com.</span><span class="sxs-lookup"><span data-stu-id="92fbf-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="92fbf-135">O conjunto de registros é do tipo MX e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="92fbf-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="92fbf-136">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="92fbf-136">It contains a single DNS record.</span></span>
<span data-ttu-id="92fbf-137">Para criar um **Conjunto de Registros** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="92fbf-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="92fbf-138">Exemplo 5: Criar um RecordSet do tipo NS</span><span class="sxs-lookup"><span data-stu-id="92fbf-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="92fbf-139">Esse comando cria um **RecordSet** chamado ns1 na área myzone.com.</span><span class="sxs-lookup"><span data-stu-id="92fbf-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="92fbf-140">O conjunto de registros é do tipo NS e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="92fbf-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="92fbf-141">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="92fbf-141">It contains a single DNS record.</span></span>
<span data-ttu-id="92fbf-142">Para criar um **Conjunto de Registros** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="92fbf-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="92fbf-143">Exemplo 6: Criar um RecordSet do tipo PTR</span><span class="sxs-lookup"><span data-stu-id="92fbf-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="92fbf-144">Esse comando cria um **RecordSet** chamado 4 na zona 3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="92fbf-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="92fbf-145">O conjunto de registros é do tipo PTR e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="92fbf-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="92fbf-146">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="92fbf-146">It contains a single DNS record.</span></span>
<span data-ttu-id="92fbf-147">Para criar um **Conjunto de Registros** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="92fbf-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="92fbf-148">Exemplo 7: Criar um RecordSet do tipo SRV</span><span class="sxs-lookup"><span data-stu-id="92fbf-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="92fbf-149">Esse comando cria um **RecordSet** chamado _sip._tcp na área myzone.com.</span><span class="sxs-lookup"><span data-stu-id="92fbf-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="92fbf-150">O conjunto de registros é do tipo SRV e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="92fbf-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="92fbf-151">Ele contém um único registro DNS, apontando para o endereço IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="92fbf-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="92fbf-152">O serviço (sip) e o protocolo (tcp) são especificados como parte do nome do conjunto de registros, não como parte dos dados de registro.</span><span class="sxs-lookup"><span data-stu-id="92fbf-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="92fbf-153">Para criar um **Conjunto de Registros** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="92fbf-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="92fbf-154">Exemplo 8: Criar um RecordSet do tipo TXT</span><span class="sxs-lookup"><span data-stu-id="92fbf-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="92fbf-155">Esse comando cria um **Texto nomeado RecordSet** na área myzone.com.</span><span class="sxs-lookup"><span data-stu-id="92fbf-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="92fbf-156">O conjunto de registros é do tipo TXT e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="92fbf-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="92fbf-157">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="92fbf-157">It contains a single DNS record.</span></span>
<span data-ttu-id="92fbf-158">Para criar um **Conjunto de Registros** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="92fbf-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="92fbf-159">Exemplo 9: Criar um RecordSet no apex de zona</span><span class="sxs-lookup"><span data-stu-id="92fbf-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="92fbf-160">Esse comando cria **um RecordSet** no apex (ou raiz) da zona myzone.com.</span><span class="sxs-lookup"><span data-stu-id="92fbf-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="92fbf-161">Para fazer isso, o nome do conjunto de registros é especificado como "@" (incluindo as aspas duplas).</span><span class="sxs-lookup"><span data-stu-id="92fbf-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="92fbf-162">Não é possível criar registros CNAME no apex de uma zona.</span><span class="sxs-lookup"><span data-stu-id="92fbf-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="92fbf-163">Essa é uma restrição dos padrões DNS; não é uma limitação do DNS do Azure.</span><span class="sxs-lookup"><span data-stu-id="92fbf-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="92fbf-164">Para criar um **Conjunto de Registros** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="92fbf-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="92fbf-165">Exemplo 10: Criar um conjunto de registros curinga</span><span class="sxs-lookup"><span data-stu-id="92fbf-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="92fbf-166">Esse comando cria um **RecordSet** chamado \* na área myzone.com.</span><span class="sxs-lookup"><span data-stu-id="92fbf-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="92fbf-167">Este é um conjunto de registros curinga.</span><span class="sxs-lookup"><span data-stu-id="92fbf-167">This is a wildcard record set.</span></span>
<span data-ttu-id="92fbf-168">Para criar um **Conjunto de Registros** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="92fbf-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="92fbf-169">Exemplo 11: Criar um conjunto de registros vazio</span><span class="sxs-lookup"><span data-stu-id="92fbf-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="92fbf-170">Esse comando cria um **RecordSet** denominado www na área myzone.com.</span><span class="sxs-lookup"><span data-stu-id="92fbf-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="92fbf-171">O conjunto de registros é do tipo A e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="92fbf-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="92fbf-172">Esse é um conjunto de registros vazio, que atua como um espaço reservado para o qual você pode adicionar registros posteriormente.</span><span class="sxs-lookup"><span data-stu-id="92fbf-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="92fbf-173">Exemplo 12: Criar um conjunto de registros e suprimir toda a confirmação</span><span class="sxs-lookup"><span data-stu-id="92fbf-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="92fbf-174">Esse comando cria um **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="92fbf-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="92fbf-175">O *parâmetro Substituir* garante que esse conjunto de registros sobrescreva qualquer conjunto de registros pré-existente com o mesmo nome e tipo (os registros existentes nesse conjunto de registros são perdidos).</span><span class="sxs-lookup"><span data-stu-id="92fbf-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="92fbf-176">O *parâmetro* Confirmar com um valor de $False suprime o prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="92fbf-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="92fbf-177">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92fbf-177">PARAMETERS</span></span>

### <span data-ttu-id="92fbf-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92fbf-178">-DefaultProfile</span></span>
<span data-ttu-id="92fbf-179">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="92fbf-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92fbf-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="92fbf-180">-DnsRecords</span></span>
<span data-ttu-id="92fbf-181">Especifica a matriz de registros DNS a ser incluído no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="92fbf-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="92fbf-182">Você pode usar o cmdlet New-AzDnsRecordConfig para criar objetos de registro DNS.</span><span class="sxs-lookup"><span data-stu-id="92fbf-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="92fbf-183">Confira os exemplos para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="92fbf-183">See the examples for more information.</span></span>

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

### <span data-ttu-id="92fbf-184">-Metadados</span><span class="sxs-lookup"><span data-stu-id="92fbf-184">-Metadata</span></span>
<span data-ttu-id="92fbf-185">Especifica uma matriz de metadados para associar ao Conjunto de Registros.</span><span class="sxs-lookup"><span data-stu-id="92fbf-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="92fbf-186">Os metadados são especificados usando pares de nome e valor que são representados como tabelas hash, por exemplo @{"dept"="shopping";" env"="production"}.</span><span class="sxs-lookup"><span data-stu-id="92fbf-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

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

### <span data-ttu-id="92fbf-187">-Nome</span><span class="sxs-lookup"><span data-stu-id="92fbf-187">-Name</span></span>
<span data-ttu-id="92fbf-188">Especifica o nome do **RecordSet a** ser criado.</span><span class="sxs-lookup"><span data-stu-id="92fbf-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="92fbf-189">-Substituir</span><span class="sxs-lookup"><span data-stu-id="92fbf-189">-Overwrite</span></span>
<span data-ttu-id="92fbf-190">Indica que esse cmdlet substitui o **RecordSet** especificado se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="92fbf-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="92fbf-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="92fbf-191">-RecordType</span></span>
<span data-ttu-id="92fbf-192">Especifica o tipo de registro DNS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="92fbf-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="92fbf-193">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="92fbf-193">Valid values are:</span></span>
- <span data-ttu-id="92fbf-194">Um</span><span class="sxs-lookup"><span data-stu-id="92fbf-194">A</span></span>
- <span data-ttu-id="92fbf-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="92fbf-195">AAAA</span></span>
- <span data-ttu-id="92fbf-196">Cname</span><span class="sxs-lookup"><span data-stu-id="92fbf-196">CNAME</span></span>
- <span data-ttu-id="92fbf-197">Mx</span><span class="sxs-lookup"><span data-stu-id="92fbf-197">MX</span></span>
- <span data-ttu-id="92fbf-198">Ns</span><span class="sxs-lookup"><span data-stu-id="92fbf-198">NS</span></span>
- <span data-ttu-id="92fbf-199">Ptr</span><span class="sxs-lookup"><span data-stu-id="92fbf-199">PTR</span></span>
- <span data-ttu-id="92fbf-200">Srv</span><span class="sxs-lookup"><span data-stu-id="92fbf-200">SRV</span></span>
- <span data-ttu-id="92fbf-201">Os registros TXT SOA são criados automaticamente quando a zona é criada e não podem ser criadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="92fbf-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="92fbf-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92fbf-202">-ResourceGroupName</span></span>
<span data-ttu-id="92fbf-203">Especifica o grupo de recursos que contém a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="92fbf-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="92fbf-204">Você também deve especificar o parâmetro *ZoneName* para especificar o nome da zona.</span><span class="sxs-lookup"><span data-stu-id="92fbf-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="92fbf-205">Como alternativa, você pode especificar a zona e o grupo de recursos passando um objeto de Zona DNS usando o *parâmetro Zona.*</span><span class="sxs-lookup"><span data-stu-id="92fbf-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="92fbf-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="92fbf-206">-TargetResourceId</span></span>
<span data-ttu-id="92fbf-207">ID do Recurso de Destino de Alias.</span><span class="sxs-lookup"><span data-stu-id="92fbf-207">Alias Target Resource Id.</span></span>

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

### <span data-ttu-id="92fbf-208">-Ttl</span><span class="sxs-lookup"><span data-stu-id="92fbf-208">-Ttl</span></span>
<span data-ttu-id="92fbf-209">Especifica o tempo de vida (TTL) para o Dns RecordSet.</span><span class="sxs-lookup"><span data-stu-id="92fbf-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="92fbf-210">-Zona</span><span class="sxs-lookup"><span data-stu-id="92fbf-210">-Zone</span></span>
<span data-ttu-id="92fbf-211">Especifica o DnsZone no qual criar o **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="92fbf-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="92fbf-212">Como alternativa, você pode especificar a zona usando os parâmetros *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="92fbf-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="92fbf-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="92fbf-213">-ZoneName</span></span>
<span data-ttu-id="92fbf-214">Especifica o nome da zona na qual se cria o **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="92fbf-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="92fbf-215">Você também deve especificar o grupo de recursos que contém a zona usando o parâmetro *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="92fbf-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="92fbf-216">Como alternativa, você pode especificar a zona e o grupo de recursos passando um objeto de Zona DNS usando o *parâmetro Zona.*</span><span class="sxs-lookup"><span data-stu-id="92fbf-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="92fbf-217">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="92fbf-217">-Confirm</span></span>
<span data-ttu-id="92fbf-218">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92fbf-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92fbf-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92fbf-219">-WhatIf</span></span>
<span data-ttu-id="92fbf-220">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="92fbf-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92fbf-221">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92fbf-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92fbf-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92fbf-222">CommonParameters</span></span>
<span data-ttu-id="92fbf-223">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92fbf-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92fbf-224">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92fbf-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92fbf-225">Entradas</span><span class="sxs-lookup"><span data-stu-id="92fbf-225">INPUTS</span></span>

### <span data-ttu-id="92fbf-226">System.String</span><span class="sxs-lookup"><span data-stu-id="92fbf-226">System.String</span></span>

### <span data-ttu-id="92fbf-227">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="92fbf-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="92fbf-228">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="92fbf-228">System.UInt32</span></span>

### <span data-ttu-id="92fbf-229">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="92fbf-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="92fbf-230">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="92fbf-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="92fbf-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span><span class="sxs-lookup"><span data-stu-id="92fbf-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="92fbf-232">Saídas</span><span class="sxs-lookup"><span data-stu-id="92fbf-232">OUTPUTS</span></span>

### <span data-ttu-id="92fbf-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="92fbf-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="92fbf-234">Notas</span><span class="sxs-lookup"><span data-stu-id="92fbf-234">NOTES</span></span>
<span data-ttu-id="92fbf-235">Você pode usar o *parâmetro Confirmar* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="92fbf-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="92fbf-236">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference Windows PowerShell tem um valor médio ou inferior.</span><span class="sxs-lookup"><span data-stu-id="92fbf-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="92fbf-237">Se você especificar *Confirmar* ou *Confirmar:$True,* este cmdlet solicitará que você confirme antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="92fbf-237">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="92fbf-238">Se você especificar *Confirm:$False,* o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="92fbf-238">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="92fbf-239">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92fbf-239">RELATED LINKS</span></span>

[<span data-ttu-id="92fbf-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="92fbf-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="92fbf-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="92fbf-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="92fbf-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="92fbf-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="92fbf-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="92fbf-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="92fbf-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="92fbf-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
