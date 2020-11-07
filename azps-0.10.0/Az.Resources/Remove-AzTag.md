---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 5b7e58545b2c463c08a961758ecdb3cbce7b222c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776332"
---
# <span data-ttu-id="faea6-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="faea6-101">Remove-AzTag</span></span>

## <span data-ttu-id="faea6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="faea6-102">SYNOPSIS</span></span>
<span data-ttu-id="faea6-103">Exclui valores ou marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="faea6-103">Deletes predefined Azure tags or values.</span></span>

## <span data-ttu-id="faea6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="faea6-104">SYNTAX</span></span>

```
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faea6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="faea6-105">DESCRIPTION</span></span>
<span data-ttu-id="faea6-106">O cmdlet **Remove-AzTag** exclui as marcas e os valores predefinidos do Azure de sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="faea6-106">The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="faea6-107">Para excluir valores específicos de uma marca predefinida, use o parâmetro *Value* .</span><span class="sxs-lookup"><span data-stu-id="faea6-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="faea6-108">Por padrão, **Remove-AzTag** exclui a marca especificada e todos os seus valores. Não é possível excluir uma marca ou um valor que seja aplicado no momento a um recurso ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="faea6-108">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="faea6-109">Antes de usar **Remove-AzTag** , use o parâmetro *Tag* do cmdlet Set-AzResourceGroup para excluir a marca ou os valores do recurso ou do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="faea6-109">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="faea6-110">O módulo de marcas do Azure que **Remove-AzTag** faz parte do pode ajudá-lo a gerenciar suas marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="faea6-110">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="faea6-111">Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="faea6-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="faea6-112">Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="faea6-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

## <span data-ttu-id="faea6-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="faea6-113">EXAMPLES</span></span>

### <span data-ttu-id="faea6-114">Exemplo 1: excluir uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="faea6-114">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="faea6-115">Esse comando exclui a marca predefinida chamada Department e todos os seus valores.</span><span class="sxs-lookup"><span data-stu-id="faea6-115">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="faea6-116">Se a marca tiver sido aplicada a recursos ou grupos de recursos, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="faea6-116">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="faea6-117">Exemplo 2: excluir um valor de uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="faea6-117">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="faea6-118">Esse comando exclui o valor HumanResources da marca de departamento predefinida.</span><span class="sxs-lookup"><span data-stu-id="faea6-118">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="faea6-119">Ele não exclui a marca.</span><span class="sxs-lookup"><span data-stu-id="faea6-119">It does not delete the tag.</span></span>
<span data-ttu-id="faea6-120">Se o valor tiver sido aplicado a recursos ou grupos de recursos, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="faea6-120">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="faea6-121">OS</span><span class="sxs-lookup"><span data-stu-id="faea6-121">PARAMETERS</span></span>

### <span data-ttu-id="faea6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faea6-122">-DefaultProfile</span></span>
<span data-ttu-id="faea6-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="faea6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faea6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="faea6-124">-Name</span></span>
<span data-ttu-id="faea6-125">Especifica o nome da marca a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="faea6-125">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="faea6-126">Por padrão, **Remove-AzTag** remove a marca especificada e todos os seus valores.</span><span class="sxs-lookup"><span data-stu-id="faea6-126">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="faea6-127">Para excluir os valores selecionados, mas não excluir a marca, use o parâmetro *Value* .</span><span class="sxs-lookup"><span data-stu-id="faea6-127">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="faea6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="faea6-128">-PassThru</span></span>
<span data-ttu-id="faea6-129">Retorna um objeto que representa a marca excluída ou a marca resultante com valor excluído.</span><span class="sxs-lookup"><span data-stu-id="faea6-129">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="faea6-130">-Valor</span><span class="sxs-lookup"><span data-stu-id="faea6-130">-Value</span></span>
<span data-ttu-id="faea6-131">Exclui os valores especificados da marca predefinida, mas não exclui a marca.</span><span class="sxs-lookup"><span data-stu-id="faea6-131">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faea6-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="faea6-132">-Confirm</span></span>
<span data-ttu-id="faea6-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faea6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faea6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faea6-134">-WhatIf</span></span>
<span data-ttu-id="faea6-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="faea6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faea6-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="faea6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faea6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faea6-137">CommonParameters</span></span>
<span data-ttu-id="faea6-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faea6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faea6-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faea6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faea6-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="faea6-140">INPUTS</span></span>

### <span data-ttu-id="faea6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="faea6-141">System.String</span></span>

### <span data-ttu-id="faea6-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="faea6-142">System.String[]</span></span>

### <span data-ttu-id="faea6-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="faea6-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="faea6-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="faea6-144">OUTPUTS</span></span>

### <span data-ttu-id="faea6-145">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="faea6-145">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="faea6-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="faea6-146">NOTES</span></span>

## <span data-ttu-id="faea6-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="faea6-147">RELATED LINKS</span></span>

[<span data-ttu-id="faea6-148">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="faea6-148">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="faea6-149">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="faea6-149">New-AzTag</span></span>](./New-AzTag.md)
