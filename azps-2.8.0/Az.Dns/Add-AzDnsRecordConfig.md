---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: ebf4efd627b904216cce239ccfee48f7ef97e35f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596561"
---
# <span data-ttu-id="3860c-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="3860c-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="3860c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3860c-102">SYNOPSIS</span></span>
<span data-ttu-id="3860c-103">Adiciona um registro DNS a um objeto de conjunto de registros local.</span><span class="sxs-lookup"><span data-stu-id="3860c-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="3860c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3860c-104">SYNTAX</span></span>

### <span data-ttu-id="3860c-105">Um</span><span class="sxs-lookup"><span data-stu-id="3860c-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3860c-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="3860c-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3860c-107">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="3860c-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3860c-108">MX</span><span class="sxs-lookup"><span data-stu-id="3860c-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3860c-109">PTR</span><span class="sxs-lookup"><span data-stu-id="3860c-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3860c-110">LOCALIZADO</span><span class="sxs-lookup"><span data-stu-id="3860c-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3860c-111">SRV</span><span class="sxs-lookup"><span data-stu-id="3860c-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3860c-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="3860c-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3860c-113">Caa</span><span class="sxs-lookup"><span data-stu-id="3860c-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3860c-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3860c-114">DESCRIPTION</span></span>
<span data-ttu-id="3860c-115">O cmdlet **Add-AzDnsRecordConfig** adiciona um registro de DNS (sistema de nomes de domínio) a um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="3860c-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="3860c-116">O objeto **Recordset** é um objeto offline, e as alterações feitas a ele não alteram as respostas de DNS até que você execute o cmdlet Set-AzDnsRecordSet para persistir a alteração no serviço DNS do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3860c-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="3860c-117">Os registros SOA são criados quando uma zona DNS é criada e são removidos quando a zona DNS é excluída.</span><span class="sxs-lookup"><span data-stu-id="3860c-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="3860c-118">Você não pode adicionar ou remover registros SOA, mas pode editá-los.</span><span class="sxs-lookup"><span data-stu-id="3860c-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="3860c-119">Você pode passar o objeto **Recordset** para esse cmdlet como um parâmetro ou usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="3860c-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="3860c-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3860c-120">EXAMPLES</span></span>

### <span data-ttu-id="3860c-121">Exemplo 1: adicionar um registro a a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="3860c-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="3860c-122">Este exemplo adiciona um registro a a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="3860c-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="3860c-123">Exemplo 2: adicionar um registro AAAA a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="3860c-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="3860c-124">Este exemplo adiciona um registro AAAA a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="3860c-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="3860c-125">Exemplo 3: adicionar um registro CNAME a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="3860c-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="3860c-126">Este exemplo adiciona um registro CNAME a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="3860c-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="3860c-127">Como um conjunto de registros CNAME pode conter no máximo um registro, ele deve inicialmente ser um conjunto de registros vazio ou os registros existentes devem ser removidos usando Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="3860c-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="3860c-128">Exemplo 4: adicionar um registro MX a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="3860c-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="3860c-129">Este exemplo adiciona um registro MX a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="3860c-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="3860c-130">O nome do registro "@" indica um conjunto de registros na zona Apex.</span><span class="sxs-lookup"><span data-stu-id="3860c-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="3860c-131">Exemplo 5: adicionar um registro NS a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="3860c-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="3860c-132">Este exemplo adiciona um registro NS a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="3860c-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="3860c-133">Exemplo 6: adicionar um registro PTR a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="3860c-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="3860c-134">Este exemplo adiciona um registro PTR a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="3860c-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="3860c-135">Exemplo 7: adicionar um registro SRV a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="3860c-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="3860c-136">Este exemplo adiciona um registro SRV a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="3860c-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="3860c-137">Exemplo 8: adicionar um registro TXT a um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="3860c-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="3860c-138">Este exemplo adiciona um registro TXT a um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="3860c-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="3860c-139">OS</span><span class="sxs-lookup"><span data-stu-id="3860c-139">PARAMETERS</span></span>

### <span data-ttu-id="3860c-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="3860c-140">-CaaFlags</span></span>
<span data-ttu-id="3860c-141">Os sinalizadores para o registro CAA a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="3860c-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="3860c-142">Deve ser um número entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="3860c-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="3860c-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="3860c-143">-CaaTag</span></span>
<span data-ttu-id="3860c-144">O campo de marca do registro CAA a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="3860c-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="3860c-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="3860c-145">-CaaValue</span></span>
<span data-ttu-id="3860c-146">O campo de valor do registro CAA a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="3860c-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="3860c-147">-CNAME</span><span class="sxs-lookup"><span data-stu-id="3860c-147">-Cname</span></span>
<span data-ttu-id="3860c-148">Especifica o nome de domínio para um registro de nome canônico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="3860c-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="3860c-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3860c-149">-DefaultProfile</span></span>
<span data-ttu-id="3860c-150">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3860c-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3860c-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="3860c-151">-Exchange</span></span>
<span data-ttu-id="3860c-152">Especifica o nome do servidor do servidor de mensagens para um registro de troca de email (MX).</span><span class="sxs-lookup"><span data-stu-id="3860c-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="3860c-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="3860c-153">-Ipv4Address</span></span>
<span data-ttu-id="3860c-154">Especifica um endereço IPv4 para um registro A.</span><span class="sxs-lookup"><span data-stu-id="3860c-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="3860c-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="3860c-155">-Ipv6Address</span></span>
<span data-ttu-id="3860c-156">Especifica um endereço IPv6 para um registro AAAA.</span><span class="sxs-lookup"><span data-stu-id="3860c-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="3860c-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="3860c-157">-Nsdname</span></span>
<span data-ttu-id="3860c-158">Especifica o nome do servidor de nomes para um registro de servidor de nomes (NS).</span><span class="sxs-lookup"><span data-stu-id="3860c-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="3860c-159">-Porta</span><span class="sxs-lookup"><span data-stu-id="3860c-159">-Port</span></span>
<span data-ttu-id="3860c-160">Especifica a porta para um registro de serviço (SRV).</span><span class="sxs-lookup"><span data-stu-id="3860c-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="3860c-161">-Preferência</span><span class="sxs-lookup"><span data-stu-id="3860c-161">-Preference</span></span>
<span data-ttu-id="3860c-162">Especifica a preferência para um registro MX.</span><span class="sxs-lookup"><span data-stu-id="3860c-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="3860c-163">-Priority</span><span class="sxs-lookup"><span data-stu-id="3860c-163">-Priority</span></span>
<span data-ttu-id="3860c-164">Especifica a prioridade para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="3860c-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="3860c-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="3860c-165">-Ptrdname</span></span>
<span data-ttu-id="3860c-166">Especifica o nome de domínio de destino de um registro de recurso de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="3860c-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="3860c-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="3860c-167">-RecordSet</span></span>
<span data-ttu-id="3860c-168">Especifica o objeto **Recordset** a ser editado.</span><span class="sxs-lookup"><span data-stu-id="3860c-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="3860c-169">-Destino</span><span class="sxs-lookup"><span data-stu-id="3860c-169">-Target</span></span>
<span data-ttu-id="3860c-170">Especifica o destino para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="3860c-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="3860c-171">-Valor</span><span class="sxs-lookup"><span data-stu-id="3860c-171">-Value</span></span>
<span data-ttu-id="3860c-172">Especifica o valor de um registro TXT.</span><span class="sxs-lookup"><span data-stu-id="3860c-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="3860c-173">-Weight</span><span class="sxs-lookup"><span data-stu-id="3860c-173">-Weight</span></span>
<span data-ttu-id="3860c-174">Especifica o peso para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="3860c-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="3860c-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3860c-175">CommonParameters</span></span>
<span data-ttu-id="3860c-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3860c-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3860c-177">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3860c-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3860c-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3860c-178">INPUTS</span></span>

### <span data-ttu-id="3860c-179">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3860c-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="3860c-180">System. String</span><span class="sxs-lookup"><span data-stu-id="3860c-180">System.String</span></span>

### <span data-ttu-id="3860c-181">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="3860c-181">System.UInt16</span></span>

### <span data-ttu-id="3860c-182">System. byte</span><span class="sxs-lookup"><span data-stu-id="3860c-182">System.Byte</span></span>

## <span data-ttu-id="3860c-183">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3860c-183">OUTPUTS</span></span>

### <span data-ttu-id="3860c-184">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3860c-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="3860c-185">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3860c-185">NOTES</span></span>

## <span data-ttu-id="3860c-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3860c-186">RELATED LINKS</span></span>

[<span data-ttu-id="3860c-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3860c-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="3860c-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="3860c-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="3860c-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3860c-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
