---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 1e0a7de22b459f5d87c4a79bb91ef4c36f88ad77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432132"
---
# <span data-ttu-id="16a5c-101">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="16a5c-101">Remove-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="16a5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="16a5c-103">Remove um registro DNS de um objeto de conjunto de registros local.</span><span class="sxs-lookup"><span data-stu-id="16a5c-103">Removes a DNS record from a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16a5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16a5c-104">SYNTAX</span></span>

### <span data-ttu-id="16a5c-105">Um</span><span class="sxs-lookup"><span data-stu-id="16a5c-105">A</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16a5c-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="16a5c-106">AAAA</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16a5c-107">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="16a5c-107">NS</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16a5c-108">MX</span><span class="sxs-lookup"><span data-stu-id="16a5c-108">MX</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16a5c-109">PTR</span><span class="sxs-lookup"><span data-stu-id="16a5c-109">PTR</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16a5c-110">LOCALIZADO</span><span class="sxs-lookup"><span data-stu-id="16a5c-110">TXT</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16a5c-111">SRV</span><span class="sxs-lookup"><span data-stu-id="16a5c-111">SRV</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16a5c-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="16a5c-112">CNAME</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16a5c-113">Caa</span><span class="sxs-lookup"><span data-stu-id="16a5c-113">Caa</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16a5c-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16a5c-114">DESCRIPTION</span></span>
<span data-ttu-id="16a5c-115">O cmdlet **Remove-AzureRmDnsRecordConfig** remove um registro de DNS (sistema de nomes de domínio) de um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="16a5c-115">The **Remove-AzureRmDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="16a5c-116">O objeto **Recordset** é um objeto offline, e as alterações feitas a ele não alteram as respostas de DNS até que você execute o cmdlet Set-AzureRmDnsRecordSet para persistir a alteração no serviço DNS do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="16a5c-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="16a5c-117">Para remover um registro, todos os campos desse tipo de registro devem corresponder exatamente.</span><span class="sxs-lookup"><span data-stu-id="16a5c-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="16a5c-118">Não é possível adicionar ou remover registros SOA.</span><span class="sxs-lookup"><span data-stu-id="16a5c-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="16a5c-119">Os registros SOA são automaticamente criados quando uma zona DNS é criada e excluída automaticamente quando a zona DNS é excluída.</span><span class="sxs-lookup"><span data-stu-id="16a5c-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="16a5c-120">Você pode passar o objeto **Recordset** para esse cmdlet como um parâmetro ou usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="16a5c-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="16a5c-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16a5c-121">EXAMPLES</span></span>

### <span data-ttu-id="16a5c-122">Exemplo 1: remover um registro A de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="16a5c-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="16a5c-123">Este exemplo remove um registro A de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="16a5c-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="16a5c-124">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="16a5c-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="16a5c-125">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="16a5c-125">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="16a5c-126">Exemplo 2: remover um registro AAAA de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="16a5c-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="16a5c-127">Este exemplo remove um registro AAAA de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="16a5c-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="16a5c-128">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="16a5c-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="16a5c-129">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="16a5c-129">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="16a5c-130">Exemplo 3: remover um registro CNAME de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="16a5c-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="16a5c-131">Este exemplo remove um registro CNAME de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="16a5c-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="16a5c-132">Como um conjunto de registros CNAME pode conter no máximo um registro, o resultado é um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="16a5c-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="16a5c-133">Exemplo 4: remover um registro MX de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="16a5c-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="16a5c-134">Este exemplo remove um registro MX de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="16a5c-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="16a5c-135">O nome do registro "@" indica um conjunto de registros na zona Apex.</span><span class="sxs-lookup"><span data-stu-id="16a5c-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="16a5c-136">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="16a5c-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="16a5c-137">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="16a5c-137">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="16a5c-138">Exemplo 5: remover um registro NS de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="16a5c-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="16a5c-139">Este exemplo remove um registro NS de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="16a5c-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="16a5c-140">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="16a5c-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="16a5c-141">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="16a5c-141">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="16a5c-142">Exemplo 6: remover um registro PTR de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="16a5c-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="16a5c-143">Este exemplo remove um registro PTR de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="16a5c-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="16a5c-144">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="16a5c-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="16a5c-145">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="16a5c-145">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="16a5c-146">Exemplo 7: remover um registro SRV de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="16a5c-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="16a5c-147">Este exemplo remove um registro SRV de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="16a5c-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="16a5c-148">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="16a5c-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="16a5c-149">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="16a5c-149">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="16a5c-150">Exemplo 8: remover um registro TXT de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="16a5c-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="16a5c-151">Este exemplo remove um registro TXT de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="16a5c-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="16a5c-152">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="16a5c-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="16a5c-153">Para remover completamente um conjunto de registros, consulte Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="16a5c-153">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="16a5c-154">OS</span><span class="sxs-lookup"><span data-stu-id="16a5c-154">PARAMETERS</span></span>

### <span data-ttu-id="16a5c-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="16a5c-155">-CaaFlags</span></span>
<span data-ttu-id="16a5c-156">Os sinalizadores para o registro CAA a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="16a5c-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="16a5c-157">Deve ser um número entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="16a5c-157">Must be a number between 0 and 255.</span></span>

```yaml
Type: Byte
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16a5c-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="16a5c-158">-CaaTag</span></span>
<span data-ttu-id="16a5c-159">O campo de marca do registro CAA a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="16a5c-159">The tag field of the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16a5c-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="16a5c-160">-CaaValue</span></span>
<span data-ttu-id="16a5c-161">O campo de valor do registro CAA a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="16a5c-161">The value field for the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16a5c-162">-CNAME</span><span class="sxs-lookup"><span data-stu-id="16a5c-162">-Cname</span></span>
<span data-ttu-id="16a5c-163">Especifica o nome de domínio para um registro de nome canônico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="16a5c-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="16a5c-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a5c-164">-DefaultProfile</span></span>
<span data-ttu-id="16a5c-165">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="16a5c-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16a5c-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="16a5c-166">-Exchange</span></span>
<span data-ttu-id="16a5c-167">Especifica o nome do servidor do servidor de mensagens para um registro de troca de email (MX).</span><span class="sxs-lookup"><span data-stu-id="16a5c-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="16a5c-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="16a5c-168">-Ipv4Address</span></span>
<span data-ttu-id="16a5c-169">Especifica um endereço IPv4 para um registro A.</span><span class="sxs-lookup"><span data-stu-id="16a5c-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="16a5c-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="16a5c-170">-Ipv6Address</span></span>
<span data-ttu-id="16a5c-171">Especifica um endereço IPv6 para um registro AAAA.</span><span class="sxs-lookup"><span data-stu-id="16a5c-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="16a5c-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="16a5c-172">-Nsdname</span></span>
<span data-ttu-id="16a5c-173">Especifica o servidor de nomes para um registro de servidor de nomes (NS).</span><span class="sxs-lookup"><span data-stu-id="16a5c-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="16a5c-174">-Porta</span><span class="sxs-lookup"><span data-stu-id="16a5c-174">-Port</span></span>
<span data-ttu-id="16a5c-175">Especifica a porta para um registro de serviço (SRV).</span><span class="sxs-lookup"><span data-stu-id="16a5c-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="16a5c-176">-Preferência</span><span class="sxs-lookup"><span data-stu-id="16a5c-176">-Preference</span></span>
<span data-ttu-id="16a5c-177">Especifica a preferência para um registro MX.</span><span class="sxs-lookup"><span data-stu-id="16a5c-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="16a5c-178">-Priority</span><span class="sxs-lookup"><span data-stu-id="16a5c-178">-Priority</span></span>
<span data-ttu-id="16a5c-179">Especifica a prioridade para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="16a5c-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="16a5c-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="16a5c-180">-Ptrdname</span></span>
<span data-ttu-id="16a5c-181">Especifica o nome de domínio de destino de um registro de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="16a5c-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="16a5c-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="16a5c-182">-RecordSet</span></span>
<span data-ttu-id="16a5c-183">Especifica o objeto **Recordset** que contém o registro a remover.</span><span class="sxs-lookup"><span data-stu-id="16a5c-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="16a5c-184">-Destino</span><span class="sxs-lookup"><span data-stu-id="16a5c-184">-Target</span></span>
<span data-ttu-id="16a5c-185">Especifica o destino para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="16a5c-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="16a5c-186">-Valor</span><span class="sxs-lookup"><span data-stu-id="16a5c-186">-Value</span></span>
<span data-ttu-id="16a5c-187">Especifica o valor de um registro TXT.</span><span class="sxs-lookup"><span data-stu-id="16a5c-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="16a5c-188">-Weight</span><span class="sxs-lookup"><span data-stu-id="16a5c-188">-Weight</span></span>
<span data-ttu-id="16a5c-189">Especifica o peso para um registro SRV.</span><span class="sxs-lookup"><span data-stu-id="16a5c-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="16a5c-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a5c-190">CommonParameters</span></span>
<span data-ttu-id="16a5c-191">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16a5c-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a5c-192">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16a5c-192">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a5c-193">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16a5c-193">INPUTS</span></span>

### <span data-ttu-id="16a5c-194">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="16a5c-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="16a5c-195">Você pode canalizar um objeto **DnsRecordSet** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16a5c-195">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="16a5c-196">Esta é uma representação offline do conjunto de registros e as atualizações dele não alteram as respostas de DNS até que você execute Set-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="16a5c-196">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="16a5c-197">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16a5c-197">OUTPUTS</span></span>

### <span data-ttu-id="16a5c-198">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="16a5c-198">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="16a5c-199">Esse cmdlet retorna o objeto **Recordset** modificado.</span><span class="sxs-lookup"><span data-stu-id="16a5c-199">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="16a5c-200">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16a5c-200">NOTES</span></span>

## <span data-ttu-id="16a5c-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16a5c-201">RELATED LINKS</span></span>

[<span data-ttu-id="16a5c-202">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="16a5c-202">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="16a5c-203">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="16a5c-203">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="16a5c-204">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="16a5c-204">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
