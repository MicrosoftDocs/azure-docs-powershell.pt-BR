---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: 07af143e1a1582670d15a15c356f673fef1f7590
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889491"
---
# <span data-ttu-id="4e9ba-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="4e9ba-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="4e9ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e9ba-102">SYNOPSIS</span></span>
<span data-ttu-id="4e9ba-103">Remove um registro DNS de um objeto de conjunto de registros local.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="4e9ba-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4e9ba-104">SYNTAX</span></span>

### <span data-ttu-id="4e9ba-105">A</span><span class="sxs-lookup"><span data-stu-id="4e9ba-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e9ba-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="4e9ba-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e9ba-107">NS</span><span class="sxs-lookup"><span data-stu-id="4e9ba-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e9ba-108">MX</span><span class="sxs-lookup"><span data-stu-id="4e9ba-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e9ba-109">PTR</span><span class="sxs-lookup"><span data-stu-id="4e9ba-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e9ba-110">TXT</span><span class="sxs-lookup"><span data-stu-id="4e9ba-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e9ba-111">SRV</span><span class="sxs-lookup"><span data-stu-id="4e9ba-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e9ba-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="4e9ba-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e9ba-113">Caa</span><span class="sxs-lookup"><span data-stu-id="4e9ba-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e9ba-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4e9ba-114">DESCRIPTION</span></span>
<span data-ttu-id="4e9ba-115">O cmdlet **Remove-AzDnsRecordConfig** remove um registro DNS (Sistema de Nomes de Domínio) de um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="4e9ba-116">O **objeto RecordSet** é um objeto offline e as alterações nele não alteram as respostas DNS até que você execute o cmdlet Set-AzDnsRecordSet para persistir a alteração no serviço DNS do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="4e9ba-117">Para remover um registro, todos os campos desse tipo de registro devem corresponder exatamente.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="4e9ba-118">Não é possível adicionar ou remover registros SOA.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="4e9ba-119">Os registros SOA são criados automaticamente quando uma zona DNS é criada e excluída automaticamente quando a zona DNS é excluída.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="4e9ba-120">Você pode passar o **objeto RecordSet** para esse cmdlet como um parâmetro ou usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="4e9ba-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e9ba-121">EXAMPLES</span></span>

### <span data-ttu-id="4e9ba-122">Exemplo 1: Remover um registro A de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4e9ba-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="4e9ba-123">Este exemplo remove um registro A de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="4e9ba-124">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="4e9ba-125">Para remover um conjunto de registros inteiramente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="4e9ba-126">Exemplo 2: Remover um registro AAAA de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4e9ba-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="4e9ba-127">Este exemplo remove um registro AAAA de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="4e9ba-128">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="4e9ba-129">Para remover um conjunto de registros inteiramente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="4e9ba-130">Exemplo 3: Remover um registro CNAME de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4e9ba-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="4e9ba-131">Este exemplo remove um registro CNAME de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="4e9ba-132">Como um conjunto de registros CNAME pode conter no máximo um registro, o resultado é um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="4e9ba-133">Exemplo 4: Remover um registro MX de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4e9ba-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="4e9ba-134">Este exemplo remove um registro MX de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="4e9ba-135">O nome do registro "@" indica um conjunto de registros no véreo de zona.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="4e9ba-136">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="4e9ba-137">Para remover um conjunto de registros inteiramente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="4e9ba-138">Exemplo 5: Remover um registro NS de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4e9ba-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="4e9ba-139">Este exemplo remove um registro NS de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="4e9ba-140">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="4e9ba-141">Para remover um conjunto de registros inteiramente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="4e9ba-142">Exemplo 6: Remover um registro PTR de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4e9ba-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="4e9ba-143">Este exemplo remove um registro PTR de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="4e9ba-144">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="4e9ba-145">Para remover um conjunto de registros inteiramente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="4e9ba-146">Exemplo 7: Remover um registro SRV de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4e9ba-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="4e9ba-147">Este exemplo remove um registro SRV de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="4e9ba-148">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="4e9ba-149">Para remover um conjunto de registros inteiramente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="4e9ba-150">Exemplo 8: Remover um registro TXT de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4e9ba-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="4e9ba-151">Este exemplo remove um registro TXT de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="4e9ba-152">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="4e9ba-153">Para remover um conjunto de registros inteiramente, consulte Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="4e9ba-154">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4e9ba-154">PARAMETERS</span></span>

### <span data-ttu-id="4e9ba-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="4e9ba-155">-CaaFlags</span></span>
<span data-ttu-id="4e9ba-156">Os sinalizadores para o registro CAA a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="4e9ba-157">Deve ser um número entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-157">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="4e9ba-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="4e9ba-158">-CaaTag</span></span>
<span data-ttu-id="4e9ba-159">O campo de marca do registro CAA a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-159">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="4e9ba-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="4e9ba-160">-CaaValue</span></span>
<span data-ttu-id="4e9ba-161">O campo de valor para o registro CAA a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-161">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="4e9ba-162">-Cname</span><span class="sxs-lookup"><span data-stu-id="4e9ba-162">-Cname</span></span>
<span data-ttu-id="4e9ba-163">Especifica o nome de domínio para um registro de nome canônico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="4e9ba-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="4e9ba-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e9ba-164">-DefaultProfile</span></span>
<span data-ttu-id="4e9ba-165">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4e9ba-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e9ba-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="4e9ba-166">-Exchange</span></span>
<span data-ttu-id="4e9ba-167">Especifica o nome do servidor do exchange de email para um registro MX (mail exchange).</span><span class="sxs-lookup"><span data-stu-id="4e9ba-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="4e9ba-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="4e9ba-168">-Ipv4Address</span></span>
<span data-ttu-id="4e9ba-169">Especifica um endereço IPv4 para um registro A.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="4e9ba-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="4e9ba-170">-Ipv6Address</span></span>
<span data-ttu-id="4e9ba-171">Especifica um endereço IPv6 para um registro AAAA.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="4e9ba-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="4e9ba-172">-Nsdname</span></span>
<span data-ttu-id="4e9ba-173">Especifica o servidor de nomes para um registro NS (servidor de nomes).</span><span class="sxs-lookup"><span data-stu-id="4e9ba-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="4e9ba-174">-Port</span><span class="sxs-lookup"><span data-stu-id="4e9ba-174">-Port</span></span>
<span data-ttu-id="4e9ba-175">Especifica a porta para um registro SRV (serviço).</span><span class="sxs-lookup"><span data-stu-id="4e9ba-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="4e9ba-176">-Preference</span><span class="sxs-lookup"><span data-stu-id="4e9ba-176">-Preference</span></span>
<span data-ttu-id="4e9ba-177">Especifica a preferência de um registro MX.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="4e9ba-178">-Priority</span><span class="sxs-lookup"><span data-stu-id="4e9ba-178">-Priority</span></span>
<span data-ttu-id="4e9ba-179">Especifica a prioridade para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="4e9ba-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="4e9ba-180">-Ptrdname</span></span>
<span data-ttu-id="4e9ba-181">Especifica o nome de domínio de destino de um registro de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="4e9ba-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="4e9ba-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="4e9ba-182">-RecordSet</span></span>
<span data-ttu-id="4e9ba-183">Especifica o **objeto RecordSet** que contém o registro a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="4e9ba-184">-Target</span><span class="sxs-lookup"><span data-stu-id="4e9ba-184">-Target</span></span>
<span data-ttu-id="4e9ba-185">Especifica o destino de um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="4e9ba-186">-Value</span><span class="sxs-lookup"><span data-stu-id="4e9ba-186">-Value</span></span>
<span data-ttu-id="4e9ba-187">Especifica o valor de um registro TXT.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="4e9ba-188">-Weight</span><span class="sxs-lookup"><span data-stu-id="4e9ba-188">-Weight</span></span>
<span data-ttu-id="4e9ba-189">Especifica o peso de um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="4e9ba-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e9ba-190">CommonParameters</span></span>
<span data-ttu-id="4e9ba-191">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e9ba-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e9ba-192">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e9ba-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e9ba-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e9ba-193">INPUTS</span></span>

### <span data-ttu-id="4e9ba-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4e9ba-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="4e9ba-195">System.String</span><span class="sxs-lookup"><span data-stu-id="4e9ba-195">System.String</span></span>

### <span data-ttu-id="4e9ba-196">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="4e9ba-196">System.UInt16</span></span>

### <span data-ttu-id="4e9ba-197">System.Byte</span><span class="sxs-lookup"><span data-stu-id="4e9ba-197">System.Byte</span></span>

## <span data-ttu-id="4e9ba-198">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4e9ba-198">OUTPUTS</span></span>

### <span data-ttu-id="4e9ba-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4e9ba-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="4e9ba-200">NOTES</span><span class="sxs-lookup"><span data-stu-id="4e9ba-200">NOTES</span></span>

## <span data-ttu-id="4e9ba-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e9ba-201">RELATED LINKS</span></span>

[<span data-ttu-id="4e9ba-202">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="4e9ba-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="4e9ba-203">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4e9ba-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="4e9ba-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4e9ba-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
