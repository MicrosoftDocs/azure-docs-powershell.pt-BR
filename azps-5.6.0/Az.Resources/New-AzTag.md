---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: b5f80abac4c114ab60dcb130f229265c4aafd78f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887859"
---
# <span data-ttu-id="267e4-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="267e4-101">New-AzTag</span></span>

## <span data-ttu-id="267e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="267e4-102">SYNOPSIS</span></span>
<span data-ttu-id="267e4-103">Cria uma marca predefinida do Azure ou adiciona valores a uma marca | Cria ou atualiza todo o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="267e4-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="267e4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="267e4-104">SYNTAX</span></span>

### <span data-ttu-id="267e4-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="267e4-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="267e4-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="267e4-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="267e4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="267e4-107">DESCRIPTION</span></span>

<span data-ttu-id="267e4-108">**CreatePredefinedTagSet**: o cmdlet **New-AzTag** cria uma marca predefinida do Azure com um valor predefinido opcional.</span><span class="sxs-lookup"><span data-stu-id="267e4-108">**CreatePredefinedTagSet**: The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="267e4-109">Você também pode usá-lo para adicionar valores adicionais a marcas predefinida existentes.</span><span class="sxs-lookup"><span data-stu-id="267e4-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="267e4-110">Para criar uma marca predefinida, insira um nome de marca exclusivo.</span><span class="sxs-lookup"><span data-stu-id="267e4-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="267e4-111">Para adicionar um valor a uma marca predefinida existente, especifique o nome da marca existente e o novo valor.</span><span class="sxs-lookup"><span data-stu-id="267e4-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="267e4-112">Este cmdlet retorna um objeto que representa a marca nova ou modificada com seus valores e o número de recursos aos quais foi aplicado.</span><span class="sxs-lookup"><span data-stu-id="267e4-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="267e4-113">O módulo Marcas do Azure do que **o New-AzTag** faz parte pode ajudá-lo a gerenciar marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="267e4-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="267e4-114">Uma marca do Azure é um par de valores de nome que você pode usar para categorizar seus recursos e grupos de recursos do Azure, como departamento ou centro de custo, ou para acompanhar observações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="267e4-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="267e4-115">Você pode definir e aplicar marcas em uma única etapa, mas marcas predefinida permitem estabelecer nomes e valores padrão, consistentes e previsíveis para as marcas em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="267e4-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="267e4-116">Para aplicar uma marca predefinida a um grupo de recursos ou recursos, use o parâmetro *Tag* do cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="267e4-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="267e4-117">Para pesquisar grupos de recursos com um nome ou nome de marca especificado e um valor, use o parâmetro *Tag* do cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="267e4-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="267e4-118">Cada marca tem um nome.</span><span class="sxs-lookup"><span data-stu-id="267e4-118">Every tag has a name.</span></span>
<span data-ttu-id="267e4-119">Os valores são opcionais.</span><span class="sxs-lookup"><span data-stu-id="267e4-119">The values are optional.</span></span>
<span data-ttu-id="267e4-120">Uma marca predefinida do Azure pode ter vários valores, mas quando você aplica a marca a um grupo de recursos ou recursos, você aplica o nome da marca e apenas um de seus valores.</span><span class="sxs-lookup"><span data-stu-id="267e4-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="267e4-121">Por exemplo, você pode criar uma marca de Departamento predefinida com um valor para cada departamento, como Finanças, Recursos Humanos e TI.</span><span class="sxs-lookup"><span data-stu-id="267e4-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="267e4-122">Quando você aplica a marca Department a um recurso, você aplica apenas um valor predefinido, como Finanças.</span><span class="sxs-lookup"><span data-stu-id="267e4-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="267e4-123">**CreateByResourceIdParameterSet**: o cmdlet **New-AzTag** com **um ResourceId** cria ou atualiza todo o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="267e4-123">**CreateByResourceIdParameterSet**: The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="267e4-124">Essa operação permite adicionar ou substituir todo o conjunto de marcas no recurso ou assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="267e4-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="267e4-125">A entidade especificada pode ter no máximo 50 marcas.</span><span class="sxs-lookup"><span data-stu-id="267e4-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="267e4-126">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="267e4-126">EXAMPLES</span></span>

### <span data-ttu-id="267e4-127">Exemplo 1: Criar uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="267e4-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="267e4-128">Este comando cria uma marca predefinida chamada FY2015.</span><span class="sxs-lookup"><span data-stu-id="267e4-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="267e4-129">Essa marca não tem valores.</span><span class="sxs-lookup"><span data-stu-id="267e4-129">This tag has no values.</span></span>
<span data-ttu-id="267e4-130">Você pode aplicar uma marca sem valores a um grupo de recursos ou recursos ou usar **New-AzTag** para adicionar valores à marca.</span><span class="sxs-lookup"><span data-stu-id="267e4-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="267e4-131">Você também pode especificar um valor ao aplicar a marca ao grupo de recursos ou recursos.</span><span class="sxs-lookup"><span data-stu-id="267e4-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="267e4-132">Exemplo 2: Criar uma marca predefinida com um valor</span><span class="sxs-lookup"><span data-stu-id="267e4-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="267e4-133">Este comando cria uma marca predefinida chamada Department com um valor de Finanças.</span><span class="sxs-lookup"><span data-stu-id="267e4-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="267e4-134">Exemplo 3: Adicionar um valor a uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="267e4-134">Example 3: Add a value to a predefined tag</span></span>
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

<span data-ttu-id="267e4-135">Esses comandos criam uma marca predefinida chamada Department com dois valores.</span><span class="sxs-lookup"><span data-stu-id="267e4-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="267e4-136">Se o nome da marca existir, **New-AzTag** adiciona o valor à marca existente em vez de criar um novo.</span><span class="sxs-lookup"><span data-stu-id="267e4-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="267e4-137">Exemplo 4: Usar uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="267e4-137">Example 4: Use a predefined tag</span></span>
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

<span data-ttu-id="267e4-138">Os comandos neste exemplo criam e usam uma marca predefinida.</span><span class="sxs-lookup"><span data-stu-id="267e4-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="267e4-139">Exemplo 5: cria ou atualiza todo o conjunto de marcas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="267e4-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="267e4-140">Este comando cria ou atualiza todo o conjunto de marcas na assinatura com {subId}.</span><span class="sxs-lookup"><span data-stu-id="267e4-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="267e4-141">Exemplo 6: cria ou atualiza todo o conjunto de marcas em um recurso</span><span class="sxs-lookup"><span data-stu-id="267e4-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

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

<span data-ttu-id="267e4-142">Este comando cria ou atualiza todo o conjunto de marcas no recurso com {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="267e4-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="267e4-143">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="267e4-143">PARAMETERS</span></span>

### <span data-ttu-id="267e4-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="267e4-144">-DefaultProfile</span></span>
<span data-ttu-id="267e4-145">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="267e4-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="267e4-146">-Name</span><span class="sxs-lookup"><span data-stu-id="267e4-146">-Name</span></span>
<span data-ttu-id="267e4-147">Especifica o nome da marca predefinido.</span><span class="sxs-lookup"><span data-stu-id="267e4-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="267e4-148">Para criar uma nova marca predefinida, insira um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="267e4-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="267e4-149">Para adicionar um valor a uma marca existente, insira o nome da marca existente.</span><span class="sxs-lookup"><span data-stu-id="267e4-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="267e4-150">Se uma marca predefinida existente tiver o nome especificado, **New-AzTag** adiciona o valor especificado, se for o caso, à marca com esse nome em vez de criar uma nova marca.</span><span class="sxs-lookup"><span data-stu-id="267e4-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="267e4-151">-Value</span><span class="sxs-lookup"><span data-stu-id="267e4-151">-Value</span></span>
<span data-ttu-id="267e4-152">Especifica um valor de marca predefinido.</span><span class="sxs-lookup"><span data-stu-id="267e4-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="267e4-153">Marcas predefinidos podem ter vários valores, mas você pode inserir apenas um valor em cada comando.</span><span class="sxs-lookup"><span data-stu-id="267e4-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="267e4-154">Esse parâmetro é opcional, pois as marcas podem ter nomes sem valores.</span><span class="sxs-lookup"><span data-stu-id="267e4-154">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="267e4-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="267e4-155">-ResourceId</span></span>
<span data-ttu-id="267e4-156">O identificador de recurso da entidade que está sendo marcada.</span><span class="sxs-lookup"><span data-stu-id="267e4-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="267e4-157">Um recurso, um grupo de recursos ou uma assinatura podem ser marcados.</span><span class="sxs-lookup"><span data-stu-id="267e4-157">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="267e4-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="267e4-158">-Tag</span></span>
<span data-ttu-id="267e4-159">As marcas a ser colocadas no recurso.</span><span class="sxs-lookup"><span data-stu-id="267e4-159">The tags to put on the resource.</span></span>

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

### <span data-ttu-id="267e4-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="267e4-160">-Confirm</span></span>
<span data-ttu-id="267e4-161">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="267e4-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="267e4-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="267e4-162">-WhatIf</span></span>
<span data-ttu-id="267e4-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="267e4-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="267e4-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="267e4-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="267e4-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="267e4-165">CommonParameters</span></span>
<span data-ttu-id="267e4-166">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="267e4-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="267e4-167">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="267e4-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="267e4-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="267e4-168">INPUTS</span></span>

### <span data-ttu-id="267e4-169">System.String</span><span class="sxs-lookup"><span data-stu-id="267e4-169">System.String</span></span>

### <span data-ttu-id="267e4-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="267e4-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="267e4-171">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="267e4-171">OUTPUTS</span></span>

### <span data-ttu-id="267e4-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="267e4-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="267e4-173">NOTES</span><span class="sxs-lookup"><span data-stu-id="267e4-173">NOTES</span></span>

## <span data-ttu-id="267e4-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="267e4-174">RELATED LINKS</span></span>

[<span data-ttu-id="267e4-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="267e4-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="267e4-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="267e4-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="267e4-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="267e4-177">Update-AzTag</span></span>](./Update-AzTag.md)