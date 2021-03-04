---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: b44c861e06c1043fd53e470cfba1e322ce1f1f48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890586"
---
# <span data-ttu-id="858f0-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="858f0-101">Get-AzTag</span></span>

## <span data-ttu-id="858f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="858f0-102">SYNOPSIS</span></span>
<span data-ttu-id="858f0-103">Obtém marcas predefinidas do Azure | Obtém todo o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="858f0-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="858f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="858f0-104">SYNTAX</span></span>

### <span data-ttu-id="858f0-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="858f0-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="858f0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="858f0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="858f0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="858f0-107">DESCRIPTION</span></span>

<span data-ttu-id="858f0-108">**GetPredefinedTagSet**: o cmdlet **Get-AzTag** obtém marcas predefinidas do Azure em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="858f0-108">**GetPredefinedTagSet**: The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="858f0-109">Este cmdlet retorna informações básicas sobre as marcas ou informações detalhadas sobre marcas e seus valores.</span><span class="sxs-lookup"><span data-stu-id="858f0-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="858f0-110">Todos os objetos de saída incluem uma propriedade Count que representa o número de recursos e grupos de recursos aos quais as marcas e valores foram aplicados.</span><span class="sxs-lookup"><span data-stu-id="858f0-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="858f0-111">O módulo Marcas do Azure do que **Get-AzTag** faz parte pode ajudá-lo a gerenciar marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="858f0-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="858f0-112">Uma marca do Azure é um par de valores de nome que você pode usar para categorizar seus recursos e grupos de recursos do Azure, como departamento ou centro de custo, ou para acompanhar observações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="858f0-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="858f0-113">Você pode definir e aplicar marcas em uma única etapa, mas marcas predefinida permitem estabelecer nomes e valores padrão, consistentes e previsíveis para as marcas em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="858f0-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="858f0-114">Para criar uma marca predefinida, use New-AzTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="858f0-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="858f0-115">Para aplicar uma marca predefinida a um grupo de recursos, use o parâmetro *Tag* do cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="858f0-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="858f0-116">Para pesquisar grupos de recursos para um nome ou nome e um valor específicos de marca, use o parâmetro *Tag* do cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="858f0-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="858f0-117">**GetByResourceIdParameterSet**: o cmdlet **Get-AzTag** com **um ResourceId** obtém todo o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="858f0-117">**GetByResourceIdParameterSet**: The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="858f0-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="858f0-118">EXAMPLES</span></span>

### <span data-ttu-id="858f0-119">Exemplo 1: Obter todas as marcas predefinida</span><span class="sxs-lookup"><span data-stu-id="858f0-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="858f0-120">Este comando obtém todas as marcas predefinida na assinatura.</span><span class="sxs-lookup"><span data-stu-id="858f0-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="858f0-121">A propriedade Count mostra quantas vezes a marca foi aplicada a recursos e grupos de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="858f0-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="858f0-122">Exemplo 2: Obter uma marca por nome</span><span class="sxs-lookup"><span data-stu-id="858f0-122">Example 2: Get a tag by name</span></span>
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="858f0-123">Este comando obtém informações detalhadas sobre a marca Department e seus valores.</span><span class="sxs-lookup"><span data-stu-id="858f0-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="858f0-124">A propriedade Count mostra quantas vezes a marca e cada um de seus valores foi aplicado a recursos e grupos de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="858f0-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="858f0-125">Exemplo 3: Obter valores de todas as marcas</span><span class="sxs-lookup"><span data-stu-id="858f0-125">Example 3: Get values of all tags</span></span>
```powershell
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

<span data-ttu-id="858f0-126">Este comando usa o *parâmetro Detailed* para obter informações detalhadas sobre todas as marcas predefinida na assinatura.</span><span class="sxs-lookup"><span data-stu-id="858f0-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="858f0-127">Usar o *parâmetro Detailed* equivale a usar o parâmetro *Name* para cada marca.</span><span class="sxs-lookup"><span data-stu-id="858f0-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="858f0-128">Exemplo 4: Obter todo o conjunto de marcas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="858f0-128">Example 4: Get the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="858f0-129">Este comando obtém todo o conjunto de marcas na assinatura com {subId}.</span><span class="sxs-lookup"><span data-stu-id="858f0-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="858f0-130">Exemplo 5: Obter todo o conjunto de marcas em um recurso</span><span class="sxs-lookup"><span data-stu-id="858f0-130">Example 5: Get the entire set of tags on a resource</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="858f0-131">Este comando obtém todo o conjunto de marcas no recurso com {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="858f0-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="858f0-132">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="858f0-132">PARAMETERS</span></span>

### <span data-ttu-id="858f0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858f0-133">-DefaultProfile</span></span>
<span data-ttu-id="858f0-134">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="858f0-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="858f0-135">-Detailed</span><span class="sxs-lookup"><span data-stu-id="858f0-135">-Detailed</span></span>
<span data-ttu-id="858f0-136">Indica que essa operação adiciona informações sobre valores de marca à saída.</span><span class="sxs-lookup"><span data-stu-id="858f0-136">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858f0-137">-Name</span><span class="sxs-lookup"><span data-stu-id="858f0-137">-Name</span></span>
<span data-ttu-id="858f0-138">Nome da marca predefinida.</span><span class="sxs-lookup"><span data-stu-id="858f0-138">Name of the predefined tag.</span></span>
<span data-ttu-id="858f0-139">Por padrão, **Get-AzTag** obtém informações básicas sobre todas as marcas predefinida na assinatura.</span><span class="sxs-lookup"><span data-stu-id="858f0-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="858f0-140">Quando você especifica o *parâmetro Name,* o *parâmetro Detailed* não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="858f0-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858f0-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="858f0-141">-ResourceId</span></span>
<span data-ttu-id="858f0-142">O identificador de recurso da entidade marcada.</span><span class="sxs-lookup"><span data-stu-id="858f0-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="858f0-143">Um recurso, um grupo de recursos ou uma assinatura podem ser marcados.</span><span class="sxs-lookup"><span data-stu-id="858f0-143">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858f0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858f0-144">CommonParameters</span></span>
<span data-ttu-id="858f0-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="858f0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858f0-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="858f0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858f0-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="858f0-147">INPUTS</span></span>

### <span data-ttu-id="858f0-148">System.String</span><span class="sxs-lookup"><span data-stu-id="858f0-148">System.String</span></span>

### <span data-ttu-id="858f0-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="858f0-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="858f0-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="858f0-150">OUTPUTS</span></span>

### <span data-ttu-id="858f0-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="858f0-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="858f0-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="858f0-152">NOTES</span></span>

## <span data-ttu-id="858f0-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="858f0-153">RELATED LINKS</span></span>

[<span data-ttu-id="858f0-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="858f0-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="858f0-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="858f0-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="858f0-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="858f0-156">Update-AzTag</span></span>](./Update-AzTag.md)
