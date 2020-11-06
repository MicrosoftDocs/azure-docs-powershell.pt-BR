---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: ee880422e01b68bb595c709c1642038f75003c49
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599369"
---
# <span data-ttu-id="2183e-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="2183e-101">New-AzTag</span></span>

## <span data-ttu-id="2183e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2183e-102">SYNOPSIS</span></span>
<span data-ttu-id="2183e-103">Cria uma marca predefinida do Azure ou adiciona valores a uma marca existente.</span><span class="sxs-lookup"><span data-stu-id="2183e-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

## <span data-ttu-id="2183e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2183e-104">SYNTAX</span></span>

```
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2183e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2183e-105">DESCRIPTION</span></span>
<span data-ttu-id="2183e-106">O cmdlet **New-AzTag** cria uma marca predefinida do Azure com um valor predefinido opcional.</span><span class="sxs-lookup"><span data-stu-id="2183e-106">The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="2183e-107">Você também pode usá-lo para adicionar valores adicionais a marcas predefinidas existentes.</span><span class="sxs-lookup"><span data-stu-id="2183e-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="2183e-108">Para criar uma marca predefinida, insira um nome exclusivo para a marca.</span><span class="sxs-lookup"><span data-stu-id="2183e-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="2183e-109">Para adicionar um valor a uma marca predefinida existente, especifique o nome da marca existente e o novo valor.</span><span class="sxs-lookup"><span data-stu-id="2183e-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="2183e-110">Esse cmdlet retorna um objeto que representa a marca nova ou modificada com seus valores e o número de recursos aos quais ele foi aplicado.</span><span class="sxs-lookup"><span data-stu-id="2183e-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="2183e-111">O módulo de marcas do Azure que **New-AzTag** faz parte do pode ajudá-lo a gerenciar marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="2183e-111">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="2183e-112">Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="2183e-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="2183e-113">Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="2183e-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="2183e-114">Para aplicar uma marca predefinida a um recurso ou grupo de recursos, use o parâmetro *tag* do cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="2183e-114">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="2183e-115">Para pesquisar grupos de recursos com um nome de marca ou nome ou valor especificado, use o parâmetro *tag* do cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2183e-115">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="2183e-116">Cada marca tem um nome.</span><span class="sxs-lookup"><span data-stu-id="2183e-116">Every tag has a name.</span></span>
<span data-ttu-id="2183e-117">Os valores são opcionais.</span><span class="sxs-lookup"><span data-stu-id="2183e-117">The values are optional.</span></span>
<span data-ttu-id="2183e-118">Uma marca predefinida do Azure pode ter vários valores, mas quando você aplica a marca a um recurso ou grupo de recursos, aplica o nome da marca e somente um de seus valores.</span><span class="sxs-lookup"><span data-stu-id="2183e-118">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="2183e-119">Por exemplo, você pode criar uma marca de departamento predefinida com um valor para cada departamento, como finanças, recursos humanos e isso.</span><span class="sxs-lookup"><span data-stu-id="2183e-119">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="2183e-120">Ao aplicar a marca de departamento a um recurso, você aplica apenas um valor predefinido, como finanças.</span><span class="sxs-lookup"><span data-stu-id="2183e-120">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="2183e-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2183e-121">EXAMPLES</span></span>

### <span data-ttu-id="2183e-122">Exemplo 1: criar uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="2183e-122">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="2183e-123">Esse comando cria uma marca predefinida chamada FY2015.</span><span class="sxs-lookup"><span data-stu-id="2183e-123">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="2183e-124">Esta marca não tem valores.</span><span class="sxs-lookup"><span data-stu-id="2183e-124">This tag has no values.</span></span>
<span data-ttu-id="2183e-125">Você pode aplicar uma marca sem valores a um recurso ou grupo de recursos ou usar **New-AzTag** para adicionar valores à marca.</span><span class="sxs-lookup"><span data-stu-id="2183e-125">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="2183e-126">Você também pode especificar um valor ao aplicar a marca ao recurso ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2183e-126">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="2183e-127">Exemplo 2: criar uma marca predefinida com um valor</span><span class="sxs-lookup"><span data-stu-id="2183e-127">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="2183e-128">Esse comando cria uma marca predefinida chamada Department com um valor de Finance.</span><span class="sxs-lookup"><span data-stu-id="2183e-128">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="2183e-129">Exemplo 3: adicionar um valor a uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="2183e-129">Example 3: Add a value to a predefined tag</span></span>
```
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

<span data-ttu-id="2183e-130">Esses comandos criam uma marca predefinida chamada Department com dois valores.</span><span class="sxs-lookup"><span data-stu-id="2183e-130">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="2183e-131">Se o nome da marca existir, **New-AzTag** adiciona o valor à marca existente, em vez de criar uma nova.</span><span class="sxs-lookup"><span data-stu-id="2183e-131">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="2183e-132">Exemplo 4: usar uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="2183e-132">Example 4: Use a predefined tag</span></span>
```
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

<span data-ttu-id="2183e-133">Os comandos neste exemplo criam e usam uma marca predefinida.</span><span class="sxs-lookup"><span data-stu-id="2183e-133">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="2183e-134">OS</span><span class="sxs-lookup"><span data-stu-id="2183e-134">PARAMETERS</span></span>

### <span data-ttu-id="2183e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2183e-135">-DefaultProfile</span></span>
<span data-ttu-id="2183e-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2183e-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2183e-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="2183e-137">-Name</span></span>
<span data-ttu-id="2183e-138">Especifica o nome da marca.</span><span class="sxs-lookup"><span data-stu-id="2183e-138">Specifies the tag name.</span></span>
<span data-ttu-id="2183e-139">Para criar uma nova marca predefinida, insira um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2183e-139">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="2183e-140">Para adicionar um valor a uma marca existente, insira o nome da marca existente.</span><span class="sxs-lookup"><span data-stu-id="2183e-140">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="2183e-141">Se uma marca predefinida existente tiver o nome especificado, **New-AzTag** adicionará o valor especificado, se houver, à marca com esse nome em vez de criar uma nova marca.</span><span class="sxs-lookup"><span data-stu-id="2183e-141">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2183e-142">-Valor</span><span class="sxs-lookup"><span data-stu-id="2183e-142">-Value</span></span>
<span data-ttu-id="2183e-143">Especifica um valor de marca.</span><span class="sxs-lookup"><span data-stu-id="2183e-143">Specifies a tag value.</span></span>
<span data-ttu-id="2183e-144">Marcas predefinidas podem ter vários valores, mas você pode inserir apenas um valor em cada comando.</span><span class="sxs-lookup"><span data-stu-id="2183e-144">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="2183e-145">Esse parâmetro é opcional, pois as marcas podem ter nomes sem valores.</span><span class="sxs-lookup"><span data-stu-id="2183e-145">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2183e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2183e-146">CommonParameters</span></span>
<span data-ttu-id="2183e-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2183e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2183e-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2183e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2183e-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2183e-149">INPUTS</span></span>

### <span data-ttu-id="2183e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2183e-150">System.String</span></span>

## <span data-ttu-id="2183e-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2183e-151">OUTPUTS</span></span>

### <span data-ttu-id="2183e-152">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="2183e-152">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="2183e-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2183e-153">NOTES</span></span>

## <span data-ttu-id="2183e-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2183e-154">RELATED LINKS</span></span>

[<span data-ttu-id="2183e-155">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="2183e-155">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="2183e-156">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="2183e-156">Remove-AzTag</span></span>](./Remove-AzTag.md)


