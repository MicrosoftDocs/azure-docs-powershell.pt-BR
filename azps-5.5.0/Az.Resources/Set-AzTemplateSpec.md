---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 681cbc620a5c6067102dfe2a67f20dd9edc42046
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118125"
---
# <span data-ttu-id="c5ab5-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="c5ab5-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="c5ab5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ab5-103">Modifica uma Especificação de Modelo.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="c5ab5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5ab5-104">SYNTAX</span></span>

### <span data-ttu-id="c5ab5-105">FromJsonStringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c5ab5-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5ab5-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5ab5-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ab5-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5ab5-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ab5-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5ab5-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ab5-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5ab5-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ab5-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5ab5-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ab5-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5ab5-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5ab5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5ab5-112">DESCRIPTION</span></span>
<span data-ttu-id="c5ab5-113">Modifica uma Especificação templace. Se a Especificação do Modelo com o nome especificado e/ou versão específica ainda não existir, ela será criada.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="c5ab5-114">Ao modificar o conteúdo do modelo ARM de uma versão de modelo de modelo, o conteúdo pode ser de uma cadeia de caracteres JSON bruto (usando o conjunto de parâmetros **UpdateVersionByNameFromJsonParameterSet)** ou de um arquivo JSON especificado (usando o conjunto de parâmetros **UpdateVersionByNameFromJsonFileParameterSet).**</span><span class="sxs-lookup"><span data-stu-id="c5ab5-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="c5ab5-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c5ab5-115">EXAMPLES</span></span>

### <span data-ttu-id="c5ab5-116">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="c5ab5-116">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="c5ab5-117">Modifica a versão "v1.0" de uma Especificação de Modelo chamada "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="c5ab5-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="c5ab5-118">A versão especificada terá $templateJson como o conteúdo do modelo ARM da versão.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="c5ab5-119">Se a Especificação do Modelo raiz e/ou a versão ainda não existirem, elas serão criadas.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="c5ab5-120">**Notas:**</span><span class="sxs-lookup"><span data-stu-id="c5ab5-120">**Notes:**</span></span> 

* <span data-ttu-id="c5ab5-121">O Modelo ARM no exemplo é uma não-operação, pois não contém recursos reais.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="c5ab5-122">A localização só é necessária quando a Especificação de Modelo ainda não existe</span><span class="sxs-lookup"><span data-stu-id="c5ab5-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="c5ab5-123">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="c5ab5-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="c5ab5-124">Modifica a versão "v2.0" de uma Especificação de Modelo chamada "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="c5ab5-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="c5ab5-125">A versão especificada terá o conteúdo do arquivo local "myTemplateContent.jsem" como o conteúdo do Modelo ARM da versão.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="c5ab5-126">Se a Especificação do Modelo raiz e/ou a versão ainda não existirem, elas serão criadas.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="c5ab5-127">**Observação:** A localização só é necessária quando a Especificação de Modelo ainda não existe</span><span class="sxs-lookup"><span data-stu-id="c5ab5-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="c5ab5-128">Exemplo 3:</span><span class="sxs-lookup"><span data-stu-id="c5ab5-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="c5ab5-129">Modifica a descrição da Especificação de Modelo chamada "myTemplateSpec" no grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="c5ab5-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="c5ab5-130">Se a Especificação do Modelo ainda não existir, ela será criada.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="c5ab5-131">**Observação:** A localização só é necessária quando a Especificação de Modelo ainda não existe</span><span class="sxs-lookup"><span data-stu-id="c5ab5-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="c5ab5-132">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5ab5-132">PARAMETERS</span></span>

### <span data-ttu-id="c5ab5-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5ab5-133">-DefaultProfile</span></span>
<span data-ttu-id="c5ab5-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5ab5-135">-Descrição</span><span class="sxs-lookup"><span data-stu-id="c5ab5-135">-Description</span></span>
<span data-ttu-id="c5ab5-136">A descrição da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-136">The description of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ab5-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c5ab5-137">-DisplayName</span></span>
<span data-ttu-id="c5ab5-138">O nome de exibição da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-138">The display name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ab5-139">-Local</span><span class="sxs-lookup"><span data-stu-id="c5ab5-139">-Location</span></span>
<span data-ttu-id="c5ab5-140">O local da especificação do modelo. Só será necessário se a especificação do modelo ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ab5-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5ab5-141">-Name</span></span>
<span data-ttu-id="c5ab5-142">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-142">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ab5-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5ab5-143">-ResourceGroupName</span></span>
<span data-ttu-id="c5ab5-144">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ab5-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5ab5-145">-ResourceId</span></span>
<span data-ttu-id="c5ab5-146">A ID de recurso totalmente qualificada da especificação do modelo. Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="c5ab5-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ab5-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="c5ab5-147">-Tag</span></span>
<span data-ttu-id="c5ab5-148">Hashtable of tags for the template spec and/or version</span><span class="sxs-lookup"><span data-stu-id="c5ab5-148">Hashtable of tags for the template spec and/or version</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ab5-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c5ab5-149">-TemplateFile</span></span>
<span data-ttu-id="c5ab5-150">O caminho do arquivo para o arquivo JSON do modelo local do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByNameFromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ab5-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="c5ab5-151">-TemplateJson</span></span>
<span data-ttu-id="c5ab5-152">O modelo JSON do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-152">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ab5-153">-Versão</span><span class="sxs-lookup"><span data-stu-id="c5ab5-153">-Version</span></span>
<span data-ttu-id="c5ab5-154">A versão da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-154">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ab5-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="c5ab5-155">-VersionDescription</span></span>
<span data-ttu-id="c5ab5-156">A descrição da versão.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-156">The description of the version.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ab5-157">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c5ab5-157">-Confirm</span></span>
<span data-ttu-id="c5ab5-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5ab5-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5ab5-159">-WhatIf</span></span>
<span data-ttu-id="c5ab5-160">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5ab5-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5ab5-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ab5-162">CommonParameters</span></span>
<span data-ttu-id="c5ab5-163">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5ab5-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ab5-164">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5ab5-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ab5-165">Entradas</span><span class="sxs-lookup"><span data-stu-id="c5ab5-165">INPUTS</span></span>

### <span data-ttu-id="c5ab5-166">System.String</span><span class="sxs-lookup"><span data-stu-id="c5ab5-166">System.String</span></span>

## <span data-ttu-id="c5ab5-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="c5ab5-167">OUTPUTS</span></span>

### <span data-ttu-id="c5ab5-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="c5ab5-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="c5ab5-169">Notas</span><span class="sxs-lookup"><span data-stu-id="c5ab5-169">NOTES</span></span>

## <span data-ttu-id="c5ab5-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5ab5-170">RELATED LINKS</span></span>
