---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: af3e2e3494aa7f7f98856db3709d4716f5b04e44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599790"
---
# <span data-ttu-id="0bd9a-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="0bd9a-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="0bd9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0bd9a-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd9a-103">Adiciona um registro DNS privado a um objeto de conjunto de registros local.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="0bd9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bd9a-104">SYNTAX</span></span>

### <span data-ttu-id="0bd9a-105">A (padrão)</span><span class="sxs-lookup"><span data-stu-id="0bd9a-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bd9a-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="0bd9a-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bd9a-107">MX</span><span class="sxs-lookup"><span data-stu-id="0bd9a-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bd9a-108">PTR</span><span class="sxs-lookup"><span data-stu-id="0bd9a-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bd9a-109">LOCALIZADO</span><span class="sxs-lookup"><span data-stu-id="0bd9a-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bd9a-110">SRV</span><span class="sxs-lookup"><span data-stu-id="0bd9a-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bd9a-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="0bd9a-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bd9a-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0bd9a-112">DESCRIPTION</span></span>
<span data-ttu-id="0bd9a-113">O cmdlet Add-AzPrivateDnsRecordConfig adiciona um registro DNS (sistema de nomes de domínio) privado a um objeto RecordSet.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="0bd9a-114">O objeto RecordSet é um objeto offline, e as alterações feitas a ele não alteram as respostas DNS particulares até que você execute o cmdlet Set-AzPrivateDnsRecordSet para persistir a alteração no serviço DNS privado do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="0bd9a-115">Os registros SOA são criados quando uma zona DNS privada é criada e são removidas quando a zona DNS privada é excluída.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="0bd9a-116">Você não pode adicionar ou remover registros SOA, mas pode editá-los.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="0bd9a-117">Você pode passar o objeto RecordSet para esse cmdlet como um parâmetro ou usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="0bd9a-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bd9a-118">EXAMPLES</span></span>

### <span data-ttu-id="0bd9a-119">Exemplo 1: adicionar um registro a a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="0bd9a-119">Example 1: Add an A record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0bd9a-120">Este exemplo adiciona um registro a a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="0bd9a-121">Exemplo 2: adicionar um registro AAAA a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="0bd9a-121">Example 2: Add an AAAA record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0bd9a-122">Este exemplo adiciona um registro AAAAA a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="0bd9a-123">Exemplo 3: adicionar um registro CNAME a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="0bd9a-123">Example 3: Add a CNAME record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="0bd9a-124">Este exemplo adiciona um registro CNAME a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="0bd9a-125">Exemplo 4: adicionar um registro MX a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="0bd9a-125">Example 4: Add a MX record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name @ -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="0bd9a-126">Este exemplo adiciona um registro MX a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="0bd9a-127">Exemplo 5: adicionar um registro PTR a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="0bd9a-127">Example 5: Add a PTR record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="0bd9a-128">Este exemplo adiciona um registro PTR a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="0bd9a-129">Exemplo 6: adicionar um registro SRV a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="0bd9a-129">Example 6: Add a SRV record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup-ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="0bd9a-130">Este exemplo adiciona um registro SRV a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="0bd9a-131">Exemplo 7: adicionar um registro TXT a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="0bd9a-131">Example 7: Add a TXT record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Value "This is a TXT Record" | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="0bd9a-132">Este exemplo adiciona um registro TXT a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="0bd9a-133">OS</span><span class="sxs-lookup"><span data-stu-id="0bd9a-133">PARAMETERS</span></span>

### <span data-ttu-id="0bd9a-134">-CNAME</span><span class="sxs-lookup"><span data-stu-id="0bd9a-134">-Cname</span></span>
<span data-ttu-id="0bd9a-135">O nome canônico do registro CNAME a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="0bd9a-136">Não deve ser relativo ao nome da zona.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="0bd9a-137">Não deve ter um ponto de terminação</span><span class="sxs-lookup"><span data-stu-id="0bd9a-137">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="0bd9a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd9a-138">-DefaultProfile</span></span>
<span data-ttu-id="0bd9a-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bd9a-140">-Exchange</span><span class="sxs-lookup"><span data-stu-id="0bd9a-140">-Exchange</span></span>
<span data-ttu-id="0bd9a-141">O host do mail Exchange para o registro MX a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="0bd9a-142">Não deve ser relativo ao nome da zona.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="0bd9a-143">Não deve ter um ponto de terminação</span><span class="sxs-lookup"><span data-stu-id="0bd9a-143">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="0bd9a-144">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="0bd9a-144">-Ipv4Address</span></span>
<span data-ttu-id="0bd9a-145">O endereço IPv4 do registro a a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-145">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="0bd9a-146">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="0bd9a-146">-Ipv6Address</span></span>
<span data-ttu-id="0bd9a-147">O endereço IPv6 para o registro AAAA a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-147">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="0bd9a-148">-Porta</span><span class="sxs-lookup"><span data-stu-id="0bd9a-148">-Port</span></span>
<span data-ttu-id="0bd9a-149">O número da porta do registro SRV a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-149">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="0bd9a-150">-Preferência</span><span class="sxs-lookup"><span data-stu-id="0bd9a-150">-Preference</span></span>
<span data-ttu-id="0bd9a-151">O valor de preferência para o registro MX a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-151">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="0bd9a-152">-Priority</span><span class="sxs-lookup"><span data-stu-id="0bd9a-152">-Priority</span></span>
<span data-ttu-id="0bd9a-153">O registro SRV do valor de prioridade a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-153">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="0bd9a-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="0bd9a-154">-Ptrdname</span></span>
<span data-ttu-id="0bd9a-155">O host de destino para o registro PTR a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="0bd9a-156">Não deve ser relativo ao nome da zona.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="0bd9a-157">Não deve ter um ponto de terminação</span><span class="sxs-lookup"><span data-stu-id="0bd9a-157">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="0bd9a-158">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="0bd9a-158">-RecordSet</span></span>
<span data-ttu-id="0bd9a-159">O conjunto de registros no qual adicionar o registro.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-159">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bd9a-160">-Destino</span><span class="sxs-lookup"><span data-stu-id="0bd9a-160">-Target</span></span>
<span data-ttu-id="0bd9a-161">O host de destino para o registro SRV a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="0bd9a-162">Não deve ser relativo ao nome da zona.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="0bd9a-163">Não deve ter um ponto de terminação</span><span class="sxs-lookup"><span data-stu-id="0bd9a-163">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="0bd9a-164">-Valor</span><span class="sxs-lookup"><span data-stu-id="0bd9a-164">-Value</span></span>
<span data-ttu-id="0bd9a-165">O valor de texto do registro TXT a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-165">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="0bd9a-166">-Weight</span><span class="sxs-lookup"><span data-stu-id="0bd9a-166">-Weight</span></span>
<span data-ttu-id="0bd9a-167">O valor de peso para o registro SRV a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-167">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="0bd9a-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd9a-168">CommonParameters</span></span>
<span data-ttu-id="0bd9a-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bd9a-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd9a-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bd9a-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd9a-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0bd9a-171">INPUTS</span></span>

### <span data-ttu-id="0bd9a-172">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0bd9a-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0bd9a-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0bd9a-173">OUTPUTS</span></span>

### <span data-ttu-id="0bd9a-174">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0bd9a-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0bd9a-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0bd9a-175">NOTES</span></span>

## <span data-ttu-id="0bd9a-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bd9a-176">RELATED LINKS</span></span>
