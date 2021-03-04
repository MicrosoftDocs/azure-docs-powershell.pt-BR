---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: d1b5fb606262b680d4e83f9c8e0a9ea166070ed4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889479"
---
# <span data-ttu-id="094da-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="094da-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="094da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="094da-102">SYNOPSIS</span></span>
<span data-ttu-id="094da-103">Atualiza as propriedades de uma zona DNS.</span><span class="sxs-lookup"><span data-stu-id="094da-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="094da-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="094da-104">SYNTAX</span></span>

### <span data-ttu-id="094da-105">Campos (Padrão)</span><span class="sxs-lookup"><span data-stu-id="094da-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="094da-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="094da-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="094da-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="094da-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="094da-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="094da-108">DESCRIPTION</span></span>
<span data-ttu-id="094da-109">O cmdlet **Set-AzDnsZone** atualiza a zona DNS especificada no serviço DNS do Azure.</span><span class="sxs-lookup"><span data-stu-id="094da-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="094da-110">Este cmdlet não atualiza os conjuntos de registros na zona.</span><span class="sxs-lookup"><span data-stu-id="094da-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="094da-111">Você pode passar um **objeto DnsZone** como um parâmetro ou usando o operador de pipeline ou, como alternativa, pode especificar os parâmetros *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="094da-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="094da-112">Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="094da-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="094da-113">Ao passar uma zona DNS como um objeto (usando o objeto Zone ou por meio do pipeline), ela não será atualizada se tiver sido alterada no DNS do Azure desde que o objeto DnsZone local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="094da-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="094da-114">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="094da-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="094da-115">Você pode suprimir esse comportamento com o parâmetro *Overwrite,* que atualiza a zona independentemente de alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="094da-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="094da-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="094da-116">EXAMPLES</span></span>

### <span data-ttu-id="094da-117">Exemplo 1: atualizar uma zona DNS</span><span class="sxs-lookup"><span data-stu-id="094da-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="094da-118">O primeiro comando obtém a zona myzone.com do grupo de recursos especificado e a armazena na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="094da-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="094da-119">O segundo comando atualiza as marcas para $Zone.</span><span class="sxs-lookup"><span data-stu-id="094da-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="094da-120">O comando final confirma a alteração.</span><span class="sxs-lookup"><span data-stu-id="094da-120">The final command commits the change.</span></span>

### <span data-ttu-id="094da-121">Exemplo 2: Atualizar marcas para uma zona</span><span class="sxs-lookup"><span data-stu-id="094da-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="094da-122">Este comando atualiza as marcas da zona chamada myzone.com sem primeiro obter explicitamente a zona.</span><span class="sxs-lookup"><span data-stu-id="094da-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="094da-123">Exemplo 3: Associando uma zona privada a uma rede virtual especificando sua ID</span><span class="sxs-lookup"><span data-stu-id="094da-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="094da-124">Esse comando associa a zona DNS privada myprivatezone.com a myvnet de rede virtual como uma rede de registro especificando sua ID.</span><span class="sxs-lookup"><span data-stu-id="094da-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="094da-125">Exemplo 4: Associando uma zona privada a uma rede virtual especificando o objeto de rede.</span><span class="sxs-lookup"><span data-stu-id="094da-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="094da-126">Este comando associa a zona DNS privada myprivatezone.com a myvnet de rede virtual como uma rede de registro passando o objeto de rede virtual representado pela variável $vnet para o cmdlet Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="094da-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="094da-127">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="094da-127">PARAMETERS</span></span>

### <span data-ttu-id="094da-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="094da-128">-DefaultProfile</span></span>
<span data-ttu-id="094da-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="094da-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="094da-130">-Name</span><span class="sxs-lookup"><span data-stu-id="094da-130">-Name</span></span>
<span data-ttu-id="094da-131">Especifica o nome da zona DNS a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="094da-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094da-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="094da-132">-Overwrite</span></span>
<span data-ttu-id="094da-133">Ao passar uma zona DNS como um objeto (usando o objeto Zone ou por meio do pipeline), ela não será atualizada se tiver sido alterada no DNS do Azure desde que o objeto DnsZone local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="094da-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="094da-134">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="094da-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="094da-135">Você pode suprimir esse comportamento com o parâmetro *Overwrite,* que atualiza a zona independentemente de alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="094da-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="094da-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="094da-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="094da-137">A lista de redes virtuais que registrarão registros de nomes de host de máquina virtual nesta zona DNS, disponível apenas para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="094da-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094da-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="094da-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="094da-139">A lista de IDs de rede virtual que registrarão registros de nomes de host de máquina virtual nessa zona DNS, disponível apenas para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="094da-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094da-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="094da-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="094da-141">A lista de redes virtuais capazes de resolver registros nessa zona DNS, disponível apenas para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="094da-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094da-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="094da-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="094da-143">A lista de IDs de rede virtual capaz de resolver registros nessa zona DNS, disponível apenas para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="094da-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094da-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="094da-144">-ResourceGroupName</span></span>
<span data-ttu-id="094da-145">Especifica o nome do grupo de recursos que contém a zona a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="094da-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="094da-146">Você também deve especificar o parâmetro ZoneName.</span><span class="sxs-lookup"><span data-stu-id="094da-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="094da-147">Como alternativa, você pode especificar a zona usando um objeto DnsZone com o *parâmetro Zone* ou o pipeline.</span><span class="sxs-lookup"><span data-stu-id="094da-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094da-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="094da-148">-Tag</span></span>
<span data-ttu-id="094da-149">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="094da-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="094da-150">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="094da-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094da-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="094da-151">-Zone</span></span>
<span data-ttu-id="094da-152">Especifica a zona DNS a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="094da-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="094da-153">Como alternativa, você pode especificar a zona usando os *parâmetros ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="094da-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="094da-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="094da-154">-Confirm</span></span>
<span data-ttu-id="094da-155">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="094da-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="094da-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="094da-156">-WhatIf</span></span>
<span data-ttu-id="094da-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="094da-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="094da-158">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="094da-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="094da-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="094da-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="094da-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="094da-160">CommonParameters</span></span>
<span data-ttu-id="094da-161">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="094da-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="094da-162">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="094da-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="094da-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="094da-163">INPUTS</span></span>

### <span data-ttu-id="094da-164">System.String</span><span class="sxs-lookup"><span data-stu-id="094da-164">System.String</span></span>

### <span data-ttu-id="094da-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="094da-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="094da-166">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="094da-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="094da-167">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="094da-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="094da-168">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="094da-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="094da-169">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="094da-169">OUTPUTS</span></span>

### <span data-ttu-id="094da-170">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="094da-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="094da-171">NOTES</span><span class="sxs-lookup"><span data-stu-id="094da-171">NOTES</span></span>
<span data-ttu-id="094da-172">Você pode usar o *parâmetro Confirm* para controlar se esse cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="094da-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="094da-173">Por padrão, o cmdlet solicita que você confirme se a variável $ConfirmPreference Windows PowerShell tem um valor médio ou inferior.</span><span class="sxs-lookup"><span data-stu-id="094da-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="094da-174">Se você especificar *Confirm* ou *Confirm:$True*, este cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="094da-174">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="094da-175">Se você especificar *Confirm:$False*, o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="094da-175">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="094da-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="094da-176">RELATED LINKS</span></span>

[<span data-ttu-id="094da-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="094da-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="094da-178">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="094da-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="094da-179">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="094da-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
