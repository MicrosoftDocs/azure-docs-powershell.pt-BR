---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: cd9700a633f1a9c09c5fafd060d318b35eaeaabb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440704"
---
# <span data-ttu-id="4b608-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="4b608-101">New-AzureRmTag</span></span>

## <span data-ttu-id="4b608-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b608-102">SYNOPSIS</span></span>
<span data-ttu-id="4b608-103">Cria uma marca predefinida do Azure ou adiciona valores a uma marca existente.</span><span class="sxs-lookup"><span data-stu-id="4b608-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b608-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b608-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b608-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b608-105">DESCRIPTION</span></span>
<span data-ttu-id="4b608-106">O cmdlet **New-AzureRmTag** cria uma marca predefinida do Azure com um valor predefinido opcional.</span><span class="sxs-lookup"><span data-stu-id="4b608-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="4b608-107">Você também pode usá-lo para adicionar valores adicionais a marcas predefinidas existentes.</span><span class="sxs-lookup"><span data-stu-id="4b608-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="4b608-108">Para criar uma marca predefinida, insira um nome exclusivo para a marca.</span><span class="sxs-lookup"><span data-stu-id="4b608-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="4b608-109">Para adicionar um valor a uma marca predefinida existente, especifique o nome da marca existente e o novo valor.</span><span class="sxs-lookup"><span data-stu-id="4b608-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="4b608-110">Esse cmdlet retorna um objeto que representa a marca nova ou modificada com seus valores e o número de recursos aos quais ele foi aplicado.</span><span class="sxs-lookup"><span data-stu-id="4b608-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="4b608-111">O módulo de marcas do Azure que **New-AzureRmTag** faz parte do pode ajudá-lo a gerenciar marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b608-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="4b608-112">Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="4b608-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="4b608-113">Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="4b608-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="4b608-114">Para aplicar uma marca predefinida a um recurso ou grupo de recursos, use o parâmetro *tag* do cmdlet New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="4b608-114">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="4b608-115">Para pesquisar grupos de recursos com um nome de marca ou nome ou valor especificado, use o parâmetro *tag* do cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4b608-115">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="4b608-116">Cada marca tem um nome.</span><span class="sxs-lookup"><span data-stu-id="4b608-116">Every tag has a name.</span></span>
<span data-ttu-id="4b608-117">Os valores são opcionais.</span><span class="sxs-lookup"><span data-stu-id="4b608-117">The values are optional.</span></span>
<span data-ttu-id="4b608-118">Uma marca predefinida do Azure pode ter vários valores, mas quando você aplica a marca a um recurso ou grupo de recursos, aplica o nome da marca e somente um de seus valores.</span><span class="sxs-lookup"><span data-stu-id="4b608-118">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="4b608-119">Por exemplo, você pode criar uma marca de departamento predefinida com um valor para cada departamento, como finanças, recursos humanos e isso.</span><span class="sxs-lookup"><span data-stu-id="4b608-119">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="4b608-120">Ao aplicar a marca de departamento a um recurso, você aplica apenas um valor predefinido, como finanças.</span><span class="sxs-lookup"><span data-stu-id="4b608-120">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="4b608-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b608-121">EXAMPLES</span></span>

### <span data-ttu-id="4b608-122">Exemplo 1: criar uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="4b608-122">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   FY2015
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="4b608-123">Esse comando cria uma marca predefinida chamada FY2015.</span><span class="sxs-lookup"><span data-stu-id="4b608-123">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="4b608-124">Esta marca não tem valores.</span><span class="sxs-lookup"><span data-stu-id="4b608-124">This tag has no values.</span></span>
<span data-ttu-id="4b608-125">Você pode aplicar uma marca sem valores a um recurso ou grupo de recursos ou usar **New-AzureRmTag** para adicionar valores à marca.</span><span class="sxs-lookup"><span data-stu-id="4b608-125">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="4b608-126">Você também pode especificar um valor ao aplicar a marca ao recurso ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b608-126">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="4b608-127">Exemplo 2: criar uma marca predefinida com um valor</span><span class="sxs-lookup"><span data-stu-id="4b608-127">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="4b608-128">Esse comando cria uma marca predefinida chamada Department com um valor de Finance.</span><span class="sxs-lookup"><span data-stu-id="4b608-128">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="4b608-129">Exemplo 3: adicionar um valor a uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="4b608-129">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="4b608-130">Esses comandos criam uma marca predefinida chamada Department com dois valores.</span><span class="sxs-lookup"><span data-stu-id="4b608-130">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="4b608-131">Se o nome da marca existir, **New-AzureRmTag** adiciona o valor à marca existente, em vez de criar uma nova.</span><span class="sxs-lookup"><span data-stu-id="4b608-131">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="4b608-132">Exemplo 4: usar uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="4b608-132">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

<span data-ttu-id="4b608-133">Os comandos neste exemplo criam e usam uma marca predefinida.</span><span class="sxs-lookup"><span data-stu-id="4b608-133">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="4b608-134">OS</span><span class="sxs-lookup"><span data-stu-id="4b608-134">PARAMETERS</span></span>

### <span data-ttu-id="4b608-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b608-135">-DefaultProfile</span></span>
<span data-ttu-id="4b608-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b608-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b608-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b608-137">-Name</span></span>
<span data-ttu-id="4b608-138">Especifica o nome da marca.</span><span class="sxs-lookup"><span data-stu-id="4b608-138">Specifies the tag name.</span></span>
<span data-ttu-id="4b608-139">Para criar uma nova marca predefinida, insira um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="4b608-139">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="4b608-140">Para adicionar um valor a uma marca existente, insira o nome da marca existente.</span><span class="sxs-lookup"><span data-stu-id="4b608-140">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="4b608-141">Se uma marca predefinida existente tiver o nome especificado, **New-AzureRmTag** adicionará o valor especificado, se houver, à marca com esse nome em vez de criar uma nova marca.</span><span class="sxs-lookup"><span data-stu-id="4b608-141">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="4b608-142">-Valor</span><span class="sxs-lookup"><span data-stu-id="4b608-142">-Value</span></span>
<span data-ttu-id="4b608-143">Especifica um valor de marca.</span><span class="sxs-lookup"><span data-stu-id="4b608-143">Specifies a tag value.</span></span>
<span data-ttu-id="4b608-144">Marcas predefinidas podem ter vários valores, mas você pode inserir apenas um valor em cada comando.</span><span class="sxs-lookup"><span data-stu-id="4b608-144">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="4b608-145">Esse parâmetro é opcional, pois as marcas podem ter nomes sem valores.</span><span class="sxs-lookup"><span data-stu-id="4b608-145">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="4b608-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b608-146">CommonParameters</span></span>
<span data-ttu-id="4b608-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b608-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b608-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b608-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b608-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b608-149">INPUTS</span></span>

### <span data-ttu-id="4b608-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4b608-150">System.String</span></span>

## <span data-ttu-id="4b608-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b608-151">OUTPUTS</span></span>

### <span data-ttu-id="4b608-152">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="4b608-152">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="4b608-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b608-153">NOTES</span></span>

## <span data-ttu-id="4b608-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b608-154">RELATED LINKS</span></span>

[<span data-ttu-id="4b608-155">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="4b608-155">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="4b608-156">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="4b608-156">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


