---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 101440e65fbc0bb21311757a8792a2d45f855364
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596554"
---
# <span data-ttu-id="a9e1c-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a9e1c-101">New-AzDnsZone</span></span>

## <span data-ttu-id="a9e1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e1c-103">Cria uma nova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="a9e1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9e1c-104">SYNTAX</span></span>

### <span data-ttu-id="a9e1c-105">IDs (padrão)</span><span class="sxs-lookup"><span data-stu-id="a9e1c-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9e1c-106">Os</span><span class="sxs-lookup"><span data-stu-id="a9e1c-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9e1c-107">Eles</span><span class="sxs-lookup"><span data-stu-id="a9e1c-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9e1c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9e1c-108">DESCRIPTION</span></span>
<span data-ttu-id="a9e1c-109">O cmdlet **New-AzDnsZone** cria uma nova zona de sistema de nomes de domínio (DNS) no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="a9e1c-110">Você deve especificar um nome de zona DNS exclusivo para o parâmetro *Name* , ou o cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="a9e1c-111">Após a criação da zona, use o cmdlet New-AzDnsRecordSet para criar conjuntos de registros na zona.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="a9e1c-112">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="a9e1c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9e1c-113">EXAMPLES</span></span>

### <span data-ttu-id="a9e1c-114">Exemplo 1: criar uma zona DNS</span><span class="sxs-lookup"><span data-stu-id="a9e1c-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a9e1c-115">Esse comando cria uma nova zona DNS chamada myzone.com no grupo de recursos especificado e armazena-a na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="a9e1c-116">Exemplo 2: criar uma zona DNS privada especificando IDs de rede virtual</span><span class="sxs-lookup"><span data-stu-id="a9e1c-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="a9e1c-117">Esse comando cria uma nova zona DNS privada chamada myprivatezone.com no grupo de recursos especificado com uma rede virtual de resolução associada (especificando sua ID) e a armazena na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="a9e1c-118">Exemplo 3: criar uma zona DNS privada especificando objetos de rede virtual</span><span class="sxs-lookup"><span data-stu-id="a9e1c-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="a9e1c-119">Esse comando cria uma nova zona DNS privada chamada myprivatezone.com no grupo de recursos especificado com uma rede virtual de resolução associada (referida pela variável $ResVirtualNetwork) e a armazena na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="a9e1c-120">Exemplo 4: criar uma zona DNS com delegação especificando o nome da zona pai</span><span class="sxs-lookup"><span data-stu-id="a9e1c-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="a9e1c-121">Esse comando cria uma nova zona DNS filho chamada mychild.zone.com no grupo de recursos e repositórios especificado na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="a9e1c-122">Ele também adiciona delegação na zona DNS pai chamada zone.com que reside na mesma assinatura e grupo de recursos que a zona filho.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="a9e1c-123">Exemplo 5: criar uma zona DNS com delegação especificando a ID da zona pai</span><span class="sxs-lookup"><span data-stu-id="a9e1c-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="a9e1c-124">Esse comando cria uma nova zona DNS filho chamada mychild.zone.com no grupo de recursos e repositórios especificado na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="a9e1c-125">Ele também adiciona delegação na zona DNS pai chamada zone.com no grupo de recursos outro-RG a assinatura fornecida é igual à da zona filho criada.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="a9e1c-126">Exemplo 6: criar uma zona DNS com delegação especificando o objeto de zona pai</span><span class="sxs-lookup"><span data-stu-id="a9e1c-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="a9e1c-127">Esse comando cria uma nova zona DNS filho chamada mychild.zone.com no grupo de recursos e repositórios especificado na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="a9e1c-128">Ele também adiciona delegação na zona DNS pai chamada zone.com conforme passado no objeto ParentZone</span><span class="sxs-lookup"><span data-stu-id="a9e1c-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="a9e1c-129">OS</span><span class="sxs-lookup"><span data-stu-id="a9e1c-129">PARAMETERS</span></span>

### <span data-ttu-id="a9e1c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e1c-130">-DefaultProfile</span></span>
<span data-ttu-id="a9e1c-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a9e1c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9e1c-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9e1c-132">-Name</span></span>
<span data-ttu-id="a9e1c-133">Especifica o nome da zona DNS a ser criada.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-133">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="a9e1c-134">-ParentZone</span></span>
<span data-ttu-id="a9e1c-135">O nome completo da zona pai para adicionar delegação (sem um ponto de terminação).</span><span class="sxs-lookup"><span data-stu-id="a9e1c-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="a9e1c-136">-ParentZoneId</span></span>
<span data-ttu-id="a9e1c-137">A ID do recurso da zona pai para adicionar delegação (sem um ponto final).</span><span class="sxs-lookup"><span data-stu-id="a9e1c-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="a9e1c-138">-ParentZoneName</span></span>
<span data-ttu-id="a9e1c-139">O nome completo da zona pai para adicionar delegação (sem um ponto de terminação).</span><span class="sxs-lookup"><span data-stu-id="a9e1c-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a9e1c-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="a9e1c-141">A lista de redes virtuais que registrarão os registros de hosts de máquina virtual nesta zona de DNS, disponível somente para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="a9e1c-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="a9e1c-143">A lista de IDs de rede virtual que registrará os registros de hosts de máquina virtual nesta zona de DNS, somente disponível para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a9e1c-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="a9e1c-145">A lista de redes virtuais capazes de resolver registros nesta zona DNS, disponível somente para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="a9e1c-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="a9e1c-147">A lista de IDs de rede virtual é capaz de resolver registros nesta zona DNS, disponível somente para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e1c-148">-ResourceGroupName</span></span>
<span data-ttu-id="a9e1c-149">Especifica o grupo de recursos no qual a zona será criada.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-149">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-150">-Marca</span><span class="sxs-lookup"><span data-stu-id="a9e1c-150">-Tag</span></span>
<span data-ttu-id="a9e1c-151">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a9e1c-152">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a9e1c-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-153">-Zonetype</span><span class="sxs-lookup"><span data-stu-id="a9e1c-153">-ZoneType</span></span>
<span data-ttu-id="a9e1c-154">O tipo da zona, pública ou particular.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="a9e1c-155">Zonas sem tipo ou com um tipo de público são disponibilizadas no plano de serviços DNS públicos para uso na hierarquia de DNS.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="a9e1c-156">As zonas com um tipo de privado são visíveis apenas de um conjunto de redes virtuais associadas (esse recurso está em visualização).</span><span class="sxs-lookup"><span data-stu-id="a9e1c-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="a9e1c-157">Esta propriedade não pode ser alterada para uma zona.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-157">This property cannot be changed for a zone.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9e1c-158">-Confirm</span></span>
<span data-ttu-id="a9e1c-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9e1c-160">-WhatIf</span></span>
<span data-ttu-id="a9e1c-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9e1c-162">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9e1c-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9e1c-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e1c-164">CommonParameters</span></span>
<span data-ttu-id="a9e1c-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e1c-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9e1c-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e1c-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9e1c-167">INPUTS</span></span>

### <span data-ttu-id="a9e1c-168">System. String</span><span class="sxs-lookup"><span data-stu-id="a9e1c-168">System.String</span></span>

### <span data-ttu-id="a9e1c-169">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. Zonetype, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a9e1c-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a9e1c-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a9e1c-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a9e1c-171">System. Collections. Generic. List ' 1 [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a9e1c-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a9e1c-172">System. Collections. Generic. List ' 1 [Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a9e1c-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a9e1c-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9e1c-173">OUTPUTS</span></span>

### <span data-ttu-id="a9e1c-174">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a9e1c-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="a9e1c-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9e1c-175">NOTES</span></span>
<span data-ttu-id="a9e1c-176">Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="a9e1c-177">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="a9e1c-178">Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-178">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="a9e1c-179">Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="a9e1c-179">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a9e1c-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9e1c-180">RELATED LINKS</span></span>

[<span data-ttu-id="a9e1c-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a9e1c-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="a9e1c-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a9e1c-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="a9e1c-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a9e1c-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
