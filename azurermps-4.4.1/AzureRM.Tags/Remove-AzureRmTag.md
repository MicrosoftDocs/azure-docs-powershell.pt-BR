---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: 909781b8cd441daab8bf5f567404a5e99e88cd0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610142"
---
# <span data-ttu-id="1f9ac-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1f9ac-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="1f9ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f9ac-102">SYNOPSIS</span></span>
<span data-ttu-id="1f9ac-103">Exclui valores ou marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f9ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f9ac-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f9ac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f9ac-105">DESCRIPTION</span></span>
<span data-ttu-id="1f9ac-106">O cmdlet **Remove-AzureRmTag** exclui as marcas e os valores predefinidos do Azure de sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="1f9ac-107">Para excluir valores específicos de uma marca predefinida, use o parâmetro *Value* .</span><span class="sxs-lookup"><span data-stu-id="1f9ac-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="1f9ac-108">Por padrão, **Remove-AzureRmTag** exclui a marca especificada e todos os seus valores. Não é possível excluir uma marca ou um valor que seja aplicado no momento a um recurso ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>

<span data-ttu-id="1f9ac-109">Antes de usar **Remove-AzureRmTag** , use o parâmetro *Tag* do cmdlet Set-AzureRMResourceGroup para excluir a marca ou os valores do recurso ou do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>

<span data-ttu-id="1f9ac-110">O módulo de marcas do Azure que **Remove-AzureRmTag** faz parte do pode ajudá-lo a gerenciar suas marcas predefinidas do Azure.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="1f9ac-111">Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="1f9ac-112">Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="1f9ac-113">Se a assinatura incluir marcas predefinidas, não será possível aplicar marcas ou valores indefinidos a nenhum recurso ou grupo de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-113">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

## <span data-ttu-id="1f9ac-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f9ac-114">EXAMPLES</span></span>

### <span data-ttu-id="1f9ac-115">Exemplo 1: excluir uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="1f9ac-115">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="1f9ac-116">Este comando exclui a marca predefinida chamada Department e todos os seus recursos.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-116">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="1f9ac-117">Se a marca tiver sido aplicada a recursos ou grupos de recursos, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-117">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="1f9ac-118">Exemplo 2: excluir um valor de uma marca predefinida</span><span class="sxs-lookup"><span data-stu-id="1f9ac-118">Example 2: Delete a value from a predefined tag</span></span>
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

<span data-ttu-id="1f9ac-119">Esse comando exclui o valor HumanResources da marca de departamento predefinida.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-119">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="1f9ac-120">Ele não exclui a marca.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-120">It does not delete the tag.</span></span>
<span data-ttu-id="1f9ac-121">Se o valor tiver sido aplicado a recursos ou grupos de recursos, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-121">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="1f9ac-122">OS</span><span class="sxs-lookup"><span data-stu-id="1f9ac-122">PARAMETERS</span></span>

### <span data-ttu-id="1f9ac-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f9ac-123">-Name</span></span>
<span data-ttu-id="1f9ac-124">Especifica o nome da marca a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-124">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="1f9ac-125">Por padrão, **Remove-AzureRmTag** remove a marca especificada e todos os seus valores.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-125">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="1f9ac-126">Para excluir os valores selecionados, mas não excluir a marca, use o parâmetro *Value* .</span><span class="sxs-lookup"><span data-stu-id="1f9ac-126">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="1f9ac-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f9ac-127">-PassThru</span></span>
<span data-ttu-id="1f9ac-128">Retorna um objeto que representa a marca excluída ou a marca resultante com valor excluído.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-128">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="1f9ac-129">-Valor</span><span class="sxs-lookup"><span data-stu-id="1f9ac-129">-Value</span></span>
<span data-ttu-id="1f9ac-130">Exclui os valores especificados da marca predefinida, mas não exclui a marca.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-130">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="1f9ac-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f9ac-131">-Confirm</span></span>
<span data-ttu-id="1f9ac-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f9ac-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f9ac-133">-WhatIf</span></span>
<span data-ttu-id="1f9ac-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f9ac-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f9ac-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f9ac-136">-DefaultProfile</span></span>
<span data-ttu-id="1f9ac-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f9ac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f9ac-138">CommonParameters</span></span>
<span data-ttu-id="1f9ac-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f9ac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f9ac-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f9ac-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f9ac-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f9ac-141">INPUTS</span></span>

### <span data-ttu-id="1f9ac-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1f9ac-142">None</span></span>

## <span data-ttu-id="1f9ac-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f9ac-143">OUTPUTS</span></span>

### <span data-ttu-id="1f9ac-144">None ou Microsoft. Azure. Commands. Tags. Model. PSTag</span><span class="sxs-lookup"><span data-stu-id="1f9ac-144">None or Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="1f9ac-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f9ac-145">NOTES</span></span>

## <span data-ttu-id="1f9ac-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f9ac-146">RELATED LINKS</span></span>

[<span data-ttu-id="1f9ac-147">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1f9ac-147">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="1f9ac-148">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1f9ac-148">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


