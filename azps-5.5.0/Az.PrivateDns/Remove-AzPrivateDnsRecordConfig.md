---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 1e3362850880f02c648fb3318db226515fc95eef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114562"
---
# <span data-ttu-id="d2909-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d2909-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="d2909-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2909-102">SYNOPSIS</span></span>
<span data-ttu-id="d2909-103">Remove um registro DNS particular de um objeto de conjunto de registros local.</span><span class="sxs-lookup"><span data-stu-id="d2909-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="d2909-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2909-104">SYNTAX</span></span>

### <span data-ttu-id="d2909-105">A (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d2909-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2909-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="d2909-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2909-107">Mx</span><span class="sxs-lookup"><span data-stu-id="d2909-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2909-108">Ptr</span><span class="sxs-lookup"><span data-stu-id="d2909-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2909-109">Txt</span><span class="sxs-lookup"><span data-stu-id="d2909-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2909-110">Srv</span><span class="sxs-lookup"><span data-stu-id="d2909-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2909-111">Cname</span><span class="sxs-lookup"><span data-stu-id="d2909-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2909-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2909-112">DESCRIPTION</span></span>
<span data-ttu-id="d2909-113">O Remove-AzPrivateDnsRecordConfig cmdlet remove um registro DNS (Sistema de Nomes de Domínio Particular) de um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="d2909-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="d2909-114">O objeto RecordSet é um objeto offline e as alterações feitas nele não alteram as respostas dns privadas até que você execute o cmdlet Set-AzPrivateDnsRecordSet para persistir a alteração no serviço DNS particular do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2909-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="d2909-115">Para remover um registro, todos os campos desse tipo de registro devem corresponder exatamente.</span><span class="sxs-lookup"><span data-stu-id="d2909-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="d2909-116">Não é possível adicionar ou remover registros SOA.</span><span class="sxs-lookup"><span data-stu-id="d2909-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="d2909-117">Os registros SOA são criados automaticamente quando uma zona DNS particular é criada e excluída automaticamente quando a zona DNS particular é excluída.</span><span class="sxs-lookup"><span data-stu-id="d2909-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="d2909-118">Você pode passar o objeto RecordSet para esse cmdlet como um parâmetro ou usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="d2909-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="d2909-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d2909-119">EXAMPLES</span></span>

### <span data-ttu-id="d2909-120">Exemplo 1: Remover um registro A de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="d2909-120">Example 1: Remove an A record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d2909-121">Este exemplo remove um registro A de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="d2909-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="d2909-122">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="d2909-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="d2909-123">Para remover um conjunto de registros completamente, consulte Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="d2909-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="d2909-124">Exemplo 2: Remover um registro AAAA de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="d2909-124">Example 2: Remove an AAAA record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d2909-125">Este exemplo remove um registro AAAA de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="d2909-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="d2909-126">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="d2909-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="d2909-127">Para remover um conjunto de registros completamente, consulte Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="d2909-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="d2909-128">Exemplo 3: Remover um registro CNAME de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="d2909-128">Example 3: Remove a CNAME record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d2909-129">Este exemplo remove um registro CNAME de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="d2909-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="d2909-130">Como um conjunto de registros CNAME pode conter no máximo um registro, o resultado é um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="d2909-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="d2909-131">Exemplo 4: Remover um registro MX de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="d2909-131">Example 4: Remove a MX record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d2909-132">Este exemplo remove um registro MX de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="d2909-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="d2909-133">O nome do registro "@" indica um conjunto de registros no apex de zona.</span><span class="sxs-lookup"><span data-stu-id="d2909-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="d2909-134">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="d2909-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="d2909-135">Para remover um conjunto de registros completamente, consulte Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="d2909-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="d2909-136">Exemplo 5: remover um registro PTR de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="d2909-136">Example 5: Remove a PTR record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d2909-137">Este exemplo remove um registro PTR de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="d2909-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="d2909-138">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="d2909-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="d2909-139">Para remover um conjunto de registros completamente, consulte Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="d2909-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="d2909-140">Exemplo 6: remover um registro SRV de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="d2909-140">Example 6: Remove a SRV record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d2909-141">Este exemplo remove um registro SRV de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="d2909-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="d2909-142">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="d2909-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="d2909-143">Para remover um conjunto de registros completamente, consulte Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="d2909-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="d2909-144">Exemplo 7: Remover um registro TXT de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="d2909-144">Example 7: Remove a TXT record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d2909-145">Este exemplo remove um registro TXT de um conjunto de registros existente.</span><span class="sxs-lookup"><span data-stu-id="d2909-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="d2909-146">Se esse for o único registro no conjunto de registros, o resultado será um conjunto de registros vazio.</span><span class="sxs-lookup"><span data-stu-id="d2909-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="d2909-147">Para remover um conjunto de registros completamente, consulte Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="d2909-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="d2909-148">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2909-148">PARAMETERS</span></span>

### <span data-ttu-id="d2909-149">-Cname</span><span class="sxs-lookup"><span data-stu-id="d2909-149">-Cname</span></span>
<span data-ttu-id="d2909-150">O nome canônico do registro CNAME a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d2909-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="d2909-151">Não deve ser relativo ao nome da zona.</span><span class="sxs-lookup"><span data-stu-id="d2909-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="d2909-152">Não deve ter um ponto de término</span><span class="sxs-lookup"><span data-stu-id="d2909-152">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="d2909-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2909-153">-DefaultProfile</span></span>
<span data-ttu-id="d2909-154">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2909-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2909-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="d2909-155">-Exchange</span></span>
<span data-ttu-id="d2909-156">O host de troca de emails do registro MX a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d2909-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="d2909-157">Não deve ser relativo ao nome da zona.</span><span class="sxs-lookup"><span data-stu-id="d2909-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="d2909-158">Não deve ter um ponto de término</span><span class="sxs-lookup"><span data-stu-id="d2909-158">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="d2909-159">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="d2909-159">-Ipv4Address</span></span>
<span data-ttu-id="d2909-160">O endereço IPv4 do registro A a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d2909-160">The IPv4 address of the A record to remove.</span></span>

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

### <span data-ttu-id="d2909-161">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="d2909-161">-Ipv6Address</span></span>
<span data-ttu-id="d2909-162">O endereço IPv6 do registro AAAA a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d2909-162">The IPv6 address of the AAAA record to remove.</span></span>

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

### <span data-ttu-id="d2909-163">-Porta</span><span class="sxs-lookup"><span data-stu-id="d2909-163">-Port</span></span>
<span data-ttu-id="d2909-164">O número da porta do registro SRV a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d2909-164">The port number of the SRV record to remove.</span></span>

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

### <span data-ttu-id="d2909-165">-Preferência</span><span class="sxs-lookup"><span data-stu-id="d2909-165">-Preference</span></span>
<span data-ttu-id="d2909-166">O valor de preferência do registro MX a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d2909-166">The preference value of the MX record to remove.</span></span>

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

### <span data-ttu-id="d2909-167">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="d2909-167">-Priority</span></span>
<span data-ttu-id="d2909-168">O valor de prioridade do registro SRV a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d2909-168">The priority value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="d2909-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="d2909-169">-Ptrdname</span></span>
<span data-ttu-id="d2909-170">O host de destino do registro PTR a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d2909-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="d2909-171">Não deve ser relativo ao nome da zona.</span><span class="sxs-lookup"><span data-stu-id="d2909-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="d2909-172">Não deve ter um ponto de término</span><span class="sxs-lookup"><span data-stu-id="d2909-172">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="d2909-173">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="d2909-173">-RecordSet</span></span>
<span data-ttu-id="d2909-174">O conjunto de registros do qual remover o registro.</span><span class="sxs-lookup"><span data-stu-id="d2909-174">The record set from which to remove the record.</span></span>

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

### <span data-ttu-id="d2909-175">-Destino</span><span class="sxs-lookup"><span data-stu-id="d2909-175">-Target</span></span>
<span data-ttu-id="d2909-176">O host de destino do registro SRV a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d2909-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="d2909-177">Não deve ser relativo ao nome da zona.</span><span class="sxs-lookup"><span data-stu-id="d2909-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="d2909-178">Não deve ter um ponto de término</span><span class="sxs-lookup"><span data-stu-id="d2909-178">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="d2909-179">-Valor</span><span class="sxs-lookup"><span data-stu-id="d2909-179">-Value</span></span>
<span data-ttu-id="d2909-180">O valor de texto do registro TXT a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d2909-180">The text value of the TXT record to remove.</span></span>

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

### <span data-ttu-id="d2909-181">-Peso</span><span class="sxs-lookup"><span data-stu-id="d2909-181">-Weight</span></span>
<span data-ttu-id="d2909-182">O valor de peso do registro SRV a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d2909-182">The weight value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="d2909-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2909-183">CommonParameters</span></span>
<span data-ttu-id="d2909-184">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2909-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2909-185">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2909-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2909-186">Entradas</span><span class="sxs-lookup"><span data-stu-id="d2909-186">INPUTS</span></span>

### <span data-ttu-id="d2909-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d2909-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d2909-188">Saídas</span><span class="sxs-lookup"><span data-stu-id="d2909-188">OUTPUTS</span></span>

### <span data-ttu-id="d2909-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d2909-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d2909-190">Notas</span><span class="sxs-lookup"><span data-stu-id="d2909-190">NOTES</span></span>

## <span data-ttu-id="d2909-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2909-191">RELATED LINKS</span></span>
