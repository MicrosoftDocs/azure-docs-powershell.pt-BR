---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: da504f6b8110335e6297d0c7efb2a1a27106e0e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427556"
---
# <span data-ttu-id="fb74f-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="fb74f-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="fb74f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb74f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb74f-103">Atualiza as propriedades de uma zona DNS.</span><span class="sxs-lookup"><span data-stu-id="fb74f-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb74f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb74f-104">SYNTAX</span></span>

### <span data-ttu-id="fb74f-105">Campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="fb74f-105">Fields (Default)</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb74f-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="fb74f-106">FieldsObjects</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb74f-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="fb74f-107">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb74f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb74f-108">DESCRIPTION</span></span>
<span data-ttu-id="fb74f-109">O cmdlet **set-AzureRmDnsZone** atualiza a zona DNS especificada no serviço DNS do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb74f-109">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="fb74f-110">Esse cmdlet não atualiza os conjuntos de registros na zona.</span><span class="sxs-lookup"><span data-stu-id="fb74f-110">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="fb74f-111">Você pode passar um objeto **dnsZone** como um parâmetro ou usar o operador pipeline ou, como alternativa, pode especificar os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="fb74f-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="fb74f-112">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="fb74f-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="fb74f-113">Ao passar uma zona DNS como um objeto (usando o objeto Zone ou via pipeline), ele não será atualizado se ele tiver sido alterado no Azure DNS desde que o objeto DnsZone local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="fb74f-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="fb74f-114">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fb74f-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="fb74f-115">Você pode suprimir esse comportamento com o parâmetro *overwrite* , que atualiza a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fb74f-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="fb74f-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb74f-116">EXAMPLES</span></span>

### <span data-ttu-id="fb74f-117">Exemplo 1: atualizar uma zona DNS</span><span class="sxs-lookup"><span data-stu-id="fb74f-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="fb74f-118">O primeiro comando obtém a zona chamada myzone.com do grupo de recursos especificado e, em seguida, armazena-a na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="fb74f-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="fb74f-119">O segundo comando atualiza as marcas para $Zone.</span><span class="sxs-lookup"><span data-stu-id="fb74f-119">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="fb74f-120">O comando final confirma a alteração.</span><span class="sxs-lookup"><span data-stu-id="fb74f-120">The final command commits the change.</span></span>

### <span data-ttu-id="fb74f-121">Exemplo 2: atualizar marcas para uma zona</span><span class="sxs-lookup"><span data-stu-id="fb74f-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="fb74f-122">Esse comando atualiza as marcas da zona chamada myzone.com sem primeiro obter a zona explicitamente.</span><span class="sxs-lookup"><span data-stu-id="fb74f-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="fb74f-123">Exemplo 3: associando uma zona privada a uma rede virtual especificando sua ID</span><span class="sxs-lookup"><span data-stu-id="fb74f-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="fb74f-124">Esse comando associa a zona DNS privada myprivatezone.com à rede virtual myvnet como uma rede de registro especificando sua ID.</span><span class="sxs-lookup"><span data-stu-id="fb74f-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="fb74f-125">Exemplo 4: associando uma zona privada a uma rede virtual especificando o objeto de rede.</span><span class="sxs-lookup"><span data-stu-id="fb74f-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="fb74f-126">Esse comando associa a zona DNS privada myprivatezone.com à rede virtual myvnet como uma rede de registro passando o objeto de rede virtual representado pela variável $vnet para o cmdlet Set-AzureRmDnsZone.</span><span class="sxs-lookup"><span data-stu-id="fb74f-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzureRmDnsZone cmdlet.</span></span>

## <span data-ttu-id="fb74f-127">OS</span><span class="sxs-lookup"><span data-stu-id="fb74f-127">PARAMETERS</span></span>

### <span data-ttu-id="fb74f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb74f-128">-DefaultProfile</span></span>
<span data-ttu-id="fb74f-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fb74f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb74f-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb74f-130">-Name</span></span>
<span data-ttu-id="fb74f-131">Especifica o nome da zona DNS a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="fb74f-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb74f-132">-Substituir</span><span class="sxs-lookup"><span data-stu-id="fb74f-132">-Overwrite</span></span>
<span data-ttu-id="fb74f-133">Ao passar uma zona DNS como um objeto (usando o objeto Zone ou via pipeline), ele não será atualizado se ele tiver sido alterado no Azure DNS desde que o objeto DnsZone local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="fb74f-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="fb74f-134">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fb74f-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="fb74f-135">Você pode suprimir esse comportamento com o parâmetro *overwrite* , que atualiza a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fb74f-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb74f-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb74f-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="fb74f-137">A lista de redes virtuais que registrarão os registros de hosts de máquina virtual nesta zona de DNS, disponível somente para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="fb74f-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="fb74f-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="fb74f-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="fb74f-139">A lista de IDs de rede virtual que registrará os registros de hosts de máquina virtual nesta zona de DNS, somente disponível para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="fb74f-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="fb74f-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb74f-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="fb74f-141">A lista de redes virtuais capazes de resolver registros nesta zona DNS, disponível somente para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="fb74f-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="fb74f-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="fb74f-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="fb74f-143">A lista de IDs de rede virtual é capaz de resolver registros nesta zona DNS, disponível somente para zonas privadas.</span><span class="sxs-lookup"><span data-stu-id="fb74f-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="fb74f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb74f-144">-ResourceGroupName</span></span>
<span data-ttu-id="fb74f-145">Especifica o nome do grupo de recursos que contém a zona a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="fb74f-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="fb74f-146">Você também deve especificar o parâmetro zonename.</span><span class="sxs-lookup"><span data-stu-id="fb74f-146">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="fb74f-147">Você também pode especificar a zona usando um objeto DnsZone com o parâmetro *Zone* ou o pipeline.</span><span class="sxs-lookup"><span data-stu-id="fb74f-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb74f-148">-Marca</span><span class="sxs-lookup"><span data-stu-id="fb74f-148">-Tag</span></span>
<span data-ttu-id="fb74f-149">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fb74f-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fb74f-150">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="fb74f-150">For example:</span></span>

<span data-ttu-id="fb74f-151">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fb74f-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb74f-152">-Zone</span><span class="sxs-lookup"><span data-stu-id="fb74f-152">-Zone</span></span>
<span data-ttu-id="fb74f-153">Especifica a zona DNS a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="fb74f-153">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="fb74f-154">Você também pode especificar a zona usando os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="fb74f-154">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb74f-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb74f-155">-Confirm</span></span>
<span data-ttu-id="fb74f-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb74f-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb74f-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb74f-157">-WhatIf</span></span>
<span data-ttu-id="fb74f-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb74f-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb74f-159">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb74f-159">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb74f-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb74f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb74f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb74f-161">CommonParameters</span></span>
<span data-ttu-id="fb74f-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb74f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb74f-163">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb74f-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb74f-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb74f-164">INPUTS</span></span>

### <span data-ttu-id="fb74f-165">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="fb74f-165">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="fb74f-166">Você pode canalizar um objeto DnsZone para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb74f-166">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="fb74f-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb74f-167">OUTPUTS</span></span>

### <span data-ttu-id="fb74f-168">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="fb74f-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="fb74f-169">Esse cmdlet retorna um objeto DnsZone que representa a zona DNS atualizada com um novo ETag.</span><span class="sxs-lookup"><span data-stu-id="fb74f-169">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="fb74f-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb74f-170">NOTES</span></span>
<span data-ttu-id="fb74f-171">Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="fb74f-171">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="fb74f-172">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.</span><span class="sxs-lookup"><span data-stu-id="fb74f-172">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="fb74f-173">Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="fb74f-173">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="fb74f-174">Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="fb74f-174">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="fb74f-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb74f-175">RELATED LINKS</span></span>

[<span data-ttu-id="fb74f-176">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="fb74f-176">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="fb74f-177">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="fb74f-177">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="fb74f-178">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="fb74f-178">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
