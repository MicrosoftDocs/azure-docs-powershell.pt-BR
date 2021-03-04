---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: ab4f7bf6693eda413587b572832706d617b3e683
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889490"
---
# <span data-ttu-id="3f4a6-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3f4a6-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="3f4a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f4a6-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4a6-103">Exclui um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-103">Deletes a record set.</span></span>

## <span data-ttu-id="3f4a6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3f4a6-104">SYNTAX</span></span>

### <span data-ttu-id="3f4a6-105">Fields</span><span class="sxs-lookup"><span data-stu-id="3f4a6-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4a6-106">Mixed</span><span class="sxs-lookup"><span data-stu-id="3f4a6-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4a6-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="3f4a6-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f4a6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3f4a6-108">DESCRIPTION</span></span>
<span data-ttu-id="3f4a6-109">O cmdlet **Remove-AzDnsRecordSet** exclui o conjunto de registros especificado da zona especificada.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="3f4a6-110">Não é possível excluir registros SOA ou NS (servidor de nomes) que são criados automaticamente no apex de zona.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="3f4a6-111">Você pode passar um **objeto RecordSet** para esse cmdlet usando o operador de pipeline ou como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="3f4a6-112">Para identificar um registro definido por nome e tipo sem usar um **objeto RecordSet,** você deve passar a zona como um **objeto DnsZone** para esse cmdlet usando o operador de pipeline ou como parâmetro ou, como alternativa, você pode especificar os parâmetros *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="3f4a6-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="3f4a6-113">Você pode usar o parâmetro Confirm e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="3f4a6-114">Ao especificar o conjunto de registros usando um **objeto RecordSet,** o conjunto de registros não será excluído se tiver sido alterado no DNS do Azure desde que o objeto **RecordSet** local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="3f4a6-115">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="3f4a6-116">Você pode suprimir isso usando o parâmetro *Overwrite,* que exclui o conjunto de registros independentemente de alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="3f4a6-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f4a6-117">EXAMPLES</span></span>

### <span data-ttu-id="3f4a6-118">Exemplo 1: Remover um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="3f4a6-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="3f4a6-119">O primeiro comando obtém o conjunto de registros especificado e o armazena na variável $RecordSet. O segundo comando remove o conjunto de registros em $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="3f4a6-120">Exemplo 2: remover um conjunto de registros e suprimir toda a confirmação</span><span class="sxs-lookup"><span data-stu-id="3f4a6-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="3f4a6-121">O primeiro comando obtém o conjunto de registros especificado.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="3f4a6-122">O segundo comando exclui o conjunto de registros, mesmo que tenha sido alterado enquanto isso.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="3f4a6-123">Os prompts de confirmação são suprimidos.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="3f4a6-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3f4a6-124">PARAMETERS</span></span>

### <span data-ttu-id="3f4a6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4a6-125">-DefaultProfile</span></span>
<span data-ttu-id="3f4a6-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3f4a6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f4a6-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3f4a6-127">-Name</span></span>
<span data-ttu-id="3f4a6-128">Especifica o nome do **RecordSet** a ser removido.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="3f4a6-129">Ao especificar o registro definido pelo nome, a zona DNS deve ser especificada usando o parâmetro *Zone* ou os parâmetros *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="3f4a6-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="3f4a6-130">Como alternativa, o conjunto de registros pode ser especificado usando um **objeto RecordSet,** passado usando o *parâmetro RecordSet.*</span><span class="sxs-lookup"><span data-stu-id="3f4a6-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="3f4a6-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="3f4a6-131">-Overwrite</span></span>
<span data-ttu-id="3f4a6-132">Ao especificar o conjunto de registros usando um **objeto RecordSet,** o conjunto de registros não será excluído se tiver sido alterado no DNS do Azure desde que o objeto **RecordSet** local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="3f4a6-133">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="3f4a6-134">Isso pode ser suprimido usando o parâmetro *Overwrite,* que exclui o conjunto de registros independentemente de alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="3f4a6-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f4a6-135">-PassThru</span></span>
<span data-ttu-id="3f4a6-136">passthru</span><span class="sxs-lookup"><span data-stu-id="3f4a6-136">passthru</span></span>

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

### <span data-ttu-id="3f4a6-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="3f4a6-137">-RecordSet</span></span>
<span data-ttu-id="3f4a6-138">Especifica o **objeto RecordSet** a ser removido.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="3f4a6-139">Como alternativa, o conjunto de registros pode ser especificado usando os parâmetros *Name* e *Zone* ou usando os parâmetros *Name,* *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="3f4a6-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="3f4a6-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="3f4a6-140">-RecordType</span></span>
<span data-ttu-id="3f4a6-141">Especifica o tipo de registro DNS.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="3f4a6-142">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="3f4a6-142">Valid values are:</span></span>
- <span data-ttu-id="3f4a6-143">A</span><span class="sxs-lookup"><span data-stu-id="3f4a6-143">A</span></span>
- <span data-ttu-id="3f4a6-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="3f4a6-144">AAAA</span></span>
- <span data-ttu-id="3f4a6-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="3f4a6-145">CNAME</span></span>
- <span data-ttu-id="3f4a6-146">MX</span><span class="sxs-lookup"><span data-stu-id="3f4a6-146">MX</span></span>
- <span data-ttu-id="3f4a6-147">NS</span><span class="sxs-lookup"><span data-stu-id="3f4a6-147">NS</span></span>
- <span data-ttu-id="3f4a6-148">PTR</span><span class="sxs-lookup"><span data-stu-id="3f4a6-148">PTR</span></span>
- <span data-ttu-id="3f4a6-149">SRV</span><span class="sxs-lookup"><span data-stu-id="3f4a6-149">SRV</span></span>
- <span data-ttu-id="3f4a6-150">Os registros SOA TXT são excluídos automaticamente quando a zona é excluída.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="3f4a6-151">Não é possível excluir manualmente os registros SOA.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-151">You cannot manually delete SOA records.</span></span>

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

### <span data-ttu-id="3f4a6-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4a6-152">-ResourceGroupName</span></span>
<span data-ttu-id="3f4a6-153">Especifica o grupo de recursos que contém a zona DNS que contém **o RecordSet** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="3f4a6-154">Esse parâmetro só é aplicável quando o conjunto de registros e a zona DNS são especificados usando os parâmetros *Name* e *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="3f4a6-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="3f4a6-155">Como alternativa, você pode especificar o conjunto de registros usando o *parâmetro RecordSet* ou os *parâmetros Name* e *Zone.*</span><span class="sxs-lookup"><span data-stu-id="3f4a6-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="3f4a6-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="3f4a6-156">-Zone</span></span>
<span data-ttu-id="3f4a6-157">Especifica a zona DNS que contém **o RecordSet** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="3f4a6-158">Esse parâmetro só é aplicável ao especificar o conjunto de registros usando o *parâmetro* Name.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="3f4a6-159">Como alternativa, você pode especificar o conjunto de registros usando o parâmetro *RecordSet* ou os parâmetros *Name*, *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="3f4a6-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="3f4a6-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="3f4a6-160">-ZoneName</span></span>
<span data-ttu-id="3f4a6-161">Especifica o nome da zona que contém **o RecordSet** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="3f4a6-162">Você também deve especificar os parâmetros *Name* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="3f4a6-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="3f4a6-163">Como alternativa, o conjunto de registros pode ser especificado usando o parâmetro *RecordSet* ou os *parâmetros Name* e *Zone.*</span><span class="sxs-lookup"><span data-stu-id="3f4a6-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="3f4a6-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f4a6-164">-Confirm</span></span>
<span data-ttu-id="3f4a6-165">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f4a6-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f4a6-166">-WhatIf</span></span>
<span data-ttu-id="3f4a6-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f4a6-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f4a6-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4a6-169">CommonParameters</span></span>
<span data-ttu-id="3f4a6-170">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4a6-171">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f4a6-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4a6-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f4a6-172">INPUTS</span></span>

### <span data-ttu-id="3f4a6-173">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="3f4a6-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="3f4a6-174">System.String</span><span class="sxs-lookup"><span data-stu-id="3f4a6-174">System.String</span></span>

### <span data-ttu-id="3f4a6-175">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="3f4a6-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="3f4a6-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3f4a6-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="3f4a6-177">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3f4a6-177">OUTPUTS</span></span>

### <span data-ttu-id="3f4a6-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f4a6-178">System.Boolean</span></span>

## <span data-ttu-id="3f4a6-179">NOTES</span><span class="sxs-lookup"><span data-stu-id="3f4a6-179">NOTES</span></span>
<span data-ttu-id="3f4a6-180">Você pode usar o *parâmetro Confirm* para controlar se esse cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="3f4a6-181">Por padrão, o cmdlet solicita que você confirme se a variável $ConfirmPreference Windows PowerShell tem um valor médio ou inferior.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="3f4a6-182">Se você especificar *Confirm* ou *Confirm:$True*, este cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-182">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="3f4a6-183">Se você especificar *Confirm:$False*, o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="3f4a6-183">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3f4a6-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f4a6-184">RELATED LINKS</span></span>

[<span data-ttu-id="3f4a6-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3f4a6-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="3f4a6-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3f4a6-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="3f4a6-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3f4a6-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
