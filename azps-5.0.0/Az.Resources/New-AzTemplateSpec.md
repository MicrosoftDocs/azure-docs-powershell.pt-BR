---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: b19653570c7bfbf62cb94107bb2fa354a9fda3f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117041"
---
# <span data-ttu-id="8da67-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="8da67-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="8da67-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8da67-102">SYNOPSIS</span></span>
<span data-ttu-id="8da67-103">Cria uma nova especificação de modelo.</span><span class="sxs-lookup"><span data-stu-id="8da67-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="8da67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8da67-104">SYNTAX</span></span>

### <span data-ttu-id="8da67-105">FromJsonStringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8da67-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da67-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8da67-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8da67-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8da67-107">DESCRIPTION</span></span>
<span data-ttu-id="8da67-108">Cria uma nova versão de especificação de modelo com o conteúdo de modelo ARM especificado.</span><span class="sxs-lookup"><span data-stu-id="8da67-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="8da67-109">O conteúdo pode vir de uma cadeia de caracteres JSON bruta (usando o conjunto de parâmetros **FromJsonStringParameterSet** ) ou de um arquivo JSON especificado (usando o conjunto de parâmetros **FromJsonFileParameterSet** ).</span><span class="sxs-lookup"><span data-stu-id="8da67-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="8da67-110">Se a especificação do modelo raiz ainda não existir, ela será criada juntamente com a versão de especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="8da67-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="8da67-111">Se já existir uma espec de modelo com o nome fornecido, ele e a versão especificada serão atualizados (qualquer outra versão existente será preservada).</span><span class="sxs-lookup"><span data-stu-id="8da67-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="8da67-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8da67-112">EXAMPLES</span></span>

### <span data-ttu-id="8da67-113">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="8da67-113">Example 1:</span></span>
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

<span data-ttu-id="8da67-114">Cria uma nova especificação de modelo versão "v 1.0" em uma especificação de modelo chamada "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="8da67-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="8da67-115">A versão especificada terá $templateJson como o conteúdo de modelo ARM da versão.</span><span class="sxs-lookup"><span data-stu-id="8da67-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="8da67-116">**Observação:** O modelo ARM no exemplo é não op, pois ele não contém recursos reais.</span><span class="sxs-lookup"><span data-stu-id="8da67-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="8da67-117">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="8da67-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="8da67-118">Cria uma nova especificação de modelo versão "v 2.0" em uma especificação de modelo chamada "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="8da67-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="8da67-119">A versão especificada terá o conteúdo do arquivo local "myTemplateContent.js" como o conteúdo do modelo ARM da versão.</span><span class="sxs-lookup"><span data-stu-id="8da67-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="8da67-120">OS</span><span class="sxs-lookup"><span data-stu-id="8da67-120">PARAMETERS</span></span>

### <span data-ttu-id="8da67-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da67-121">-DefaultProfile</span></span>
<span data-ttu-id="8da67-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8da67-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8da67-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="8da67-123">-Description</span></span>
<span data-ttu-id="8da67-124">A descrição da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="8da67-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="8da67-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8da67-125">-DisplayName</span></span>
<span data-ttu-id="8da67-126">O nome de exibição da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="8da67-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="8da67-127">-Force</span><span class="sxs-lookup"><span data-stu-id="8da67-127">-Force</span></span>
<span data-ttu-id="8da67-128">Não peça confirmação ao substituir uma versão existente.</span><span class="sxs-lookup"><span data-stu-id="8da67-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="8da67-129">-Local</span><span class="sxs-lookup"><span data-stu-id="8da67-129">-Location</span></span>
<span data-ttu-id="8da67-130">A localização da especificação do modelo. Só é necessário se a especificação do modelo ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="8da67-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="8da67-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="8da67-131">-Name</span></span>
<span data-ttu-id="8da67-132">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="8da67-132">The name of the template spec.</span></span>

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

### <span data-ttu-id="8da67-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da67-133">-ResourceGroupName</span></span>
<span data-ttu-id="8da67-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8da67-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="8da67-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8da67-135">-TemplateFile</span></span>
<span data-ttu-id="8da67-136">O caminho do arquivo para o arquivo JSON do modelo do Azure Resource Manager local.</span><span class="sxs-lookup"><span data-stu-id="8da67-136">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="8da67-137">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="8da67-137">-TemplateJson</span></span>
<span data-ttu-id="8da67-138">O modelo JSON do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8da67-138">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="8da67-139">-Versão</span><span class="sxs-lookup"><span data-stu-id="8da67-139">-Version</span></span>
<span data-ttu-id="8da67-140">A versão da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="8da67-140">The version of the template spec.</span></span>

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

### <span data-ttu-id="8da67-141">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="8da67-141">-VersionDescription</span></span>
<span data-ttu-id="8da67-142">A descrição da versão.</span><span class="sxs-lookup"><span data-stu-id="8da67-142">The description of the version.</span></span>

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

### <span data-ttu-id="8da67-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8da67-143">-Confirm</span></span>
<span data-ttu-id="8da67-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da67-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8da67-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da67-145">-WhatIf</span></span>
<span data-ttu-id="8da67-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8da67-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8da67-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8da67-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8da67-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da67-148">CommonParameters</span></span>
<span data-ttu-id="8da67-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da67-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da67-150">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8da67-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da67-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8da67-151">INPUTS</span></span>

### <span data-ttu-id="8da67-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8da67-152">System.String</span></span>

## <span data-ttu-id="8da67-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8da67-153">OUTPUTS</span></span>

### <span data-ttu-id="8da67-154">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="8da67-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="8da67-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8da67-155">NOTES</span></span>

## <span data-ttu-id="8da67-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8da67-156">RELATED LINKS</span></span>
