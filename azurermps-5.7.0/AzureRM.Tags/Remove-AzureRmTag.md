---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/remove-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: f51411c4683a79283ad5e0a73554f6db3ce7e52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602000"
---
# <span data-ttu-id="948ee-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="948ee-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="948ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="948ee-102">SYNOPSIS</span></span>
<span data-ttu-id="948ee-103">Exclui valores ou marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="948ee-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="948ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="948ee-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="948ee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="948ee-105">DESCRIPTION</span></span>
<span data-ttu-id="948ee-106">O cmdlet **Remove-AzureRmTag** exclui as marcas e os valores predefinidos do Azure de sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="948ee-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="948ee-107">Para excluir valores específicos de uma marca predefinida, use o parâmetro *Value* .</span><span class="sxs-lookup"><span data-stu-id="948ee-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="948ee-108">Por padrão, **Remove-AzureRmTag** exclui a marca especificada e todos os seus valores. Não é possível excluir uma marca ou um valor que seja aplicado no momento a um recurso ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="948ee-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>

<span data-ttu-id="948ee-109">Antes de usar **Remove-AzureRmTag** , use o parâmetro *Tag* do cmdlet Set-AzureRMResourceGroup para excluir a marca ou os valores do recurso ou do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="948ee-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>

<span data-ttu-id="948ee-110">O módulo de marcas do Azure que **Remove-AzureRmTag** faz parte do pode ajudá-lo a gerenciar suas marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="948ee-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="948ee-111">Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="948ee-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="948ee-112">Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="948ee-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="948ee-113">Se a assinatura incluir marcas predefinidas, não será possível aplicar marcas ou valores indefinidos a nenhum recurso ou grupo de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="948ee-113">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

## <span data-ttu-id="948ee-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="948ee-114">EXAMPLES</span></span>

### <span data-ttu-id="948ee-115">Exemplo 1: excluir uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="948ee-115">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="948ee-116">Este comando exclui a marca predefinida chamada Department e todos os seus recursos.</span><span class="sxs-lookup"><span data-stu-id="948ee-116">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="948ee-117">Se a marca tiver sido aplicada a recursos ou grupos de recursos, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="948ee-117">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="948ee-118">Exemplo 2: excluir um valor de uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="948ee-118">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="948ee-119">Esse comando exclui o valor HumanResources da marca de departamento predefinida.</span><span class="sxs-lookup"><span data-stu-id="948ee-119">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="948ee-120">Ele não exclui a marca.</span><span class="sxs-lookup"><span data-stu-id="948ee-120">It does not delete the tag.</span></span>
<span data-ttu-id="948ee-121">Se o valor tiver sido aplicado a recursos ou grupos de recursos, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="948ee-121">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="948ee-122">OS</span><span class="sxs-lookup"><span data-stu-id="948ee-122">PARAMETERS</span></span>

### <span data-ttu-id="948ee-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948ee-123">-DefaultProfile</span></span>
<span data-ttu-id="948ee-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="948ee-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948ee-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="948ee-125">-Name</span></span>
<span data-ttu-id="948ee-126">Especifica o nome da marca a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="948ee-126">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="948ee-127">Por padrão, **Remove-AzureRmTag** remove a marca especificada e todos os seus valores.</span><span class="sxs-lookup"><span data-stu-id="948ee-127">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="948ee-128">Para excluir os valores selecionados, mas não excluir a marca, use o parâmetro *Value* .</span><span class="sxs-lookup"><span data-stu-id="948ee-128">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948ee-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="948ee-129">-PassThru</span></span>
<span data-ttu-id="948ee-130">Retorna um objeto que representa a marca excluída ou a marca resultante com valor excluído.</span><span class="sxs-lookup"><span data-stu-id="948ee-130">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948ee-131">-Valor</span><span class="sxs-lookup"><span data-stu-id="948ee-131">-Value</span></span>
<span data-ttu-id="948ee-132">Exclui os valores especificados da marca predefinida, mas não exclui a marca.</span><span class="sxs-lookup"><span data-stu-id="948ee-132">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948ee-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="948ee-133">-Confirm</span></span>
<span data-ttu-id="948ee-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="948ee-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948ee-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="948ee-135">-WhatIf</span></span>
<span data-ttu-id="948ee-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="948ee-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="948ee-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="948ee-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948ee-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948ee-138">CommonParameters</span></span>
<span data-ttu-id="948ee-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="948ee-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948ee-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948ee-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948ee-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="948ee-141">INPUTS</span></span>

### <span data-ttu-id="948ee-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="948ee-142">None</span></span>

## <span data-ttu-id="948ee-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="948ee-143">OUTPUTS</span></span>

### <span data-ttu-id="948ee-144">None ou Microsoft. Azure. Commands. Tags. Model. PSTag</span><span class="sxs-lookup"><span data-stu-id="948ee-144">None or Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="948ee-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="948ee-145">NOTES</span></span>

## <span data-ttu-id="948ee-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="948ee-146">RELATED LINKS</span></span>

[<span data-ttu-id="948ee-147">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="948ee-147">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="948ee-148">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="948ee-148">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


