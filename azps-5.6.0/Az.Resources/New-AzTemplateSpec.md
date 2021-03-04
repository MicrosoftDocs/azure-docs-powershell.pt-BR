---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: 72c668f195024ac88e6d8ed67c08c6db6d0e3445
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888192"
---
# <span data-ttu-id="bd2b4-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="bd2b4-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="bd2b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd2b4-102">SYNOPSIS</span></span>
<span data-ttu-id="bd2b4-103">Cria uma nova Especificação de Modelo.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="bd2b4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bd2b4-104">SYNTAX</span></span>

### <span data-ttu-id="bd2b4-105">FromJsonStringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bd2b4-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd2b4-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd2b4-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd2b4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bd2b4-107">DESCRIPTION</span></span>
<span data-ttu-id="bd2b4-108">Cria uma nova versão de Especificação de Modelo com o conteúdo ARM Template especificado.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="bd2b4-109">O conteúdo pode vir de uma cadeia de caracteres JSON bruta (usando o conjunto de **parâmetros FromJsonStringParameterSet)** ou de um arquivo JSON especificado (usando o conjunto de **parâmetros FromJsonFileParameterSet).**</span><span class="sxs-lookup"><span data-stu-id="bd2b4-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="bd2b4-110">Se a Especificação de Modelo raiz ainda não existir, ela será criada juntamente com a versão De Especificação do Modelo.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="bd2b4-111">Se uma Especificação de Modelo já existir com o nome determinado, ela e a versão especificada serão atualizadas (quaisquer outras versões existentes serão preservadas).</span><span class="sxs-lookup"><span data-stu-id="bd2b4-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="bd2b4-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd2b4-112">EXAMPLES</span></span>

### <span data-ttu-id="bd2b4-113">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="bd2b4-113">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="bd2b4-114">Cria uma nova versão de Especificação de Modelo "v1.0" em uma Especificação de Modelo chamada "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="bd2b4-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="bd2b4-115">A versão especificada terá $templateJson como o conteúdo do modelo ARM versão.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="bd2b4-116">**Observação:** O ARM modelo no exemplo é um no-op, pois ele não contém recursos reais.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="bd2b4-117">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="bd2b4-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="bd2b4-118">Cria uma nova versão de Especificação de Modelo "v2.0" em uma Especificação de Modelo chamada "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="bd2b4-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="bd2b4-119">A versão especificada terá o conteúdo do arquivo local "myTemplateContent.json" como o conteúdo do modelo ARM versão.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="bd2b4-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bd2b4-120">PARAMETERS</span></span>

### <span data-ttu-id="bd2b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd2b4-121">-DefaultProfile</span></span>
<span data-ttu-id="bd2b4-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd2b4-123">-Description</span><span class="sxs-lookup"><span data-stu-id="bd2b4-123">-Description</span></span>
<span data-ttu-id="bd2b4-124">A descrição da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="bd2b4-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bd2b4-125">-DisplayName</span></span>
<span data-ttu-id="bd2b4-126">O nome de exibição da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="bd2b4-127">-Force</span><span class="sxs-lookup"><span data-stu-id="bd2b4-127">-Force</span></span>
<span data-ttu-id="bd2b4-128">Não peça confirmação ao sobrescrever uma versão existente.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="bd2b4-129">-Location</span><span class="sxs-lookup"><span data-stu-id="bd2b4-129">-Location</span></span>
<span data-ttu-id="bd2b4-130">O local da especificação do modelo. Somente será necessário se a especificação do modelo ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="bd2b4-131">-Name</span><span class="sxs-lookup"><span data-stu-id="bd2b4-131">-Name</span></span>
<span data-ttu-id="bd2b4-132">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-132">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd2b4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd2b4-133">-ResourceGroupName</span></span>
<span data-ttu-id="bd2b4-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="bd2b4-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd2b4-135">-Tag</span></span>
<span data-ttu-id="bd2b4-136">Hashtable de marcas para os novos recursos de especificação de modelo.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-136">Hashtable of tags for the new template spec resource(s).</span></span>

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

### <span data-ttu-id="bd2b4-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="bd2b4-137">-TemplateFile</span></span>
<span data-ttu-id="bd2b4-138">O caminho do arquivo para o arquivo JSON do modelo JSON local do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-138">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd2b4-139">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="bd2b4-139">-TemplateJson</span></span>
<span data-ttu-id="bd2b4-140">O modelo JSON do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-140">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd2b4-141">-Version</span><span class="sxs-lookup"><span data-stu-id="bd2b4-141">-Version</span></span>
<span data-ttu-id="bd2b4-142">A versão da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-142">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd2b4-143">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="bd2b4-143">-VersionDescription</span></span>
<span data-ttu-id="bd2b4-144">A descrição da versão.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-144">The description of the version.</span></span>

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

### <span data-ttu-id="bd2b4-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd2b4-145">-Confirm</span></span>
<span data-ttu-id="bd2b4-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd2b4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd2b4-147">-WhatIf</span></span>
<span data-ttu-id="bd2b4-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd2b4-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd2b4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd2b4-150">CommonParameters</span></span>
<span data-ttu-id="bd2b4-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd2b4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd2b4-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd2b4-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd2b4-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd2b4-153">INPUTS</span></span>

### <span data-ttu-id="bd2b4-154">System.String</span><span class="sxs-lookup"><span data-stu-id="bd2b4-154">System.String</span></span>

## <span data-ttu-id="bd2b4-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bd2b4-155">OUTPUTS</span></span>

### <span data-ttu-id="bd2b4-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="bd2b4-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="bd2b4-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="bd2b4-157">NOTES</span></span>

## <span data-ttu-id="bd2b4-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd2b4-158">RELATED LINKS</span></span>
