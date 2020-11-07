---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 9b6d84f9007a872db0e41efa78d8e16d7269eb02
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775911"
---
# <span data-ttu-id="91973-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="91973-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="91973-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91973-102">SYNOPSIS</span></span>
<span data-ttu-id="91973-103">Atualiza as propriedades de uma zona DNS.</span><span class="sxs-lookup"><span data-stu-id="91973-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="91973-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91973-104">SYNTAX</span></span>

### <span data-ttu-id="91973-105">Campos</span><span class="sxs-lookup"><span data-stu-id="91973-105">Fields</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91973-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="91973-106">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91973-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91973-107">DESCRIPTION</span></span>
<span data-ttu-id="91973-108">O cmdlet **set-AzDnsZone** atualiza a zona DNS especificada no serviço DNS do Azure.</span><span class="sxs-lookup"><span data-stu-id="91973-108">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="91973-109">Esse cmdlet não atualiza os conjuntos de registros na zona.</span><span class="sxs-lookup"><span data-stu-id="91973-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="91973-110">Você pode passar um objeto **dnsZone** como um parâmetro ou usar o operador pipeline ou, como alternativa, pode especificar os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="91973-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="91973-111">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="91973-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="91973-112">Ao passar uma zona DNS como um objeto (usando o objeto Zone ou via pipeline), ele não será atualizado se ele tiver sido alterado no Azure DNS desde que o objeto DnsZone local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="91973-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="91973-113">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="91973-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="91973-114">Você pode suprimir esse comportamento com o parâmetro *overwrite* , que atualiza a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="91973-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="91973-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91973-115">EXAMPLES</span></span>

### <span data-ttu-id="91973-116">Exemplo 1: atualizar uma zona DNS</span><span class="sxs-lookup"><span data-stu-id="91973-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="91973-117">O primeiro comando obtém a zona chamada myzone.com do grupo de recursos especificado e, em seguida, armazena-a na variável $Zone.</span><span class="sxs-lookup"><span data-stu-id="91973-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="91973-118">O segundo comando atualiza as marcas para $Zone.</span><span class="sxs-lookup"><span data-stu-id="91973-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="91973-119">O comando final confirma a alteração.</span><span class="sxs-lookup"><span data-stu-id="91973-119">The final command commits the change.</span></span>

### <span data-ttu-id="91973-120">Exemplo 2: atualizar marcas para uma zona</span><span class="sxs-lookup"><span data-stu-id="91973-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="91973-121">Esse comando atualiza as marcas da zona chamada myzone.com sem primeiro obter a zona explicitamente.</span><span class="sxs-lookup"><span data-stu-id="91973-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="91973-122">OS</span><span class="sxs-lookup"><span data-stu-id="91973-122">PARAMETERS</span></span>

### <span data-ttu-id="91973-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="91973-123">-Name</span></span>
<span data-ttu-id="91973-124">Especifica o nome da zona DNS a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="91973-124">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91973-125">-Substituir</span><span class="sxs-lookup"><span data-stu-id="91973-125">-Overwrite</span></span>
<span data-ttu-id="91973-126">Ao passar uma zona DNS como um objeto (usando o objeto Zone ou via pipeline), ele não será atualizado se ele tiver sido alterado no Azure DNS desde que o objeto DnsZone local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="91973-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="91973-127">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="91973-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="91973-128">Você pode suprimir esse comportamento com o parâmetro *overwrite* , que atualiza a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="91973-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="91973-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91973-129">-ResourceGroupName</span></span>
<span data-ttu-id="91973-130">Especifica o nome do grupo de recursos que contém a zona a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="91973-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="91973-131">Você também deve especificar o parâmetro zonename.</span><span class="sxs-lookup"><span data-stu-id="91973-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="91973-132">Você também pode especificar a zona usando um objeto DnsZone com o parâmetro *Zone* ou o pipeline.</span><span class="sxs-lookup"><span data-stu-id="91973-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91973-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="91973-133">-Tag</span></span>
<span data-ttu-id="91973-134">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="91973-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="91973-135">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="91973-135">For example:</span></span>

<span data-ttu-id="91973-136">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="91973-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91973-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="91973-137">-Zone</span></span>
<span data-ttu-id="91973-138">Especifica a zona DNS a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="91973-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="91973-139">Você também pode especificar a zona usando os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="91973-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="91973-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91973-140">-Confirm</span></span>
<span data-ttu-id="91973-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91973-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91973-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91973-142">-WhatIf</span></span>
<span data-ttu-id="91973-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91973-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91973-144">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91973-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91973-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91973-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91973-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91973-146">CommonParameters</span></span>
<span data-ttu-id="91973-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91973-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91973-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91973-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91973-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91973-149">INPUTS</span></span>

### <span data-ttu-id="91973-150">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="91973-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="91973-151">Você pode canalizar um objeto DnsZone para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91973-151">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="91973-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91973-152">OUTPUTS</span></span>

### <span data-ttu-id="91973-153">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="91973-153">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="91973-154">Esse cmdlet retorna um objeto DnsZone que representa a zona DNS atualizada com um novo ETag.</span><span class="sxs-lookup"><span data-stu-id="91973-154">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="91973-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91973-155">NOTES</span></span>
<span data-ttu-id="91973-156">Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="91973-156">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="91973-157">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.</span><span class="sxs-lookup"><span data-stu-id="91973-157">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="91973-158">Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="91973-158">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="91973-159">Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="91973-159">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="91973-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91973-160">RELATED LINKS</span></span>

[<span data-ttu-id="91973-161">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="91973-161">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="91973-162">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="91973-162">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="91973-163">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="91973-163">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)