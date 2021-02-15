---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 0ad3df8e010beec777bd059bbef708774570792d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118140"
---
# <span data-ttu-id="b0ecf-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="b0ecf-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="b0ecf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="b0ecf-103">Obtém um modelo ARM What-If resultado para uma implantação no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-103">Gets an ARM template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="b0ecf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0ecf-104">SYNTAX</span></span>

### <span data-ttu-id="b0ecf-105">ByTemplateFileWithNoParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b0ecf-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0ecf-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b0ecf-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0ecf-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b0ecf-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0ecf-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b0ecf-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0ecf-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b0ecf-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0ecf-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b0ecf-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0ecf-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b0ecf-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0ecf-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b0ecf-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0ecf-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b0ecf-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0ecf-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b0ecf-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0ecf-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b0ecf-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0ecf-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b0ecf-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0ecf-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0ecf-117">DESCRIPTION</span></span>
<span data-ttu-id="b0ecf-118">O cmdlet **Get-AzDeploymentWhatIfResult** obtém o modelo ARM What-If resultado de uma implantação de modelo no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="b0ecf-119">Ela retorna uma lista de alterações indicando quais recursos serão atualizados se a implantação for aplicada sem fazer alterações nos recursos reais.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="b0ecf-120">Para especificar o formato do resultado de retorno, use o parâmetro *Formatação* De resultado.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="b0ecf-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b0ecf-121">EXAMPLES</span></span>

### <span data-ttu-id="b0ecf-122">Exemplo 1: Obter um What-If no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="b0ecf-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="b0ecf-123">Esse comando obtém um What-If no escopo da assinatura atual usando um arquivo de modelo personalizado e um arquivo de parâmetro no disco.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="b0ecf-124">O comando usa o *parâmetro Local* para especificar onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="b0ecf-125">O comando usa o parâmetro *TemplateFile* para especificar um arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="b0ecf-126">O comando usa o parâmetro *TemplateParameterFile* para especificar um arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="b0ecf-127">O comando usa o parâmetro *ResultFormat* para definir o What-If para incluir cargas completas de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="b0ecf-128">Exemplo 2: Obter um What-If no escopo da assinatura com ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="b0ecf-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="b0ecf-129">Esse comando obtém um What-If no escopo da assinatura atual usando um arquivo de modelo personalizado e um arquivo de parâmetro no disco.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="b0ecf-130">O comando usa o *parâmetro Local* para especificar onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="b0ecf-131">O comando usa o parâmetro *TemplateFile* para especificar um arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="b0ecf-132">O comando usa o parâmetro *TemplateParameterFile* para especificar um arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="b0ecf-133">O comando usa o parâmetro *ResultFormat* para definir o What-If para conter somente IDs de recurso.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="b0ecf-134">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0ecf-134">PARAMETERS</span></span>

### <span data-ttu-id="b0ecf-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0ecf-135">-DefaultProfile</span></span>
<span data-ttu-id="b0ecf-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0ecf-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="b0ecf-137">-ExcludeChangeType</span></span>
<span data-ttu-id="b0ecf-138">Lista separada por vírgulas dos tipos de alteração de recursos a serem excluídos What-If resultados.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ecf-139">-Local</span><span class="sxs-lookup"><span data-stu-id="b0ecf-139">-Location</span></span>
<span data-ttu-id="b0ecf-140">O local para armazenar dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-140">The location to store deployment data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ecf-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0ecf-141">-Name</span></span>
<span data-ttu-id="b0ecf-142">O nome da implantação que ele vai criar.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="b0ecf-143">Se não especificado, o padrão é o nome do arquivo de modelo quando um arquivo de modelo é fornecido; padrão para a hora atual quando um objeto de modelo é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="b0ecf-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ecf-144">-Pré-</span><span class="sxs-lookup"><span data-stu-id="b0ecf-144">-Pre</span></span>
<span data-ttu-id="b0ecf-145">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b0ecf-146">-Formatação de Resultado</span><span class="sxs-lookup"><span data-stu-id="b0ecf-146">-ResultFormat</span></span>
<span data-ttu-id="b0ecf-147">O What-If de resultados.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-147">The What-If result format.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ecf-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="b0ecf-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="b0ecf-149">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="b0ecf-150">Essa verificação solicitaria que o usuário fornecesse um valor para os parâmetros ausentes, mas fornecer o -SkipTemplateParameterPrompt ignorará esse prompt e um erro imediatamente se um parâmetro não tiver sido vinculado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="b0ecf-151">Para scripts não interativos, -SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso nem todos os parâmetros necessários sejam satisfeitos.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="b0ecf-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b0ecf-152">-TemplateFile</span></span>
<span data-ttu-id="b0ecf-153">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-153">Local path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0ecf-154">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="b0ecf-154">-TemplateObject</span></span>
<span data-ttu-id="b0ecf-155">Uma tabela hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-155">A hash table which represents the template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0ecf-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b0ecf-156">-TemplateParameterFile</span></span>
<span data-ttu-id="b0ecf-157">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-157">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0ecf-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b0ecf-158">-TemplateParameterObject</span></span>
<span data-ttu-id="b0ecf-159">Uma tabela hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-159">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0ecf-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b0ecf-160">-TemplateParameterUri</span></span>
<span data-ttu-id="b0ecf-161">Uri para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-161">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0ecf-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b0ecf-162">-TemplateUri</span></span>
<span data-ttu-id="b0ecf-163">Uri para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-163">Uri to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0ecf-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0ecf-164">CommonParameters</span></span>
<span data-ttu-id="b0ecf-165">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0ecf-166">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0ecf-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0ecf-167">Entradas</span><span class="sxs-lookup"><span data-stu-id="b0ecf-167">INPUTS</span></span>

### <span data-ttu-id="b0ecf-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b0ecf-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b0ecf-169">System.String</span><span class="sxs-lookup"><span data-stu-id="b0ecf-169">System.String</span></span>

## <span data-ttu-id="b0ecf-170">Saídas</span><span class="sxs-lookup"><span data-stu-id="b0ecf-170">OUTPUTS</span></span>

### <span data-ttu-id="b0ecf-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="b0ecf-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="b0ecf-172">Notas</span><span class="sxs-lookup"><span data-stu-id="b0ecf-172">NOTES</span></span>

## <span data-ttu-id="b0ecf-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0ecf-173">RELATED LINKS</span></span>
