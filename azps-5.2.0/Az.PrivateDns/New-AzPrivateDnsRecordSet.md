---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 1a7042c94457f23302aa8d2899475d7b117e65b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262359"
---
# <span data-ttu-id="69a04-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="69a04-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="69a04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69a04-102">SYNOPSIS</span></span>
<span data-ttu-id="69a04-103">Cria um conjunto de registros em uma zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="69a04-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="69a04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69a04-104">SYNTAX</span></span>

### <span data-ttu-id="69a04-105">Campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="69a04-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a04-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="69a04-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a04-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="69a04-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69a04-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69a04-108">DESCRIPTION</span></span>
<span data-ttu-id="69a04-109">O cmdlet New-AzPrivateDnsRecordSet cria um novo conjunto de registros DNS (sistema de nomes de domínio) privado com o nome e o tipo especificados na zona privada especificada.</span><span class="sxs-lookup"><span data-stu-id="69a04-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="69a04-110">Um objeto RecordSet é um conjunto de registros DNS privados com o mesmo nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="69a04-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="69a04-111">Observe que o nome é relativo à zona privada e não ao nome totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="69a04-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="69a04-112">O parâmetro PrivateDnsRecord especifica os registros no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="69a04-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="69a04-113">Esse parâmetro usa uma matriz de registros DNS privados, construídos usando New-AzPrivateDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="69a04-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="69a04-114">Você pode usar o operador de pipeline para passar um objeto PSPrivateDnsZone para esse cmdlet, ou pode passar um objeto PSPrivateDnsZone como o parâmetro de zona ou pode especificar a zona pela ResourceId, ou também pode especificar a zona por nome.</span><span class="sxs-lookup"><span data-stu-id="69a04-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="69a04-115">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="69a04-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="69a04-116">Se um conjunto de registros correspondente já existir (mesmo nome e tipo de registro), você deverá especificar o parâmetro overwrite, caso contrário, o cmdlet não criará um novo conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="69a04-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="69a04-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69a04-117">EXAMPLES</span></span>

### <span data-ttu-id="69a04-118">Exemplo 1: criar um conjunto de registros do tipo A</span><span class="sxs-lookup"><span data-stu-id="69a04-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="69a04-119">Este exemplo cria um conjunto de registros chamado www na zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="69a04-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="69a04-120">O conjunto de registros é do tipo A e tem uma TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="69a04-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="69a04-121">Ele contém um único registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="69a04-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="69a04-122">Exemplo 2: criar um conjunto de registros do tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="69a04-122">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="69a04-123">Este exemplo cria um conjunto de registros chamado www na zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="69a04-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="69a04-124">O conjunto de registros é do tipo AAAA e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="69a04-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="69a04-125">Ele contém um único registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="69a04-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="69a04-126">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="69a04-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="69a04-127">Exemplo 3: criar um conjunto de registros do tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="69a04-127">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="69a04-128">Este exemplo cria um conjunto de registros chamado www na zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="69a04-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="69a04-129">O conjunto de registros é do tipo CNAME e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="69a04-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="69a04-130">Ele contém um único registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="69a04-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="69a04-131">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="69a04-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="69a04-132">Exemplo 4: criar um conjunto de registros do tipo MX</span><span class="sxs-lookup"><span data-stu-id="69a04-132">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="69a04-133">Esse comando cria um conjunto de registros chamado www na zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="69a04-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="69a04-134">O conjunto de registros é do tipo MX e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="69a04-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="69a04-135">Ele contém um único registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="69a04-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="69a04-136">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="69a04-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="69a04-137">Exemplo 5: criar um conjunto de registros do tipo PTR</span><span class="sxs-lookup"><span data-stu-id="69a04-137">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="69a04-138">Esse comando cria um conjunto de registros chamado 4 na zona privada 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="69a04-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="69a04-139">O conjunto de registros é do tipo PTR e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="69a04-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="69a04-140">Ele contém um único registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="69a04-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="69a04-141">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="69a04-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="69a04-142">Exemplo 6: criar um conjunto de registros do tipo SRV</span><span class="sxs-lookup"><span data-stu-id="69a04-142">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="69a04-143">Esse comando cria um conjunto de registros chamado _sip. _ TCP na zona particular myzone.com.</span><span class="sxs-lookup"><span data-stu-id="69a04-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="69a04-144">O conjunto de registros é do tipo SRV e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="69a04-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="69a04-145">Ele contém um único registro DNS privado, apontando para o endereço de IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="69a04-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="69a04-146">O serviço (SIP) e o protocolo (TCP) são especificados como parte do nome do conjunto de registros, não como parte dos dados do registro.</span><span class="sxs-lookup"><span data-stu-id="69a04-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="69a04-147">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="69a04-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="69a04-148">Exemplo 7: criar um conjunto de registros do tipo TXT</span><span class="sxs-lookup"><span data-stu-id="69a04-148">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="69a04-149">Esse comando cria um conjunto de registros chamado texto na zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="69a04-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="69a04-150">O conjunto de registros é do tipo TXT e tem um TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="69a04-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="69a04-151">Ele contém um único registro DNS privado.</span><span class="sxs-lookup"><span data-stu-id="69a04-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="69a04-152">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="69a04-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="69a04-153">Exemplo 8: criar um conjunto de registros na zona Apex</span><span class="sxs-lookup"><span data-stu-id="69a04-153">Example 8:  Create a RecordSet at the zone apex</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="69a04-154">Esse comando cria um conjunto de registros no Apex (ou raiz) da zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="69a04-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="69a04-155">Para fazer isso, o nome do conjunto de registros é especificado como "@" (incluindo as aspas duplas).</span><span class="sxs-lookup"><span data-stu-id="69a04-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="69a04-156">Não é possível criar registros CNAME na Apex de uma zona.</span><span class="sxs-lookup"><span data-stu-id="69a04-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="69a04-157">Isso é uma restrição dos padrões de DNS; Ele não é uma limitação do Azure particular DNS.</span><span class="sxs-lookup"><span data-stu-id="69a04-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="69a04-158">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="69a04-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="69a04-159">Exemplo 9: criar um conjunto de registros curinga</span><span class="sxs-lookup"><span data-stu-id="69a04-159">Example 9:  Create a wildcard Record Set</span></span>

```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="69a04-160">Esse comando cria um conjunto de registros chamado \* na zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="69a04-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="69a04-161">Este é um conjunto de registros curinga.</span><span class="sxs-lookup"><span data-stu-id="69a04-161">This is a wildcard record set.</span></span> <span data-ttu-id="69a04-162">Para criar um conjunto de registros usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="69a04-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="69a04-163">Exemplo 10: criar um conjunto de registros vazio</span><span class="sxs-lookup"><span data-stu-id="69a04-163">Example 10:  Create an empty Record Set</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords @()

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="69a04-164">Esse comando cria um conjunto de registros chamado \* na zona privada myzone.com.</span><span class="sxs-lookup"><span data-stu-id="69a04-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="69a04-165">O conjunto de registros é do tipo A e tem uma TTL de 1 hora (3600 segundos).</span><span class="sxs-lookup"><span data-stu-id="69a04-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="69a04-166">Esse é um conjunto de registros vazio, que atua como um espaço reservado para o qual você pode adicionar registros mais tarde.</span><span class="sxs-lookup"><span data-stu-id="69a04-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="69a04-167">Exemplo 11: criar um conjunto de registros e suprimir todas as confirmações</span><span class="sxs-lookup"><span data-stu-id="69a04-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="69a04-168">Esse comando cria um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="69a04-168">This command creates a RecordSet.</span></span> <span data-ttu-id="69a04-169">O parâmetro overwrite garante que esse registro substitua o conjunto de registros preexistentes com o mesmo nome e tipo (os registros existentes nesse conjunto de registros são perdidos).</span><span class="sxs-lookup"><span data-stu-id="69a04-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="69a04-170">O parâmetro Confirm com um valor de $False suprime o prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="69a04-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="69a04-171">OS</span><span class="sxs-lookup"><span data-stu-id="69a04-171">PARAMETERS</span></span>

### <span data-ttu-id="69a04-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a04-172">-DefaultProfile</span></span>
<span data-ttu-id="69a04-173">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69a04-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69a04-174">-Metadados</span><span class="sxs-lookup"><span data-stu-id="69a04-174">-Metadata</span></span>
<span data-ttu-id="69a04-175">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="69a04-175">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a04-176">-Nome</span><span class="sxs-lookup"><span data-stu-id="69a04-176">-Name</span></span>
<span data-ttu-id="69a04-177">O nome dos registros nesse conjunto de registros (relativo ao nome da zona e sem um ponto final).</span><span class="sxs-lookup"><span data-stu-id="69a04-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a04-178">-Substituir</span><span class="sxs-lookup"><span data-stu-id="69a04-178">-Overwrite</span></span>
<span data-ttu-id="69a04-179">Não falha se o conjunto de registros já existir.</span><span class="sxs-lookup"><span data-stu-id="69a04-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="69a04-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="69a04-180">-ParentResourceId</span></span>
<span data-ttu-id="69a04-181">ResourceId de zona DNS particular.</span><span class="sxs-lookup"><span data-stu-id="69a04-181">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a04-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="69a04-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="69a04-183">Os registros DNS particulares que fazem parte deste conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="69a04-183">The private dns records that are part of this record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordBase[]
Parameter Sets: (All)
Aliases: PrivateDnsRecords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a04-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="69a04-184">-RecordType</span></span>
<span data-ttu-id="69a04-185">O tipo de registro DNS privado nesse conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="69a04-185">The type of Private DNS records in this record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a04-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69a04-186">-ResourceGroupName</span></span>
<span data-ttu-id="69a04-187">O grupo de recursos ao qual a zona pertence.</span><span class="sxs-lookup"><span data-stu-id="69a04-187">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a04-188">-TTL</span><span class="sxs-lookup"><span data-stu-id="69a04-188">-Ttl</span></span>
<span data-ttu-id="69a04-189">O valor TTL de todos os registros nesse conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="69a04-189">The TTL value of all the records in this record set.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a04-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="69a04-190">-Zone</span></span>
<span data-ttu-id="69a04-191">O objeto PrivateDnsZone que representa a zona na qual criar o conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="69a04-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69a04-192">-Zonename</span><span class="sxs-lookup"><span data-stu-id="69a04-192">-ZoneName</span></span>
<span data-ttu-id="69a04-193">A zona na qual criar o conjunto de registros (sem um ponto final).</span><span class="sxs-lookup"><span data-stu-id="69a04-193">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a04-194">-Confirme</span><span class="sxs-lookup"><span data-stu-id="69a04-194">-Confirm</span></span>
<span data-ttu-id="69a04-195">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69a04-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a04-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69a04-196">-WhatIf</span></span>
<span data-ttu-id="69a04-197">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69a04-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69a04-198">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69a04-198">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a04-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a04-199">CommonParameters</span></span>
<span data-ttu-id="69a04-200">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69a04-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a04-201">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69a04-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a04-202">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69a04-202">INPUTS</span></span>

### <span data-ttu-id="69a04-203">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="69a04-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="69a04-204">System. String</span><span class="sxs-lookup"><span data-stu-id="69a04-204">System.String</span></span>

## <span data-ttu-id="69a04-205">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69a04-205">OUTPUTS</span></span>

### <span data-ttu-id="69a04-206">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="69a04-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="69a04-207">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69a04-207">NOTES</span></span>

## <span data-ttu-id="69a04-208">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69a04-208">RELATED LINKS</span></span>
