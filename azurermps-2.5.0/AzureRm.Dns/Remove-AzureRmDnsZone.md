---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: ''
schema: 2.0.0
ms.openlocfilehash: c12c5532a85bacb5cd854f4f2ad87ad0d8b68178
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786536"
---
# <span data-ttu-id="18481-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="18481-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="18481-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18481-102">SYNOPSIS</span></span>
<span data-ttu-id="18481-103">Remove uma zona DNS de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="18481-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18481-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18481-104">SYNTAX</span></span>

### <span data-ttu-id="18481-105">Campos</span><span class="sxs-lookup"><span data-stu-id="18481-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18481-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="18481-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18481-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18481-107">DESCRIPTION</span></span>
<span data-ttu-id="18481-108">O cmdlet **Remove-AzureRmDnsZone** exclui permanentemente uma zona de sistema de nomes de domínio (DNS) de um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="18481-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="18481-109">Todos os conjuntos de registros contidos na zona também são excluídos.</span><span class="sxs-lookup"><span data-stu-id="18481-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="18481-110">Você pode passar um objeto **dnsZone** usando o parâmetro *Name* ou usando o operador pipeline ou, como alternativa, pode especificar os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="18481-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="18481-111">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="18481-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="18481-112">Ao especificar a zona usando um objeto **dnsZone** (passado por meio do parâmetro pipeline ou *Zone* ), a zona não é excluída se foi alterada no Azure DNS, pois o objeto **dnsZone** local foi recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, operações em conjuntos de registros dentro da zona não).</span><span class="sxs-lookup"><span data-stu-id="18481-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="18481-113">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="18481-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="18481-114">Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="18481-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="18481-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18481-115">EXAMPLES</span></span>

### <span data-ttu-id="18481-116">Exemplo 1: remover uma zona</span><span class="sxs-lookup"><span data-stu-id="18481-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="18481-117">Esse comando Remove a zona chamada myzone.com do grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="18481-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="18481-118">OS</span><span class="sxs-lookup"><span data-stu-id="18481-118">PARAMETERS</span></span>

### <span data-ttu-id="18481-119">-Force</span><span class="sxs-lookup"><span data-stu-id="18481-119">-Force</span></span>
<span data-ttu-id="18481-120">Esse parâmetro é preterido para esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18481-120">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="18481-121">Ela será removida em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="18481-121">It will be removed in a future release.</span></span>

<span data-ttu-id="18481-122">Para controlar se esse cmdlet solicita confirmação, use o parâmetro *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="18481-122">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="18481-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="18481-123">-Name</span></span>
<span data-ttu-id="18481-124">Especifica o nome da zona DNS que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="18481-124">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="18481-125">Você também deve especificar o parâmetro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="18481-125">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="18481-126">Você também pode especificar a zona DNS usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="18481-126">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="18481-127">-Substituir</span><span class="sxs-lookup"><span data-stu-id="18481-127">-Overwrite</span></span>
<span data-ttu-id="18481-128">Ao especificar a zona usando um objeto **dnsZone** (passado por meio do parâmetro pipeline ou *Zone* ), a zona não é excluída se foi alterada no Azure DNS, pois o objeto **dnsZone** local foi recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, operações em conjuntos de registros dentro da zona não).</span><span class="sxs-lookup"><span data-stu-id="18481-128">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="18481-129">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="18481-129">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="18481-130">Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="18481-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="18481-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18481-131">-PassThru</span></span>
<span data-ttu-id="18481-132">PassThru</span><span class="sxs-lookup"><span data-stu-id="18481-132">passthru</span></span>

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

### <span data-ttu-id="18481-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18481-133">-ResourceGroupName</span></span>
<span data-ttu-id="18481-134">Especifica o nome do grupo de recursos que contém a zona a ser removida.</span><span class="sxs-lookup"><span data-stu-id="18481-134">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="18481-135">Você também deve especificar o parâmetro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="18481-135">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="18481-136">Como alternativa, você pode especificar a zona DNS usando um objeto **dnsZone** , passado pelo pipeline ou pelo parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="18481-136">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="18481-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="18481-137">-Zone</span></span>
<span data-ttu-id="18481-138">Especifica a zona DNS a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="18481-138">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="18481-139">O objeto **dnsZone** aprovado também pode ser passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="18481-139">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="18481-140">Você também pode especificar a zona DNS a ser excluída usando os parâmetros *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="18481-140">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="18481-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18481-141">-Confirm</span></span>
<span data-ttu-id="18481-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18481-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18481-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18481-143">-WhatIf</span></span>
<span data-ttu-id="18481-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18481-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18481-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18481-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18481-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18481-146">CommonParameters</span></span>
<span data-ttu-id="18481-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18481-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18481-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18481-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18481-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18481-149">INPUTS</span></span>

### <span data-ttu-id="18481-150">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="18481-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="18481-151">Você pode canalizar um objeto **dnsZone** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18481-151">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="18481-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18481-152">OUTPUTS</span></span>

### <span data-ttu-id="18481-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="18481-153">None</span></span>
<span data-ttu-id="18481-154">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="18481-154">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="18481-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18481-155">NOTES</span></span>
<span data-ttu-id="18481-156">Devido ao impacto potencialmente alto na exclusão de uma zona DNS, por padrão, esse cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem qualquer valor diferente de None.</span><span class="sxs-lookup"><span data-stu-id="18481-156">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="18481-157">Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="18481-157">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="18481-158">Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="18481-158">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="18481-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18481-159">RELATED LINKS</span></span>

[<span data-ttu-id="18481-160">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="18481-160">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="18481-161">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="18481-161">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="18481-162">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="18481-162">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
