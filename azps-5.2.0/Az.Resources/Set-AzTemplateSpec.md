---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 681cbc620a5c6067102dfe2a67f20dd9edc42046
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261716"
---
# <span data-ttu-id="9fe3f-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="9fe3f-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="9fe3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fe3f-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe3f-103">Modifica uma especificação de modelo.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="9fe3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fe3f-104">SYNTAX</span></span>

### <span data-ttu-id="9fe3f-105">FromJsonStringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9fe3f-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fe3f-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe3f-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe3f-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe3f-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe3f-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe3f-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe3f-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe3f-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe3f-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe3f-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe3f-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe3f-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe3f-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fe3f-112">DESCRIPTION</span></span>
<span data-ttu-id="9fe3f-113">Modifica uma especificação de Templace. Se a especificação do modelo com o nome especificado e/ou a versão específica ainda não existir, ela será criada.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="9fe3f-114">Ao modificar o conteúdo de modelo ARM da versão de especificação do modelo, o conteúdo pode vir de uma cadeia de caracteres JSON bruta (usando o conjunto de parâmetros **UpdateVersionByNameFromJsonParameterSet** ) ou de um arquivo JSON especificado (usando o conjunto de parâmetros **UpdateVersionByNameFromJsonFileParameterSet** ).</span><span class="sxs-lookup"><span data-stu-id="9fe3f-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="9fe3f-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fe3f-115">EXAMPLES</span></span>

### <span data-ttu-id="9fe3f-116">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="9fe3f-116">Example 1:</span></span>
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

<span data-ttu-id="9fe3f-117">Modifica a versão "v 1.0" de uma especificação de modelo chamada "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="9fe3f-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="9fe3f-118">A versão especificada terá $templateJson como o conteúdo de modelo ARM da versão.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="9fe3f-119">Se a especificação do modelo raiz e/ou a versão ainda não existir, elas serão criadas.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="9fe3f-120">**Informa**</span><span class="sxs-lookup"><span data-stu-id="9fe3f-120">**Notes:**</span></span> 

* <span data-ttu-id="9fe3f-121">O modelo ARM no exemplo é não op, pois ele não contém recursos reais.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="9fe3f-122">A localização só é necessária quando a especificação do modelo ainda não existe</span><span class="sxs-lookup"><span data-stu-id="9fe3f-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="9fe3f-123">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="9fe3f-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="9fe3f-124">Modifica a versão "v 2.0" de uma especificação de modelo chamada "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="9fe3f-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="9fe3f-125">A versão especificada terá o conteúdo do arquivo local "myTemplateContent.js" como o conteúdo do modelo ARM da versão.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="9fe3f-126">Se a especificação do modelo raiz e/ou a versão ainda não existir, elas serão criadas.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="9fe3f-127">**Observação:** A localização só é necessária quando a especificação do modelo ainda não existe</span><span class="sxs-lookup"><span data-stu-id="9fe3f-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="9fe3f-128">Exemplo 3:</span><span class="sxs-lookup"><span data-stu-id="9fe3f-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="9fe3f-129">Modifica a descrição da especificação do modelo chamada "myTemplateSpec" no grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="9fe3f-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="9fe3f-130">Se a especificação do modelo ainda não existir, ela será criada.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="9fe3f-131">**Observação:** A localização só é necessária quando a especificação do modelo ainda não existe</span><span class="sxs-lookup"><span data-stu-id="9fe3f-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="9fe3f-132">OS</span><span class="sxs-lookup"><span data-stu-id="9fe3f-132">PARAMETERS</span></span>

### <span data-ttu-id="9fe3f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe3f-133">-DefaultProfile</span></span>
<span data-ttu-id="9fe3f-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fe3f-135">-Descrição</span><span class="sxs-lookup"><span data-stu-id="9fe3f-135">-Description</span></span>
<span data-ttu-id="9fe3f-136">A descrição da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-136">The description of the template spec.</span></span>

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

### <span data-ttu-id="9fe3f-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9fe3f-137">-DisplayName</span></span>
<span data-ttu-id="9fe3f-138">O nome de exibição da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-138">The display name of the template spec.</span></span>

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

### <span data-ttu-id="9fe3f-139">-Local</span><span class="sxs-lookup"><span data-stu-id="9fe3f-139">-Location</span></span>
<span data-ttu-id="9fe3f-140">A localização da especificação do modelo. Só é necessário se a especificação do modelo ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="9fe3f-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="9fe3f-141">-Name</span></span>
<span data-ttu-id="9fe3f-142">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-142">The name of the template spec.</span></span>

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

### <span data-ttu-id="9fe3f-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe3f-143">-ResourceGroupName</span></span>
<span data-ttu-id="9fe3f-144">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="9fe3f-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fe3f-145">-ResourceId</span></span>
<span data-ttu-id="9fe3f-146">A ID de recurso totalmente qualificado da especificação do modelo. exemplo:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="9fe3f-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="9fe3f-147">-Marca</span><span class="sxs-lookup"><span data-stu-id="9fe3f-147">-Tag</span></span>
<span data-ttu-id="9fe3f-148">Hashtable de marcas para a especificação do modelo e/ou versão</span><span class="sxs-lookup"><span data-stu-id="9fe3f-148">Hashtable of tags for the template spec and/or version</span></span>

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

### <span data-ttu-id="9fe3f-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9fe3f-149">-TemplateFile</span></span>
<span data-ttu-id="9fe3f-150">O caminho do arquivo para o arquivo JSON do modelo do Azure Resource Manager local.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="9fe3f-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="9fe3f-151">-TemplateJson</span></span>
<span data-ttu-id="9fe3f-152">O modelo JSON do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-152">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="9fe3f-153">-Versão</span><span class="sxs-lookup"><span data-stu-id="9fe3f-153">-Version</span></span>
<span data-ttu-id="9fe3f-154">A versão da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-154">The version of the template spec.</span></span>

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

### <span data-ttu-id="9fe3f-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="9fe3f-155">-VersionDescription</span></span>
<span data-ttu-id="9fe3f-156">A descrição da versão.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-156">The description of the version.</span></span>

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

### <span data-ttu-id="9fe3f-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9fe3f-157">-Confirm</span></span>
<span data-ttu-id="9fe3f-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe3f-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe3f-159">-WhatIf</span></span>
<span data-ttu-id="9fe3f-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fe3f-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe3f-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe3f-162">CommonParameters</span></span>
<span data-ttu-id="9fe3f-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe3f-164">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fe3f-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe3f-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fe3f-165">INPUTS</span></span>

### <span data-ttu-id="9fe3f-166">System. String</span><span class="sxs-lookup"><span data-stu-id="9fe3f-166">System.String</span></span>

## <span data-ttu-id="9fe3f-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fe3f-167">OUTPUTS</span></span>

### <span data-ttu-id="9fe3f-168">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="9fe3f-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="9fe3f-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fe3f-169">NOTES</span></span>

## <span data-ttu-id="9fe3f-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fe3f-170">RELATED LINKS</span></span>
