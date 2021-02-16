---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114022"
---
# <span data-ttu-id="bfd99-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="bfd99-101">Remove-AzTag</span></span>

## <span data-ttu-id="bfd99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfd99-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd99-103">Exclui marcas ou valores predefinidos do Azure | Exclui todo o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="bfd99-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="bfd99-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfd99-104">SYNTAX</span></span>

### <span data-ttu-id="bfd99-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfd99-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfd99-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfd99-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="bfd99-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfd99-107">DESCRIPTION</span></span>

<span data-ttu-id="bfd99-108">**RemovePredefinedTagSet:** o cmdlet **Remove-AzTag** exclui marcas e valores predefinidos do Azure da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="bfd99-108">**RemovePredefinedTagSet**: The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="bfd99-109">Para excluir valores específicos de uma marca predefinida, use o *parâmetro* Valor.</span><span class="sxs-lookup"><span data-stu-id="bfd99-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="bfd99-110">Por padrão, **Remove-AzTag** exclui a marca especificada e todos os seus valores. Não é possível excluir uma marca ou valor aplicado atualmente a um grupo de recursos ou recursos.</span><span class="sxs-lookup"><span data-stu-id="bfd99-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="bfd99-111">Antes de **usar Remove-AzTag,** use o parâmetro Tag do cmdlet Set-AzResourceGroup para excluir a marca ou os valores do grupo de recursos ou recursos. </span><span class="sxs-lookup"><span data-stu-id="bfd99-111">Before using **Remove-AzTag**, use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="bfd99-112">O módulo Marcas do Azure do **que Remove-AzTag** faz parte pode ajudá-lo a gerenciar suas marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfd99-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="bfd99-113">Uma marca do Azure é um par de valores de nome que você pode usar para categorizar seus recursos e grupos de recursos do Azure, como por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="bfd99-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="bfd99-114">Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinida permitem estabelecer nomes e valores padrão, consistentes e previsíveis para as marcas em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="bfd99-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="bfd99-115">**RemoveByResourceIdParameterSet:** o cmdlet **Remove-AzTag** com **um ResourceId** exclui todo o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="bfd99-115">**RemoveByResourceIdParameterSet**: The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="bfd99-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bfd99-116">EXAMPLES</span></span>

### <span data-ttu-id="bfd99-117">Exemplo 1: Excluir uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="bfd99-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="bfd99-118">Esse comando exclui a marca predefinida denominada Departamento e todos os seus valores.</span><span class="sxs-lookup"><span data-stu-id="bfd99-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="bfd99-119">Se a marca tiver sido aplicada a todos os recursos ou grupos de recursos, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="bfd99-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="bfd99-120">Exemplo 2: Excluir um valor de uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="bfd99-120">Example 2: Delete a value from a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="bfd99-121">Esse comando exclui o valor HumanResources da marca Departamento predefinida.</span><span class="sxs-lookup"><span data-stu-id="bfd99-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="bfd99-122">Ele não exclui a marca.</span><span class="sxs-lookup"><span data-stu-id="bfd99-122">It does not delete the tag.</span></span>
<span data-ttu-id="bfd99-123">Se o valor tiver sido aplicado a qualquer recurso ou grupos de recursos, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="bfd99-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="bfd99-124">Exemplo 3: exclui todo o conjunto de marcas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="bfd99-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="bfd99-125">Esse comando exclui todo o conjunto de marcas na assinatura com {subId}.</span><span class="sxs-lookup"><span data-stu-id="bfd99-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="bfd99-126">Ele não retornará o objeto excluído se não passar em "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="bfd99-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="bfd99-127">Exemplo 4: exclui todo o conjunto de marcas em um recurso</span><span class="sxs-lookup"><span data-stu-id="bfd99-127">Example 4: Deletes the entire set of tags on a resource</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="bfd99-128">Esse comando exclui todo o conjunto de marcas no recurso com {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="bfd99-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="bfd99-129">Ele retorna o oject excluído ao passar em "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="bfd99-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="bfd99-130">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfd99-130">PARAMETERS</span></span>

### <span data-ttu-id="bfd99-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd99-131">-DefaultProfile</span></span>
<span data-ttu-id="bfd99-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bfd99-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfd99-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfd99-133">-Name</span></span>
<span data-ttu-id="bfd99-134">Especifica o Nome da marca predefinida a ser removido.</span><span class="sxs-lookup"><span data-stu-id="bfd99-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="bfd99-135">Por padrão, **Remove-AzTag** remove a marca especificada e todos os seus valores.</span><span class="sxs-lookup"><span data-stu-id="bfd99-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="bfd99-136">Para excluir os valores selecionados, mas não excluir a marca, use o *parâmetro* Valor.</span><span class="sxs-lookup"><span data-stu-id="bfd99-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfd99-137">-Valor</span><span class="sxs-lookup"><span data-stu-id="bfd99-137">-Value</span></span>
<span data-ttu-id="bfd99-138">Exclui os valores especificados da marca predefinida, mas não exclui a marca.</span><span class="sxs-lookup"><span data-stu-id="bfd99-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfd99-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfd99-139">-ResourceId</span></span>
<span data-ttu-id="bfd99-140">O identificador de recurso da entidade marcada.</span><span class="sxs-lookup"><span data-stu-id="bfd99-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="bfd99-141">Um recurso, um grupo de recursos ou uma assinatura podem ser marcados.</span><span class="sxs-lookup"><span data-stu-id="bfd99-141">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfd99-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfd99-142">-PassThru</span></span>
<span data-ttu-id="bfd99-143">Retorna um objeto que representa a marca excluída ou a marca resultante com valor excluído.</span><span class="sxs-lookup"><span data-stu-id="bfd99-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfd99-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bfd99-144">-Confirm</span></span>
<span data-ttu-id="bfd99-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfd99-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfd99-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfd99-146">-WhatIf</span></span>
<span data-ttu-id="bfd99-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bfd99-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfd99-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bfd99-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfd99-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd99-149">CommonParameters</span></span>
<span data-ttu-id="bfd99-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfd99-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd99-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfd99-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd99-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="bfd99-152">INPUTS</span></span>

### <span data-ttu-id="bfd99-153">System.String</span><span class="sxs-lookup"><span data-stu-id="bfd99-153">System.String</span></span>

### <span data-ttu-id="bfd99-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="bfd99-154">System.String[]</span></span>

### <span data-ttu-id="bfd99-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bfd99-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bfd99-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="bfd99-156">OUTPUTS</span></span>

### <span data-ttu-id="bfd99-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="bfd99-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="bfd99-158">Notas</span><span class="sxs-lookup"><span data-stu-id="bfd99-158">NOTES</span></span>

## <span data-ttu-id="bfd99-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfd99-159">RELATED LINKS</span></span>

[<span data-ttu-id="bfd99-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="bfd99-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="bfd99-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="bfd99-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="bfd99-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="bfd99-162">Update-AzTag</span></span>](./Update-AzTag.md)