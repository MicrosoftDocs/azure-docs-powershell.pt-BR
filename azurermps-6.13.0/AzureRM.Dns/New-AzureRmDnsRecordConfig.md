---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 6c2acfe611a8b2c5ef9ecb11173ca9e5210e00e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426352"
---
# <span data-ttu-id="0ba21-101">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="0ba21-101">New-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="0ba21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ba21-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba21-103">Cria um novo objeto local de registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0ba21-103">Creates a new DNS record local object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ba21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ba21-104">SYNTAX</span></span>

### <span data-ttu-id="0ba21-105">Um</span><span class="sxs-lookup"><span data-stu-id="0ba21-105">A</span></span>
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ba21-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="0ba21-106">Aaaa</span></span>
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ba21-107">Série</span><span class="sxs-lookup"><span data-stu-id="0ba21-107">Ns</span></span>
```
New-AzureRmDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba21-108">MX</span><span class="sxs-lookup"><span data-stu-id="0ba21-108">Mx</span></span>
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ba21-109">PTR</span><span class="sxs-lookup"><span data-stu-id="0ba21-109">Ptr</span></span>
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba21-110">Localizado</span><span class="sxs-lookup"><span data-stu-id="0ba21-110">Txt</span></span>
```
New-AzureRmDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba21-111">SRV</span><span class="sxs-lookup"><span data-stu-id="0ba21-111">Srv</span></span>
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba21-112">CName</span><span class="sxs-lookup"><span data-stu-id="0ba21-112">CName</span></span>
```
New-AzureRmDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba21-113">Caa</span><span class="sxs-lookup"><span data-stu-id="0ba21-113">Caa</span></span>
```
New-AzureRmDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ba21-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0ba21-114">DESCRIPTION</span></span>
<span data-ttu-id="0ba21-115">O cmdlet **New-AzureRmDnsRecordConfig** cria um objeto **DnsRecord** local.</span><span class="sxs-lookup"><span data-stu-id="0ba21-115">The **New-AzureRmDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="0ba21-116">Uma matriz desses objetos é passada para o cmdlet New-AzureRmDnsRecordSet usando o parâmetro *DnsRecords* para especificar os registros a serem criados no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="0ba21-116">An array of these objects is passed to the New-AzureRmDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="0ba21-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ba21-117">EXAMPLES</span></span>

### <span data-ttu-id="0ba21-118">Exemplo 1: criar um conjunto de registros do tipo A</span><span class="sxs-lookup"><span data-stu-id="0ba21-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="0ba21-119">Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0ba21-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0ba21-120">O conjunto de registros é do tipo A e tem uma TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0ba21-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0ba21-121">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0ba21-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="0ba21-122">Exemplo 2: criar um conjunto de registros do tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="0ba21-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0ba21-123">Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0ba21-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0ba21-124">O conjunto de registros é do tipo AAAA e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0ba21-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0ba21-125">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0ba21-125">It contains a single DNS record.</span></span>
<span data-ttu-id="0ba21-126">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0ba21-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0ba21-127">Exemplo 3: criar um conjunto de registros do tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="0ba21-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0ba21-128">Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0ba21-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0ba21-129">O conjunto de registros é do tipo CNAME e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0ba21-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0ba21-130">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0ba21-130">It contains a single DNS record.</span></span>
<span data-ttu-id="0ba21-131">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0ba21-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0ba21-132">Exemplo 4: criar um conjunto de registros do tipo MX</span><span class="sxs-lookup"><span data-stu-id="0ba21-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0ba21-133">Esse comando cria um **conjunto de registros** chamado www na região MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0ba21-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="0ba21-134">O conjunto de registros é do tipo MX e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0ba21-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0ba21-135">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0ba21-135">It contains a single DNS record.</span></span>
<span data-ttu-id="0ba21-136">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0ba21-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0ba21-137">Exemplo 5: criar um conjunto de registros do tipo NS</span><span class="sxs-lookup"><span data-stu-id="0ba21-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0ba21-138">Esse comando cria um **conjunto de registros** chamado ns1 na zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0ba21-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="0ba21-139">O conjunto de registros é do tipo NS e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0ba21-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0ba21-140">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0ba21-140">It contains a single DNS record.</span></span>
<span data-ttu-id="0ba21-141">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0ba21-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0ba21-142">Exemplo 6: criar um conjunto de registros do tipo PTR</span><span class="sxs-lookup"><span data-stu-id="0ba21-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="0ba21-143">Esse comando cria um **conjunto de registros** chamado 4 na zona 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="0ba21-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="0ba21-144">O conjunto de registros é do tipo PTR e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0ba21-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0ba21-145">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0ba21-145">It contains a single DNS record.</span></span>
<span data-ttu-id="0ba21-146">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0ba21-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0ba21-147">Exemplo 7: criar um conjunto de registros do tipo SRV</span><span class="sxs-lookup"><span data-stu-id="0ba21-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0ba21-148">Esse comando cria um **conjunto de registros** chamado _sip. _ TCP na zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0ba21-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="0ba21-149">O conjunto de registros é do tipo SRV e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0ba21-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0ba21-150">Ele contém um único registro DNS, apontando para o endereço de IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="0ba21-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="0ba21-151">O serviço (SIP) e o protocolo (TCP) são especificados como parte do nome do conjunto de registros, não como parte dos dados do registro.</span><span class="sxs-lookup"><span data-stu-id="0ba21-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="0ba21-152">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0ba21-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0ba21-153">Exemplo 8: criar um conjunto de registros do tipo TXT</span><span class="sxs-lookup"><span data-stu-id="0ba21-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="0ba21-154">Esse comando cria um **conjunto de registros** chamado texto na zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="0ba21-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="0ba21-155">O conjunto de registros é do tipo TXT e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="0ba21-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="0ba21-156">Ele contém um único registro DNS.</span><span class="sxs-lookup"><span data-stu-id="0ba21-156">It contains a single DNS record.</span></span>
<span data-ttu-id="0ba21-157">Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="0ba21-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="0ba21-158">OS</span><span class="sxs-lookup"><span data-stu-id="0ba21-158">PARAMETERS</span></span>

### <span data-ttu-id="0ba21-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="0ba21-159">-CaaFlags</span></span>
<span data-ttu-id="0ba21-160">Os sinalizadores para o registro CAA a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0ba21-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="0ba21-161">Deve ser um número entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="0ba21-161">Must be a number between 0 and 255.</span></span>

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="0ba21-162">-CaaTag</span></span>
<span data-ttu-id="0ba21-163">O campo de marca do registro CAA a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0ba21-163">The tag field of the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="0ba21-164">-CaaValue</span></span>
<span data-ttu-id="0ba21-165">O campo de valor do registro CAA a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0ba21-165">The value field for the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-166">-CNAME</span><span class="sxs-lookup"><span data-stu-id="0ba21-166">-Cname</span></span>
<span data-ttu-id="0ba21-167">Especifica o nome de domínio para um registro de nome canônico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="0ba21-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba21-168">-DefaultProfile</span></span>
<span data-ttu-id="0ba21-169">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0ba21-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ba21-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="0ba21-170">-Exchange</span></span>
<span data-ttu-id="0ba21-171">Especifica o nome do servidor do servidor de mensagens para um registro de troca de email (MX).</span><span class="sxs-lookup"><span data-stu-id="0ba21-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="0ba21-172">-Ipv4Address</span></span>
<span data-ttu-id="0ba21-173">Especifica um endereço IPv4 para um registro A.</span><span class="sxs-lookup"><span data-stu-id="0ba21-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="0ba21-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="0ba21-174">-Ipv6Address</span></span>
<span data-ttu-id="0ba21-175">Especifica um endereço IPv6 para um registro AAAA.</span><span class="sxs-lookup"><span data-stu-id="0ba21-175">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="0ba21-176">-Nsdname</span></span>
<span data-ttu-id="0ba21-177">Especifica o nome do servidor de nomes para um registro de servidor de nomes (NS).</span><span class="sxs-lookup"><span data-stu-id="0ba21-177">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-178">-Porta</span><span class="sxs-lookup"><span data-stu-id="0ba21-178">-Port</span></span>
<span data-ttu-id="0ba21-179">Especifica a porta para um registro de serviço (SRV).</span><span class="sxs-lookup"><span data-stu-id="0ba21-179">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-180">-Preferência</span><span class="sxs-lookup"><span data-stu-id="0ba21-180">-Preference</span></span>
<span data-ttu-id="0ba21-181">Especifica a preferência para um registro MX.</span><span class="sxs-lookup"><span data-stu-id="0ba21-181">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-182">-Priority</span><span class="sxs-lookup"><span data-stu-id="0ba21-182">-Priority</span></span>
<span data-ttu-id="0ba21-183">Especifica a prioridade para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="0ba21-183">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="0ba21-184">-Ptrdname</span></span>
<span data-ttu-id="0ba21-185">Especifica o nome de domínio de destino de um registro de recurso de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="0ba21-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-186">-Destino</span><span class="sxs-lookup"><span data-stu-id="0ba21-186">-Target</span></span>
<span data-ttu-id="0ba21-187">Especifica o destino para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="0ba21-187">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-188">-Valor</span><span class="sxs-lookup"><span data-stu-id="0ba21-188">-Value</span></span>
<span data-ttu-id="0ba21-189">Especifica o valor de um registro TXT.</span><span class="sxs-lookup"><span data-stu-id="0ba21-189">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-190">-Weight</span><span class="sxs-lookup"><span data-stu-id="0ba21-190">-Weight</span></span>
<span data-ttu-id="0ba21-191">Especifica o peso para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="0ba21-191">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba21-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba21-192">CommonParameters</span></span>
<span data-ttu-id="0ba21-193">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ba21-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba21-194">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ba21-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba21-195">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0ba21-195">INPUTS</span></span>

### <span data-ttu-id="0ba21-196">System. String</span><span class="sxs-lookup"><span data-stu-id="0ba21-196">System.String</span></span>

### <span data-ttu-id="0ba21-197">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="0ba21-197">System.UInt16</span></span>

### <span data-ttu-id="0ba21-198">System. byte</span><span class="sxs-lookup"><span data-stu-id="0ba21-198">System.Byte</span></span>

## <span data-ttu-id="0ba21-199">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0ba21-199">OUTPUTS</span></span>

### <span data-ttu-id="0ba21-200">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="0ba21-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="0ba21-201">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0ba21-201">NOTES</span></span>

## <span data-ttu-id="0ba21-202">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ba21-202">RELATED LINKS</span></span>

[<span data-ttu-id="0ba21-203">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="0ba21-203">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="0ba21-204">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0ba21-204">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="0ba21-205">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="0ba21-205">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)
