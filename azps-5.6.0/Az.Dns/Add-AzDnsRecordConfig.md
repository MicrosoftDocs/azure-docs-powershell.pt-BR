---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: 885c7ad64b207f74fa7953050a6ceba9ecc44f43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889505"
---
# <span data-ttu-id="4c0a6-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="4c0a6-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="4c0a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0a6-103">Adiciona um registro DNS a um objeto de conjunto de registros local.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="4c0a6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4c0a6-104">SYNTAX</span></span>

### <span data-ttu-id="4c0a6-105">A</span><span class="sxs-lookup"><span data-stu-id="4c0a6-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c0a6-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="4c0a6-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c0a6-107">NS</span><span class="sxs-lookup"><span data-stu-id="4c0a6-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c0a6-108">MX</span><span class="sxs-lookup"><span data-stu-id="4c0a6-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c0a6-109">PTR</span><span class="sxs-lookup"><span data-stu-id="4c0a6-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c0a6-110">TXT</span><span class="sxs-lookup"><span data-stu-id="4c0a6-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c0a6-111">SRV</span><span class="sxs-lookup"><span data-stu-id="4c0a6-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c0a6-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="4c0a6-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c0a6-113">Caa</span><span class="sxs-lookup"><span data-stu-id="4c0a6-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c0a6-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4c0a6-114">DESCRIPTION</span></span>
<span data-ttu-id="4c0a6-115">O cmdlet **Add-AzDnsRecordConfig** adiciona um registro DNS (Sistema de Nomes de Domínio) a um **objeto RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="4c0a6-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="4c0a6-116">O **objeto RecordSet** é um objeto offline e as alterações nele não alteram as respostas DNS até que você execute o cmdlet Set-AzDnsRecordSet para persistir a alteração no serviço DNS do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="4c0a6-117">Os registros SOA são criados quando uma zona DNS é criada e são removidas quando a zona DNS é excluída.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="4c0a6-118">Você não pode adicionar ou remover registros SOA, mas pode editá-los.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="4c0a6-119">Você pode passar o **objeto RecordSet** para esse cmdlet como um parâmetro ou usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="4c0a6-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c0a6-120">EXAMPLES</span></span>

### <span data-ttu-id="4c0a6-121">Exemplo 1: Adicionar um registro A a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4c0a6-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="4c0a6-122">Este exemplo adiciona um registro A a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="4c0a6-123">Exemplo 2: Adicionar um registro AAAA a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4c0a6-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="4c0a6-124">Este exemplo adiciona um registro AAAA a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="4c0a6-125">Exemplo 3: Adicionar um registro CNAME a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4c0a6-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="4c0a6-126">Este exemplo adiciona um registro CNAME a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="4c0a6-127">Como um conjunto de registros CNAME pode conter no máximo um registro, ele deve inicialmente ser um conjunto de registros vazio ou os registros existentes devem ser removidos usando Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="4c0a6-128">Exemplo 4: Adicionar um registro MX a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4c0a6-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="4c0a6-129">Este exemplo adiciona um registro MX a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="4c0a6-130">O nome do registro "@" indica um conjunto de registros no véreo de zona.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="4c0a6-131">Exemplo 5: Adicionar um registro NS a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4c0a6-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="4c0a6-132">Este exemplo adiciona um registro NS a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="4c0a6-133">Exemplo 6: Adicionar um registro PTR a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4c0a6-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="4c0a6-134">Este exemplo adiciona um registro PTR a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="4c0a6-135">Exemplo 7: Adicionar um registro SRV a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4c0a6-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="4c0a6-136">Este exemplo adiciona um registro SRV a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="4c0a6-137">Exemplo 8: Adicionar um registro TXT a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4c0a6-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="4c0a6-138">Este exemplo adiciona um registro TXT a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="4c0a6-139">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4c0a6-139">PARAMETERS</span></span>

### <span data-ttu-id="4c0a6-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="4c0a6-140">-CaaFlags</span></span>
<span data-ttu-id="4c0a6-141">Os sinalizadores para o registro CAA a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="4c0a6-142">Deve ser um número entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="4c0a6-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="4c0a6-143">-CaaTag</span></span>
<span data-ttu-id="4c0a6-144">O campo de marca do registro CAA a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="4c0a6-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="4c0a6-145">-CaaValue</span></span>
<span data-ttu-id="4c0a6-146">O campo de valor para o registro CAA a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="4c0a6-147">-Cname</span><span class="sxs-lookup"><span data-stu-id="4c0a6-147">-Cname</span></span>
<span data-ttu-id="4c0a6-148">Especifica o nome de domínio para um registro de nome canônico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="4c0a6-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0a6-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0a6-149">-DefaultProfile</span></span>
<span data-ttu-id="4c0a6-150">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4c0a6-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c0a6-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="4c0a6-151">-Exchange</span></span>
<span data-ttu-id="4c0a6-152">Especifica o nome do servidor do exchange de email para um registro MX (mail exchange).</span><span class="sxs-lookup"><span data-stu-id="4c0a6-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0a6-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="4c0a6-153">-Ipv4Address</span></span>
<span data-ttu-id="4c0a6-154">Especifica um endereço IPv4 para um registro A.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="4c0a6-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="4c0a6-155">-Ipv6Address</span></span>
<span data-ttu-id="4c0a6-156">Especifica um endereço IPv6 para um registro AAAA.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-156">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0a6-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="4c0a6-157">-Nsdname</span></span>
<span data-ttu-id="4c0a6-158">Especifica o nome do servidor de nomes para um registro NS (servidor de nomes).</span><span class="sxs-lookup"><span data-stu-id="4c0a6-158">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0a6-159">-Port</span><span class="sxs-lookup"><span data-stu-id="4c0a6-159">-Port</span></span>
<span data-ttu-id="4c0a6-160">Especifica a porta para um registro SRV (serviço).</span><span class="sxs-lookup"><span data-stu-id="4c0a6-160">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0a6-161">-Preference</span><span class="sxs-lookup"><span data-stu-id="4c0a6-161">-Preference</span></span>
<span data-ttu-id="4c0a6-162">Especifica a preferência de um registro MX.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-162">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0a6-163">-Priority</span><span class="sxs-lookup"><span data-stu-id="4c0a6-163">-Priority</span></span>
<span data-ttu-id="4c0a6-164">Especifica a prioridade para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-164">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0a6-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="4c0a6-165">-Ptrdname</span></span>
<span data-ttu-id="4c0a6-166">Especifica o nome de domínio de destino de um registro de recurso de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="4c0a6-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0a6-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="4c0a6-167">-RecordSet</span></span>
<span data-ttu-id="4c0a6-168">Especifica o **objeto RecordSet** a ser editado.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-168">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0a6-169">-Target</span><span class="sxs-lookup"><span data-stu-id="4c0a6-169">-Target</span></span>
<span data-ttu-id="4c0a6-170">Especifica o destino de um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-170">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0a6-171">-Value</span><span class="sxs-lookup"><span data-stu-id="4c0a6-171">-Value</span></span>
<span data-ttu-id="4c0a6-172">Especifica o valor de um registro TXT.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-172">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0a6-173">-Weight</span><span class="sxs-lookup"><span data-stu-id="4c0a6-173">-Weight</span></span>
<span data-ttu-id="4c0a6-174">Especifica o peso de um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-174">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0a6-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0a6-175">CommonParameters</span></span>
<span data-ttu-id="4c0a6-176">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c0a6-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0a6-177">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c0a6-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0a6-178">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c0a6-178">INPUTS</span></span>

### <span data-ttu-id="4c0a6-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4c0a6-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="4c0a6-180">System.String</span><span class="sxs-lookup"><span data-stu-id="4c0a6-180">System.String</span></span>

### <span data-ttu-id="4c0a6-181">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="4c0a6-181">System.UInt16</span></span>

### <span data-ttu-id="4c0a6-182">System.Byte</span><span class="sxs-lookup"><span data-stu-id="4c0a6-182">System.Byte</span></span>

## <span data-ttu-id="4c0a6-183">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4c0a6-183">OUTPUTS</span></span>

### <span data-ttu-id="4c0a6-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4c0a6-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="4c0a6-185">NOTES</span><span class="sxs-lookup"><span data-stu-id="4c0a6-185">NOTES</span></span>

## <span data-ttu-id="4c0a6-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c0a6-186">RELATED LINKS</span></span>

[<span data-ttu-id="4c0a6-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4c0a6-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="4c0a6-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="4c0a6-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="4c0a6-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4c0a6-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
