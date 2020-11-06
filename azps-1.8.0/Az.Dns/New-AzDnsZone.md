---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: eb7a2f3494521a5505db0224bb1ae0ff948d406f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600891"
---
# <span data-ttu-id="dac25-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="dac25-101">New-AzDnsZone</span></span>

## <span data-ttu-id="dac25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dac25-102">SYNOPSIS</span></span>
<span data-ttu-id="dac25-103">Cria uma nova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="dac25-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="dac25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dac25-104">SYNTAX</span></span>

### <span data-ttu-id="dac25-105">IDs (padrão)</span><span class="sxs-lookup"><span data-stu-id="dac25-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dac25-106">Eles</span><span class="sxs-lookup"><span data-stu-id="dac25-106">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dac25-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dac25-107">DESCRIPTION</span></span>
<span data-ttu-id="dac25-108">O cmdlet **New-AzDnsZone** cria uma nova zona de sistema de nomes de domínio (DNS) no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="dac25-108">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="dac25-109">Você deve especificar um nome de zona DNS exclusivo para o parâmetro *Name* , ou o cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="dac25-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="dac25-110">Após a criação da zona, use o cmdlet New-AzDnsRecordSet para criar conjuntos de registros na zona.</span><span class="sxs-lookup"><span data-stu-id="dac25-110">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="dac25-111">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="dac25-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="dac25-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dac25-112">EXAMPLES</span></span>

### <span data-ttu-id="dac25-113">Exemplo 1: criar uma zona DNS</span><span class="sxs-lookup"><span data-stu-id="dac25-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="dac25-114">Esse comando cria uma nova zona DNS chamada myzone.com no grupo de recursos especificado e armazena-a na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="dac25-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="dac25-115">Exemplo 2: criar uma zona DNS privada especificando IDs de rede virtual</span><span class="sxs-lookup"><span data-stu-id="dac25-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="dac25-116">Esse comando cria uma nova zona DNS privada chamada myprivatezone.com no grupo de recursos especificado com uma rede virtual de resolução associada (especificando sua ID) e a armazena na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="dac25-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="dac25-117">Exemplo 3: criar uma zona DNS privada especificando objetos de rede virtual</span><span class="sxs-lookup"><span data-stu-id="dac25-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="dac25-118">Esse comando cria uma nova zona DNS privada chamada myprivatezone.com no grupo de recursos especificado com uma rede virtual de resolução associada (referida pela variável $ResVirtualNetwork) e a armazena na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="dac25-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="dac25-119">OS</span><span class="sxs-lookup"><span data-stu-id="dac25-119">PARAMETERS</span></span>

### <span data-ttu-id="dac25-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac25-120">-DefaultProfile</span></span>
<span data-ttu-id="dac25-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dac25-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dac25-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="dac25-122">-Name</span></span>
<span data-ttu-id="dac25-123">Especifica o nome da zona DNS a ser criada.</span><span class="sxs-lookup"><span data-stu-id="dac25-123">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="dac25-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dac25-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="dac25-125">A lista de redes virtuais que registrarão os registros de hosts de máquina virtual nesta zona de DNS, disponível somente para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="dac25-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="dac25-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="dac25-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="dac25-127">A lista de IDs de rede virtual que registrará os registros de hosts de máquina virtual nesta zona de DNS, somente disponível para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="dac25-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="dac25-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dac25-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="dac25-129">A lista de redes virtuais capazes de resolver registros nesta zona DNS, disponível somente para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="dac25-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="dac25-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="dac25-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="dac25-131">A lista de IDs de rede virtual é capaz de resolver registros nesta zona DNS, disponível somente para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="dac25-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="dac25-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dac25-132">-ResourceGroupName</span></span>
<span data-ttu-id="dac25-133">Especifica o grupo de recursos no qual a zona será criada.</span><span class="sxs-lookup"><span data-stu-id="dac25-133">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="dac25-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="dac25-134">-Tag</span></span>
<span data-ttu-id="dac25-135">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="dac25-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dac25-136">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="dac25-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="dac25-137">-Zonetype</span><span class="sxs-lookup"><span data-stu-id="dac25-137">-ZoneType</span></span>
<span data-ttu-id="dac25-138">O tipo da zona, pública ou particular.</span><span class="sxs-lookup"><span data-stu-id="dac25-138">The type of the zone, Public or Private.</span></span> <span data-ttu-id="dac25-139">Zonas sem tipo ou com um tipo de público são disponibilizadas no plano de serviços DNS públicos para uso na hierarquia de DNS.</span><span class="sxs-lookup"><span data-stu-id="dac25-139">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="dac25-140">As zonas com um tipo de privado são visíveis apenas de um conjunto de redes virtuais associadas (esse recurso está em visualização).</span><span class="sxs-lookup"><span data-stu-id="dac25-140">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="dac25-141">Esta propriedade não pode ser alterada para uma zona.</span><span class="sxs-lookup"><span data-stu-id="dac25-141">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="dac25-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dac25-142">-Confirm</span></span>
<span data-ttu-id="dac25-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dac25-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dac25-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dac25-144">-WhatIf</span></span>
<span data-ttu-id="dac25-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dac25-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dac25-146">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dac25-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dac25-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dac25-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dac25-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac25-148">CommonParameters</span></span>
<span data-ttu-id="dac25-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dac25-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac25-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dac25-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac25-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dac25-151">INPUTS</span></span>

### <span data-ttu-id="dac25-152">System. String</span><span class="sxs-lookup"><span data-stu-id="dac25-152">System.String</span></span>

### <span data-ttu-id="dac25-153">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. Zonetype, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dac25-153">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="dac25-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dac25-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dac25-155">System. Collections. Generic. List ' 1 [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dac25-155">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dac25-156">System. Collections. Generic. List ' 1 [Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dac25-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="dac25-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dac25-157">OUTPUTS</span></span>

### <span data-ttu-id="dac25-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="dac25-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="dac25-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dac25-159">NOTES</span></span>
<span data-ttu-id="dac25-160">Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="dac25-160">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="dac25-161">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.</span><span class="sxs-lookup"><span data-stu-id="dac25-161">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="dac25-162">Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="dac25-162">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="dac25-163">Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="dac25-163">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="dac25-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dac25-164">RELATED LINKS</span></span>

[<span data-ttu-id="dac25-165">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="dac25-165">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="dac25-166">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="dac25-166">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="dac25-167">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="dac25-167">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
