---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
ms.openlocfilehash: 9db3efc71b751f291c5bb8636246ed6927200c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427934"
---
# <span data-ttu-id="ffb34-101">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ffb34-101">Set-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="ffb34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ffb34-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb34-103">Atualiza um conjunto de registros DNS.</span><span class="sxs-lookup"><span data-stu-id="ffb34-103">Updates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffb34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffb34-104">SYNTAX</span></span>

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffb34-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ffb34-105">DESCRIPTION</span></span>
<span data-ttu-id="ffb34-106">O cmdlet **set-AzureRmDnsRecordSet** atualiza um conjunto de registros no serviço DNS do Azure a partir de um objeto **Recordset** local.</span><span class="sxs-lookup"><span data-stu-id="ffb34-106">The **Set-AzureRmDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>

<span data-ttu-id="ffb34-107">Você pode passar um objeto **Recordset** como um parâmetro ou usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="ffb34-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>

<span data-ttu-id="ffb34-108">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="ffb34-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="ffb34-109">O conjunto de registros não será atualizado se tiver sido alterado no Azure DNS desde a recuperação do objeto **Recordset** local.</span><span class="sxs-lookup"><span data-stu-id="ffb34-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="ffb34-110">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="ffb34-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="ffb34-111">Você pode suprimir esse comportamento usando o parâmetro *overwrite* , que atualiza o conjunto de registros independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="ffb34-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="ffb34-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffb34-112">EXAMPLES</span></span>

### <span data-ttu-id="ffb34-113">Exemplo 1: atualizar um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="ffb34-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ffb34-114">O primeiro comando usa o cmdlet Get-AzureRmDnsRecordSet para obter o conjunto de registros especificado e, em seguida, armazena-o na variável $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ffb34-114">The first command uses the Get-AzureRmDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="ffb34-115">O segundo e o terceiro comandos são operações off-line para adicionar dois registros a ao conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="ffb34-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>

<span data-ttu-id="ffb34-116">O comando final usa o cmdlet **set-AzureRmDnsRecordSet** para confirmar a atualização.</span><span class="sxs-lookup"><span data-stu-id="ffb34-116">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="ffb34-117">Exemplo 2: atualizar um registro SOA</span><span class="sxs-lookup"><span data-stu-id="ffb34-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="ffb34-118">O primeiro comando usa o cmdlet **Get-AzureRmDnsRecordset** para obter o conjunto de registros especificado e, em seguida, armazena-o na variável $Recordset.</span><span class="sxs-lookup"><span data-stu-id="ffb34-118">The first command uses the **Get-AzureRmDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="ffb34-119">O segundo comando atualiza o registro SOA especificado em $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ffb34-119">The second command updates the specified SOA record in $RecordSet.</span></span>

<span data-ttu-id="ffb34-120">O comando final usa o cmdlet **set-AzureRmDnsRecordSet** para propagar a atualização em $Recordset.</span><span class="sxs-lookup"><span data-stu-id="ffb34-120">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="ffb34-121">OS</span><span class="sxs-lookup"><span data-stu-id="ffb34-121">PARAMETERS</span></span>

### <span data-ttu-id="ffb34-122">-Substituir</span><span class="sxs-lookup"><span data-stu-id="ffb34-122">-Overwrite</span></span>
<span data-ttu-id="ffb34-123">Indica a atualização do conjunto de registros independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="ffb34-123">Indicates to update the record set regardless of concurrent changes.</span></span>

<span data-ttu-id="ffb34-124">O conjunto de registros não será atualizado se tiver sido alterado no Azure DNS desde que o objeto **Recordset** local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="ffb34-124">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="ffb34-125">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="ffb34-125">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="ffb34-126">Para suprimir esse comportamento, você pode usar o parâmetro *overwrite* , que faz com que o conjunto de registros seja atualizado independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="ffb34-126">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb34-127">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="ffb34-127">-RecordSet</span></span>
<span data-ttu-id="ffb34-128">Especifica o **conjunto de registros** a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="ffb34-128">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffb34-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ffb34-129">-Confirm</span></span>
<span data-ttu-id="ffb34-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffb34-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffb34-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffb34-131">-WhatIf</span></span>
<span data-ttu-id="ffb34-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffb34-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffb34-133">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffb34-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffb34-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffb34-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffb34-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb34-135">-DefaultProfile</span></span>
<span data-ttu-id="ffb34-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ffb34-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb34-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb34-137">CommonParameters</span></span>
<span data-ttu-id="ffb34-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffb34-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb34-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffb34-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb34-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ffb34-140">INPUTS</span></span>

### <span data-ttu-id="ffb34-141">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ffb34-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="ffb34-142">Você pode passar um objeto **Recordset** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffb34-142">You can pass a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="ffb34-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ffb34-143">OUTPUTS</span></span>

### <span data-ttu-id="ffb34-144">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ffb34-144">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="ffb34-145">Esse cmdlet retorna um objeto que representa o objeto **Recordset** atualizado.</span><span class="sxs-lookup"><span data-stu-id="ffb34-145">This cmdlet returns an object that represents the updated **RecordSet** object.</span></span>

## <span data-ttu-id="ffb34-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ffb34-146">NOTES</span></span>
<span data-ttu-id="ffb34-147">Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="ffb34-147">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ffb34-148">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.</span><span class="sxs-lookup"><span data-stu-id="ffb34-148">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="ffb34-149">Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="ffb34-149">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="ffb34-150">Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="ffb34-150">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="ffb34-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffb34-151">RELATED LINKS</span></span>

[<span data-ttu-id="ffb34-152">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ffb34-152">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ffb34-153">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ffb34-153">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ffb34-154">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ffb34-154">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)
