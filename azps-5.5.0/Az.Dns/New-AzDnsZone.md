---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126985"
---
# <span data-ttu-id="ffb30-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="ffb30-101">New-AzDnsZone</span></span>

## <span data-ttu-id="ffb30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ffb30-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb30-103">Cria uma nova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="ffb30-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="ffb30-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ffb30-104">SYNTAX</span></span>

### <span data-ttu-id="ffb30-105">Ids (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ffb30-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffb30-106">Nomes</span><span class="sxs-lookup"><span data-stu-id="ffb30-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffb30-107">Objetos</span><span class="sxs-lookup"><span data-stu-id="ffb30-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffb30-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ffb30-108">DESCRIPTION</span></span>
<span data-ttu-id="ffb30-109">O cmdlet **New-AzDnsZone** cria uma nova zona DNS (Sistema de Nomes de Domínio) no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="ffb30-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="ffb30-110">Você deve especificar um nome de zona DNS exclusivo *para* o parâmetro Nome ou o cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="ffb30-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="ffb30-111">Depois que a zona for criada, use o cmdlet New-AzDnsRecordSet para criar conjuntos de registros na zona.</span><span class="sxs-lookup"><span data-stu-id="ffb30-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="ffb30-112">Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="ffb30-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="ffb30-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ffb30-113">EXAMPLES</span></span>

### <span data-ttu-id="ffb30-114">Exemplo 1: Criar uma zona DNS</span><span class="sxs-lookup"><span data-stu-id="ffb30-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ffb30-115">Esse comando cria uma nova zona DNS chamada myzone.com no grupo de recursos especificado e a armazena na variável $Zone dados.</span><span class="sxs-lookup"><span data-stu-id="ffb30-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="ffb30-116">Exemplo 2: criar uma zona DNS particular especificando IDs de rede virtual</span><span class="sxs-lookup"><span data-stu-id="ffb30-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="ffb30-117">Esse comando cria uma nova zona DNS particular chamada myprivatezone.com no grupo de recursos especificado com uma rede virtual de resolução associada (especificando sua ID) e a armazena na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="ffb30-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="ffb30-118">Exemplo 3: criar uma zona DNS particular especificando objetos de rede virtual</span><span class="sxs-lookup"><span data-stu-id="ffb30-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="ffb30-119">Esse comando cria uma nova zona DNS particular chamada myprivatezone.com no grupo de recursos especificado com uma rede virtual de resolução associada (chamada de variável $ResVirtualNetwork) e a armazena na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="ffb30-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="ffb30-120">Exemplo 4: Criar uma zona DNS com delegação especificando o nome da zona pai</span><span class="sxs-lookup"><span data-stu-id="ffb30-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="ffb30-121">Esse comando cria uma nova zona DNS filho chamada mychild.zone.com no grupo de recursos especificado e armazena na variável $Zone filho.</span><span class="sxs-lookup"><span data-stu-id="ffb30-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="ffb30-122">Ele também adiciona delegação na zona DNS pai chamada zone.com residindo na mesma assinatura e grupo de recursos da zona filho.</span><span class="sxs-lookup"><span data-stu-id="ffb30-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="ffb30-123">Exemplo 5: Criar uma zona DNS com delegação especificando a ID da zona pai</span><span class="sxs-lookup"><span data-stu-id="ffb30-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="ffb30-124">Esse comando cria uma nova zona DNS filho chamada mychild.zone.com no grupo de recursos especificado e armazena na variável $Zone filho.</span><span class="sxs-lookup"><span data-stu-id="ffb30-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="ffb30-125">Ele também adiciona uma delegação na zona DNS pai chamada zone.com no grupo de recursos que outra assinatura fornecida é igual à da zona filho criada.</span><span class="sxs-lookup"><span data-stu-id="ffb30-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="ffb30-126">Exemplo 6: Criar uma zona DNS com delegação especificando o objeto de zona pai</span><span class="sxs-lookup"><span data-stu-id="ffb30-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="ffb30-127">Esse comando cria uma nova zona DNS filho chamada mychild.zone.com no grupo de recursos especificado e armazena na variável $Zone filho.</span><span class="sxs-lookup"><span data-stu-id="ffb30-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="ffb30-128">Ele também adiciona delegação na zona DNS pai chamada zone.com conforme passado no objeto ParentZone</span><span class="sxs-lookup"><span data-stu-id="ffb30-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="ffb30-129">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffb30-129">PARAMETERS</span></span>

### <span data-ttu-id="ffb30-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb30-130">-DefaultProfile</span></span>
<span data-ttu-id="ffb30-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ffb30-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffb30-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffb30-132">-Name</span></span>
<span data-ttu-id="ffb30-133">Especifica o nome da zona DNS a ser criada.</span><span class="sxs-lookup"><span data-stu-id="ffb30-133">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="ffb30-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="ffb30-134">-ParentZone</span></span>
<span data-ttu-id="ffb30-135">O nome completo da zona pai para adicionar delegação (sem um ponto de término).</span><span class="sxs-lookup"><span data-stu-id="ffb30-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="ffb30-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="ffb30-136">-ParentZoneId</span></span>
<span data-ttu-id="ffb30-137">A ID do recurso da zona pai para adicionar delegação (sem um ponto de término).</span><span class="sxs-lookup"><span data-stu-id="ffb30-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="ffb30-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="ffb30-138">-ParentZoneName</span></span>
<span data-ttu-id="ffb30-139">O nome completo da zona pai para adicionar delegação (sem um ponto de término).</span><span class="sxs-lookup"><span data-stu-id="ffb30-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="ffb30-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ffb30-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="ffb30-141">A lista de redes virtuais que registrarão registros de nomes de host de máquina virtual nessa zona DNS, disponível apenas para zonas particulares.</span><span class="sxs-lookup"><span data-stu-id="ffb30-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="ffb30-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ffb30-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="ffb30-143">A lista de IDs de rede virtual que registrarão registros de nomes de host de máquina virtual nessa zona DNS, disponível somente para zonas particulares.</span><span class="sxs-lookup"><span data-stu-id="ffb30-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="ffb30-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ffb30-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="ffb30-145">A lista de redes virtuais capazes de resolver registros nessa zona DNS, disponível apenas para zonas particulares.</span><span class="sxs-lookup"><span data-stu-id="ffb30-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="ffb30-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ffb30-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="ffb30-147">A lista de IDs de rede virtual capaz de resolver registros nessa zona DNS, disponível apenas para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="ffb30-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="ffb30-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffb30-148">-ResourceGroupName</span></span>
<span data-ttu-id="ffb30-149">Especifica o grupo de recursos no qual criar a zona.</span><span class="sxs-lookup"><span data-stu-id="ffb30-149">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="ffb30-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="ffb30-150">-Tag</span></span>
<span data-ttu-id="ffb30-151">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ffb30-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ffb30-152">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ffb30-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ffb30-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="ffb30-153">-ZoneType</span></span>
<span data-ttu-id="ffb30-154">O tipo da zona, Público ou Particular.</span><span class="sxs-lookup"><span data-stu-id="ffb30-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="ffb30-155">Zonas sem um tipo ou com um tipo de Público são disponibilizadas no plano público de serviço DNS para uso na hierarquia DNS.</span><span class="sxs-lookup"><span data-stu-id="ffb30-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="ffb30-156">As zonas com um tipo de Particular só ficam visíveis com o conjunto de redes virtuais associadas (este recurso está na visualização).</span><span class="sxs-lookup"><span data-stu-id="ffb30-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="ffb30-157">Essa propriedade não pode ser alterada para uma zona.</span><span class="sxs-lookup"><span data-stu-id="ffb30-157">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="ffb30-158">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ffb30-158">-Confirm</span></span>
<span data-ttu-id="ffb30-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffb30-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffb30-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffb30-160">-WhatIf</span></span>
<span data-ttu-id="ffb30-161">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ffb30-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffb30-162">O cmdlet não é executado. Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ffb30-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffb30-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffb30-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffb30-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb30-164">CommonParameters</span></span>
<span data-ttu-id="ffb30-165">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffb30-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb30-166">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffb30-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb30-167">Entradas</span><span class="sxs-lookup"><span data-stu-id="ffb30-167">INPUTS</span></span>

### <span data-ttu-id="ffb30-168">System.String</span><span class="sxs-lookup"><span data-stu-id="ffb30-168">System.String</span></span>

### <span data-ttu-id="ffb30-169">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ffb30-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ffb30-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ffb30-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ffb30-171">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ffb30-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ffb30-172">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ffb30-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ffb30-173">Saídas</span><span class="sxs-lookup"><span data-stu-id="ffb30-173">OUTPUTS</span></span>

### <span data-ttu-id="ffb30-174">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="ffb30-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="ffb30-175">Notas</span><span class="sxs-lookup"><span data-stu-id="ffb30-175">NOTES</span></span>
<span data-ttu-id="ffb30-176">Você pode usar o *parâmetro Confirmar* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="ffb30-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ffb30-177">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference Windows PowerShell tem um valor médio ou inferior.</span><span class="sxs-lookup"><span data-stu-id="ffb30-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="ffb30-178">Se você especificar *Confirmar* ou *Confirmar:$True,* este cmdlet solicitará que você confirme antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="ffb30-178">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="ffb30-179">Se você especificar *Confirm:$False,* o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="ffb30-179">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ffb30-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffb30-180">RELATED LINKS</span></span>

[<span data-ttu-id="ffb30-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="ffb30-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="ffb30-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ffb30-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="ffb30-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="ffb30-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
