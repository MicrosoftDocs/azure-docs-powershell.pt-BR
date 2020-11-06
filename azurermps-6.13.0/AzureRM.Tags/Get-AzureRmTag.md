---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 945af88df11e210c3af3a11bd69123dd32befe4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440705"
---
# <span data-ttu-id="d9acf-101">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="d9acf-101">Get-AzureRmTag</span></span>

## <span data-ttu-id="d9acf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9acf-102">SYNOPSIS</span></span>
<span data-ttu-id="d9acf-103">Obtém marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9acf-103">Gets predefined Azure tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9acf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9acf-104">SYNTAX</span></span>

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9acf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9acf-105">DESCRIPTION</span></span>
<span data-ttu-id="d9acf-106">O cmdlet **Get-AzureRmTag** tem marcas predefinidas do Azure na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="d9acf-106">The **Get-AzureRmTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="d9acf-107">Esse cmdlet retorna informações básicas sobre as marcas ou informações detalhadas sobre marcas e seus valores.</span><span class="sxs-lookup"><span data-stu-id="d9acf-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="d9acf-108">Todos os objetos de saída incluem uma propriedade Count que representa o número de recursos e grupos de recursos aos quais as marcas e os valores foram aplicados.</span><span class="sxs-lookup"><span data-stu-id="d9acf-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="d9acf-109">O módulo de marcas do Azure que **Get-AzureRMTag** é parte de pode ajudá-lo a gerenciar marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9acf-109">The Azure Tags module that **Get-AzureRMTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="d9acf-110">Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="d9acf-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="d9acf-111">Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="d9acf-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="d9acf-112">Para criar uma marca predefinida, use o cmdlet New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="d9acf-112">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="d9acf-113">Para aplicar uma marca predefinida a um grupo de recursos, use o parâmetro *tag* do cmdlet New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="d9acf-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="d9acf-114">Para pesquisar grupos de recursos para um nome de marca ou nome ou valor específico, use o parâmetro *tag* do cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d9acf-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

## <span data-ttu-id="d9acf-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9acf-115">EXAMPLES</span></span>

### <span data-ttu-id="d9acf-116">Exemplo 1: obter todas as marcas predefinidas</span><span class="sxs-lookup"><span data-stu-id="d9acf-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="d9acf-117">Este comando obtém todas as marcas predefinidas na assinatura.</span><span class="sxs-lookup"><span data-stu-id="d9acf-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="d9acf-118">A propriedade Count mostra quantas vezes a marca foi aplicada a recursos e grupos de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="d9acf-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="d9acf-119">Exemplo 2: obter uma marca por nome</span><span class="sxs-lookup"><span data-stu-id="d9acf-119">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="d9acf-120">Esse comando obtém informações detalhadas sobre a marca do departamento e seus valores.</span><span class="sxs-lookup"><span data-stu-id="d9acf-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="d9acf-121">A propriedade Count mostra quantas vezes a marca e cada um dos seus valores foram aplicados a recursos e grupos de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="d9acf-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="d9acf-122">Exemplo 3: obter valores de todas as marcas</span><span class="sxs-lookup"><span data-stu-id="d9acf-122">Example 3: Get values of all tags</span></span>
```
PS C:\>Get-AzureRmTag -Detailed

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

<span data-ttu-id="d9acf-123">Esse comando usa o parâmetro *detalhado* para obter informações detalhadas sobre todas as marcas predefinidas na assinatura.</span><span class="sxs-lookup"><span data-stu-id="d9acf-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="d9acf-124">Usar o parâmetro *detailed* é o equivalente a usar o parâmetro *Name* para cada marca.</span><span class="sxs-lookup"><span data-stu-id="d9acf-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="d9acf-125">OS</span><span class="sxs-lookup"><span data-stu-id="d9acf-125">PARAMETERS</span></span>

### <span data-ttu-id="d9acf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9acf-126">-DefaultProfile</span></span>
<span data-ttu-id="d9acf-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9acf-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9acf-128">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="d9acf-128">-Detailed</span></span>
<span data-ttu-id="d9acf-129">Indica que essa operação adiciona informações sobre valores de marca à saída.</span><span class="sxs-lookup"><span data-stu-id="d9acf-129">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="d9acf-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9acf-130">-Name</span></span>
<span data-ttu-id="d9acf-131">Especifica o nome da marca a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="d9acf-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="d9acf-132">Por padrão, **Get-AzureRmTag** Obtém informações básicas sobre todas as marcas predefinidas na assinatura.</span><span class="sxs-lookup"><span data-stu-id="d9acf-132">By default, **Get-AzureRmTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="d9acf-133">Quando você especifica o parâmetro *Name* , o parâmetro *detalhado* não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="d9acf-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="d9acf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9acf-134">CommonParameters</span></span>
<span data-ttu-id="d9acf-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9acf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9acf-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9acf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9acf-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9acf-137">INPUTS</span></span>

### <span data-ttu-id="d9acf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d9acf-138">System.String</span></span>

### <span data-ttu-id="d9acf-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d9acf-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d9acf-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9acf-140">OUTPUTS</span></span>

### <span data-ttu-id="d9acf-141">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="d9acf-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="d9acf-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9acf-142">NOTES</span></span>

## <span data-ttu-id="d9acf-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9acf-143">RELATED LINKS</span></span>

[<span data-ttu-id="d9acf-144">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="d9acf-144">New-AzureRmTag</span></span>](./New-AzureRmTag.md)

[<span data-ttu-id="d9acf-145">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="d9acf-145">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


