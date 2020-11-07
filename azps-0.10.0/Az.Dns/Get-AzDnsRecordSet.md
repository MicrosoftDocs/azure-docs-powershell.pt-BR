---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 7e1ea1213759e9c4edf9524a36637aff1ef1c12b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776739"
---
# <span data-ttu-id="a266a-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a266a-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="a266a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a266a-102">SYNOPSIS</span></span>
<span data-ttu-id="a266a-103">Obtém um conjunto de registros DNS.</span><span class="sxs-lookup"><span data-stu-id="a266a-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="a266a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a266a-104">SYNTAX</span></span>

### <span data-ttu-id="a266a-105">Campos</span><span class="sxs-lookup"><span data-stu-id="a266a-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### <span data-ttu-id="a266a-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="a266a-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
```

## <span data-ttu-id="a266a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a266a-107">DESCRIPTION</span></span>
<span data-ttu-id="a266a-108">O cmdlet **Get-AzDnsRecordSet** Obtém o conjunto de registros DNS (Domain Name System) com o nome e o tipo especificados, na zona especificada.</span><span class="sxs-lookup"><span data-stu-id="a266a-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="a266a-109">Se você não especificar os parâmetros *Name* ou *RecordType* , esse cmdlet retornará todos os conjuntos de registros do tipo especificado na zona.</span><span class="sxs-lookup"><span data-stu-id="a266a-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="a266a-110">Se você especificar o parâmetro *RecordType* , mas não o parâmetro *Name* , esse cmdlet retornará todos os conjuntos de registros do tipo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="a266a-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="a266a-111">Você pode usar o operador de pipeline para passar um objeto **dnsZone** para esse cmdlet, ou pode passar um objeto **dnsZone** como o parâmetro de *zona* ou também pode especificar a zona e o grupo de recursos por nome.</span><span class="sxs-lookup"><span data-stu-id="a266a-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="a266a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a266a-112">EXAMPLES</span></span>

### <span data-ttu-id="a266a-113">Exemplo 1: obter conjuntos de registros com um nome e tipo especificados</span><span class="sxs-lookup"><span data-stu-id="a266a-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="a266a-114">Esse comando obtém o conjunto de registros do tipo de registro um chamado www no grupo de recursos e zona especificados e, em seguida, armazena-o na variável $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="a266a-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="a266a-115">Como os parâmetros *Name* e *RecordType* são especificados, apenas um objeto **Recordset** é retornado.</span><span class="sxs-lookup"><span data-stu-id="a266a-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="a266a-116">Exemplo 2: obter conjuntos de registros de um tipo especificado</span><span class="sxs-lookup"><span data-stu-id="a266a-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="a266a-117">Esse comando obtém uma matriz de todos os conjuntos de registros do tipo de registro A na zona chamada myzone.com no grupo de recursos chamado MyResource Group e, em seguida, os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="a266a-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="a266a-118">Exemplo 3: obter todos os conjuntos de registros em uma zona</span><span class="sxs-lookup"><span data-stu-id="a266a-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="a266a-119">Esse comando obtém uma matriz de todos os conjuntos de registros na zona chamada myzone.com no grupo de recursos chamado MyResource Group e, em seguida, os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="a266a-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="a266a-120">Exemplo 4: obter todos os conjuntos de registros em uma zona usando um objeto DnsZone</span><span class="sxs-lookup"><span data-stu-id="a266a-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="a266a-121">Este exemplo é equivalente ao exemplo 3 acima.</span><span class="sxs-lookup"><span data-stu-id="a266a-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="a266a-122">Neste momento, a região é especificada usando um objeto Zone.</span><span class="sxs-lookup"><span data-stu-id="a266a-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="a266a-123">OS</span><span class="sxs-lookup"><span data-stu-id="a266a-123">PARAMETERS</span></span>

### <span data-ttu-id="a266a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a266a-124">-Name</span></span>
<span data-ttu-id="a266a-125">Especifica o nome do **conjunto de registros** a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="a266a-125">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="a266a-126">Se você não especificar o parâmetro *Name* , todos os conjuntos de registros do tipo especificado serão retornados.</span><span class="sxs-lookup"><span data-stu-id="a266a-126">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a266a-127">-RecordType</span><span class="sxs-lookup"><span data-stu-id="a266a-127">-RecordType</span></span>
<span data-ttu-id="a266a-128">Especifica o tipo de registro DNS que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a266a-128">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="a266a-129">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="a266a-129">Valid values are:</span></span> 

- <span data-ttu-id="a266a-130">Um</span><span class="sxs-lookup"><span data-stu-id="a266a-130">A</span></span>
- <span data-ttu-id="a266a-131">AAAA</span><span class="sxs-lookup"><span data-stu-id="a266a-131">AAAA</span></span>
- <span data-ttu-id="a266a-132">CNAME</span><span class="sxs-lookup"><span data-stu-id="a266a-132">CNAME</span></span>
- <span data-ttu-id="a266a-133">MX</span><span class="sxs-lookup"><span data-stu-id="a266a-133">MX</span></span>
- <span data-ttu-id="a266a-134">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="a266a-134">NS</span></span>
- <span data-ttu-id="a266a-135">PTR</span><span class="sxs-lookup"><span data-stu-id="a266a-135">PTR</span></span>
- <span data-ttu-id="a266a-136">SOA</span><span class="sxs-lookup"><span data-stu-id="a266a-136">SOA</span></span>
- <span data-ttu-id="a266a-137">SRV</span><span class="sxs-lookup"><span data-stu-id="a266a-137">SRV</span></span>
- <span data-ttu-id="a266a-138">LOCALIZADO</span><span class="sxs-lookup"><span data-stu-id="a266a-138">TXT</span></span>

<span data-ttu-id="a266a-139">Se você não especificar o parâmetro *RecordType* , também deverá omitir o parâmetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="a266a-139">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="a266a-140">Em seguida, esse cmdlet retorna todos os conjuntos de registros na zona (de todos os nomes e tipos).</span><span class="sxs-lookup"><span data-stu-id="a266a-140">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a266a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a266a-141">-ResourceGroupName</span></span>
<span data-ttu-id="a266a-142">Especifica o grupo de recursos que contém a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="a266a-142">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="a266a-143">O nome da zona também deve ser especificado, usando o parâmetro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="a266a-143">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="a266a-144">Você também pode especificar a zona e o grupo de recursos passando um objeto **dnsZone** usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="a266a-144">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a266a-145">-Zone</span><span class="sxs-lookup"><span data-stu-id="a266a-145">-Zone</span></span>
<span data-ttu-id="a266a-146">Especifica a zona DNS que contém o conjunto de registros que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a266a-146">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="a266a-147">Você também pode especificar a zona usando os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a266a-147">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a266a-148">-Zonename</span><span class="sxs-lookup"><span data-stu-id="a266a-148">-ZoneName</span></span>
<span data-ttu-id="a266a-149">Especifica o nome da zona DNS que contém o conjunto de registros a obter.</span><span class="sxs-lookup"><span data-stu-id="a266a-149">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="a266a-150">O grupo de recursos que contém a zona também deve ser especificado, usando o parâmetro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a266a-150">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="a266a-151">Você também pode especificar a zona e o grupo de recursos, passando um objeto de zona DNS usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="a266a-151">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a266a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a266a-152">CommonParameters</span></span>
<span data-ttu-id="a266a-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a266a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a266a-154">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a266a-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a266a-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a266a-155">INPUTS</span></span>

### <span data-ttu-id="a266a-156">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a266a-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="a266a-157">Você pode canalizar um objeto **dnsZone** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a266a-157">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="a266a-158">O objeto **dnsZone** representa a zona na qual procurar o objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a266a-158">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="a266a-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a266a-159">OUTPUTS</span></span>

### <span data-ttu-id="a266a-160">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a266a-160">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="a266a-161">Esse cmdlet retorna um ou mais objetos que representam os conjuntos de registros que são encontrados.</span><span class="sxs-lookup"><span data-stu-id="a266a-161">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="a266a-162">Haverá no máximo um conjunto de **registros** retornado se os parâmetros *Name* e *RecordType* forem especificados; caso contrário, vários objetos **Recordset** serão retornados como uma matriz.</span><span class="sxs-lookup"><span data-stu-id="a266a-162">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="a266a-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a266a-163">NOTES</span></span>

## <span data-ttu-id="a266a-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a266a-164">RELATED LINKS</span></span>

[<span data-ttu-id="a266a-165">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a266a-165">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="a266a-166">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a266a-166">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="a266a-167">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a266a-167">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


