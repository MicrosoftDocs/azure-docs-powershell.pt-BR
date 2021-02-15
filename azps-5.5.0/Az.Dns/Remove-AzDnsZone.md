---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111903"
---
# <span data-ttu-id="32c0a-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="32c0a-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="32c0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="32c0a-103">Remove uma zona DNS de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="32c0a-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="32c0a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32c0a-104">SYNTAX</span></span>

### <span data-ttu-id="32c0a-105">Campos</span><span class="sxs-lookup"><span data-stu-id="32c0a-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32c0a-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="32c0a-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32c0a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="32c0a-107">DESCRIPTION</span></span>
<span data-ttu-id="32c0a-108">O cmdlet **Remove-AzDnsZone** exclui permanentemente uma zona DNS (Sistema de Nomes de Domínio) de um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="32c0a-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="32c0a-109">Todos os conjuntos de registros contidos na zona também são excluídos.</span><span class="sxs-lookup"><span data-stu-id="32c0a-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="32c0a-110">Você pode passar um objeto  **DnsZone** usando o parâmetro Nome ou usando o operador de pipeline ou, alternativamente, pode especificar os parâmetros *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="32c0a-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="32c0a-111">Você pode usar o parâmetro Confirmar e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="32c0a-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="32c0a-112">Ao especificar a zona usando um objeto **DnsZone** (passado pelo parâmetro pipeline ou Zona), a zona não será excluída se tiver sido alterada no DNS do Azure desde que o objeto **DnsZone** local foi recuperado (somente as operações diretamente na contagem de recursos de zona DNS como alterações, as operações em conjuntos de registros dentro da zona não o fazem). </span><span class="sxs-lookup"><span data-stu-id="32c0a-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="32c0a-113">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="32c0a-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="32c0a-114">Isso pode ser suprimido usando o parâmetro *Substituir,* que exclui a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="32c0a-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="32c0a-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="32c0a-115">EXAMPLES</span></span>

### <span data-ttu-id="32c0a-116">Exemplo 1: Remover uma zona</span><span class="sxs-lookup"><span data-stu-id="32c0a-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="32c0a-117">Esse comando remove a zona chamada myzone.com do grupo de recursos chamado MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="32c0a-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="32c0a-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32c0a-118">PARAMETERS</span></span>

### <span data-ttu-id="32c0a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32c0a-119">-DefaultProfile</span></span>
<span data-ttu-id="32c0a-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="32c0a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32c0a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="32c0a-121">-Name</span></span>
<span data-ttu-id="32c0a-122">Especifica o nome da zona DNS que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="32c0a-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="32c0a-123">Você também deve especificar o parâmetro *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="32c0a-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="32c0a-124">Como alternativa, você pode especificar a zona DNS usando o *parâmetro* Zona.</span><span class="sxs-lookup"><span data-stu-id="32c0a-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="32c0a-125">-Substituir</span><span class="sxs-lookup"><span data-stu-id="32c0a-125">-Overwrite</span></span>
<span data-ttu-id="32c0a-126">Ao especificar a zona usando um objeto **DnsZone** (passado pelo parâmetro pipeline ou Zona), a zona não será excluída se tiver sido alterada no DNS do Azure desde que o objeto **DnsZone** local foi recuperado (somente as operações diretamente na contagem de recursos de zona DNS como alterações, as operações em conjuntos de registros dentro da zona não o fazem). </span><span class="sxs-lookup"><span data-stu-id="32c0a-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="32c0a-127">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="32c0a-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="32c0a-128">Isso pode ser suprimido usando o parâmetro *Substituir,* que exclui a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="32c0a-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="32c0a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32c0a-129">-PassThru</span></span>
<span data-ttu-id="32c0a-130">Passthru</span><span class="sxs-lookup"><span data-stu-id="32c0a-130">passthru</span></span>

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

### <span data-ttu-id="32c0a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32c0a-131">-ResourceGroupName</span></span>
<span data-ttu-id="32c0a-132">Especifica o nome do grupo de recursos que contém a zona a ser removido.</span><span class="sxs-lookup"><span data-stu-id="32c0a-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="32c0a-133">Você também deve especificar o parâmetro *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="32c0a-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="32c0a-134">Como alternativa, você pode especificar a zona DNS usando um objeto **DnsZone,** passado pelo pipeline ou pelo parâmetro *Zona.*</span><span class="sxs-lookup"><span data-stu-id="32c0a-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="32c0a-135">-Zona</span><span class="sxs-lookup"><span data-stu-id="32c0a-135">-Zone</span></span>
<span data-ttu-id="32c0a-136">Especifica a zona DNS a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="32c0a-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="32c0a-137">O **objeto DnsZone** passado também pode ser passado por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="32c0a-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="32c0a-138">Como alternativa, você pode especificar a zona DNS a ser excluído usando os parâmetros *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="32c0a-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="32c0a-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="32c0a-139">-Confirm</span></span>
<span data-ttu-id="32c0a-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32c0a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32c0a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32c0a-141">-WhatIf</span></span>
<span data-ttu-id="32c0a-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="32c0a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32c0a-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32c0a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32c0a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32c0a-144">CommonParameters</span></span>
<span data-ttu-id="32c0a-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32c0a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32c0a-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32c0a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32c0a-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="32c0a-147">INPUTS</span></span>

### <span data-ttu-id="32c0a-148">System.String</span><span class="sxs-lookup"><span data-stu-id="32c0a-148">System.String</span></span>

### <span data-ttu-id="32c0a-149">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="32c0a-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="32c0a-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="32c0a-150">OUTPUTS</span></span>

### <span data-ttu-id="32c0a-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="32c0a-151">System.Boolean</span></span>

## <span data-ttu-id="32c0a-152">Notas</span><span class="sxs-lookup"><span data-stu-id="32c0a-152">NOTES</span></span>
<span data-ttu-id="32c0a-153">Devido ao potencialmente alto impacto da exclusão de uma zona DNS, por padrão, esse cmdlet solicita confirmação se a variável $ConfirmPreference Windows PowerShell tiver algum valor diferente de Nenhum.</span><span class="sxs-lookup"><span data-stu-id="32c0a-153">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="32c0a-154">Se você especificar *Confirmar* ou *Confirmar:$True,* este cmdlet solicitará que você confirme antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="32c0a-154">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="32c0a-155">Se você especificar *Confirm:$False,* o cmdlet não solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="32c0a-155">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="32c0a-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32c0a-156">RELATED LINKS</span></span>

[<span data-ttu-id="32c0a-157">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="32c0a-157">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="32c0a-158">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="32c0a-158">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="32c0a-159">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="32c0a-159">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
