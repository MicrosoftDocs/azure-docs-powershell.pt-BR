---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1b2ee31c136c24478ddd69d58c264ce44886c057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775915"
---
# <span data-ttu-id="0a129-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a129-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="0a129-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a129-102">SYNOPSIS</span></span>
<span data-ttu-id="0a129-103">Atualiza um conjunto de registros DNS.</span><span class="sxs-lookup"><span data-stu-id="0a129-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="0a129-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a129-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a129-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a129-105">DESCRIPTION</span></span>
<span data-ttu-id="0a129-106">O cmdlet **set-AzDnsRecordSet** atualiza um conjunto de registros no serviço DNS do Azure a partir de um objeto **Recordset** local.</span><span class="sxs-lookup"><span data-stu-id="0a129-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>

<span data-ttu-id="0a129-107">Você pode passar um objeto **Recordset** como um parâmetro ou usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="0a129-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>

<span data-ttu-id="0a129-108">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="0a129-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="0a129-109">O conjunto de registros não será atualizado se tiver sido alterado no Azure DNS desde a recuperação do objeto **Recordset** local.</span><span class="sxs-lookup"><span data-stu-id="0a129-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="0a129-110">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="0a129-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="0a129-111">Você pode suprimir esse comportamento usando o parâmetro *overwrite* , que atualiza o conjunto de registros independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="0a129-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="0a129-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a129-112">EXAMPLES</span></span>

### <span data-ttu-id="0a129-113">Exemplo 1: atualizar um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="0a129-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="0a129-114">O primeiro comando usa o cmdlet Get-AzDnsRecordSet para obter o conjunto de registros especificado e, em seguida, armazena-o na variável $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="0a129-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="0a129-115">O segundo e o terceiro comandos são operações off-line para adicionar dois registros a ao conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="0a129-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>

<span data-ttu-id="0a129-116">O comando final usa o cmdlet **set-AzDnsRecordSet** para confirmar a atualização.</span><span class="sxs-lookup"><span data-stu-id="0a129-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="0a129-117">Exemplo 2: atualizar um registro SOA</span><span class="sxs-lookup"><span data-stu-id="0a129-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="0a129-118">O primeiro comando usa o cmdlet **Get-AzDnsRecordset** para obter o conjunto de registros especificado e, em seguida, armazena-o na variável $Recordset.</span><span class="sxs-lookup"><span data-stu-id="0a129-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="0a129-119">O segundo comando atualiza o registro SOA especificado em $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="0a129-119">The second command updates the specified SOA record in $RecordSet.</span></span>

<span data-ttu-id="0a129-120">O comando final usa o cmdlet **set-AzDnsRecordSet** para propagar a atualização em $Recordset.</span><span class="sxs-lookup"><span data-stu-id="0a129-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="0a129-121">OS</span><span class="sxs-lookup"><span data-stu-id="0a129-121">PARAMETERS</span></span>

### <span data-ttu-id="0a129-122">-Substituir</span><span class="sxs-lookup"><span data-stu-id="0a129-122">-Overwrite</span></span>
<span data-ttu-id="0a129-123">Indica a atualização do conjunto de registros independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="0a129-123">Indicates to update the record set regardless of concurrent changes.</span></span>

<span data-ttu-id="0a129-124">O conjunto de registros não será atualizado se tiver sido alterado no Azure DNS desde que o objeto **Recordset** local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="0a129-124">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="0a129-125">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="0a129-125">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="0a129-126">Para suprimir esse comportamento, você pode usar o parâmetro *overwrite* , que faz com que o conjunto de registros seja atualizado independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="0a129-126">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a129-127">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="0a129-127">-RecordSet</span></span>
<span data-ttu-id="0a129-128">Especifica o **conjunto de registros** a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="0a129-128">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a129-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0a129-129">-Confirm</span></span>
<span data-ttu-id="0a129-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a129-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a129-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a129-131">-WhatIf</span></span>
<span data-ttu-id="0a129-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0a129-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a129-133">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0a129-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a129-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a129-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a129-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a129-135">CommonParameters</span></span>
<span data-ttu-id="0a129-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a129-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a129-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a129-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a129-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a129-138">INPUTS</span></span>

### <span data-ttu-id="0a129-139">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a129-139">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="0a129-140">Você pode passar um objeto **Recordset** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a129-140">You can pass a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="0a129-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a129-141">OUTPUTS</span></span>

### <span data-ttu-id="0a129-142">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a129-142">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="0a129-143">Esse cmdlet retorna um objeto que representa o objeto **Recordset** atualizado.</span><span class="sxs-lookup"><span data-stu-id="0a129-143">This cmdlet returns an object that represents the updated **RecordSet** object.</span></span>

## <span data-ttu-id="0a129-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a129-144">NOTES</span></span>
<span data-ttu-id="0a129-145">Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="0a129-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="0a129-146">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.</span><span class="sxs-lookup"><span data-stu-id="0a129-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="0a129-147">Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="0a129-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="0a129-148">Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="0a129-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="0a129-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a129-149">RELATED LINKS</span></span>

[<span data-ttu-id="0a129-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a129-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="0a129-151">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a129-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="0a129-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a129-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)