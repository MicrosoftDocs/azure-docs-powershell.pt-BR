---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: 2d0eb49a46e0d6fbbe02d145e42195d059c5176f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117187"
---
# <span data-ttu-id="70516-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="70516-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="70516-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70516-102">SYNOPSIS</span></span>
<span data-ttu-id="70516-103">Cria uma nova Especificação de Modelo.</span><span class="sxs-lookup"><span data-stu-id="70516-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="70516-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70516-104">SYNTAX</span></span>

### <span data-ttu-id="70516-105">FromJsonStringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="70516-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70516-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="70516-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70516-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="70516-107">DESCRIPTION</span></span>
<span data-ttu-id="70516-108">Cria uma nova versão de Especificação de Modelo com o conteúdo de Modelo ARM especificado.</span><span class="sxs-lookup"><span data-stu-id="70516-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="70516-109">O conteúdo pode ser de uma cadeia de caracteres JSON bruto (usando o conjunto de parâmetros **FromJsonStringParameterSet)** ou de um arquivo JSON especificado (usando o conjunto de parâmetros **FromJsonFileParameterSet).**</span><span class="sxs-lookup"><span data-stu-id="70516-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="70516-110">Se a Especificação raiz do Modelo ainda não existir, ela será criada juntamente com a versão da Especificação de Modelo.</span><span class="sxs-lookup"><span data-stu-id="70516-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="70516-111">Se uma Especificação de Modelo já existir com o nome determinado, ela e a versão especificada serão atualizadas (quaisquer outras versões existentes serão preservadas).</span><span class="sxs-lookup"><span data-stu-id="70516-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="70516-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="70516-112">EXAMPLES</span></span>

### <span data-ttu-id="70516-113">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="70516-113">Example 1:</span></span>
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

<span data-ttu-id="70516-114">Cria uma nova versão da Especificação de Modelo "v1.0" em uma Especificação de Modelo chamada "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="70516-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="70516-115">A versão especificada terá $templateJson como o conteúdo do modelo ARM da versão.</span><span class="sxs-lookup"><span data-stu-id="70516-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="70516-116">**Observação:** O Modelo ARM no exemplo é uma não-operação, pois não contém recursos reais.</span><span class="sxs-lookup"><span data-stu-id="70516-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="70516-117">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="70516-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="70516-118">Cria uma nova versão da Especificação de Modelo "v2.0" em uma Especificação de Modelo chamada "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="70516-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="70516-119">A versão especificada terá o conteúdo do arquivo local "myTemplateContent.jsem" como o conteúdo do Modelo ARM da versão.</span><span class="sxs-lookup"><span data-stu-id="70516-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="70516-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70516-120">PARAMETERS</span></span>

### <span data-ttu-id="70516-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70516-121">-DefaultProfile</span></span>
<span data-ttu-id="70516-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70516-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70516-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="70516-123">-Description</span></span>
<span data-ttu-id="70516-124">A descrição da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="70516-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="70516-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="70516-125">-DisplayName</span></span>
<span data-ttu-id="70516-126">O nome de exibição da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="70516-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="70516-127">-Forçar</span><span class="sxs-lookup"><span data-stu-id="70516-127">-Force</span></span>
<span data-ttu-id="70516-128">Não peça confirmação ao sobrescrever uma versão existente.</span><span class="sxs-lookup"><span data-stu-id="70516-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="70516-129">-Local</span><span class="sxs-lookup"><span data-stu-id="70516-129">-Location</span></span>
<span data-ttu-id="70516-130">O local da especificação do modelo. Só será necessário se a especificação do modelo ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="70516-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="70516-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="70516-131">-Name</span></span>
<span data-ttu-id="70516-132">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="70516-132">The name of the template spec.</span></span>

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

### <span data-ttu-id="70516-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70516-133">-ResourceGroupName</span></span>
<span data-ttu-id="70516-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="70516-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="70516-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="70516-135">-Tag</span></span>
<span data-ttu-id="70516-136">Hashtable of tags for the new template spec resource(s).</span><span class="sxs-lookup"><span data-stu-id="70516-136">Hashtable of tags for the new template spec resource(s).</span></span>

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

### <span data-ttu-id="70516-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="70516-137">-TemplateFile</span></span>
<span data-ttu-id="70516-138">O caminho do arquivo para o arquivo JSON do modelo local do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="70516-138">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="70516-139">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="70516-139">-TemplateJson</span></span>
<span data-ttu-id="70516-140">O modelo JSON do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="70516-140">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="70516-141">-Versão</span><span class="sxs-lookup"><span data-stu-id="70516-141">-Version</span></span>
<span data-ttu-id="70516-142">A versão da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="70516-142">The version of the template spec.</span></span>

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

### <span data-ttu-id="70516-143">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="70516-143">-VersionDescription</span></span>
<span data-ttu-id="70516-144">A descrição da versão.</span><span class="sxs-lookup"><span data-stu-id="70516-144">The description of the version.</span></span>

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

### <span data-ttu-id="70516-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="70516-145">-Confirm</span></span>
<span data-ttu-id="70516-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70516-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70516-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70516-147">-WhatIf</span></span>
<span data-ttu-id="70516-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="70516-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70516-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70516-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70516-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70516-150">CommonParameters</span></span>
<span data-ttu-id="70516-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70516-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70516-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70516-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70516-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="70516-153">INPUTS</span></span>

### <span data-ttu-id="70516-154">System.String</span><span class="sxs-lookup"><span data-stu-id="70516-154">System.String</span></span>

## <span data-ttu-id="70516-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="70516-155">OUTPUTS</span></span>

### <span data-ttu-id="70516-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="70516-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="70516-157">Notas</span><span class="sxs-lookup"><span data-stu-id="70516-157">NOTES</span></span>

## <span data-ttu-id="70516-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70516-158">RELATED LINKS</span></span>
