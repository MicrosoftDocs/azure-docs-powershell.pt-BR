---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: aa011c7a858f08e3528fb2cdd7d67bcff37d76d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110982"
---
# <span data-ttu-id="da7a6-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="da7a6-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="da7a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="da7a6-103">Obtém um modelo ARM What-If resultado para uma implantação em escopo de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="da7a6-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="da7a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da7a6-104">SYNTAX</span></span>

### <span data-ttu-id="da7a6-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="da7a6-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7a6-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="da7a6-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7a6-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="da7a6-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7a6-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="da7a6-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7a6-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="da7a6-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7a6-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="da7a6-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7a6-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="da7a6-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7a6-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="da7a6-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7a6-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="da7a6-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7a6-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="da7a6-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7a6-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="da7a6-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da7a6-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="da7a6-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da7a6-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da7a6-117">DESCRIPTION</span></span>
<span data-ttu-id="da7a6-118">O cmdlet **Get-AzResourceGroupDeploymentWhatIfResult** Obtém o modelo ARM What-If resultado para uma implantação de modelo no escopo do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="da7a6-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="da7a6-119">Ele retorna uma lista de alterações indicando quais recursos serão atualizados se a implantação for aplicada sem fazer alterações em recursos reais.</span><span class="sxs-lookup"><span data-stu-id="da7a6-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="da7a6-120">Para especificar o formato do resultado retornado, use o parâmetro *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="da7a6-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="da7a6-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da7a6-121">EXAMPLES</span></span>

### <span data-ttu-id="da7a6-122">Exemplo 1: obter um resultado de What-If em escopo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="da7a6-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="da7a6-123">Esse comando obtém um resultado What-If no escopo do grupo de recursos especificado usando um arquivo de modelo personalizado e um arquivo de parâmetro no disco.</span><span class="sxs-lookup"><span data-stu-id="da7a6-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="da7a6-124">O comando usa o parâmetro *ResourceGroupName* para especificar um grupo de recursos onde o modelo será implantado.</span><span class="sxs-lookup"><span data-stu-id="da7a6-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="da7a6-125">O comando usa o parâmetro *TemplateFile* para especificar um arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="da7a6-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="da7a6-126">O comando usa o parâmetro *TemplateParameterFile* para especificar um arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="da7a6-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="da7a6-127">O comando usa o parâmetro *ResultFormat* para definir o resultado What-If para incluir cargas de recursos completas.</span><span class="sxs-lookup"><span data-stu-id="da7a6-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="da7a6-128">Exemplo 2: obter um resultado What-If em escopo do grupo de recursos com ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="da7a6-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="da7a6-129">Esse comando obtém um resultado What-If no escopo do grupo de recursos especificado usando um arquivo de modelo personalizado e um arquivo de parâmetro no disco.</span><span class="sxs-lookup"><span data-stu-id="da7a6-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="da7a6-130">O comando usa o parâmetro *ResourceGroupName* para especificar um grupo de recursos onde o modelo será implantado.</span><span class="sxs-lookup"><span data-stu-id="da7a6-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="da7a6-131">O comando usa o parâmetro *TemplateFile* para especificar um arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="da7a6-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="da7a6-132">O comando usa o parâmetro *TemplateParameterFile* para especificar um arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="da7a6-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="da7a6-133">O comando usa o parâmetro *ResultFormat* para definir o resultado What-If para conter somente as IDs do recurso.</span><span class="sxs-lookup"><span data-stu-id="da7a6-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="da7a6-134">OS</span><span class="sxs-lookup"><span data-stu-id="da7a6-134">PARAMETERS</span></span>

### <span data-ttu-id="da7a6-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="da7a6-135">-ApiVersion</span></span>
<span data-ttu-id="da7a6-136">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="da7a6-136">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="da7a6-137">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="da7a6-137">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a6-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7a6-138">-DefaultProfile</span></span>
<span data-ttu-id="da7a6-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da7a6-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da7a6-140">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="da7a6-140">-ExcludeChangeType</span></span>
<span data-ttu-id="da7a6-141">Tipos de alteração de recursos separados por vírgula a serem excluídos dos resultados de What-If.</span><span class="sxs-lookup"><span data-stu-id="da7a6-141">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="da7a6-142">-Mode</span><span class="sxs-lookup"><span data-stu-id="da7a6-142">-Mode</span></span>
<span data-ttu-id="da7a6-143">O modo de implantação.</span><span class="sxs-lookup"><span data-stu-id="da7a6-143">The deployment mode.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7a6-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="da7a6-144">-Name</span></span>
<span data-ttu-id="da7a6-145">O nome da implantação que será criada.</span><span class="sxs-lookup"><span data-stu-id="da7a6-145">The name of the deployment it's going to create.</span></span> <span data-ttu-id="da7a6-146">Se não for especificado, o padrão será o nome do arquivo de modelo quando um arquivo de modelo for fornecido; o padrão é a hora atual quando um objeto de modelo é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="da7a6-146">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7a6-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="da7a6-147">-Pre</span></span>
<span data-ttu-id="da7a6-148">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="da7a6-148">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="da7a6-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da7a6-149">-ResourceGroupName</span></span>
<span data-ttu-id="da7a6-150">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="da7a6-150">The resource group name.</span></span>

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

### <span data-ttu-id="da7a6-151">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="da7a6-151">-ResultFormat</span></span>
<span data-ttu-id="da7a6-152">O formato de resultado What-If.</span><span class="sxs-lookup"><span data-stu-id="da7a6-152">The What-If result format.</span></span>

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

### <span data-ttu-id="da7a6-153">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="da7a6-153">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="da7a6-154">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="da7a6-154">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="da7a6-155">Essa verificação solicitaria que o usuário forneça um valor para os parâmetros ausentes, mas fornecer o-SkipTemplateParameterPrompt ignorará esse prompt e o erro será imediatamente se um parâmetro não fosse associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="da7a6-155">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="da7a6-156">Para scripts não interativos,-SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso não seja satisfeito todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="da7a6-156">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="da7a6-157">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="da7a6-157">-TemplateFile</span></span>
<span data-ttu-id="da7a6-158">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="da7a6-158">Local path to the template file.</span></span>

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

### <span data-ttu-id="da7a6-159">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="da7a6-159">-TemplateObject</span></span>
<span data-ttu-id="da7a6-160">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="da7a6-160">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="da7a6-161">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="da7a6-161">-TemplateParameterFile</span></span>
<span data-ttu-id="da7a6-162">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="da7a6-162">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="da7a6-163">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="da7a6-163">-TemplateParameterObject</span></span>
<span data-ttu-id="da7a6-164">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="da7a6-164">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="da7a6-165">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="da7a6-165">-TemplateParameterUri</span></span>
<span data-ttu-id="da7a6-166">URL para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="da7a6-166">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="da7a6-167">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="da7a6-167">-TemplateUri</span></span>
<span data-ttu-id="da7a6-168">URL para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="da7a6-168">Uri to the template file.</span></span>

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

### <span data-ttu-id="da7a6-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7a6-169">CommonParameters</span></span>
<span data-ttu-id="da7a6-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da7a6-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7a6-171">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da7a6-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7a6-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da7a6-172">INPUTS</span></span>

### <span data-ttu-id="da7a6-173">System. String</span><span class="sxs-lookup"><span data-stu-id="da7a6-173">System.String</span></span>

### <span data-ttu-id="da7a6-174">Microsoft. Azure. Management. ResourceManager. Models. Deploymentmode</span><span class="sxs-lookup"><span data-stu-id="da7a6-174">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="da7a6-175">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="da7a6-175">System.Collections.Hashtable</span></span>

## <span data-ttu-id="da7a6-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da7a6-176">OUTPUTS</span></span>

### <span data-ttu-id="da7a6-177">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. imdeployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="da7a6-177">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="da7a6-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da7a6-178">NOTES</span></span>

## <span data-ttu-id="da7a6-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da7a6-179">RELATED LINKS</span></span>
