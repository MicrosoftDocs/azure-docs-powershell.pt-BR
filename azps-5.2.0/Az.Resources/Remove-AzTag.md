---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261848"
---
# <span data-ttu-id="14b3d-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="14b3d-101">Remove-AzTag</span></span>

## <span data-ttu-id="14b3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="14b3d-103">Exclui valores ou marcas do Azure predefinidas | Exclui todo o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="14b3d-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="14b3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14b3d-104">SYNTAX</span></span>

### <span data-ttu-id="14b3d-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="14b3d-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14b3d-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14b3d-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="14b3d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14b3d-107">DESCRIPTION</span></span>

<span data-ttu-id="14b3d-108">**RemovePredefinedTagSet**: o cmdlet **Remove-AzTag** exclui as marcas e os valores predefinidos do Azure de sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="14b3d-108">**RemovePredefinedTagSet**: The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="14b3d-109">Para excluir valores específicos de uma marca predefinida, use o parâmetro *Value* .</span><span class="sxs-lookup"><span data-stu-id="14b3d-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="14b3d-110">Por padrão, **Remove-AzTag** exclui a marca especificada e todos os seus valores. Não é possível excluir uma marca ou um valor que seja aplicado no momento a um recurso ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14b3d-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="14b3d-111">Antes de usar **Remove-AzTag**, use o parâmetro *Tag* do cmdlet Set-AzResourceGroup para excluir a marca ou os valores do recurso ou do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14b3d-111">Before using **Remove-AzTag**, use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="14b3d-112">O módulo de marcas do Azure que **Remove-AzTag** faz parte do pode ajudá-lo a gerenciar suas marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="14b3d-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="14b3d-113">Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="14b3d-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="14b3d-114">Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="14b3d-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="14b3d-115">**RemoveByResourceIdParameterSet**: o cmdlet **Remove-AzTag** com uma **ResourceId** exclui todo o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="14b3d-115">**RemoveByResourceIdParameterSet**: The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="14b3d-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14b3d-116">EXAMPLES</span></span>

### <span data-ttu-id="14b3d-117">Exemplo 1: excluir uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="14b3d-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="14b3d-118">Esse comando exclui a marca predefinida chamada Department e todos os seus valores.</span><span class="sxs-lookup"><span data-stu-id="14b3d-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="14b3d-119">Se a marca tiver sido aplicada a recursos ou grupos de recursos, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="14b3d-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="14b3d-120">Exemplo 2: excluir um valor de uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="14b3d-120">Example 2: Delete a value from a predefined tag</span></span>
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

<span data-ttu-id="14b3d-121">Esse comando exclui o valor HumanResources da marca de departamento predefinida.</span><span class="sxs-lookup"><span data-stu-id="14b3d-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="14b3d-122">Ele não exclui a marca.</span><span class="sxs-lookup"><span data-stu-id="14b3d-122">It does not delete the tag.</span></span>
<span data-ttu-id="14b3d-123">Se o valor tiver sido aplicado a recursos ou grupos de recursos, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="14b3d-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="14b3d-124">Exemplo 3: exclui todo o conjunto de marcas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="14b3d-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="14b3d-125">Esse comando exclui todo o conjunto de marcas na assinatura com {subId}.</span><span class="sxs-lookup"><span data-stu-id="14b3d-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="14b3d-126">Ele não retornará o objeto excluído se não passar "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="14b3d-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="14b3d-127">Exemplo 4: exclui todo o conjunto de marcas em um recurso</span><span class="sxs-lookup"><span data-stu-id="14b3d-127">Example 4: Deletes the entire set of tags on a resource</span></span>

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

<span data-ttu-id="14b3d-128">Esse comando exclui todo o conjunto de marcas no recurso com {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="14b3d-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="14b3d-129">Ele retorna o oject excluído ao passar "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="14b3d-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="14b3d-130">OS</span><span class="sxs-lookup"><span data-stu-id="14b3d-130">PARAMETERS</span></span>

### <span data-ttu-id="14b3d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b3d-131">-DefaultProfile</span></span>
<span data-ttu-id="14b3d-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14b3d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14b3d-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="14b3d-133">-Name</span></span>
<span data-ttu-id="14b3d-134">Especifica o nome da marca predefinida a ser removida.</span><span class="sxs-lookup"><span data-stu-id="14b3d-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="14b3d-135">Por padrão, **Remove-AzTag** remove a marca especificada e todos os seus valores.</span><span class="sxs-lookup"><span data-stu-id="14b3d-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="14b3d-136">Para excluir os valores selecionados, mas não excluir a marca, use o parâmetro *Value* .</span><span class="sxs-lookup"><span data-stu-id="14b3d-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="14b3d-137">-Valor</span><span class="sxs-lookup"><span data-stu-id="14b3d-137">-Value</span></span>
<span data-ttu-id="14b3d-138">Exclui os valores especificados da marca predefinida, mas não exclui a marca.</span><span class="sxs-lookup"><span data-stu-id="14b3d-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="14b3d-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14b3d-139">-ResourceId</span></span>
<span data-ttu-id="14b3d-140">O identificador de recurso para a entidade marcada.</span><span class="sxs-lookup"><span data-stu-id="14b3d-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="14b3d-141">Um recurso, um grupo de recursos ou uma assinatura pode estar marcado.</span><span class="sxs-lookup"><span data-stu-id="14b3d-141">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="14b3d-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14b3d-142">-PassThru</span></span>
<span data-ttu-id="14b3d-143">Retorna um objeto que representa a marca excluída ou a marca resultante com valor excluído.</span><span class="sxs-lookup"><span data-stu-id="14b3d-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="14b3d-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14b3d-144">-Confirm</span></span>
<span data-ttu-id="14b3d-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14b3d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14b3d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14b3d-146">-WhatIf</span></span>
<span data-ttu-id="14b3d-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14b3d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14b3d-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14b3d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14b3d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b3d-149">CommonParameters</span></span>
<span data-ttu-id="14b3d-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b3d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b3d-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14b3d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b3d-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14b3d-152">INPUTS</span></span>

### <span data-ttu-id="14b3d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="14b3d-153">System.String</span></span>

### <span data-ttu-id="14b3d-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="14b3d-154">System.String[]</span></span>

### <span data-ttu-id="14b3d-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="14b3d-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="14b3d-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14b3d-156">OUTPUTS</span></span>

### <span data-ttu-id="14b3d-157">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="14b3d-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="14b3d-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14b3d-158">NOTES</span></span>

## <span data-ttu-id="14b3d-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14b3d-159">RELATED LINKS</span></span>

[<span data-ttu-id="14b3d-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="14b3d-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="14b3d-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="14b3d-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="14b3d-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="14b3d-162">Update-AzTag</span></span>](./Update-AzTag.md)