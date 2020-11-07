---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6368cffa168772a384deb99f5a8388aef84f85b2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786113"
---
# <span data-ttu-id="31513-101">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="31513-101">New-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="31513-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31513-102">SYNOPSIS</span></span>
<span data-ttu-id="31513-103">Cria um novo objeto local de registro DNS.</span><span class="sxs-lookup"><span data-stu-id="31513-103">Creates a new DNS record local object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31513-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31513-104">SYNTAX</span></span>

### <span data-ttu-id="31513-105">Um</span><span class="sxs-lookup"><span data-stu-id="31513-105">A</span></span>
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="31513-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="31513-106">Aaaa</span></span>
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="31513-107">Série</span><span class="sxs-lookup"><span data-stu-id="31513-107">Ns</span></span>
```
New-AzureRmDnsRecordConfig -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="31513-108">MX</span><span class="sxs-lookup"><span data-stu-id="31513-108">Mx</span></span>
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="31513-109">PTR</span><span class="sxs-lookup"><span data-stu-id="31513-109">Ptr</span></span>
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="31513-110">Localizado</span><span class="sxs-lookup"><span data-stu-id="31513-110">Txt</span></span>
```
New-AzureRmDnsRecordConfig -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="31513-111">SRV</span><span class="sxs-lookup"><span data-stu-id="31513-111">Srv</span></span>
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="31513-112">CName</span><span class="sxs-lookup"><span data-stu-id="31513-112">CName</span></span>
```
New-AzureRmDnsRecordConfig -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="31513-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31513-113">DESCRIPTION</span></span>
<span data-ttu-id="31513-114">O cmdlet **New-AzureRmDnsRecordConfig** cria um objeto **DnsRecord** local.</span><span class="sxs-lookup"><span data-stu-id="31513-114">The **New-AzureRmDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="31513-115">Uma matriz desses objetos é passada para o cmdlet New-AzureRmDnsRecordSet usando o parâmetro *DnsRecords* para especificar os registros a serem criados no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="31513-115">An array of these objects is passed to the New-AzureRmDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="31513-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31513-116">EXAMPLES</span></span>

### <span data-ttu-id="31513-117">Exemplo 1: criar um conjunto de registros do tipo A</span><span class="sxs-lookup"><span data-stu-id="31513-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="31513-118">Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="31513-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="31513-119">O conjunto de registros é do tipo A e tem uma TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="31513-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="31513-120">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="31513-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="31513-121">Exemplo 2: criar um conjunto de registros do tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="31513-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="31513-122">Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="31513-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="31513-123">O conjunto de registros é do tipo AAAA e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="31513-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="31513-124">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="31513-124">It contains a single DNS record.</span></span>

<span data-ttu-id="31513-125">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="31513-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="31513-126">Exemplo 3: criar um conjunto de registros do tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="31513-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="31513-127">Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="31513-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="31513-128">O conjunto de registros é do tipo CNAME e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="31513-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="31513-129">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="31513-129">It contains a single DNS record.</span></span>

<span data-ttu-id="31513-130">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="31513-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="31513-131">Exemplo 4: criar um conjunto de registros do tipo MX</span><span class="sxs-lookup"><span data-stu-id="31513-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="31513-132">Esse comando cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="31513-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="31513-133">O conjunto de registros é do tipo MX e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="31513-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="31513-134">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="31513-134">It contains a single DNS record.</span></span>

<span data-ttu-id="31513-135">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="31513-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="31513-136">Exemplo 5: criar um conjunto de registros do tipo NS</span><span class="sxs-lookup"><span data-stu-id="31513-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="31513-137">Esse comando cria um **conjunto de registros** chamado ns1 na zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="31513-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="31513-138">O conjunto de registros é do tipo NS e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="31513-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="31513-139">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="31513-139">It contains a single DNS record.</span></span>

<span data-ttu-id="31513-140">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="31513-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="31513-141">Exemplo 6: criar um conjunto de registros do tipo PTR</span><span class="sxs-lookup"><span data-stu-id="31513-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="31513-142">Esse comando cria um **conjunto de registros** chamado 4 na zona 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="31513-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="31513-143">O conjunto de registros é do tipo PTR e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="31513-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="31513-144">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="31513-144">It contains a single DNS record.</span></span>

<span data-ttu-id="31513-145">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="31513-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="31513-146">Exemplo 7: criar um conjunto de registros do tipo SRV</span><span class="sxs-lookup"><span data-stu-id="31513-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="31513-147">Esse comando cria um **conjunto de registros** chamado _sip. _ TCP na zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="31513-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="31513-148">O conjunto de registros é do tipo SRV e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="31513-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="31513-149">Ele contém um único registro DNS, apontando para o endereço de IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="31513-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="31513-150">O serviço (SIP) e o protocolo (TCP) são especificados como parte do nome do conjunto de registros, não como parte dos dados do registro.</span><span class="sxs-lookup"><span data-stu-id="31513-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="31513-151">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="31513-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="31513-152">Exemplo 8: criar um conjunto de registros do tipo TXT</span><span class="sxs-lookup"><span data-stu-id="31513-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="31513-153">Esse comando cria um **conjunto de registros** chamado texto na zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="31513-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="31513-154">O conjunto de registros é do tipo TXT e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="31513-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="31513-155">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="31513-155">It contains a single DNS record.</span></span>

<span data-ttu-id="31513-156">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="31513-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="31513-157">OS</span><span class="sxs-lookup"><span data-stu-id="31513-157">PARAMETERS</span></span>

### <span data-ttu-id="31513-158">-CNAME</span><span class="sxs-lookup"><span data-stu-id="31513-158">-Cname</span></span>
<span data-ttu-id="31513-159">Especifica o nome de domínio para um registro de nome canônico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="31513-159">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31513-160">-Exchange</span><span class="sxs-lookup"><span data-stu-id="31513-160">-Exchange</span></span>
<span data-ttu-id="31513-161">Especifica o nome do servidor do servidor de mensagens para um registro de troca de email (MX).</span><span class="sxs-lookup"><span data-stu-id="31513-161">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31513-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="31513-162">-Ipv4Address</span></span>
<span data-ttu-id="31513-163">Especifica um endereço IPv4 para um registro A.</span><span class="sxs-lookup"><span data-stu-id="31513-163">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="31513-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="31513-164">-Ipv6Address</span></span>
<span data-ttu-id="31513-165">Especifica um endereço IPv6 para um registro AAAA.</span><span class="sxs-lookup"><span data-stu-id="31513-165">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31513-166">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="31513-166">-Nsdname</span></span>
<span data-ttu-id="31513-167">Especifica o nome do servidor de nomes para um registro de servidor de nomes (NS).</span><span class="sxs-lookup"><span data-stu-id="31513-167">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31513-168">-Porta</span><span class="sxs-lookup"><span data-stu-id="31513-168">-Port</span></span>
<span data-ttu-id="31513-169">Especifica a porta para um registro de serviço (SRV).</span><span class="sxs-lookup"><span data-stu-id="31513-169">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31513-170">-Preferência</span><span class="sxs-lookup"><span data-stu-id="31513-170">-Preference</span></span>
<span data-ttu-id="31513-171">Especifica a preferência para um registro MX.</span><span class="sxs-lookup"><span data-stu-id="31513-171">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31513-172">-Priority</span><span class="sxs-lookup"><span data-stu-id="31513-172">-Priority</span></span>
<span data-ttu-id="31513-173">Especifica a prioridade para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="31513-173">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31513-174">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="31513-174">-Ptrdname</span></span>
<span data-ttu-id="31513-175">Especifica o nome de domínio de destino de um registro de recurso de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="31513-175">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31513-176">-Destino</span><span class="sxs-lookup"><span data-stu-id="31513-176">-Target</span></span>
<span data-ttu-id="31513-177">Especifica o destino para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="31513-177">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31513-178">-Valor</span><span class="sxs-lookup"><span data-stu-id="31513-178">-Value</span></span>
<span data-ttu-id="31513-179">Especifica o valor de um registro TXT.</span><span class="sxs-lookup"><span data-stu-id="31513-179">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31513-180">-Weight</span><span class="sxs-lookup"><span data-stu-id="31513-180">-Weight</span></span>
<span data-ttu-id="31513-181">Especifica o peso para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="31513-181">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31513-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31513-182">CommonParameters</span></span>
<span data-ttu-id="31513-183">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31513-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31513-184">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31513-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31513-185">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31513-185">INPUTS</span></span>

### <span data-ttu-id="31513-186">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="31513-186">None.</span></span>

## <span data-ttu-id="31513-187">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31513-187">OUTPUTS</span></span>

### <span data-ttu-id="31513-188">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="31513-188">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="31513-189">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31513-189">NOTES</span></span>

## <span data-ttu-id="31513-190">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31513-190">RELATED LINKS</span></span>

[<span data-ttu-id="31513-191">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="31513-191">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="31513-192">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="31513-192">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="31513-193">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="31513-193">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)
