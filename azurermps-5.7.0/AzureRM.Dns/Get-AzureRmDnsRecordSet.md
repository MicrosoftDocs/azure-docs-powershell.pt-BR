---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: 5c7a2a42964be10aa02f4c3205e701b310febb78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432508"
---
# <span data-ttu-id="af1d9-101">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af1d9-101">Get-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="af1d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="af1d9-103">Obtém um conjunto de registros DNS.</span><span class="sxs-lookup"><span data-stu-id="af1d9-103">Gets a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af1d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af1d9-104">SYNTAX</span></span>

### <span data-ttu-id="af1d9-105">Campos</span><span class="sxs-lookup"><span data-stu-id="af1d9-105">Fields</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af1d9-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="af1d9-106">Object</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af1d9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af1d9-107">DESCRIPTION</span></span>
<span data-ttu-id="af1d9-108">O cmdlet **Get-AzureRmDnsRecordSet** Obtém o conjunto de registros DNS (Domain Name System) com o nome e o tipo especificados, na zona especificada.</span><span class="sxs-lookup"><span data-stu-id="af1d9-108">The **Get-AzureRmDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="af1d9-109">Se você não especificar os parâmetros *Name* ou *RecordType* , esse cmdlet retornará todos os conjuntos de registros do tipo especificado na zona.</span><span class="sxs-lookup"><span data-stu-id="af1d9-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="af1d9-110">Se você especificar o parâmetro *RecordType* , mas não o parâmetro *Name* , esse cmdlet retornará todos os conjuntos de registros do tipo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="af1d9-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="af1d9-111">Você pode usar o operador de pipeline para passar um objeto **dnsZone** para esse cmdlet, ou pode passar um objeto **dnsZone** como o parâmetro de *zona* ou também pode especificar a zona e o grupo de recursos por nome.</span><span class="sxs-lookup"><span data-stu-id="af1d9-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="af1d9-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af1d9-112">EXAMPLES</span></span>

### <span data-ttu-id="af1d9-113">Exemplo 1: obter conjuntos de registros com um nome e tipo especificados</span><span class="sxs-lookup"><span data-stu-id="af1d9-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="af1d9-114">Esse comando obtém o conjunto de registros do tipo de registro um chamado www no grupo de recursos e zona especificados e, em seguida, armazena-o na variável $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="af1d9-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="af1d9-115">Como os parâmetros *Name* e *RecordType* são especificados, apenas um objeto **Recordset** é retornado.</span><span class="sxs-lookup"><span data-stu-id="af1d9-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="af1d9-116">Exemplo 2: obter conjuntos de registros de um tipo especificado</span><span class="sxs-lookup"><span data-stu-id="af1d9-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="af1d9-117">Esse comando obtém uma matriz de todos os conjuntos de registros do tipo de registro A na zona chamada myzone.com no grupo de recursos chamado MyResource Group e, em seguida, os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="af1d9-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="af1d9-118">Exemplo 3: obter todos os conjuntos de registros em uma zona</span><span class="sxs-lookup"><span data-stu-id="af1d9-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="af1d9-119">Esse comando obtém uma matriz de todos os conjuntos de registros na zona chamada myzone.com no grupo de recursos chamado MyResource Group e, em seguida, os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="af1d9-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="af1d9-120">Exemplo 4: obter todos os conjuntos de registros em uma zona usando um objeto DnsZone</span><span class="sxs-lookup"><span data-stu-id="af1d9-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

<span data-ttu-id="af1d9-121">Este exemplo é equivalente ao exemplo 3 acima.</span><span class="sxs-lookup"><span data-stu-id="af1d9-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="af1d9-122">Neste momento, a região é especificada usando um objeto Zone.</span><span class="sxs-lookup"><span data-stu-id="af1d9-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="af1d9-123">OS</span><span class="sxs-lookup"><span data-stu-id="af1d9-123">PARAMETERS</span></span>

### <span data-ttu-id="af1d9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af1d9-124">-DefaultProfile</span></span>
<span data-ttu-id="af1d9-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="af1d9-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af1d9-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="af1d9-126">-Name</span></span>
<span data-ttu-id="af1d9-127">Especifica o nome do **conjunto de registros** a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="af1d9-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="af1d9-128">Se você não especificar o parâmetro *Name* , todos os conjuntos de registros do tipo especificado serão retornados.</span><span class="sxs-lookup"><span data-stu-id="af1d9-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="af1d9-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="af1d9-129">-RecordType</span></span>
<span data-ttu-id="af1d9-130">Especifica o tipo de registro DNS que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="af1d9-130">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="af1d9-131">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="af1d9-131">Valid values are:</span></span> 

- <span data-ttu-id="af1d9-132">Um</span><span class="sxs-lookup"><span data-stu-id="af1d9-132">A</span></span>
- <span data-ttu-id="af1d9-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="af1d9-133">AAAA</span></span>
- <span data-ttu-id="af1d9-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="af1d9-134">CNAME</span></span>
- <span data-ttu-id="af1d9-135">MX</span><span class="sxs-lookup"><span data-stu-id="af1d9-135">MX</span></span>
- <span data-ttu-id="af1d9-136">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="af1d9-136">NS</span></span>
- <span data-ttu-id="af1d9-137">PTR</span><span class="sxs-lookup"><span data-stu-id="af1d9-137">PTR</span></span>
- <span data-ttu-id="af1d9-138">SOA</span><span class="sxs-lookup"><span data-stu-id="af1d9-138">SOA</span></span>
- <span data-ttu-id="af1d9-139">SRV</span><span class="sxs-lookup"><span data-stu-id="af1d9-139">SRV</span></span>
- <span data-ttu-id="af1d9-140">LOCALIZADO</span><span class="sxs-lookup"><span data-stu-id="af1d9-140">TXT</span></span>

<span data-ttu-id="af1d9-141">Se você não especificar o parâmetro *RecordType* , também deverá omitir o parâmetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="af1d9-141">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="af1d9-142">Em seguida, esse cmdlet retorna todos os conjuntos de registros na zona (de todos os nomes e tipos).</span><span class="sxs-lookup"><span data-stu-id="af1d9-142">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

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

### <span data-ttu-id="af1d9-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af1d9-143">-ResourceGroupName</span></span>
<span data-ttu-id="af1d9-144">Especifica o grupo de recursos que contém a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="af1d9-144">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="af1d9-145">O nome da zona também deve ser especificado, usando o parâmetro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="af1d9-145">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="af1d9-146">Você também pode especificar a zona e o grupo de recursos passando um objeto **dnsZone** usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="af1d9-146">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="af1d9-147">-Zone</span><span class="sxs-lookup"><span data-stu-id="af1d9-147">-Zone</span></span>
<span data-ttu-id="af1d9-148">Especifica a zona DNS que contém o conjunto de registros que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="af1d9-148">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="af1d9-149">Você também pode especificar a zona usando os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="af1d9-149">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="af1d9-150">-Zonename</span><span class="sxs-lookup"><span data-stu-id="af1d9-150">-ZoneName</span></span>
<span data-ttu-id="af1d9-151">Especifica o nome da zona DNS que contém o conjunto de registros a obter.</span><span class="sxs-lookup"><span data-stu-id="af1d9-151">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="af1d9-152">O grupo de recursos que contém a zona também deve ser especificado, usando o parâmetro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="af1d9-152">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="af1d9-153">Você também pode especificar a zona e o grupo de recursos, passando um objeto de zona DNS usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="af1d9-153">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="af1d9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af1d9-154">CommonParameters</span></span>
<span data-ttu-id="af1d9-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af1d9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af1d9-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af1d9-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af1d9-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af1d9-157">INPUTS</span></span>

### <span data-ttu-id="af1d9-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="af1d9-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="af1d9-159">Você pode canalizar um objeto **dnsZone** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af1d9-159">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="af1d9-160">O objeto **dnsZone** representa a zona na qual procurar o objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="af1d9-160">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="af1d9-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af1d9-161">OUTPUTS</span></span>

### <span data-ttu-id="af1d9-162">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af1d9-162">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="af1d9-163">Esse cmdlet retorna um ou mais objetos que representam os conjuntos de registros que são encontrados.</span><span class="sxs-lookup"><span data-stu-id="af1d9-163">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="af1d9-164">Haverá no máximo um conjunto de **registros** retornado se os parâmetros *Name* e *RecordType* forem especificados; caso contrário, vários objetos **Recordset** serão retornados como uma matriz.</span><span class="sxs-lookup"><span data-stu-id="af1d9-164">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="af1d9-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af1d9-165">NOTES</span></span>

## <span data-ttu-id="af1d9-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af1d9-166">RELATED LINKS</span></span>

[<span data-ttu-id="af1d9-167">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af1d9-167">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="af1d9-168">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af1d9-168">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="af1d9-169">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af1d9-169">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)


