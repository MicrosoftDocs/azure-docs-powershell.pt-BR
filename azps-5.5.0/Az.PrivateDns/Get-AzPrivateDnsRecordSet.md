---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: ade9d95b6388a667f55df24db107a2326fa001ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117251"
---
# <span data-ttu-id="945b6-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="945b6-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="945b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="945b6-102">SYNOPSIS</span></span>
<span data-ttu-id="945b6-103">Obtém um conjunto de registros de uma zona DNS particular.</span><span class="sxs-lookup"><span data-stu-id="945b6-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="945b6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="945b6-104">SYNTAX</span></span>

### <span data-ttu-id="945b6-105">FieldsWithNoName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="945b6-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="945b6-106">Campos</span><span class="sxs-lookup"><span data-stu-id="945b6-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="945b6-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="945b6-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="945b6-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="945b6-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="945b6-109">Resourceid</span><span class="sxs-lookup"><span data-stu-id="945b6-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="945b6-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="945b6-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="945b6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="945b6-111">DESCRIPTION</span></span>
<span data-ttu-id="945b6-112">O Get-AzPrivateDnsRecordSet cmdlet obtém o registro DNS (Sistema de Nomes de Domínio Particular) definido com o nome e o tipo especificados, na zona privada especificada.</span><span class="sxs-lookup"><span data-stu-id="945b6-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="945b6-113">Se você não especificar os parâmetros Nome ou RecordType, esse cmdlet retornará todos os conjuntos de registros do tipo especificado na zona privada.</span><span class="sxs-lookup"><span data-stu-id="945b6-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="945b6-114">Se você especificar o parâmetro RecordType, mas não o parâmetro Nome, esse cmdlet retornará todos os conjuntos de registros do tipo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="945b6-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="945b6-115">Você pode usar o operador de pipeline para passar um objeto PSPrivateDnsZone para esse cmdlet, ou pode passar um objeto PSPrivateDnsZone como o parâmetro Zona ou, como alternativa, pode especificar a zona e o grupo de recursos por nome.</span><span class="sxs-lookup"><span data-stu-id="945b6-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="945b6-116">Você também pode especificar a zona privada usando a ID de Recurso da zona privada.</span><span class="sxs-lookup"><span data-stu-id="945b6-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="945b6-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="945b6-117">EXAMPLES</span></span>

### <span data-ttu-id="945b6-118">Exemplo 1: Obter conjuntos de registros com um nome e tipo especificados</span><span class="sxs-lookup"><span data-stu-id="945b6-118">Example 1: Get record sets with a specified name and type</span></span>
```powershell
PS C:\>$RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="945b6-119">Esse comando obtém o conjunto de registros do tipo de registro A nomeado www no grupo de recursos especificado e na zona privada e, em seguida, armazena-o na variável $RecordSet registro.</span><span class="sxs-lookup"><span data-stu-id="945b6-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="945b6-120">Como os parâmetros Nome e RecordType são especificados, apenas um objeto RecordSet é retornado.</span><span class="sxs-lookup"><span data-stu-id="945b6-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="945b6-121">Exemplo 2: Obter conjuntos de registros de um tipo especificado</span><span class="sxs-lookup"><span data-stu-id="945b6-121">Example 2: Get record sets of a specified type</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www2
Name              : www2
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {2.3.4.5}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="945b6-122">Esse comando obtém uma matriz de todos os conjuntos de registros do tipo de registro A na zona privada chamada myzone.com no grupo de recursos chamado MyResourceGroup e os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="945b6-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="945b6-123">Exemplo 3: Obter todos os conjuntos de registros em uma zona privada</span><span class="sxs-lookup"><span data-stu-id="945b6-123">Example 3: Get all record sets in a private zone</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="945b6-124">Esse comando obtém uma matriz de todos os conjuntos de registros na zona privada chamada myzone.com no grupo de recursos chamado MyResourceGroup e os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="945b6-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="945b6-125">Exemplo 4: Obter todos os conjuntos de registros em uma zona privada, usando um objeto PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="945b6-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
```powershell
PS C:\> $Zone = Get-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzPrivateDnsRecordSet -Zone $Zone

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="945b6-126">Este exemplo equivale ao Exemplo 3 acima.</span><span class="sxs-lookup"><span data-stu-id="945b6-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="945b6-127">Desta vez, a zona privada é especificada usando um objeto de zona particular.</span><span class="sxs-lookup"><span data-stu-id="945b6-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="945b6-128">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="945b6-128">PARAMETERS</span></span>

### <span data-ttu-id="945b6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="945b6-129">-DefaultProfile</span></span>
<span data-ttu-id="945b6-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="945b6-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="945b6-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="945b6-131">-Name</span></span>
<span data-ttu-id="945b6-132">O nome dos registros neste conjunto de registros (em relação ao nome da zona e sem um ponto de término).</span><span class="sxs-lookup"><span data-stu-id="945b6-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Object, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945b6-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="945b6-133">-ParentResourceId</span></span>
<span data-ttu-id="945b6-134">ID de Recurso de Zona DNS Particular.</span><span class="sxs-lookup"><span data-stu-id="945b6-134">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId, ResourceIdWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945b6-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="945b6-135">-RecordType</span></span>
<span data-ttu-id="945b6-136">O tipo de registros DNS neste conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="945b6-136">The type of DNS records in this record set.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: FieldsWithNoName, ObjectWithNoName, ResourceIdWithNoName
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: Fields, Object, ResourceId
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945b6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="945b6-137">-ResourceGroupName</span></span>
<span data-ttu-id="945b6-138">O grupo de recursos ao qual a zona pertence.</span><span class="sxs-lookup"><span data-stu-id="945b6-138">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945b6-139">-Zona</span><span class="sxs-lookup"><span data-stu-id="945b6-139">-Zone</span></span>
<span data-ttu-id="945b6-140">O objeto DnsZone que representa a zona na qual criar o conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="945b6-140">The DnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object, ObjectWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="945b6-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="945b6-141">-ZoneName</span></span>
<span data-ttu-id="945b6-142">A zona na qual criar o conjunto de registros (sem um ponto de término).</span><span class="sxs-lookup"><span data-stu-id="945b6-142">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945b6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945b6-143">CommonParameters</span></span>
<span data-ttu-id="945b6-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="945b6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945b6-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="945b6-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945b6-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="945b6-146">INPUTS</span></span>

### <span data-ttu-id="945b6-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="945b6-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="945b6-148">System.String</span><span class="sxs-lookup"><span data-stu-id="945b6-148">System.String</span></span>

## <span data-ttu-id="945b6-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="945b6-149">OUTPUTS</span></span>

### <span data-ttu-id="945b6-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="945b6-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="945b6-151">Notas</span><span class="sxs-lookup"><span data-stu-id="945b6-151">NOTES</span></span>

## <span data-ttu-id="945b6-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="945b6-152">RELATED LINKS</span></span>
