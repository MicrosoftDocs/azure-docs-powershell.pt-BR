---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117469"
---
# <span data-ttu-id="424f7-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="424f7-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="424f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="424f7-102">SYNOPSIS</span></span>
<span data-ttu-id="424f7-103">Exclui um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="424f7-103">Deletes a record set.</span></span>

## <span data-ttu-id="424f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="424f7-104">SYNTAX</span></span>

### <span data-ttu-id="424f7-105">Campos</span><span class="sxs-lookup"><span data-stu-id="424f7-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="424f7-106">Misto</span><span class="sxs-lookup"><span data-stu-id="424f7-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="424f7-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="424f7-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="424f7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="424f7-108">DESCRIPTION</span></span>
<span data-ttu-id="424f7-109">O cmdlet **Remove-AzDnsRecordSet** exclui o conjunto de registros especificado da zona especificada.</span><span class="sxs-lookup"><span data-stu-id="424f7-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="424f7-110">Não é possível excluir registros de SOA ou de servidor de nomes (NS) criados automaticamente na zona Apex.</span><span class="sxs-lookup"><span data-stu-id="424f7-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="424f7-111">Você pode passar um objeto **Recordset** para esse cmdlet usando o operador pipeline ou como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="424f7-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="424f7-112">Para identificar um registro definido por nome e tipo sem usar um objeto **Recordset** , você deve passar a zona como um objeto **dnsZone** para esse cmdlet usando o operador pipeline ou como um parâmetro ou, como alternativa, você pode especificar os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="424f7-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="424f7-113">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="424f7-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="424f7-114">Ao especificar o conjunto de registros usando um objeto **Recordset** , o conjunto de registros não é excluído se foi alterado no Azure DNS desde que o objeto **Recordset** local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="424f7-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="424f7-115">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="424f7-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="424f7-116">Você pode suprimir isso usando o parâmetro *overwrite* , que exclui o conjunto de registros independentemente de alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="424f7-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="424f7-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="424f7-117">EXAMPLES</span></span>

### <span data-ttu-id="424f7-118">Exemplo 1: remover um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="424f7-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="424f7-119">O primeiro comando obtém o conjunto de registros especificado e, em seguida, armazena-o na variável $RecordSet. O segundo comando Remove o conjunto de registros no $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="424f7-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="424f7-120">Exemplo 2: remover um conjunto de registros e suprimir todas as confirmações</span><span class="sxs-lookup"><span data-stu-id="424f7-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="424f7-121">O primeiro comando obtém o conjunto de registros especificado.</span><span class="sxs-lookup"><span data-stu-id="424f7-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="424f7-122">O segundo comando exclui o conjunto de registros, mesmo que ele tenha sido alterado enquanto isso.</span><span class="sxs-lookup"><span data-stu-id="424f7-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="424f7-123">As solicitações de confirmação são suprimidas.</span><span class="sxs-lookup"><span data-stu-id="424f7-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="424f7-124">OS</span><span class="sxs-lookup"><span data-stu-id="424f7-124">PARAMETERS</span></span>

### <span data-ttu-id="424f7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424f7-125">-DefaultProfile</span></span>
<span data-ttu-id="424f7-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="424f7-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="424f7-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="424f7-127">-Name</span></span>
<span data-ttu-id="424f7-128">Especifica o nome do **conjunto de registros** a ser removido.</span><span class="sxs-lookup"><span data-stu-id="424f7-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="424f7-129">Ao especificar o registro definido por nome, a zona de DNS deve ser especificada usando o parâmetro de *zona* ou os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="424f7-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="424f7-130">Como alternativa, o conjunto de registros pode ser especificado usando um objeto **Recordset** , passado usando o parâmetro *Recordset* .</span><span class="sxs-lookup"><span data-stu-id="424f7-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424f7-131">-Substituir</span><span class="sxs-lookup"><span data-stu-id="424f7-131">-Overwrite</span></span>
<span data-ttu-id="424f7-132">Ao especificar o conjunto de registros usando um objeto **Recordset** , o conjunto de registros não é excluído se foi alterado no Azure DNS desde que o objeto **Recordset** local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="424f7-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="424f7-133">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="424f7-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="424f7-134">Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui o conjunto de registros independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="424f7-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="424f7-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="424f7-135">-PassThru</span></span>
<span data-ttu-id="424f7-136">PassThru</span><span class="sxs-lookup"><span data-stu-id="424f7-136">passthru</span></span>

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

### <span data-ttu-id="424f7-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="424f7-137">-RecordSet</span></span>
<span data-ttu-id="424f7-138">Especifica o objeto **Recordset** a ser removido.</span><span class="sxs-lookup"><span data-stu-id="424f7-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="424f7-139">Como alternativa, o conjunto de registros pode ser especificado usando os parâmetros *Name* e *Zone* ou usando os parâmetros *Name* , *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="424f7-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="424f7-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="424f7-140">-RecordType</span></span>
<span data-ttu-id="424f7-141">Especifica o tipo de registro DNS.</span><span class="sxs-lookup"><span data-stu-id="424f7-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="424f7-142">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="424f7-142">Valid values are:</span></span>
- <span data-ttu-id="424f7-143">Um</span><span class="sxs-lookup"><span data-stu-id="424f7-143">A</span></span>
- <span data-ttu-id="424f7-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="424f7-144">AAAA</span></span>
- <span data-ttu-id="424f7-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="424f7-145">CNAME</span></span>
- <span data-ttu-id="424f7-146">MX</span><span class="sxs-lookup"><span data-stu-id="424f7-146">MX</span></span>
- <span data-ttu-id="424f7-147">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="424f7-147">NS</span></span>
- <span data-ttu-id="424f7-148">PTR</span><span class="sxs-lookup"><span data-stu-id="424f7-148">PTR</span></span>
- <span data-ttu-id="424f7-149">SRV</span><span class="sxs-lookup"><span data-stu-id="424f7-149">SRV</span></span>
- <span data-ttu-id="424f7-150">Os registros TXT SOA são excluídos automaticamente quando a zona é excluída.</span><span class="sxs-lookup"><span data-stu-id="424f7-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="424f7-151">Não é possível excluir manualmente os registros SOA.</span><span class="sxs-lookup"><span data-stu-id="424f7-151">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424f7-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424f7-152">-ResourceGroupName</span></span>
<span data-ttu-id="424f7-153">Especifica o grupo de recursos que contém a zona DNS que contém o **conjunto de registros** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="424f7-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="424f7-154">Esse parâmetro é aplicável somente quando o conjunto de registros e a zona DNS são especificados usando os parâmetros *Name* e *zonename* .</span><span class="sxs-lookup"><span data-stu-id="424f7-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="424f7-155">Como alternativa, você pode especificar o conjunto de registros usando o parâmetro *Recordset* ou os parâmetros *Name* e *Zone* .</span><span class="sxs-lookup"><span data-stu-id="424f7-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424f7-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="424f7-156">-Zone</span></span>
<span data-ttu-id="424f7-157">Especifica a zona DNS que contém o **conjunto de registros** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="424f7-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="424f7-158">Esse parâmetro é aplicável somente quando se especifica o conjunto de registros usando o parâmetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="424f7-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="424f7-159">Como alternativa, você pode especificar o conjunto de registros usando o parâmetro *Recordset* ou os parâmetros *Name* , *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="424f7-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="424f7-160">-Zonename</span><span class="sxs-lookup"><span data-stu-id="424f7-160">-ZoneName</span></span>
<span data-ttu-id="424f7-161">Especifica o nome da zona que contém o **conjunto de registros** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="424f7-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="424f7-162">Você também deve especificar os parâmetros *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="424f7-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="424f7-163">Como alternativa, o conjunto de registros pode ser especificado usando o parâmetro *Recordset* ou os parâmetros *Name* e *Zone* .</span><span class="sxs-lookup"><span data-stu-id="424f7-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424f7-164">-Confirme</span><span class="sxs-lookup"><span data-stu-id="424f7-164">-Confirm</span></span>
<span data-ttu-id="424f7-165">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424f7-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="424f7-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="424f7-166">-WhatIf</span></span>
<span data-ttu-id="424f7-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="424f7-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="424f7-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="424f7-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="424f7-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424f7-169">CommonParameters</span></span>
<span data-ttu-id="424f7-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424f7-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424f7-171">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424f7-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424f7-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="424f7-172">INPUTS</span></span>

### <span data-ttu-id="424f7-173">Microsoft. Azure. Management. DNS. Models. RecordType</span><span class="sxs-lookup"><span data-stu-id="424f7-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="424f7-174">System. String</span><span class="sxs-lookup"><span data-stu-id="424f7-174">System.String</span></span>

### <span data-ttu-id="424f7-175">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="424f7-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="424f7-176">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="424f7-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="424f7-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="424f7-177">OUTPUTS</span></span>

### <span data-ttu-id="424f7-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="424f7-178">System.Boolean</span></span>

## <span data-ttu-id="424f7-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="424f7-179">NOTES</span></span>
<span data-ttu-id="424f7-180">Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="424f7-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="424f7-181">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.</span><span class="sxs-lookup"><span data-stu-id="424f7-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="424f7-182">Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="424f7-182">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="424f7-183">Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="424f7-183">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="424f7-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="424f7-184">RELATED LINKS</span></span>

[<span data-ttu-id="424f7-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="424f7-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="424f7-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="424f7-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="424f7-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="424f7-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
