---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 1f2289351da276a0422828c082bb51d8dc267a20
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776417"
---
# <span data-ttu-id="7b50c-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="7b50c-101">Get-AzTag</span></span>

## <span data-ttu-id="7b50c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b50c-102">SYNOPSIS</span></span>
<span data-ttu-id="7b50c-103">Obtém marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b50c-103">Gets predefined Azure tags.</span></span>

## <span data-ttu-id="7b50c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b50c-104">SYNTAX</span></span>

```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b50c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b50c-105">DESCRIPTION</span></span>
<span data-ttu-id="7b50c-106">O cmdlet **Get-AzTag** tem marcas predefinidas do Azure na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="7b50c-106">The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="7b50c-107">Esse cmdlet retorna informações básicas sobre as marcas ou informações detalhadas sobre marcas e seus valores.</span><span class="sxs-lookup"><span data-stu-id="7b50c-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="7b50c-108">Todos os objetos de saída incluem uma propriedade Count que representa o número de recursos e grupos de recursos aos quais as marcas e os valores foram aplicados.</span><span class="sxs-lookup"><span data-stu-id="7b50c-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="7b50c-109">O módulo de marcas do Azure que **Get-AzTag** é parte de pode ajudá-lo a gerenciar marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b50c-109">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="7b50c-110">Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="7b50c-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="7b50c-111">Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="7b50c-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="7b50c-112">Para criar uma marca predefinida, use o cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="7b50c-112">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="7b50c-113">Para aplicar uma marca predefinida a um grupo de recursos, use o parâmetro *tag* do cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="7b50c-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="7b50c-114">Para pesquisar grupos de recursos para um nome de marca ou nome ou valor específico, use o parâmetro *tag* do cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7b50c-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="7b50c-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b50c-115">EXAMPLES</span></span>

### <span data-ttu-id="7b50c-116">Exemplo 1: obter todas as marcas predefinidas</span><span class="sxs-lookup"><span data-stu-id="7b50c-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="7b50c-117">Este comando obtém todas as marcas predefinidas na assinatura.</span><span class="sxs-lookup"><span data-stu-id="7b50c-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="7b50c-118">A propriedade Count mostra quantas vezes a marca foi aplicada a recursos e grupos de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="7b50c-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="7b50c-119">Exemplo 2: obter uma marca por nome</span><span class="sxs-lookup"><span data-stu-id="7b50c-119">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="7b50c-120">Esse comando obtém informações detalhadas sobre a marca do departamento e seus valores.</span><span class="sxs-lookup"><span data-stu-id="7b50c-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="7b50c-121">A propriedade Count mostra quantas vezes a marca e cada um dos seus valores foram aplicados a recursos e grupos de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="7b50c-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="7b50c-122">Exemplo 3: obter valores de todas as marcas</span><span class="sxs-lookup"><span data-stu-id="7b50c-122">Example 3: Get values of all tags</span></span>
```
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

<span data-ttu-id="7b50c-123">Esse comando usa o parâmetro *detalhado* para obter informações detalhadas sobre todas as marcas predefinidas na assinatura.</span><span class="sxs-lookup"><span data-stu-id="7b50c-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="7b50c-124">Usar o parâmetro *detailed* é o equivalente a usar o parâmetro *Name* para cada marca.</span><span class="sxs-lookup"><span data-stu-id="7b50c-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="7b50c-125">OS</span><span class="sxs-lookup"><span data-stu-id="7b50c-125">PARAMETERS</span></span>

### <span data-ttu-id="7b50c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b50c-126">-DefaultProfile</span></span>
<span data-ttu-id="7b50c-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b50c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b50c-128">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="7b50c-128">-Detailed</span></span>
<span data-ttu-id="7b50c-129">Indica que essa operação adiciona informações sobre valores de marca à saída.</span><span class="sxs-lookup"><span data-stu-id="7b50c-129">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="7b50c-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b50c-130">-Name</span></span>
<span data-ttu-id="7b50c-131">Especifica o nome da marca a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="7b50c-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="7b50c-132">Por padrão, **Get-AzTag** Obtém informações básicas sobre todas as marcas predefinidas na assinatura.</span><span class="sxs-lookup"><span data-stu-id="7b50c-132">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="7b50c-133">Quando você especifica o parâmetro *Name* , o parâmetro *detalhado* não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="7b50c-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b50c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b50c-134">CommonParameters</span></span>
<span data-ttu-id="7b50c-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b50c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b50c-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b50c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b50c-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b50c-137">INPUTS</span></span>

### <span data-ttu-id="7b50c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7b50c-138">System.String</span></span>

### <span data-ttu-id="7b50c-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7b50c-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7b50c-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b50c-140">OUTPUTS</span></span>

### <span data-ttu-id="7b50c-141">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="7b50c-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="7b50c-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b50c-142">NOTES</span></span>

## <span data-ttu-id="7b50c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b50c-143">RELATED LINKS</span></span>

[<span data-ttu-id="7b50c-144">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="7b50c-144">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="7b50c-145">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="7b50c-145">Remove-AzTag</span></span>](./Remove-AzTag.md)

