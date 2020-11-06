---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: b5b7356a2cda001bb615700b38657cc0d3249ec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609538"
---
# <span data-ttu-id="aa74c-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="aa74c-101">New-AzureRmTag</span></span>

## <span data-ttu-id="aa74c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa74c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa74c-103">Cria uma marca predefinida do Azure ou adiciona valores a uma marca existente.</span><span class="sxs-lookup"><span data-stu-id="aa74c-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa74c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa74c-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa74c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa74c-105">DESCRIPTION</span></span>
<span data-ttu-id="aa74c-106">O cmdlet **New-AzureRmTag** cria uma marca predefinida do Azure com um valor predefinido opcional.</span><span class="sxs-lookup"><span data-stu-id="aa74c-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="aa74c-107">Você também pode usá-lo para adicionar valores adicionais a marcas predefinidas existentes.</span><span class="sxs-lookup"><span data-stu-id="aa74c-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="aa74c-108">Para criar uma marca predefinida, insira um nome exclusivo para a marca.</span><span class="sxs-lookup"><span data-stu-id="aa74c-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="aa74c-109">Para adicionar um valor a uma marca predefinida existente, especifique o nome da marca existente e o novo valor.</span><span class="sxs-lookup"><span data-stu-id="aa74c-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>

<span data-ttu-id="aa74c-110">Esse cmdlet retorna um objeto que representa a marca nova ou modificada com seus valores e o número de recursos aos quais ele foi aplicado.</span><span class="sxs-lookup"><span data-stu-id="aa74c-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>

<span data-ttu-id="aa74c-111">O módulo de marcas do Azure que **New-AzureRmTag** faz parte do pode ajudá-lo a gerenciar marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="aa74c-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="aa74c-112">Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="aa74c-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="aa74c-113">Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="aa74c-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="aa74c-114">Se a assinatura incluir marcas predefinidas, não será possível aplicar marcas ou valores indefinidos a nenhum recurso ou grupo de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="aa74c-114">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="aa74c-115">Para aplicar uma marca predefinida a um recurso ou grupo de recursos, use o parâmetro *tag* do cmdlet New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="aa74c-115">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="aa74c-116">Para pesquisar grupos de recursos com um nome de marca ou nome ou valor especificado, use o parâmetro *tag* do cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="aa74c-116">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

<span data-ttu-id="aa74c-117">Cada marca tem um nome.</span><span class="sxs-lookup"><span data-stu-id="aa74c-117">Every tag has a name.</span></span>
<span data-ttu-id="aa74c-118">Os valores são opcionais.</span><span class="sxs-lookup"><span data-stu-id="aa74c-118">The values are optional.</span></span>
<span data-ttu-id="aa74c-119">Uma marca predefinida do Azure pode ter vários valores, mas quando você aplica a marca a um recurso ou grupo de recursos, aplica o nome da marca e somente um de seus valores.</span><span class="sxs-lookup"><span data-stu-id="aa74c-119">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="aa74c-120">Por exemplo, você pode criar uma marca de departamento predefinida com um valor para cada departamento, como finanças, recursos humanos e isso.</span><span class="sxs-lookup"><span data-stu-id="aa74c-120">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="aa74c-121">Ao aplicar a marca de departamento a um recurso, você aplica apenas um valor predefinido, como finanças.</span><span class="sxs-lookup"><span data-stu-id="aa74c-121">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="aa74c-122">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa74c-122">EXAMPLES</span></span>

### <span data-ttu-id="aa74c-123">Exemplo 1: criar uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="aa74c-123">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="aa74c-124">Esse comando cria uma marca predefinida chamada FY2015.</span><span class="sxs-lookup"><span data-stu-id="aa74c-124">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="aa74c-125">Esta marca não tem valores.</span><span class="sxs-lookup"><span data-stu-id="aa74c-125">This tag has no values.</span></span>
<span data-ttu-id="aa74c-126">Você pode aplicar uma marca sem valores a um recurso ou grupo de recursos ou usar **New-AzureRmTag** para adicionar valores à marca.</span><span class="sxs-lookup"><span data-stu-id="aa74c-126">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="aa74c-127">Você também pode especificar um valor ao aplicar a marca ao recurso ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa74c-127">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="aa74c-128">Exemplo 2: criar uma marca predefinida com um valor</span><span class="sxs-lookup"><span data-stu-id="aa74c-128">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="aa74c-129">Esse comando cria uma marca predefinida chamada Department com um valor de Finance.</span><span class="sxs-lookup"><span data-stu-id="aa74c-129">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="aa74c-130">Exemplo 3: adicionar um valor a uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="aa74c-130">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="aa74c-131">Esses comandos criam uma marca predefinida chamada Department com dois valores.</span><span class="sxs-lookup"><span data-stu-id="aa74c-131">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="aa74c-132">Se o nome da marca existir, **New-AzureRmTag** adiciona o valor à marca existente, em vez de criar uma nova.</span><span class="sxs-lookup"><span data-stu-id="aa74c-132">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="aa74c-133">Exemplo 4: usar uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="aa74c-133">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

<span data-ttu-id="aa74c-134">Os comandos neste exemplo criam e usam uma marca predefinida.</span><span class="sxs-lookup"><span data-stu-id="aa74c-134">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="aa74c-135">OS</span><span class="sxs-lookup"><span data-stu-id="aa74c-135">PARAMETERS</span></span>

### <span data-ttu-id="aa74c-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa74c-136">-Name</span></span>
<span data-ttu-id="aa74c-137">Especifica o nome da marca.</span><span class="sxs-lookup"><span data-stu-id="aa74c-137">Specifies the tag name.</span></span>
<span data-ttu-id="aa74c-138">Para criar uma nova marca predefinida, insira um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="aa74c-138">To create a new predefined tag, enter a unique name.</span></span>

<span data-ttu-id="aa74c-139">Para adicionar um valor a uma marca existente, insira o nome da marca existente.</span><span class="sxs-lookup"><span data-stu-id="aa74c-139">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="aa74c-140">Se uma marca predefinida existente tiver o nome especificado, **New-AzureRmTag** adicionará o valor especificado, se houver, à marca com esse nome em vez de criar uma nova marca.</span><span class="sxs-lookup"><span data-stu-id="aa74c-140">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="aa74c-141">-Valor</span><span class="sxs-lookup"><span data-stu-id="aa74c-141">-Value</span></span>
<span data-ttu-id="aa74c-142">Especifica um valor de marca.</span><span class="sxs-lookup"><span data-stu-id="aa74c-142">Specifies a tag value.</span></span>
<span data-ttu-id="aa74c-143">Marcas predefinidas podem ter vários valores, mas você pode inserir apenas um valor em cada comando.</span><span class="sxs-lookup"><span data-stu-id="aa74c-143">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="aa74c-144">Esse parâmetro é opcional, pois as marcas podem ter nomes sem valores.</span><span class="sxs-lookup"><span data-stu-id="aa74c-144">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="aa74c-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa74c-145">-DefaultProfile</span></span>
<span data-ttu-id="aa74c-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa74c-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa74c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa74c-147">CommonParameters</span></span>
<span data-ttu-id="aa74c-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa74c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa74c-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa74c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa74c-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa74c-150">INPUTS</span></span>

### <span data-ttu-id="aa74c-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="aa74c-151">None</span></span>

## <span data-ttu-id="aa74c-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa74c-152">OUTPUTS</span></span>

### <span data-ttu-id="aa74c-153">Microsoft. Azure. Commands. Tags. Model. PSTag</span><span class="sxs-lookup"><span data-stu-id="aa74c-153">Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="aa74c-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa74c-154">NOTES</span></span>

## <span data-ttu-id="aa74c-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa74c-155">RELATED LINKS</span></span>

[<span data-ttu-id="aa74c-156">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="aa74c-156">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="aa74c-157">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="aa74c-157">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


