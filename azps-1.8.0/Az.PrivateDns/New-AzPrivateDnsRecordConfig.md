---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: fc5686e22167613550b236bd234c649317ba8cca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599784"
---
# <span data-ttu-id="597e8-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="597e8-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="597e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="597e8-102">SYNOPSIS</span></span>
<span data-ttu-id="597e8-103">Cria um novo objeto local de registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="597e8-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="597e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="597e8-104">SYNTAX</span></span>

### <span data-ttu-id="597e8-105">A (padrão)</span><span class="sxs-lookup"><span data-stu-id="597e8-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="597e8-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="597e8-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="597e8-107">MX</span><span class="sxs-lookup"><span data-stu-id="597e8-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="597e8-108">PTR</span><span class="sxs-lookup"><span data-stu-id="597e8-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="597e8-109">LOCALIZADO</span><span class="sxs-lookup"><span data-stu-id="597e8-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="597e8-110">SRV</span><span class="sxs-lookup"><span data-stu-id="597e8-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="597e8-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="597e8-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="597e8-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="597e8-112">DESCRIPTION</span></span>
<span data-ttu-id="597e8-113">O cmdlet New-AzPrivateDnsRecordConfig cria um objeto PSPrivateDnsRecord local.</span><span class="sxs-lookup"><span data-stu-id="597e8-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="597e8-114">Uma matriz desses objetos é passada para o cmdlet New-AzPrivateDnsRecordSet usando o parâmetro PrivateDnsRecord para especificar os registros a serem criados no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="597e8-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="597e8-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="597e8-115">EXAMPLES</span></span>

### <span data-ttu-id="597e8-116">Exemplo 1: criar um conjunto de registros do tipo A</span><span class="sxs-lookup"><span data-stu-id="597e8-116">Example 1: Create a RecordSet of type A</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="597e8-117">Este exemplo cria um conjunto de registros chamado www na zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="597e8-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="597e8-118">O conjunto de registros é do tipo A e tem uma TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="597e8-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="597e8-119">Ele contém um único registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="597e8-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="597e8-120">Exemplo 2: criar um conjunto de registros do tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="597e8-120">Example 2: Create a RecordSet of type AAAA</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="597e8-121">Este exemplo cria um conjunto de registros chamado www na zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="597e8-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="597e8-122">O conjunto de registros é do tipo AAAA e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="597e8-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="597e8-123">Ele contém um único registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="597e8-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="597e8-124">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="597e8-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="597e8-125">Exemplo 3: criar um conjunto de registros do tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="597e8-125">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="597e8-126">Este exemplo cria um conjunto de registros chamado www na zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="597e8-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="597e8-127">O conjunto de registros é do tipo CNAME e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="597e8-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="597e8-128">Ele contém um único registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="597e8-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="597e8-129">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="597e8-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="597e8-130">Exemplo 4: criar um conjunto de registros do tipo MX</span><span class="sxs-lookup"><span data-stu-id="597e8-130">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="597e8-131">Esse comando cria um conjunto de registros chamado www na zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="597e8-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="597e8-132">O conjunto de registros é do tipo MX e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="597e8-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="597e8-133">Ele contém um único registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="597e8-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="597e8-134">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="597e8-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="597e8-135">Exemplo 5: criar um conjunto de registros do tipo PTR</span><span class="sxs-lookup"><span data-stu-id="597e8-135">Example 5: Create a RecordSet of type PTR</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="597e8-136">Esse comando cria um conjunto de registros chamado 4 na zona privada 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="597e8-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="597e8-137">O conjunto de registros é do tipo PTR e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="597e8-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="597e8-138">Ele contém um único registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="597e8-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="597e8-139">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="597e8-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="597e8-140">Exemplo 6: criar um conjunto de registros do tipo SRV</span><span class="sxs-lookup"><span data-stu-id="597e8-140">Example 6: Create a RecordSet of type SRV</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="597e8-141">Esse comando cria um conjunto de registros chamado _sip. _ TCP na zona particular myzone.com.</span><span class="sxs-lookup"><span data-stu-id="597e8-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="597e8-142">O conjunto de registros é do tipo SRV e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="597e8-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="597e8-143">Ele contém um único registro DNS privado, apontando para o endereço de IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="597e8-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="597e8-144">O serviço (SIP) e o protocolo (TCP) são especificados como parte do nome do conjunto de registros, não como parte dos dados do registro.</span><span class="sxs-lookup"><span data-stu-id="597e8-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="597e8-145">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="597e8-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="597e8-146">Exemplo 7: criar um conjunto de registros do tipo TXT</span><span class="sxs-lookup"><span data-stu-id="597e8-146">Example 7: Create a RecordSet of type TXT</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="597e8-147">Esse comando cria um conjunto de registros chamado texto na zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="597e8-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="597e8-148">O conjunto de registros é do tipo TXT e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="597e8-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="597e8-149">Ele contém um único registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="597e8-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="597e8-150">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="597e8-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="597e8-151">OS</span><span class="sxs-lookup"><span data-stu-id="597e8-151">PARAMETERS</span></span>

### <span data-ttu-id="597e8-152">-CNAME</span><span class="sxs-lookup"><span data-stu-id="597e8-152">-Cname</span></span>
<span data-ttu-id="597e8-153">O nome canônico do registro CNAME a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="597e8-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="597e8-154">Não deve ser relativo ao nome da zona.</span><span class="sxs-lookup"><span data-stu-id="597e8-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="597e8-155">Não deve ter um ponto de terminação</span><span class="sxs-lookup"><span data-stu-id="597e8-155">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597e8-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="597e8-156">-DefaultProfile</span></span>
<span data-ttu-id="597e8-157">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="597e8-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="597e8-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="597e8-158">-Exchange</span></span>
<span data-ttu-id="597e8-159">O host do mail Exchange para o registro MX a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="597e8-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="597e8-160">Não deve ser relativo ao nome da zona.</span><span class="sxs-lookup"><span data-stu-id="597e8-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="597e8-161">Não deve ter um ponto de terminação</span><span class="sxs-lookup"><span data-stu-id="597e8-161">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597e8-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="597e8-162">-Ipv4Address</span></span>
<span data-ttu-id="597e8-163">O endereço IPv4 do registro a a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="597e8-163">The IPv4 address for the A record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597e8-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="597e8-164">-Ipv6Address</span></span>
<span data-ttu-id="597e8-165">O endereço IPv6 para o registro AAAA a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="597e8-165">The IPv6 address for the AAAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597e8-166">-Porta</span><span class="sxs-lookup"><span data-stu-id="597e8-166">-Port</span></span>
<span data-ttu-id="597e8-167">O número da porta do registro SRV a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="597e8-167">The port number for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597e8-168">-Preferência</span><span class="sxs-lookup"><span data-stu-id="597e8-168">-Preference</span></span>
<span data-ttu-id="597e8-169">O valor de preferência para o registro MX a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="597e8-169">The preference value for the MX record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597e8-170">-Priority</span><span class="sxs-lookup"><span data-stu-id="597e8-170">-Priority</span></span>
<span data-ttu-id="597e8-171">O registro SRV do valor de prioridade a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="597e8-171">The priority value SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597e8-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="597e8-172">-Ptrdname</span></span>
<span data-ttu-id="597e8-173">O host de destino para o registro PTR a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="597e8-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="597e8-174">Não deve ser relativo ao nome da zona.</span><span class="sxs-lookup"><span data-stu-id="597e8-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="597e8-175">Não deve ter um ponto de terminação</span><span class="sxs-lookup"><span data-stu-id="597e8-175">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597e8-176">-Destino</span><span class="sxs-lookup"><span data-stu-id="597e8-176">-Target</span></span>
<span data-ttu-id="597e8-177">O host de destino para o registro SRV a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="597e8-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="597e8-178">Não deve ser relativo ao nome da zona.</span><span class="sxs-lookup"><span data-stu-id="597e8-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="597e8-179">Não deve ter um ponto de terminação</span><span class="sxs-lookup"><span data-stu-id="597e8-179">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597e8-180">-Valor</span><span class="sxs-lookup"><span data-stu-id="597e8-180">-Value</span></span>
<span data-ttu-id="597e8-181">O valor de texto do registro TXT a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="597e8-181">The text value for the TXT record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597e8-182">-Weight</span><span class="sxs-lookup"><span data-stu-id="597e8-182">-Weight</span></span>
<span data-ttu-id="597e8-183">O valor de peso para o registro SRV a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="597e8-183">The weight value for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597e8-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="597e8-184">CommonParameters</span></span>
<span data-ttu-id="597e8-185">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="597e8-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="597e8-186">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="597e8-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="597e8-187">SENSORES</span><span class="sxs-lookup"><span data-stu-id="597e8-187">INPUTS</span></span>

### <span data-ttu-id="597e8-188">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="597e8-188">None</span></span>

## <span data-ttu-id="597e8-189">EXIBE</span><span class="sxs-lookup"><span data-stu-id="597e8-189">OUTPUTS</span></span>

### <span data-ttu-id="597e8-190">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="597e8-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="597e8-191">INFORMA</span><span class="sxs-lookup"><span data-stu-id="597e8-191">NOTES</span></span>

## <span data-ttu-id="597e8-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="597e8-192">RELATED LINKS</span></span>
