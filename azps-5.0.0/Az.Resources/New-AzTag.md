---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281885"
---
# <span data-ttu-id="9b663-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="9b663-101">New-AzTag</span></span>

## <span data-ttu-id="9b663-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b663-102">SYNOPSIS</span></span>
<span data-ttu-id="9b663-103">Cria uma marca predefinida do Azure ou adiciona valores a uma marca existente | Cria ou atualiza todo o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="9b663-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="9b663-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b663-104">SYNTAX</span></span>

### <span data-ttu-id="9b663-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b663-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b663-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b663-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="9b663-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b663-107">DESCRIPTION</span></span>

<span data-ttu-id="9b663-108">**CreatePredefinedTagSet** : o cmdlet **New-AzTag** cria uma marca predefinida do Azure com um valor predefinido opcional.</span><span class="sxs-lookup"><span data-stu-id="9b663-108">**CreatePredefinedTagSet** : The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="9b663-109">Você também pode usá-lo para adicionar valores adicionais a marcas predefinidas existentes.</span><span class="sxs-lookup"><span data-stu-id="9b663-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="9b663-110">Para criar uma marca predefinida, insira um nome exclusivo para a marca.</span><span class="sxs-lookup"><span data-stu-id="9b663-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="9b663-111">Para adicionar um valor a uma marca predefinida existente, especifique o nome da marca existente e o novo valor.</span><span class="sxs-lookup"><span data-stu-id="9b663-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="9b663-112">Esse cmdlet retorna um objeto que representa a marca nova ou modificada com seus valores e o número de recursos aos quais ele foi aplicado.</span><span class="sxs-lookup"><span data-stu-id="9b663-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="9b663-113">O módulo de marcas do Azure que **New-AzTag** faz parte do pode ajudá-lo a gerenciar marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="9b663-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="9b663-114">Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="9b663-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="9b663-115">Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="9b663-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="9b663-116">Para aplicar uma marca predefinida a um recurso ou grupo de recursos, use o parâmetro *tag* do cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="9b663-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="9b663-117">Para pesquisar grupos de recursos com um nome de marca ou nome ou valor especificado, use o parâmetro *tag* do cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9b663-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="9b663-118">Cada marca tem um nome.</span><span class="sxs-lookup"><span data-stu-id="9b663-118">Every tag has a name.</span></span>
<span data-ttu-id="9b663-119">Os valores são opcionais.</span><span class="sxs-lookup"><span data-stu-id="9b663-119">The values are optional.</span></span>
<span data-ttu-id="9b663-120">Uma marca predefinida do Azure pode ter vários valores, mas quando você aplica a marca a um recurso ou grupo de recursos, aplica o nome da marca e somente um de seus valores.</span><span class="sxs-lookup"><span data-stu-id="9b663-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="9b663-121">Por exemplo, você pode criar uma marca de departamento predefinida com um valor para cada departamento, como finanças, recursos humanos e isso.</span><span class="sxs-lookup"><span data-stu-id="9b663-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="9b663-122">Ao aplicar a marca de departamento a um recurso, você aplica apenas um valor predefinido, como finanças.</span><span class="sxs-lookup"><span data-stu-id="9b663-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="9b663-123">**CreateByResourceIdParameterSet** : o cmdlet **New-AzTag** com uma **ResourceId** cria ou atualiza todo o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="9b663-123">**CreateByResourceIdParameterSet** : The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="9b663-124">Esta operação permite adicionar ou substituir o conjunto inteiro de marcas no recurso ou assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="9b663-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="9b663-125">A entidade especificada pode ter no máximo 50 marcas.</span><span class="sxs-lookup"><span data-stu-id="9b663-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="9b663-126">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b663-126">EXAMPLES</span></span>

### <span data-ttu-id="9b663-127">Exemplo 1: criar uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="9b663-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="9b663-128">Esse comando cria uma marca predefinida chamada FY2015.</span><span class="sxs-lookup"><span data-stu-id="9b663-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="9b663-129">Esta marca não tem valores.</span><span class="sxs-lookup"><span data-stu-id="9b663-129">This tag has no values.</span></span>
<span data-ttu-id="9b663-130">Você pode aplicar uma marca sem valores a um recurso ou grupo de recursos ou usar **New-AzTag** para adicionar valores à marca.</span><span class="sxs-lookup"><span data-stu-id="9b663-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="9b663-131">Você também pode especificar um valor ao aplicar a marca ao recurso ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9b663-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="9b663-132">Exemplo 2: criar uma marca predefinida com um valor</span><span class="sxs-lookup"><span data-stu-id="9b663-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="9b663-133">Esse comando cria uma marca predefinida chamada Department com um valor de Finance.</span><span class="sxs-lookup"><span data-stu-id="9b663-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="9b663-134">Exemplo 3: adicionar um valor a uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="9b663-134">Example 3: Add a value to a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="9b663-135">Esses comandos criam uma marca predefinida chamada Department com dois valores.</span><span class="sxs-lookup"><span data-stu-id="9b663-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="9b663-136">Se o nome da marca existir, **New-AzTag** adiciona o valor à marca existente, em vez de criar uma nova.</span><span class="sxs-lookup"><span data-stu-id="9b663-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="9b663-137">Exemplo 4: usar uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="9b663-137">Example 4: Use a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

<span data-ttu-id="9b663-138">Os comandos neste exemplo criam e usam uma marca predefinida.</span><span class="sxs-lookup"><span data-stu-id="9b663-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="9b663-139">Exemplo 5: cria ou atualiza todo o conjunto de marcas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="9b663-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="9b663-140">Esse comando cria ou atualiza todo o conjunto de marcas na assinatura com {subId}.</span><span class="sxs-lookup"><span data-stu-id="9b663-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="9b663-141">Exemplo 6: cria ou atualiza todo o conjunto de marcas em um recurso</span><span class="sxs-lookup"><span data-stu-id="9b663-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="9b663-142">Esse comando cria ou atualiza todo o conjunto de marcas no recurso com {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="9b663-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="9b663-143">OS</span><span class="sxs-lookup"><span data-stu-id="9b663-143">PARAMETERS</span></span>

### <span data-ttu-id="9b663-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b663-144">-DefaultProfile</span></span>
<span data-ttu-id="9b663-145">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b663-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b663-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b663-146">-Name</span></span>
<span data-ttu-id="9b663-147">Especifica o nome de marca predefinido.</span><span class="sxs-lookup"><span data-stu-id="9b663-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="9b663-148">Para criar uma nova marca predefinida, insira um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="9b663-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="9b663-149">Para adicionar um valor a uma marca existente, insira o nome da marca existente.</span><span class="sxs-lookup"><span data-stu-id="9b663-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="9b663-150">Se uma marca predefinida existente tiver o nome especificado, **New-AzTag** adicionará o valor especificado, se houver, à marca com esse nome em vez de criar uma nova marca.</span><span class="sxs-lookup"><span data-stu-id="9b663-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b663-151">-Valor</span><span class="sxs-lookup"><span data-stu-id="9b663-151">-Value</span></span>
<span data-ttu-id="9b663-152">Especifica um valor de marca predefinido.</span><span class="sxs-lookup"><span data-stu-id="9b663-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="9b663-153">Marcas predefinidas podem ter vários valores, mas você pode inserir apenas um valor em cada comando.</span><span class="sxs-lookup"><span data-stu-id="9b663-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="9b663-154">Esse parâmetro é opcional, pois as marcas podem ter nomes sem valores.</span><span class="sxs-lookup"><span data-stu-id="9b663-154">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b663-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b663-155">-ResourceId</span></span>
<span data-ttu-id="9b663-156">O identificador de recurso para a entidade que está sendo marcada.</span><span class="sxs-lookup"><span data-stu-id="9b663-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="9b663-157">Um recurso, um grupo de recursos ou uma assinatura pode estar marcado.</span><span class="sxs-lookup"><span data-stu-id="9b663-157">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b663-158">-Marca</span><span class="sxs-lookup"><span data-stu-id="9b663-158">-Tag</span></span>
<span data-ttu-id="9b663-159">As marcas a serem colocadas no recurso.</span><span class="sxs-lookup"><span data-stu-id="9b663-159">The tags to put on the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b663-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b663-160">-Confirm</span></span>
<span data-ttu-id="9b663-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b663-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b663-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b663-162">-WhatIf</span></span>
<span data-ttu-id="9b663-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b663-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b663-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b663-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b663-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b663-165">CommonParameters</span></span>
<span data-ttu-id="9b663-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b663-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b663-167">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b663-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b663-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b663-168">INPUTS</span></span>

### <span data-ttu-id="9b663-169">System. String</span><span class="sxs-lookup"><span data-stu-id="9b663-169">System.String</span></span>

### <span data-ttu-id="9b663-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b663-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9b663-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b663-171">OUTPUTS</span></span>

### <span data-ttu-id="9b663-172">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="9b663-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="9b663-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b663-173">NOTES</span></span>

## <span data-ttu-id="9b663-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b663-174">RELATED LINKS</span></span>

[<span data-ttu-id="9b663-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="9b663-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="9b663-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="9b663-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="9b663-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="9b663-177">Update-AzTag</span></span>](./Update-AzTag.md)