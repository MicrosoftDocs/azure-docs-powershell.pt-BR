---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115804"
---
# <span data-ttu-id="af3fe-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af3fe-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="af3fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="af3fe-103">Obtém um conjunto de registros DNS.</span><span class="sxs-lookup"><span data-stu-id="af3fe-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="af3fe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af3fe-104">SYNTAX</span></span>

### <span data-ttu-id="af3fe-105">Campos</span><span class="sxs-lookup"><span data-stu-id="af3fe-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af3fe-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="af3fe-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af3fe-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="af3fe-107">DESCRIPTION</span></span>
<span data-ttu-id="af3fe-108">O cmdlet **Get-AzDnsRecordSet** obtém o registro DNS (Sistema de Nomes de Domínio) definido com o nome e o tipo especificados, na zona especificada.</span><span class="sxs-lookup"><span data-stu-id="af3fe-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="af3fe-109">Se você não especificar os parâmetros *Nome* ou *RecordType,* esse cmdlet retornará todos os conjuntos de registros do tipo especificado na zona.</span><span class="sxs-lookup"><span data-stu-id="af3fe-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="af3fe-110">Se você especificar o parâmetro  *RecordType,* mas não o parâmetro Nome, esse cmdlet retornará todos os conjuntos de registros do tipo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="af3fe-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="af3fe-111">Você pode usar o operador de pipeline para passar um objeto **DnsZone** para esse cmdlet, ou pode passar um objeto **DnsZone** como o parâmetro *Zona* ou, alternativamente, pode especificar a zona e o grupo de recursos por nome.</span><span class="sxs-lookup"><span data-stu-id="af3fe-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="af3fe-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="af3fe-112">EXAMPLES</span></span>

### <span data-ttu-id="af3fe-113">Exemplo 1: Obter conjuntos de registros com um nome e tipo especificados</span><span class="sxs-lookup"><span data-stu-id="af3fe-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="af3fe-114">Esse comando obtém o conjunto de registros do tipo de registro A nomeado www no grupo de recursos e zona especificados e o armazena na variável $RecordSet registro.</span><span class="sxs-lookup"><span data-stu-id="af3fe-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="af3fe-115">Como os *parâmetros Nome* e *RecordType* são especificados, apenas um objeto **RecordSet** é retornado.</span><span class="sxs-lookup"><span data-stu-id="af3fe-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="af3fe-116">Exemplo 2: Obter conjuntos de registros de um tipo especificado</span><span class="sxs-lookup"><span data-stu-id="af3fe-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="af3fe-117">Esse comando obtém uma matriz de todos os conjuntos de registros do tipo de registro A na zona chamada myzone.com no grupo de recursos chamado MyResourceGroup e os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="af3fe-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="af3fe-118">Exemplo 3: Obter todos os conjuntos de registros em uma zona</span><span class="sxs-lookup"><span data-stu-id="af3fe-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="af3fe-119">Esse comando obtém uma matriz de todos os conjuntos de registros na zona chamada myzone.com no grupo de recursos chamado MyResourceGroup e os armazena na variável $RecordSets dados.</span><span class="sxs-lookup"><span data-stu-id="af3fe-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="af3fe-120">Exemplo 4: Obter todos os conjuntos de registros em uma zona, usando um objeto DnsZone</span><span class="sxs-lookup"><span data-stu-id="af3fe-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="af3fe-121">Este exemplo equivale ao Exemplo 3 acima.</span><span class="sxs-lookup"><span data-stu-id="af3fe-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="af3fe-122">Desta vez, a zona é especificada usando um objeto de zona.</span><span class="sxs-lookup"><span data-stu-id="af3fe-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="af3fe-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af3fe-123">PARAMETERS</span></span>

### <span data-ttu-id="af3fe-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af3fe-124">-DefaultProfile</span></span>
<span data-ttu-id="af3fe-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="af3fe-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af3fe-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="af3fe-126">-Name</span></span>
<span data-ttu-id="af3fe-127">Especifica o nome do **RecordSet a** ser obter.</span><span class="sxs-lookup"><span data-stu-id="af3fe-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="af3fe-128">Se você não especificar o parâmetro *Nome,* todos os conjuntos de registros do tipo especificado serão retornados.</span><span class="sxs-lookup"><span data-stu-id="af3fe-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="af3fe-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="af3fe-129">-RecordType</span></span>
<span data-ttu-id="af3fe-130">Especifica o tipo de registro DNS que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="af3fe-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="af3fe-131">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="af3fe-131">Valid values are:</span></span> 
- <span data-ttu-id="af3fe-132">Um</span><span class="sxs-lookup"><span data-stu-id="af3fe-132">A</span></span>
- <span data-ttu-id="af3fe-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="af3fe-133">AAAA</span></span>
- <span data-ttu-id="af3fe-134">Cname</span><span class="sxs-lookup"><span data-stu-id="af3fe-134">CNAME</span></span>
- <span data-ttu-id="af3fe-135">Mx</span><span class="sxs-lookup"><span data-stu-id="af3fe-135">MX</span></span>
- <span data-ttu-id="af3fe-136">Ns</span><span class="sxs-lookup"><span data-stu-id="af3fe-136">NS</span></span>
- <span data-ttu-id="af3fe-137">Ptr</span><span class="sxs-lookup"><span data-stu-id="af3fe-137">PTR</span></span>
- <span data-ttu-id="af3fe-138">SOA</span><span class="sxs-lookup"><span data-stu-id="af3fe-138">SOA</span></span>
- <span data-ttu-id="af3fe-139">Srv</span><span class="sxs-lookup"><span data-stu-id="af3fe-139">SRV</span></span>
- <span data-ttu-id="af3fe-140">TXT Se você não especificar o parâmetro *RecordType,* também deverá omitir o *parâmetro* Nome.</span><span class="sxs-lookup"><span data-stu-id="af3fe-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="af3fe-141">Esse cmdlet retorna todos os conjuntos de registros na zona (de todos os nomes e tipos).</span><span class="sxs-lookup"><span data-stu-id="af3fe-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

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

### <span data-ttu-id="af3fe-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af3fe-142">-ResourceGroupName</span></span>
<span data-ttu-id="af3fe-143">Especifica o grupo de recursos que contém a zona DNS.</span><span class="sxs-lookup"><span data-stu-id="af3fe-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="af3fe-144">O nome da zona também deve ser especificado, usando o parâmetro *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="af3fe-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="af3fe-145">Como alternativa, você pode especificar a zona e o grupo de recursos passando um objeto **DnsZone** usando o *parâmetro Zona.*</span><span class="sxs-lookup"><span data-stu-id="af3fe-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="af3fe-146">-Zona</span><span class="sxs-lookup"><span data-stu-id="af3fe-146">-Zone</span></span>
<span data-ttu-id="af3fe-147">Especifica a zona DNS que contém o conjunto de registros que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="af3fe-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="af3fe-148">Como alternativa, você pode especificar a zona usando os parâmetros *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="af3fe-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="af3fe-149">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="af3fe-149">-ZoneName</span></span>
<span data-ttu-id="af3fe-150">Especifica o nome da zona DNS que contém o conjunto de registros a ser obter.</span><span class="sxs-lookup"><span data-stu-id="af3fe-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="af3fe-151">O grupo de recursos que contém a zona também deve ser especificado, usando o parâmetro *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="af3fe-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="af3fe-152">Como alternativa, você pode especificar a zona e o grupo de recursos passando um objeto de Zona DNS usando o *parâmetro Zona.*</span><span class="sxs-lookup"><span data-stu-id="af3fe-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="af3fe-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af3fe-153">CommonParameters</span></span>
<span data-ttu-id="af3fe-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af3fe-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af3fe-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af3fe-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af3fe-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="af3fe-156">INPUTS</span></span>

### <span data-ttu-id="af3fe-157">System.String</span><span class="sxs-lookup"><span data-stu-id="af3fe-157">System.String</span></span>

### <span data-ttu-id="af3fe-158">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="af3fe-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="af3fe-159">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="af3fe-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="af3fe-160">Saídas</span><span class="sxs-lookup"><span data-stu-id="af3fe-160">OUTPUTS</span></span>

### <span data-ttu-id="af3fe-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af3fe-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="af3fe-162">Notas</span><span class="sxs-lookup"><span data-stu-id="af3fe-162">NOTES</span></span>

## <span data-ttu-id="af3fe-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af3fe-163">RELATED LINKS</span></span>

[<span data-ttu-id="af3fe-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af3fe-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="af3fe-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af3fe-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="af3fe-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af3fe-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


