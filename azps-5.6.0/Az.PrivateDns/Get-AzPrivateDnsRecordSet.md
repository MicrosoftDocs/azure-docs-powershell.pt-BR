---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7ddc6b9621bbf156b386a0f67337edcc32e0363c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901447"
---
# <span data-ttu-id="fdc44-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fdc44-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="fdc44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdc44-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc44-103">Obtém um conjunto de registros de uma zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="fdc44-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="fdc44-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fdc44-104">SYNTAX</span></span>

### <span data-ttu-id="fdc44-105">FieldsWithNoName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fdc44-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdc44-106">Fields</span><span class="sxs-lookup"><span data-stu-id="fdc44-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdc44-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="fdc44-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdc44-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="fdc44-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdc44-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdc44-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdc44-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="fdc44-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdc44-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fdc44-111">DESCRIPTION</span></span>
<span data-ttu-id="fdc44-112">O Get-AzPrivateDnsRecordSet cmdlet obtém o registro DNS (Sistema de Nomes de Domínio Privado) definido com o nome e o tipo especificados, na zona privada especificada.</span><span class="sxs-lookup"><span data-stu-id="fdc44-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="fdc44-113">Se você não especificar os parâmetros Name ou RecordType, este cmdlet retornará todos os conjuntos de registros do tipo especificado na zona privada.</span><span class="sxs-lookup"><span data-stu-id="fdc44-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="fdc44-114">Se você especificar o parâmetro RecordType, mas não o parâmetro Name, este cmdlet retornará todos os conjuntos de registros do tipo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="fdc44-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="fdc44-115">Você pode usar o operador de pipeline para passar um objeto PSPrivateDnsZone para esse cmdlet, ou pode passar um objeto PSPrivateDnsZone como o parâmetro Zone ou, como alternativa, você pode especificar a zona e o grupo de recursos pelo nome.</span><span class="sxs-lookup"><span data-stu-id="fdc44-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="fdc44-116">Você também pode especificar a zona privada usando a ID de Recurso da zona privada.</span><span class="sxs-lookup"><span data-stu-id="fdc44-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="fdc44-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdc44-117">EXAMPLES</span></span>

### <span data-ttu-id="fdc44-118">Exemplo 1: Obter conjuntos de registros com um nome e tipo especificados</span><span class="sxs-lookup"><span data-stu-id="fdc44-118">Example 1: Get record sets with a specified name and type</span></span>
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

<span data-ttu-id="fdc44-119">Esse comando obtém o conjunto de registros do tipo de registro A denominado www no grupo de recursos especificado e zona privada e o armazena na variável $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="fdc44-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="fdc44-120">Como os parâmetros Name e RecordType são especificados, apenas um objeto RecordSet é retornado.</span><span class="sxs-lookup"><span data-stu-id="fdc44-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="fdc44-121">Exemplo 2: Obter conjuntos de registros de um tipo especificado</span><span class="sxs-lookup"><span data-stu-id="fdc44-121">Example 2: Get record sets of a specified type</span></span>
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

<span data-ttu-id="fdc44-122">Este comando obtém uma matriz de todos os conjuntos de registros do tipo de registro A na zona privada chamada myzone.com no grupo de recursos chamado MyResourceGroup e os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="fdc44-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="fdc44-123">Exemplo 3: Obter todos os conjuntos de registros em uma zona privada</span><span class="sxs-lookup"><span data-stu-id="fdc44-123">Example 3: Get all record sets in a private zone</span></span>
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

<span data-ttu-id="fdc44-124">Esse comando obtém uma matriz de todos os conjuntos de registros na zona privada chamada myzone.com no grupo de recursos chamado MyResourceGroup e os armazena na variável $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="fdc44-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="fdc44-125">Exemplo 4: Obter todos os conjuntos de registros em uma zona privada, usando um objeto PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="fdc44-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
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

<span data-ttu-id="fdc44-126">Este exemplo equivale ao Exemplo 3 acima.</span><span class="sxs-lookup"><span data-stu-id="fdc44-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="fdc44-127">Desta vez, a zona privada é especificada usando um objeto de zona privada.</span><span class="sxs-lookup"><span data-stu-id="fdc44-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="fdc44-128">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fdc44-128">PARAMETERS</span></span>

### <span data-ttu-id="fdc44-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc44-129">-DefaultProfile</span></span>
<span data-ttu-id="fdc44-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdc44-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdc44-131">-Name</span><span class="sxs-lookup"><span data-stu-id="fdc44-131">-Name</span></span>
<span data-ttu-id="fdc44-132">O nome dos registros neste conjunto de registros (em relação ao nome da zona e sem um ponto final).</span><span class="sxs-lookup"><span data-stu-id="fdc44-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="fdc44-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fdc44-133">-ParentResourceId</span></span>
<span data-ttu-id="fdc44-134">ResourceID de zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="fdc44-134">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="fdc44-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="fdc44-135">-RecordType</span></span>
<span data-ttu-id="fdc44-136">O tipo de registros DNS neste conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="fdc44-136">The type of DNS records in this record set.</span></span>

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

### <span data-ttu-id="fdc44-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdc44-137">-ResourceGroupName</span></span>
<span data-ttu-id="fdc44-138">O grupo de recursos ao qual a zona pertence.</span><span class="sxs-lookup"><span data-stu-id="fdc44-138">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="fdc44-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="fdc44-139">-Zone</span></span>
<span data-ttu-id="fdc44-140">O objeto DnsZone que representa a zona na qual criar o conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="fdc44-140">The DnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="fdc44-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="fdc44-141">-ZoneName</span></span>
<span data-ttu-id="fdc44-142">A zona na qual criar o conjunto de registros (sem um ponto final).</span><span class="sxs-lookup"><span data-stu-id="fdc44-142">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="fdc44-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc44-143">CommonParameters</span></span>
<span data-ttu-id="fdc44-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdc44-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc44-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdc44-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc44-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fdc44-146">INPUTS</span></span>

### <span data-ttu-id="fdc44-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="fdc44-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="fdc44-148">System.String</span><span class="sxs-lookup"><span data-stu-id="fdc44-148">System.String</span></span>

## <span data-ttu-id="fdc44-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fdc44-149">OUTPUTS</span></span>

### <span data-ttu-id="fdc44-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fdc44-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="fdc44-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="fdc44-151">NOTES</span></span>

## <span data-ttu-id="fdc44-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdc44-152">RELATED LINKS</span></span>
