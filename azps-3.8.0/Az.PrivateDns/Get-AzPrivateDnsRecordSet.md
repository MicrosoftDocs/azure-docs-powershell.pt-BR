---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: ade9d95b6388a667f55df24db107a2326fa001ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942482"
---
# <span data-ttu-id="b5c1e-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b5c1e-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="b5c1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c1e-103">Obtém um conjunto de registros de uma zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="b5c1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5c1e-104">SYNTAX</span></span>

### <span data-ttu-id="b5c1e-105">FieldsWithNoName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b5c1e-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5c1e-106">Campos</span><span class="sxs-lookup"><span data-stu-id="b5c1e-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5c1e-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="b5c1e-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5c1e-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="b5c1e-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5c1e-109">Identificação</span><span class="sxs-lookup"><span data-stu-id="b5c1e-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5c1e-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="b5c1e-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5c1e-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5c1e-111">DESCRIPTION</span></span>
<span data-ttu-id="b5c1e-112">O cmdlet Get-AzPrivateDnsRecordSet Obtém o conjunto de registros DNS (sistema de nomes de domínio) privado com o nome e o tipo especificados, na zona privada especificada.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="b5c1e-113">Se você não especificar os parâmetros Name ou RecordType, esse cmdlet retornará todos os conjuntos de registros do tipo especificado na zona privada.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="b5c1e-114">Se você especificar o parâmetro RecordType, mas não o parâmetro Name, esse cmdlet retornará todos os conjuntos de registros do tipo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="b5c1e-115">Você pode usar o operador de pipeline para passar um objeto PSPrivateDnsZone para esse cmdlet, ou pode passar um objeto PSPrivateDnsZone como o parâmetro de zona ou também pode especificar a zona e o grupo de recursos por nome.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="b5c1e-116">Você também pode especificar a zona privada usando a ID do recurso da zona privada.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="b5c1e-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5c1e-117">EXAMPLES</span></span>

### <span data-ttu-id="b5c1e-118">Exemplo 1: obter conjuntos de registros com um nome e tipo especificados</span><span class="sxs-lookup"><span data-stu-id="b5c1e-118">Example 1: Get record sets with a specified name and type</span></span>
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

<span data-ttu-id="b5c1e-119">Esse comando obtém o conjunto de registros do tipo de registro um chamado www no grupo de recursos e na zona privada especificado e, em seguida, armazena-o na variável $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="b5c1e-120">Como os parâmetros Name e RecordType são especificados, apenas um objeto RecordSet é retornado.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="b5c1e-121">Exemplo 2: obter conjuntos de registros de um tipo especificado</span><span class="sxs-lookup"><span data-stu-id="b5c1e-121">Example 2: Get record sets of a specified type</span></span>
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

<span data-ttu-id="b5c1e-122">Esse comando obtém uma matriz de todos os conjuntos de registros do tipo de registro A na zona privada chamada myzone.com no grupo de recursos chamado MyResource e, em seguida, os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="b5c1e-123">Exemplo 3: obter todos os conjuntos de registros em uma zona privada</span><span class="sxs-lookup"><span data-stu-id="b5c1e-123">Example 3: Get all record sets in a private zone</span></span>
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

<span data-ttu-id="b5c1e-124">Esse comando obtém uma matriz de todos os conjuntos de registros na zona privada chamada myzone.com no grupo de recursos chamado MyResource Group e, em seguida, os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="b5c1e-125">Exemplo 4: obter todos os conjuntos de registros em uma zona privada, usando um objeto PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b5c1e-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
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

<span data-ttu-id="b5c1e-126">Este exemplo é equivalente ao exemplo 3 acima.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="b5c1e-127">Nesse momento, a zona privada é especificada usando um objeto de zona particular.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="b5c1e-128">OS</span><span class="sxs-lookup"><span data-stu-id="b5c1e-128">PARAMETERS</span></span>

### <span data-ttu-id="b5c1e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c1e-129">-DefaultProfile</span></span>
<span data-ttu-id="b5c1e-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5c1e-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5c1e-131">-Name</span></span>
<span data-ttu-id="b5c1e-132">O nome dos registros nesse conjunto de registros (relativo ao nome da zona e sem um ponto final).</span><span class="sxs-lookup"><span data-stu-id="b5c1e-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="b5c1e-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b5c1e-133">-ParentResourceId</span></span>
<span data-ttu-id="b5c1e-134">ResourceId de zona DNS particular.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-134">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="b5c1e-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="b5c1e-135">-RecordType</span></span>
<span data-ttu-id="b5c1e-136">O tipo de registros DNS nesse conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-136">The type of DNS records in this record set.</span></span>

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

### <span data-ttu-id="b5c1e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c1e-137">-ResourceGroupName</span></span>
<span data-ttu-id="b5c1e-138">O grupo de recursos ao qual a zona pertence.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-138">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="b5c1e-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="b5c1e-139">-Zone</span></span>
<span data-ttu-id="b5c1e-140">O objeto DnsZone que representa a zona na qual criar o conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-140">The DnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="b5c1e-141">-Zonename</span><span class="sxs-lookup"><span data-stu-id="b5c1e-141">-ZoneName</span></span>
<span data-ttu-id="b5c1e-142">A zona na qual criar o conjunto de registros (sem um ponto final).</span><span class="sxs-lookup"><span data-stu-id="b5c1e-142">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="b5c1e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c1e-143">CommonParameters</span></span>
<span data-ttu-id="b5c1e-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c1e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c1e-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c1e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c1e-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5c1e-146">INPUTS</span></span>

### <span data-ttu-id="b5c1e-147">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b5c1e-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="b5c1e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b5c1e-148">System.String</span></span>

## <span data-ttu-id="b5c1e-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5c1e-149">OUTPUTS</span></span>

### <span data-ttu-id="b5c1e-150">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b5c1e-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="b5c1e-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5c1e-151">NOTES</span></span>

## <span data-ttu-id="b5c1e-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5c1e-152">RELATED LINKS</span></span>
