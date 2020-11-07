---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942340"
---
# <span data-ttu-id="367bd-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="367bd-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="367bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="367bd-102">SYNOPSIS</span></span>
<span data-ttu-id="367bd-103">Obtém um conjunto de registros DNS.</span><span class="sxs-lookup"><span data-stu-id="367bd-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="367bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="367bd-104">SYNTAX</span></span>

### <span data-ttu-id="367bd-105">Campos</span><span class="sxs-lookup"><span data-stu-id="367bd-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="367bd-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="367bd-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="367bd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="367bd-107">DESCRIPTION</span></span>
<span data-ttu-id="367bd-108">O cmdlet **Get-AzDnsRecordSet** Obtém o conjunto de registros DNS (Domain Name System) com o nome e o tipo especificados, na zona especificada.</span><span class="sxs-lookup"><span data-stu-id="367bd-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="367bd-109">Se você não especificar os parâmetros *Name* ou *RecordType* , esse cmdlet retornará todos os conjuntos de registros do tipo especificado na zona.</span><span class="sxs-lookup"><span data-stu-id="367bd-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="367bd-110">Se você especificar o parâmetro *RecordType* , mas não o parâmetro *Name* , esse cmdlet retornará todos os conjuntos de registros do tipo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="367bd-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="367bd-111">Você pode usar o operador de pipeline para passar um objeto **dnsZone** para esse cmdlet, ou pode passar um objeto **dnsZone** como o parâmetro de *zona* ou também pode especificar a zona e o grupo de recursos por nome.</span><span class="sxs-lookup"><span data-stu-id="367bd-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="367bd-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="367bd-112">EXAMPLES</span></span>

### <span data-ttu-id="367bd-113">Exemplo 1: obter conjuntos de registros com um nome e tipo especificados</span><span class="sxs-lookup"><span data-stu-id="367bd-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="367bd-114">Esse comando obtém o conjunto de registros do tipo de registro um chamado www no grupo de recursos e zona especificados e, em seguida, armazena-o na variável $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="367bd-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="367bd-115">Como os parâmetros *Name* e *RecordType* são especificados, apenas um objeto **Recordset** é retornado.</span><span class="sxs-lookup"><span data-stu-id="367bd-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="367bd-116">Exemplo 2: obter conjuntos de registros de um tipo especificado</span><span class="sxs-lookup"><span data-stu-id="367bd-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="367bd-117">Esse comando obtém uma matriz de todos os conjuntos de registros do tipo de registro A na zona chamada myzone.com no grupo de recursos chamado MyResource Group e, em seguida, os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="367bd-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="367bd-118">Exemplo 3: obter todos os conjuntos de registros em uma zona</span><span class="sxs-lookup"><span data-stu-id="367bd-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="367bd-119">Esse comando obtém uma matriz de todos os conjuntos de registros na zona chamada myzone.com no grupo de recursos chamado MyResource Group e, em seguida, os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="367bd-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="367bd-120">Exemplo 4: obter todos os conjuntos de registros em uma zona usando um objeto DnsZone</span><span class="sxs-lookup"><span data-stu-id="367bd-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="367bd-121">Este exemplo é equivalente ao exemplo 3 acima.</span><span class="sxs-lookup"><span data-stu-id="367bd-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="367bd-122">Neste momento, a região é especificada usando um objeto Zone.</span><span class="sxs-lookup"><span data-stu-id="367bd-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="367bd-123">OS</span><span class="sxs-lookup"><span data-stu-id="367bd-123">PARAMETERS</span></span>

### <span data-ttu-id="367bd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367bd-124">-DefaultProfile</span></span>
<span data-ttu-id="367bd-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="367bd-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="367bd-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="367bd-126">-Name</span></span>
<span data-ttu-id="367bd-127">Especifica o nome do **conjunto de registros** a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="367bd-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="367bd-128">Se você não especificar o parâmetro *Name* , todos os conjuntos de registros do tipo especificado serão retornados.</span><span class="sxs-lookup"><span data-stu-id="367bd-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367bd-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="367bd-129">-RecordType</span></span>
<span data-ttu-id="367bd-130">Especifica o tipo de registro DNS que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="367bd-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="367bd-131">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="367bd-131">Valid values are:</span></span> 
- <span data-ttu-id="367bd-132">Um</span><span class="sxs-lookup"><span data-stu-id="367bd-132">A</span></span>
- <span data-ttu-id="367bd-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="367bd-133">AAAA</span></span>
- <span data-ttu-id="367bd-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="367bd-134">CNAME</span></span>
- <span data-ttu-id="367bd-135">MX</span><span class="sxs-lookup"><span data-stu-id="367bd-135">MX</span></span>
- <span data-ttu-id="367bd-136">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="367bd-136">NS</span></span>
- <span data-ttu-id="367bd-137">PTR</span><span class="sxs-lookup"><span data-stu-id="367bd-137">PTR</span></span>
- <span data-ttu-id="367bd-138">SOA</span><span class="sxs-lookup"><span data-stu-id="367bd-138">SOA</span></span>
- <span data-ttu-id="367bd-139">SRV</span><span class="sxs-lookup"><span data-stu-id="367bd-139">SRV</span></span>
- <span data-ttu-id="367bd-140">TXT se você não especificar o parâmetro *RecordType* , também deverá omitir o parâmetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="367bd-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="367bd-141">Em seguida, esse cmdlet retorna todos os conjuntos de registros na zona (de todos os nomes e tipos).</span><span class="sxs-lookup"><span data-stu-id="367bd-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367bd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="367bd-142">-ResourceGroupName</span></span>
<span data-ttu-id="367bd-143">Especifica o grupo de recursos que contém a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="367bd-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="367bd-144">O nome da zona também deve ser especificado, usando o parâmetro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="367bd-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="367bd-145">Você também pode especificar a zona e o grupo de recursos passando um objeto **dnsZone** usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="367bd-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367bd-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="367bd-146">-Zone</span></span>
<span data-ttu-id="367bd-147">Especifica a zona DNS que contém o conjunto de registros que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="367bd-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="367bd-148">Você também pode especificar a zona usando os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="367bd-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="367bd-149">-Zonename</span><span class="sxs-lookup"><span data-stu-id="367bd-149">-ZoneName</span></span>
<span data-ttu-id="367bd-150">Especifica o nome da zona DNS que contém o conjunto de registros a obter.</span><span class="sxs-lookup"><span data-stu-id="367bd-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="367bd-151">O grupo de recursos que contém a zona também deve ser especificado, usando o parâmetro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="367bd-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="367bd-152">Você também pode especificar a zona e o grupo de recursos, passando um objeto de zona DNS usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="367bd-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367bd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367bd-153">CommonParameters</span></span>
<span data-ttu-id="367bd-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="367bd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367bd-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="367bd-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367bd-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="367bd-156">INPUTS</span></span>

### <span data-ttu-id="367bd-157">System. String</span><span class="sxs-lookup"><span data-stu-id="367bd-157">System.String</span></span>

### <span data-ttu-id="367bd-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="367bd-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="367bd-159">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. RecordType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="367bd-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="367bd-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="367bd-160">OUTPUTS</span></span>

### <span data-ttu-id="367bd-161">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="367bd-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="367bd-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="367bd-162">NOTES</span></span>

## <span data-ttu-id="367bd-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="367bd-163">RELATED LINKS</span></span>

[<span data-ttu-id="367bd-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="367bd-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="367bd-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="367bd-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="367bd-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="367bd-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


