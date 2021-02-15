---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118136"
---
# <span data-ttu-id="c33cc-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="c33cc-101">Get-AzTag</span></span>

## <span data-ttu-id="c33cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c33cc-102">SYNOPSIS</span></span>
<span data-ttu-id="c33cc-103">Obtém marcas predefinidas do Azure | Obtém todo o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="c33cc-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="c33cc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c33cc-104">SYNTAX</span></span>

### <span data-ttu-id="c33cc-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="c33cc-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c33cc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c33cc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c33cc-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c33cc-107">DESCRIPTION</span></span>

<span data-ttu-id="c33cc-108">**GetPredefinedTagSet:** o cmdlet **Get-AzTag** recebe marcas predefinidas do Azure em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="c33cc-108">**GetPredefinedTagSet**: The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="c33cc-109">Este cmdlet retorna informações básicas sobre as marcas ou informações detalhadas sobre marcas e seus valores.</span><span class="sxs-lookup"><span data-stu-id="c33cc-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="c33cc-110">Todos os objetos de saída incluem uma propriedade Count que representa o número de recursos e grupos de recursos aos quais as marcas e valores foram aplicados.</span><span class="sxs-lookup"><span data-stu-id="c33cc-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="c33cc-111">O módulo Marcas do Azure do **que Get-AzTag** faz parte pode ajudá-lo a gerenciar marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="c33cc-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="c33cc-112">Uma marca do Azure é um par de valores de nome que você pode usar para categorizar seus recursos e grupos de recursos do Azure, como por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="c33cc-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="c33cc-113">Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinida permitem estabelecer nomes e valores padrão, consistentes e previsíveis para as marcas em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="c33cc-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="c33cc-114">Para criar uma marca predefinida, use New-AzTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c33cc-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="c33cc-115">Para aplicar uma marca predefinida a um grupo de recursos, use o parâmetro *Tag* do cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="c33cc-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="c33cc-116">Para pesquisar em grupos de recursos um nome  ou nome e um valor de marca específicos, use o parâmetro Tag do cmdlet Get-AzResourceGroup dados.</span><span class="sxs-lookup"><span data-stu-id="c33cc-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="c33cc-117">**GetByResourceIdParameterSet:** o cmdlet **Get-AzTag** com **um ResourceId** obtém todo o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="c33cc-117">**GetByResourceIdParameterSet**: The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="c33cc-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c33cc-118">EXAMPLES</span></span>

### <span data-ttu-id="c33cc-119">Exemplo 1: Obter todas as marcas predefinidos</span><span class="sxs-lookup"><span data-stu-id="c33cc-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="c33cc-120">Esse comando obtém todas as marcas predefinida na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c33cc-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="c33cc-121">A propriedade Count mostra quantas vezes a marca foi aplicada aos recursos e grupos de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c33cc-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="c33cc-122">Exemplo 2: Obter uma marca por nome</span><span class="sxs-lookup"><span data-stu-id="c33cc-122">Example 2: Get a tag by name</span></span>
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

<span data-ttu-id="c33cc-123">Este comando obtém informações detalhadas sobre a marca Departamento e seus valores.</span><span class="sxs-lookup"><span data-stu-id="c33cc-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="c33cc-124">A propriedade Count mostra quantas vezes a marca e cada um de seus valores foi aplicado a recursos e grupos de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c33cc-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="c33cc-125">Exemplo 3: Obter valores de todas as marcas</span><span class="sxs-lookup"><span data-stu-id="c33cc-125">Example 3: Get values of all tags</span></span>
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

<span data-ttu-id="c33cc-126">Esse comando usa o *parâmetro Detalhado* para obter informações detalhadas sobre todas as marcas predefinida na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c33cc-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="c33cc-127">Usar o *parâmetro Detalhado* equivale a usar o parâmetro *Nome* para cada marca.</span><span class="sxs-lookup"><span data-stu-id="c33cc-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="c33cc-128">Exemplo 4: Obter todo o conjunto de marcas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="c33cc-128">Example 4: Get the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="c33cc-129">Esse comando obtém todo o conjunto de marcas na assinatura com {subId}.</span><span class="sxs-lookup"><span data-stu-id="c33cc-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="c33cc-130">Exemplo 5: Obter todo o conjunto de marcas em um recurso</span><span class="sxs-lookup"><span data-stu-id="c33cc-130">Example 5: Get the entire set of tags on a resource</span></span>

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

<span data-ttu-id="c33cc-131">Esse comando obtém todo o conjunto de marcas no recurso com {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="c33cc-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="c33cc-132">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c33cc-132">PARAMETERS</span></span>

### <span data-ttu-id="c33cc-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c33cc-133">-DefaultProfile</span></span>
<span data-ttu-id="c33cc-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c33cc-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c33cc-135">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="c33cc-135">-Detailed</span></span>
<span data-ttu-id="c33cc-136">Indica que essa operação adiciona informações sobre valores de marca à saída.</span><span class="sxs-lookup"><span data-stu-id="c33cc-136">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="c33cc-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="c33cc-137">-Name</span></span>
<span data-ttu-id="c33cc-138">Nome da marca predefinida.</span><span class="sxs-lookup"><span data-stu-id="c33cc-138">Name of the predefined tag.</span></span>
<span data-ttu-id="c33cc-139">Por padrão, **o Get-AzTag** obtém informações básicas sobre todas as marcas predefinida na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c33cc-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="c33cc-140">Quando você especifica o *parâmetro Nome,* o *parâmetro* Detalhado não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="c33cc-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="c33cc-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c33cc-141">-ResourceId</span></span>
<span data-ttu-id="c33cc-142">O identificador de recurso da entidade marcada.</span><span class="sxs-lookup"><span data-stu-id="c33cc-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="c33cc-143">Um recurso, um grupo de recursos ou uma assinatura podem ser marcados.</span><span class="sxs-lookup"><span data-stu-id="c33cc-143">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="c33cc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33cc-144">CommonParameters</span></span>
<span data-ttu-id="c33cc-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c33cc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33cc-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c33cc-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33cc-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="c33cc-147">INPUTS</span></span>

### <span data-ttu-id="c33cc-148">System.String</span><span class="sxs-lookup"><span data-stu-id="c33cc-148">System.String</span></span>

### <span data-ttu-id="c33cc-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c33cc-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c33cc-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="c33cc-150">OUTPUTS</span></span>

### <span data-ttu-id="c33cc-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="c33cc-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="c33cc-152">Notas</span><span class="sxs-lookup"><span data-stu-id="c33cc-152">NOTES</span></span>

## <span data-ttu-id="c33cc-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c33cc-153">RELATED LINKS</span></span>

[<span data-ttu-id="c33cc-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="c33cc-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="c33cc-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="c33cc-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="c33cc-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="c33cc-156">Update-AzTag</span></span>](./Update-AzTag.md)
