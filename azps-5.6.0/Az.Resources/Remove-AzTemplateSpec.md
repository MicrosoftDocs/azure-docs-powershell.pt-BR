---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 6383a1fb0a6dbaa20bee50a268d8f78abf59de65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888812"
---
# <span data-ttu-id="79848-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="79848-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="79848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79848-102">SYNOPSIS</span></span>
<span data-ttu-id="79848-103">Remove uma especificação de modelo</span><span class="sxs-lookup"><span data-stu-id="79848-103">Removes a Template Spec</span></span>

## <span data-ttu-id="79848-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="79848-104">SYNTAX</span></span>

### <span data-ttu-id="79848-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="79848-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79848-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79848-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79848-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="79848-107">DESCRIPTION</span></span>
<span data-ttu-id="79848-108">Remove uma Especificação de Modelo especificada. Se o parâmetro **version -Version** for fornecido, somente a versão especificada será removida.</span><span class="sxs-lookup"><span data-stu-id="79848-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="79848-109">Se nenhuma versão específica for fornecida, a Especificação do Modelo e todas as suas versões serão removidas.</span><span class="sxs-lookup"><span data-stu-id="79848-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="79848-110">Se o **sinalizador -Force** estiver presente, não haverá prompt de confirmação para remoção.</span><span class="sxs-lookup"><span data-stu-id="79848-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="79848-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79848-111">EXAMPLES</span></span>

### <span data-ttu-id="79848-112">Exemplo 1: Removendo uma versão específica pelo nome</span><span class="sxs-lookup"><span data-stu-id="79848-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="79848-113">Remove a versão 'v1.0' da Especificação de Modelo denominada 'MyTemplateSpec' dentro do grupo de recursos 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="79848-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="79848-114">Exemplo 2: Removendo uma versão específica por id de recurso</span><span class="sxs-lookup"><span data-stu-id="79848-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="79848-115">Remove a versão 'v1.0' da Especificação de Modelo denominada 'MyTemplateSpec' dentro do grupo de recursos 'myRG' de subId de \{ assinatura \} .</span><span class="sxs-lookup"><span data-stu-id="79848-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="79848-116">Exemplo 3: Removendo uma Especificação de Modelo e todas as versões por nome</span><span class="sxs-lookup"><span data-stu-id="79848-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="79848-117">Remove a Especificação de Modelo denominada 'MyTemplateSpec' e todas as suas versões dentro do grupo de recursos 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="79848-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="79848-118">Exemplo 3: Removendo uma Especificação de Modelo e todas as versões por id de recurso</span><span class="sxs-lookup"><span data-stu-id="79848-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="79848-119">Remove a Especificação de Modelo denominada 'MyTemplateSpec' e todas as suas versões dentro do grupo de recursos 'myRG' de subId de \{ assinatura \} .</span><span class="sxs-lookup"><span data-stu-id="79848-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="79848-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="79848-120">PARAMETERS</span></span>

### <span data-ttu-id="79848-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79848-121">-DefaultProfile</span></span>
<span data-ttu-id="79848-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79848-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79848-123">-Force</span><span class="sxs-lookup"><span data-stu-id="79848-123">-Force</span></span>
<span data-ttu-id="79848-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="79848-124">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79848-125">-Name</span><span class="sxs-lookup"><span data-stu-id="79848-125">-Name</span></span>
<span data-ttu-id="79848-126">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="79848-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79848-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79848-127">-ResourceGroupName</span></span>
<span data-ttu-id="79848-128">O nome do grupo de recursos da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="79848-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79848-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79848-129">-ResourceId</span></span>
<span data-ttu-id="79848-130">A ID de recurso totalmente qualificada da especificação do modelo. Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="79848-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79848-131">-Version</span><span class="sxs-lookup"><span data-stu-id="79848-131">-Version</span></span>
<span data-ttu-id="79848-132">A versão da especificação do modelo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="79848-132">The version of the template spec to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79848-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79848-133">-Confirm</span></span>
<span data-ttu-id="79848-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79848-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79848-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79848-135">-WhatIf</span></span>
<span data-ttu-id="79848-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="79848-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79848-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79848-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79848-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79848-138">CommonParameters</span></span>
<span data-ttu-id="79848-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79848-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79848-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79848-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79848-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79848-141">INPUTS</span></span>

### <span data-ttu-id="79848-142">System.String</span><span class="sxs-lookup"><span data-stu-id="79848-142">System.String</span></span>

## <span data-ttu-id="79848-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="79848-143">OUTPUTS</span></span>

### <span data-ttu-id="79848-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79848-144">System.Boolean</span></span>

## <span data-ttu-id="79848-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="79848-145">NOTES</span></span>

## <span data-ttu-id="79848-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79848-146">RELATED LINKS</span></span>
