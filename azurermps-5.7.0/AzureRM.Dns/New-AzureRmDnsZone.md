---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 28fabce7590644c230643822c206515957839127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602647"
---
# <span data-ttu-id="2c9b8-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2c9b8-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="2c9b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9b8-103">Cria uma nova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c9b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c9b8-104">SYNTAX</span></span>

### <span data-ttu-id="2c9b8-105">IDs (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c9b8-105">Ids (Default)</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c9b8-106">Eles</span><span class="sxs-lookup"><span data-stu-id="2c9b8-106">Objects</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c9b8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c9b8-107">DESCRIPTION</span></span>
<span data-ttu-id="2c9b8-108">O cmdlet **New-AzureRmDnsZone** cria uma nova zona de sistema de nomes de domínio (DNS) no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-108">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="2c9b8-109">Você deve especificar um nome de zona DNS exclusivo para o parâmetro *Name* , ou o cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="2c9b8-110">Após a criação da zona, use o cmdlet New-AzureRmDnsRecordSet para criar conjuntos de registros na zona.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-110">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="2c9b8-111">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="2c9b8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c9b8-112">EXAMPLES</span></span>

### <span data-ttu-id="2c9b8-113">Exemplo 1: criar uma zona DNS</span><span class="sxs-lookup"><span data-stu-id="2c9b8-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2c9b8-114">Esse comando cria uma nova zona DNS chamada myzone.com no grupo de recursos especificado e armazena-a na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="2c9b8-115">Exemplo 2: criar uma zona DNS privada especificando IDs de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2c9b8-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="2c9b8-116">Esse comando cria uma nova zona DNS privada chamada myprivatezone.com no grupo de recursos especificado com uma rede virtual de resolução associada (especificando sua ID) e a armazena na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="2c9b8-117">Exemplo 3: criar uma zona DNS privada especificando objetos de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2c9b8-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzureRmVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="2c9b8-118">Esse comando cria uma nova zona DNS privada chamada myprivatezone.com no grupo de recursos especificado com uma rede virtual de resolução associada (referida pela variável $ResVirtualNetwork) e a armazena na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="2c9b8-119">OS</span><span class="sxs-lookup"><span data-stu-id="2c9b8-119">PARAMETERS</span></span>

### <span data-ttu-id="2c9b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9b8-120">-DefaultProfile</span></span>
<span data-ttu-id="2c9b8-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2c9b8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c9b8-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c9b8-122">-Name</span></span>
<span data-ttu-id="2c9b8-123">Especifica o nome da zona DNS a ser criada.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-123">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9b8-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2c9b8-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="2c9b8-125">A lista de redes virtuais que registrarão os registros de hosts de máquina virtual nesta zona de DNS, disponível somente para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="2c9b8-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2c9b8-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="2c9b8-127">A lista de IDs de rede virtual que registrará os registros de hosts de máquina virtual nesta zona de DNS, somente disponível para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="2c9b8-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2c9b8-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="2c9b8-129">A lista de redes virtuais capazes de resolver registros nesta zona DNS, disponível somente para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="2c9b8-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2c9b8-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="2c9b8-131">A lista de IDs de rede virtual é capaz de resolver registros nesta zona DNS, disponível somente para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="2c9b8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c9b8-132">-ResourceGroupName</span></span>
<span data-ttu-id="2c9b8-133">Especifica o grupo de recursos no qual a zona será criada.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-133">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9b8-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="2c9b8-134">-Tag</span></span>
<span data-ttu-id="2c9b8-135">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2c9b8-136">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="2c9b8-136">For example:</span></span>

<span data-ttu-id="2c9b8-137">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2c9b8-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9b8-138">-Zonetype</span><span class="sxs-lookup"><span data-stu-id="2c9b8-138">-ZoneType</span></span>
<span data-ttu-id="2c9b8-139">O tipo da zona, pública ou particular.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-139">The type of the zone, Public or Private.</span></span> <span data-ttu-id="2c9b8-140">Zonas sem tipo ou com um tipo de público são disponibilizadas no plano de serviços DNS públicos para uso na hierarquia de DNS.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-140">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="2c9b8-141">As zonas com um tipo de privado são visíveis apenas de um conjunto de redes virtuais associadas (esse recurso está em visualização).</span><span class="sxs-lookup"><span data-stu-id="2c9b8-141">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="2c9b8-142">Esta propriedade não pode ser alterada para uma zona.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-142">This property cannot be changed for a zone.</span></span>

```yaml
Type: ZoneType
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9b8-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c9b8-143">-Confirm</span></span>
<span data-ttu-id="2c9b8-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9b8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c9b8-145">-WhatIf</span></span>
<span data-ttu-id="2c9b8-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c9b8-147">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-147">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c9b8-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9b8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9b8-149">CommonParameters</span></span>
<span data-ttu-id="2c9b8-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9b8-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9b8-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9b8-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c9b8-152">INPUTS</span></span>

### <span data-ttu-id="2c9b8-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2c9b8-153">None</span></span>
<span data-ttu-id="2c9b8-154">Não é possível canalizar a entrada para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-154">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="2c9b8-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c9b8-155">OUTPUTS</span></span>

### <span data-ttu-id="2c9b8-156">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="2c9b8-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="2c9b8-157">Esse cmdlet retorna um objeto Microsoft. Azure. Commands. DNS. DnsZone que representa a nova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-157">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="2c9b8-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c9b8-158">NOTES</span></span>
<span data-ttu-id="2c9b8-159">Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-159">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2c9b8-160">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-160">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="2c9b8-161">Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-161">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="2c9b8-162">Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-162">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2c9b8-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c9b8-163">RELATED LINKS</span></span>

[<span data-ttu-id="2c9b8-164">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2c9b8-164">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="2c9b8-165">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2c9b8-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="2c9b8-166">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2c9b8-166">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
