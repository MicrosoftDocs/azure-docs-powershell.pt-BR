---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: a5f3871f0ab63d875c2a0389c5585f0871fb0cb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775918"
---
# <span data-ttu-id="8e788-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="8e788-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="8e788-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e788-102">SYNOPSIS</span></span>
<span data-ttu-id="8e788-103">Adiciona um registro DNS a um objeto de conjunto de registros local.</span><span class="sxs-lookup"><span data-stu-id="8e788-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="8e788-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e788-104">SYNTAX</span></span>

### <span data-ttu-id="8e788-105">Um</span><span class="sxs-lookup"><span data-stu-id="8e788-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="8e788-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="8e788-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="8e788-107">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="8e788-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="8e788-108">MX</span><span class="sxs-lookup"><span data-stu-id="8e788-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="8e788-109">PTR</span><span class="sxs-lookup"><span data-stu-id="8e788-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="8e788-110">LOCALIZADO</span><span class="sxs-lookup"><span data-stu-id="8e788-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="8e788-111">SRV</span><span class="sxs-lookup"><span data-stu-id="8e788-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="8e788-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="8e788-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="8e788-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e788-113">DESCRIPTION</span></span>
<span data-ttu-id="8e788-114">O cmdlet **Add-AzDnsRecordConfig** adiciona um registro de DNS (sistema de nomes de domínio) a um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="8e788-114">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="8e788-115">O objeto **Recordset** é um objeto offline, e as alterações feitas a ele não alteram as respostas de DNS até que você execute o cmdlet Set-AzDnsRecordSet para persistir a alteração no serviço DNS do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8e788-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="8e788-116">Os registros SOA são criados quando uma zona DNS é criada e são removidos quando a zona DNS é excluída.</span><span class="sxs-lookup"><span data-stu-id="8e788-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="8e788-117">Você não pode adicionar ou remover registros SOA, mas pode editá-los.</span><span class="sxs-lookup"><span data-stu-id="8e788-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="8e788-118">Você pode passar o objeto **Recordset** para esse cmdlet como um parâmetro ou usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e788-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="8e788-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e788-119">EXAMPLES</span></span>

### <span data-ttu-id="8e788-120">Exemplo 1: adicionar um registro a a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8e788-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="8e788-121">Este exemplo adiciona um registro a a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="8e788-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="8e788-122">Exemplo 2: adicionar um registro AAAA a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8e788-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="8e788-123">Este exemplo adiciona um registro AAAA a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="8e788-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="8e788-124">Exemplo 3: adicionar um registro CNAME a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8e788-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="8e788-125">Este exemplo adiciona um registro CNAME a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="8e788-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="8e788-126">Como um conjunto de registros CNAME pode conter no máximo um registro, ele deve inicialmente ser um conjunto de registros vazio ou os registros existentes devem ser removidos usando Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="8e788-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="8e788-127">Exemplo 4: adicionar um registro MX a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8e788-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="8e788-128">Este exemplo adiciona um registro MX a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="8e788-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="8e788-129">O nome do registro "@" indica um conjunto de registros na zona Apex.</span><span class="sxs-lookup"><span data-stu-id="8e788-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="8e788-130">Exemplo 5: adicionar um registro NS a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8e788-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="8e788-131">Este exemplo adiciona um registro NS a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="8e788-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="8e788-132">Exemplo 6: adicionar um registro PTR a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8e788-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="8e788-133">Este exemplo adiciona um registro PTR a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="8e788-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="8e788-134">Exemplo 7: adicionar um registro SRV a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8e788-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="8e788-135">Este exemplo adiciona um registro SRV a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="8e788-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="8e788-136">Exemplo 8: adicionar um registro TXT a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8e788-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="8e788-137">Este exemplo adiciona um registro TXT a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="8e788-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="8e788-138">OS</span><span class="sxs-lookup"><span data-stu-id="8e788-138">PARAMETERS</span></span>

### <span data-ttu-id="8e788-139">-CNAME</span><span class="sxs-lookup"><span data-stu-id="8e788-139">-Cname</span></span>
<span data-ttu-id="8e788-140">Especifica o nome de domínio para um registro de nome canônico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="8e788-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e788-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="8e788-141">-Exchange</span></span>
<span data-ttu-id="8e788-142">Especifica o nome do servidor do servidor de mensagens para um registro de troca de email (MX).</span><span class="sxs-lookup"><span data-stu-id="8e788-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e788-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="8e788-143">-Ipv4Address</span></span>
<span data-ttu-id="8e788-144">Especifica um endereço IPv4 para um registro A.</span><span class="sxs-lookup"><span data-stu-id="8e788-144">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="8e788-145">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="8e788-145">-Ipv6Address</span></span>
<span data-ttu-id="8e788-146">Especifica um endereço IPv6 para um registro AAAA.</span><span class="sxs-lookup"><span data-stu-id="8e788-146">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e788-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="8e788-147">-Nsdname</span></span>
<span data-ttu-id="8e788-148">Especifica o nome do servidor de nomes para um registro de servidor de nomes (NS).</span><span class="sxs-lookup"><span data-stu-id="8e788-148">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e788-149">-Porta</span><span class="sxs-lookup"><span data-stu-id="8e788-149">-Port</span></span>
<span data-ttu-id="8e788-150">Especifica a porta para um registro de serviço (SRV).</span><span class="sxs-lookup"><span data-stu-id="8e788-150">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e788-151">-Preferência</span><span class="sxs-lookup"><span data-stu-id="8e788-151">-Preference</span></span>
<span data-ttu-id="8e788-152">Especifica a preferência para um registro MX.</span><span class="sxs-lookup"><span data-stu-id="8e788-152">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e788-153">-Priority</span><span class="sxs-lookup"><span data-stu-id="8e788-153">-Priority</span></span>
<span data-ttu-id="8e788-154">Especifica a prioridade para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="8e788-154">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e788-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="8e788-155">-Ptrdname</span></span>
<span data-ttu-id="8e788-156">Especifica o nome de domínio de destino de um registro de recurso de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="8e788-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e788-157">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="8e788-157">-RecordSet</span></span>
<span data-ttu-id="8e788-158">Especifica o objeto **Recordset** a ser editado.</span><span class="sxs-lookup"><span data-stu-id="8e788-158">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e788-159">-Destino</span><span class="sxs-lookup"><span data-stu-id="8e788-159">-Target</span></span>
<span data-ttu-id="8e788-160">Especifica o destino para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="8e788-160">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e788-161">-Valor</span><span class="sxs-lookup"><span data-stu-id="8e788-161">-Value</span></span>
<span data-ttu-id="8e788-162">Especifica o valor de um registro TXT.</span><span class="sxs-lookup"><span data-stu-id="8e788-162">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e788-163">-Weight</span><span class="sxs-lookup"><span data-stu-id="8e788-163">-Weight</span></span>
<span data-ttu-id="8e788-164">Especifica o peso para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="8e788-164">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e788-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e788-165">CommonParameters</span></span>
<span data-ttu-id="8e788-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e788-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e788-167">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e788-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e788-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e788-168">INPUTS</span></span>

### <span data-ttu-id="8e788-169">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e788-169">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="8e788-170">Você pode canalizar um objeto **Recordset** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e788-170">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="8e788-171">Esta é uma representação offline do **conjunto de registros** e as alterações feitas não alteram as respostas de DNS até que você execute o cmdlet Set-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="8e788-171">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="8e788-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e788-172">OUTPUTS</span></span>

### <span data-ttu-id="8e788-173">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e788-173">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="8e788-174">Esse cmdlet retorna o objeto **Recordset** modificado.</span><span class="sxs-lookup"><span data-stu-id="8e788-174">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="8e788-175">Além disso, o objeto passado é modificado diretamente.</span><span class="sxs-lookup"><span data-stu-id="8e788-175">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="8e788-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e788-176">NOTES</span></span>

## <span data-ttu-id="8e788-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e788-177">RELATED LINKS</span></span>

[<span data-ttu-id="8e788-178">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e788-178">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="8e788-179">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="8e788-179">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="8e788-180">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8e788-180">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)