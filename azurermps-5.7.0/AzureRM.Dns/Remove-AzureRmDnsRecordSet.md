---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
ms.openlocfilehash: fce5cbe993861d2a0d97bffd4bf4c7dbe19cc535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602738"
---
# <span data-ttu-id="1105f-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1105f-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="1105f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1105f-102">SYNOPSIS</span></span>
<span data-ttu-id="1105f-103">Exclui um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="1105f-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1105f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1105f-104">SYNTAX</span></span>

### <span data-ttu-id="1105f-105">Campos</span><span class="sxs-lookup"><span data-stu-id="1105f-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1105f-106">Misto</span><span class="sxs-lookup"><span data-stu-id="1105f-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1105f-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="1105f-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1105f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1105f-108">DESCRIPTION</span></span>
<span data-ttu-id="1105f-109">O cmdlet **Remove-AzureRmDnsRecordSet** exclui o conjunto de registros especificado da zona especificada.</span><span class="sxs-lookup"><span data-stu-id="1105f-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="1105f-110">Não é possível excluir registros de SOA ou de servidor de nomes (NS) criados automaticamente na zona Apex.</span><span class="sxs-lookup"><span data-stu-id="1105f-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>

<span data-ttu-id="1105f-111">Você pode passar um objeto **Recordset** para esse cmdlet usando o operador pipeline ou como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1105f-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="1105f-112">Para identificar um registro definido por nome e tipo sem usar um objeto **Recordset** , você deve passar a zona como um objeto **dnsZone** para esse cmdlet usando o operador pipeline ou como um parâmetro ou, como alternativa, você pode especificar os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="1105f-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="1105f-113">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="1105f-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="1105f-114">Ao especificar o conjunto de registros usando um objeto **Recordset** , o conjunto de registros não é excluído se foi alterado no Azure DNS desde que o objeto **Recordset** local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="1105f-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="1105f-115">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1105f-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="1105f-116">Você pode suprimir isso usando o parâmetro *overwrite* , que exclui o conjunto de registros independentemente de alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1105f-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="1105f-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1105f-117">EXAMPLES</span></span>

### <span data-ttu-id="1105f-118">Exemplo 1: remover um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="1105f-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="1105f-119">O primeiro comando obtém o conjunto de registros especificado e, em seguida, armazena-o na variável $RecordSet. O segundo comando Remove o conjunto de registros no $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="1105f-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="1105f-120">Exemplo 2: remover um conjunto de registros e suprimir todas as confirmações</span><span class="sxs-lookup"><span data-stu-id="1105f-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="1105f-121">O primeiro comando obtém o conjunto de registros especificado.</span><span class="sxs-lookup"><span data-stu-id="1105f-121">The first command gets the specified record set.</span></span>

<span data-ttu-id="1105f-122">O segundo comando exclui o conjunto de registros, mesmo que ele tenha sido alterado enquanto isso.</span><span class="sxs-lookup"><span data-stu-id="1105f-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="1105f-123">As solicitações de confirmação são suprimidas.</span><span class="sxs-lookup"><span data-stu-id="1105f-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="1105f-124">OS</span><span class="sxs-lookup"><span data-stu-id="1105f-124">PARAMETERS</span></span>

### <span data-ttu-id="1105f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1105f-125">-DefaultProfile</span></span>
<span data-ttu-id="1105f-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1105f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1105f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="1105f-127">-Force</span></span>
<span data-ttu-id="1105f-128">Esse parâmetro é preterido para esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1105f-128">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="1105f-129">Ela será removida em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="1105f-129">It will be removed in a future release.</span></span>

<span data-ttu-id="1105f-130">Para controlar se esse cmdlet solicita confirmação, use o parâmetro *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="1105f-130">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="1105f-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="1105f-131">-Name</span></span>
<span data-ttu-id="1105f-132">Especifica o nome do **conjunto de registros** a ser removido.</span><span class="sxs-lookup"><span data-stu-id="1105f-132">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="1105f-133">Ao especificar o registro definido por nome, a zona de DNS deve ser especificada usando o parâmetro de *zona* ou os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="1105f-133">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="1105f-134">Como alternativa, o conjunto de registros pode ser especificado usando um objeto **Recordset** , passado usando o parâmetro *Recordset* .</span><span class="sxs-lookup"><span data-stu-id="1105f-134">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1105f-135">-Substituir</span><span class="sxs-lookup"><span data-stu-id="1105f-135">-Overwrite</span></span>
<span data-ttu-id="1105f-136">Ao especificar o conjunto de registros usando um objeto **Recordset** , o conjunto de registros não é excluído se foi alterado no Azure DNS desde que o objeto **Recordset** local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="1105f-136">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="1105f-137">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1105f-137">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="1105f-138">Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui o conjunto de registros independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1105f-138">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="1105f-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1105f-139">-PassThru</span></span>
<span data-ttu-id="1105f-140">PassThru</span><span class="sxs-lookup"><span data-stu-id="1105f-140">passthru</span></span>

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

### <span data-ttu-id="1105f-141">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="1105f-141">-RecordSet</span></span>
<span data-ttu-id="1105f-142">Especifica o objeto **Recordset** a ser removido.</span><span class="sxs-lookup"><span data-stu-id="1105f-142">Specifies the **RecordSet** object to remove.</span></span>

<span data-ttu-id="1105f-143">Como alternativa, o conjunto de registros pode ser especificado usando os parâmetros *Name* e *Zone* ou usando os parâmetros *Name* , *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="1105f-143">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1105f-144">-RecordType</span><span class="sxs-lookup"><span data-stu-id="1105f-144">-RecordType</span></span>
<span data-ttu-id="1105f-145">Especifica o tipo de registro DNS.</span><span class="sxs-lookup"><span data-stu-id="1105f-145">Specifies the type of DNS record.</span></span>

<span data-ttu-id="1105f-146">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1105f-146">Valid values are:</span></span>

- <span data-ttu-id="1105f-147">Um</span><span class="sxs-lookup"><span data-stu-id="1105f-147">A</span></span>
- <span data-ttu-id="1105f-148">AAAA</span><span class="sxs-lookup"><span data-stu-id="1105f-148">AAAA</span></span>
- <span data-ttu-id="1105f-149">CNAME</span><span class="sxs-lookup"><span data-stu-id="1105f-149">CNAME</span></span>
- <span data-ttu-id="1105f-150">MX</span><span class="sxs-lookup"><span data-stu-id="1105f-150">MX</span></span>
- <span data-ttu-id="1105f-151">SÉRIE</span><span class="sxs-lookup"><span data-stu-id="1105f-151">NS</span></span>
- <span data-ttu-id="1105f-152">PTR</span><span class="sxs-lookup"><span data-stu-id="1105f-152">PTR</span></span>
- <span data-ttu-id="1105f-153">SRV</span><span class="sxs-lookup"><span data-stu-id="1105f-153">SRV</span></span>
- <span data-ttu-id="1105f-154">LOCALIZADO</span><span class="sxs-lookup"><span data-stu-id="1105f-154">TXT</span></span>

<span data-ttu-id="1105f-155">Os registros SOA são excluídos automaticamente quando a zona é excluída.</span><span class="sxs-lookup"><span data-stu-id="1105f-155">SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="1105f-156">Não é possível excluir manualmente os registros SOA.</span><span class="sxs-lookup"><span data-stu-id="1105f-156">You cannot manually delete SOA records.</span></span>

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1105f-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1105f-157">-ResourceGroupName</span></span>
<span data-ttu-id="1105f-158">Especifica o grupo de recursos que contém a zona DNS que contém o **conjunto de registros** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="1105f-158">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="1105f-159">Esse parâmetro é aplicável somente quando o conjunto de registros e a zona DNS são especificados usando os parâmetros *Name* e *zonename* .</span><span class="sxs-lookup"><span data-stu-id="1105f-159">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>

<span data-ttu-id="1105f-160">Como alternativa, você pode especificar o conjunto de registros usando o parâmetro *Recordset* ou os parâmetros *Name* e *Zone* .</span><span class="sxs-lookup"><span data-stu-id="1105f-160">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="1105f-161">-Zone</span><span class="sxs-lookup"><span data-stu-id="1105f-161">-Zone</span></span>
<span data-ttu-id="1105f-162">Especifica a zona DNS que contém o **conjunto de registros** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="1105f-162">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="1105f-163">Esse parâmetro é aplicável somente quando se especifica o conjunto de registros usando o parâmetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="1105f-163">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>

<span data-ttu-id="1105f-164">Como alternativa, você pode especificar o conjunto de registros usando o parâmetro *Recordset* ou os parâmetros *Name* , *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="1105f-164">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1105f-165">-Zonename</span><span class="sxs-lookup"><span data-stu-id="1105f-165">-ZoneName</span></span>
<span data-ttu-id="1105f-166">Especifica o nome da zona que contém o **conjunto de registros** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="1105f-166">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="1105f-167">Você também deve especificar os parâmetros *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="1105f-167">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="1105f-168">Como alternativa, o conjunto de registros pode ser especificado usando o parâmetro *Recordset* ou os parâmetros *Name* e *Zone* .</span><span class="sxs-lookup"><span data-stu-id="1105f-168">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="1105f-169">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1105f-169">-Confirm</span></span>
<span data-ttu-id="1105f-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1105f-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1105f-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1105f-171">-WhatIf</span></span>
<span data-ttu-id="1105f-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1105f-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1105f-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1105f-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1105f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1105f-174">CommonParameters</span></span>
<span data-ttu-id="1105f-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1105f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1105f-176">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1105f-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1105f-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1105f-177">INPUTS</span></span>

### <span data-ttu-id="1105f-178">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1105f-178">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="1105f-179">Você pode canalizar um objeto **Recordset** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1105f-179">You can pipe a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="1105f-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1105f-180">OUTPUTS</span></span>

### <span data-ttu-id="1105f-181">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1105f-181">None</span></span>
<span data-ttu-id="1105f-182">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1105f-182">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1105f-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1105f-183">NOTES</span></span>
<span data-ttu-id="1105f-184">Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="1105f-184">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1105f-185">Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.</span><span class="sxs-lookup"><span data-stu-id="1105f-185">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="1105f-186">Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="1105f-186">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="1105f-187">Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="1105f-187">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1105f-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1105f-188">RELATED LINKS</span></span>

[<span data-ttu-id="1105f-189">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1105f-189">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="1105f-190">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1105f-190">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="1105f-191">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1105f-191">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
