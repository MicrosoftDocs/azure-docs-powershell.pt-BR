---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: aa67873ba55f815e7fdd8ada4658370c16e65c4e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126984"
---
# <span data-ttu-id="6b653-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6b653-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="6b653-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b653-102">SYNOPSIS</span></span>
<span data-ttu-id="6b653-103">Remove um registro DNS de um objeto de conjunto de registros local.</span><span class="sxs-lookup"><span data-stu-id="6b653-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="6b653-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b653-104">SYNTAX</span></span>

### <span data-ttu-id="6b653-105">Um</span><span class="sxs-lookup"><span data-stu-id="6b653-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b653-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="6b653-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b653-107">Ns</span><span class="sxs-lookup"><span data-stu-id="6b653-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b653-108">Mx</span><span class="sxs-lookup"><span data-stu-id="6b653-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b653-109">Ptr</span><span class="sxs-lookup"><span data-stu-id="6b653-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b653-110">Txt</span><span class="sxs-lookup"><span data-stu-id="6b653-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b653-111">Srv</span><span class="sxs-lookup"><span data-stu-id="6b653-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b653-112">Cname</span><span class="sxs-lookup"><span data-stu-id="6b653-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b653-113">Caa</span><span class="sxs-lookup"><span data-stu-id="6b653-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b653-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b653-114">DESCRIPTION</span></span>
<span data-ttu-id="6b653-115">O cmdlet **Remove-AzDnsRecordConfig** remove um registro DNS (Sistema de Nomes de Domínio) de um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="6b653-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="6b653-116">O objeto **RecordSet** é um objeto offline e as alterações feitas nele não alteram as respostas dns até que você execute o cmdlet Set-AzDnsRecordSet para persistir a alteração no serviço DNS do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6b653-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="6b653-117">Para remover um registro, todos os campos desse tipo de registro devem corresponder exatamente.</span><span class="sxs-lookup"><span data-stu-id="6b653-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="6b653-118">Não é possível adicionar ou remover registros SOA.</span><span class="sxs-lookup"><span data-stu-id="6b653-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="6b653-119">Os registros SOA são criados automaticamente quando uma zona DNS é criada e excluída automaticamente quando a zona DNS é excluída.</span><span class="sxs-lookup"><span data-stu-id="6b653-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="6b653-120">Você pode passar o objeto **RecordSet** para esse cmdlet como um parâmetro ou usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="6b653-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="6b653-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b653-121">EXAMPLES</span></span>

### <span data-ttu-id="6b653-122">Exemplo 1: Remover um registro A de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="6b653-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="6b653-123">Este exemplo remove um registro A de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="6b653-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="6b653-124">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="6b653-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="6b653-125">Para remover um conjunto de registros completamente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6b653-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6b653-126">Exemplo 2: Remover um registro AAAA de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="6b653-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="6b653-127">Este exemplo remove um registro AAAA de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="6b653-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="6b653-128">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="6b653-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="6b653-129">Para remover um conjunto de registros completamente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6b653-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6b653-130">Exemplo 3: Remover um registro CNAME de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="6b653-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="6b653-131">Este exemplo remove um registro CNAME de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="6b653-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="6b653-132">Como um conjunto de registros CNAME pode conter no máximo um registro, o resultado é um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="6b653-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="6b653-133">Exemplo 4: Remover um registro MX de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="6b653-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="6b653-134">Este exemplo remove um registro MX de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="6b653-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="6b653-135">O nome do registro "@" indica um conjunto de registros no apex de zona.</span><span class="sxs-lookup"><span data-stu-id="6b653-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="6b653-136">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="6b653-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6b653-137">Para remover um conjunto de registros completamente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6b653-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6b653-138">Exemplo 5: Remover um registro NS de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="6b653-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="6b653-139">Este exemplo remove um registro NS de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="6b653-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="6b653-140">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="6b653-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6b653-141">Para remover um conjunto de registros completamente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6b653-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6b653-142">Exemplo 6: remover um registro PTR de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="6b653-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="6b653-143">Este exemplo remove um registro PTR de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="6b653-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="6b653-144">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="6b653-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6b653-145">Para remover um conjunto de registros completamente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6b653-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6b653-146">Exemplo 7: remover um registro SRV de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="6b653-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="6b653-147">Este exemplo remove um registro SRV de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="6b653-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="6b653-148">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="6b653-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6b653-149">Para remover um conjunto de registros completamente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6b653-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6b653-150">Exemplo 8: remover um registro TXT de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="6b653-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="6b653-151">Este exemplo remove um registro TXT de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="6b653-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="6b653-152">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="6b653-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6b653-153">Para remover um conjunto de registros completamente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6b653-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="6b653-154">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b653-154">PARAMETERS</span></span>

### <span data-ttu-id="6b653-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="6b653-155">-CaaFlags</span></span>
<span data-ttu-id="6b653-156">Os sinalizadores do registro CAA a adicionar.</span><span class="sxs-lookup"><span data-stu-id="6b653-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="6b653-157">Deve ser um número entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="6b653-157">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="6b653-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="6b653-158">-CaaTag</span></span>
<span data-ttu-id="6b653-159">O campo de marca do registro CAA a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="6b653-159">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="6b653-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="6b653-160">-CaaValue</span></span>
<span data-ttu-id="6b653-161">O campo de valor para o registro CAA a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="6b653-161">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="6b653-162">-Cname</span><span class="sxs-lookup"><span data-stu-id="6b653-162">-Cname</span></span>
<span data-ttu-id="6b653-163">Especifica o nome de domínio de um registro de nome canônico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="6b653-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="6b653-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b653-164">-DefaultProfile</span></span>
<span data-ttu-id="6b653-165">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6b653-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b653-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="6b653-166">-Exchange</span></span>
<span data-ttu-id="6b653-167">Especifica o nome do servidor de troca de emails para um registro MX .</span><span class="sxs-lookup"><span data-stu-id="6b653-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="6b653-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="6b653-168">-Ipv4Address</span></span>
<span data-ttu-id="6b653-169">Especifica um endereço IPv4 para um registro A.</span><span class="sxs-lookup"><span data-stu-id="6b653-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="6b653-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="6b653-170">-Ipv6Address</span></span>
<span data-ttu-id="6b653-171">Especifica um endereço IPv6 para um registro AAAA.</span><span class="sxs-lookup"><span data-stu-id="6b653-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="6b653-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="6b653-172">-Nsdname</span></span>
<span data-ttu-id="6b653-173">Especifica o servidor de nomes de um registro NS (servidor de nomes).</span><span class="sxs-lookup"><span data-stu-id="6b653-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="6b653-174">-Porta</span><span class="sxs-lookup"><span data-stu-id="6b653-174">-Port</span></span>
<span data-ttu-id="6b653-175">Especifica a porta para um registro SRV (serviço).</span><span class="sxs-lookup"><span data-stu-id="6b653-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="6b653-176">-Preferência</span><span class="sxs-lookup"><span data-stu-id="6b653-176">-Preference</span></span>
<span data-ttu-id="6b653-177">Especifica a preferência de um registro MX.</span><span class="sxs-lookup"><span data-stu-id="6b653-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="6b653-178">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="6b653-178">-Priority</span></span>
<span data-ttu-id="6b653-179">Especifica a prioridade de um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="6b653-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="6b653-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="6b653-180">-Ptrdname</span></span>
<span data-ttu-id="6b653-181">Especifica o nome de domínio de destino de um registro de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="6b653-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="6b653-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="6b653-182">-RecordSet</span></span>
<span data-ttu-id="6b653-183">Especifica o objeto **RecordSet** que contém o registro a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6b653-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="6b653-184">-Destino</span><span class="sxs-lookup"><span data-stu-id="6b653-184">-Target</span></span>
<span data-ttu-id="6b653-185">Especifica o destino de um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="6b653-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="6b653-186">-Valor</span><span class="sxs-lookup"><span data-stu-id="6b653-186">-Value</span></span>
<span data-ttu-id="6b653-187">Especifica o valor de um registro TXT.</span><span class="sxs-lookup"><span data-stu-id="6b653-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="6b653-188">-Peso</span><span class="sxs-lookup"><span data-stu-id="6b653-188">-Weight</span></span>
<span data-ttu-id="6b653-189">Especifica a peso de um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="6b653-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="6b653-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b653-190">CommonParameters</span></span>
<span data-ttu-id="6b653-191">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b653-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b653-192">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b653-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b653-193">Entradas</span><span class="sxs-lookup"><span data-stu-id="6b653-193">INPUTS</span></span>

### <span data-ttu-id="6b653-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b653-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="6b653-195">System.String</span><span class="sxs-lookup"><span data-stu-id="6b653-195">System.String</span></span>

### <span data-ttu-id="6b653-196">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="6b653-196">System.UInt16</span></span>

### <span data-ttu-id="6b653-197">System.Byte</span><span class="sxs-lookup"><span data-stu-id="6b653-197">System.Byte</span></span>

## <span data-ttu-id="6b653-198">Saídas</span><span class="sxs-lookup"><span data-stu-id="6b653-198">OUTPUTS</span></span>

### <span data-ttu-id="6b653-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b653-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="6b653-200">Notas</span><span class="sxs-lookup"><span data-stu-id="6b653-200">NOTES</span></span>

## <span data-ttu-id="6b653-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b653-201">RELATED LINKS</span></span>

[<span data-ttu-id="6b653-202">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6b653-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="6b653-203">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b653-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="6b653-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b653-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
