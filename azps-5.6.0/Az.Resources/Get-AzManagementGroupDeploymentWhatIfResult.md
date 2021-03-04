---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 981d9e771a988a4166f542854959b38e140d2061
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887867"
---
# <span data-ttu-id="f2226-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f2226-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="f2226-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2226-102">SYNOPSIS</span></span>
<span data-ttu-id="f2226-103">Obtém um modelo What-If resultado de uma implantação no escopo do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f2226-103">Gets a template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="f2226-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f2226-104">SYNTAX</span></span>

### <span data-ttu-id="f2226-105">ByTemplateFileWithNoParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f2226-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2226-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f2226-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2226-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f2226-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2226-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f2226-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2226-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f2226-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2226-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f2226-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2226-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f2226-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2226-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f2226-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2226-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f2226-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2226-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f2226-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2226-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f2226-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2226-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f2226-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2226-117">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f2226-117">DESCRIPTION</span></span>
<span data-ttu-id="f2226-118">O cmdlet **Get-AzManagementGroupDeploymentWhatIfResult** obtém o resultado do What-If modelo ARM para uma implantação de modelo no escopo do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="f2226-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="f2226-119">Ele retorna uma lista de alterações que indicam quais recursos serão atualizados se a implantação for aplicada sem fazer alterações nos recursos reais.</span><span class="sxs-lookup"><span data-stu-id="f2226-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="f2226-120">Para especificar o formato do resultado de retorno, use o *parâmetro ResultFormat.*</span><span class="sxs-lookup"><span data-stu-id="f2226-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="f2226-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2226-121">EXAMPLES</span></span>

### <span data-ttu-id="f2226-122">Exemplo 1: obter um What-If no escopo do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f2226-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="f2226-123">Esse comando obtém um What-If no escopo do grupo de gerenciamento usando um arquivo de modelo personalizado e um arquivo de parâmetro no disco.</span><span class="sxs-lookup"><span data-stu-id="f2226-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="f2226-124">O comando usa o *parâmetro Location* para especificar onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="f2226-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="f2226-125">O comando usa o *parâmetro ManagementGroupId* para especificar o grupo de gerenciamento no qual o modelo será implantado.</span><span class="sxs-lookup"><span data-stu-id="f2226-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="f2226-126">O comando usa o *parâmetro TemplateFile* para especificar um arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="f2226-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="f2226-127">O comando usa o *parâmetro TemplateParameterFile* para especificar um arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="f2226-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="f2226-128">O comando usa o *parâmetro ResultFormat* para definir o What-If para incluir cargas completas de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2226-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="f2226-129">Exemplo 2: obter um What-If no escopo do grupo de gerenciamento com ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="f2226-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="f2226-130">Esse comando obtém um What-If no escopo do grupo de gerenciamento usando um arquivo de modelo personalizado e um arquivo de parâmetro no disco.</span><span class="sxs-lookup"><span data-stu-id="f2226-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="f2226-131">O comando usa o *parâmetro Location* para especificar onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="f2226-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="f2226-132">O comando usa o *parâmetro ManagementGroupId* para especificar o grupo de gerenciamento no qual o modelo será implantado.</span><span class="sxs-lookup"><span data-stu-id="f2226-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="f2226-133">O comando usa o *parâmetro TemplateFile* para especificar um arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="f2226-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="f2226-134">O comando usa o *parâmetro TemplateParameterFile* para especificar um arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="f2226-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="f2226-135">O comando usa o *parâmetro ResultFormat* para definir o What-If result para conter apenas IDs de recurso.</span><span class="sxs-lookup"><span data-stu-id="f2226-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="f2226-136">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f2226-136">PARAMETERS</span></span>

### <span data-ttu-id="f2226-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2226-137">-DefaultProfile</span></span>
<span data-ttu-id="f2226-138">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2226-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2226-139">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="f2226-139">-ExcludeChangeType</span></span>
<span data-ttu-id="f2226-140">Lista separada por vírgulas dos tipos de alteração de recursos a serem excluídos dos What-If resultados.</span><span class="sxs-lookup"><span data-stu-id="f2226-140">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="f2226-141">-Location</span><span class="sxs-lookup"><span data-stu-id="f2226-141">-Location</span></span>
<span data-ttu-id="f2226-142">O local para armazenar dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="f2226-142">The location to store deployment data.</span></span>

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

### <span data-ttu-id="f2226-143">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f2226-143">-ManagementGroupId</span></span>
<span data-ttu-id="f2226-144">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f2226-144">The management group ID.</span></span>

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

### <span data-ttu-id="f2226-145">-Name</span><span class="sxs-lookup"><span data-stu-id="f2226-145">-Name</span></span>
<span data-ttu-id="f2226-146">O nome da implantação que ele criará.</span><span class="sxs-lookup"><span data-stu-id="f2226-146">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="f2226-147">Se não for especificado, o padrão é o nome do arquivo de modelo quando um arquivo de modelo é fornecido; padrão para a hora atual em que um objeto template é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="f2226-147">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="f2226-148">-Pre</span><span class="sxs-lookup"><span data-stu-id="f2226-148">-Pre</span></span>
<span data-ttu-id="f2226-149">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="f2226-149">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f2226-150">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="f2226-150">-ResultFormat</span></span>
<span data-ttu-id="f2226-151">O What-If de resultados.</span><span class="sxs-lookup"><span data-stu-id="f2226-151">The What-If result format.</span></span>

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

### <span data-ttu-id="f2226-152">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="f2226-152">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="f2226-153">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="f2226-153">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="f2226-154">Essa verificação solicitaria que o usuário fornecesse um valor para os parâmetros ausentes, mas o fornecimento de -SkipTemplateParameterPrompt ignorará esse prompt e o excluirá imediatamente se um parâmetro não tiver sido vinculado no modelo.</span><span class="sxs-lookup"><span data-stu-id="f2226-154">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="f2226-155">Para scripts não interativos, -SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso nem todos os parâmetros necessários sejam atendidos.</span><span class="sxs-lookup"><span data-stu-id="f2226-155">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="f2226-156">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f2226-156">-TemplateFile</span></span>
<span data-ttu-id="f2226-157">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="f2226-157">Local path to the template file.</span></span> <span data-ttu-id="f2226-158">Tipo de arquivo de modelo com suporte: json e bicep.</span><span class="sxs-lookup"><span data-stu-id="f2226-158">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="f2226-159">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="f2226-159">-TemplateObject</span></span>
<span data-ttu-id="f2226-160">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="f2226-160">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="f2226-161">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f2226-161">-TemplateParameterFile</span></span>
<span data-ttu-id="f2226-162">Um arquivo que tem os parâmetros do modelo.</span><span class="sxs-lookup"><span data-stu-id="f2226-162">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="f2226-163">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f2226-163">-TemplateParameterObject</span></span>
<span data-ttu-id="f2226-164">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f2226-164">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="f2226-165">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f2226-165">-TemplateParameterUri</span></span>
<span data-ttu-id="f2226-166">Uri para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="f2226-166">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="f2226-167">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f2226-167">-TemplateUri</span></span>
<span data-ttu-id="f2226-168">Uri para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="f2226-168">Uri to the template file.</span></span>

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

### <span data-ttu-id="f2226-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2226-169">CommonParameters</span></span>
<span data-ttu-id="f2226-170">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2226-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2226-171">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2226-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2226-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2226-172">INPUTS</span></span>

### <span data-ttu-id="f2226-173">System.String</span><span class="sxs-lookup"><span data-stu-id="f2226-173">System.String</span></span>

### <span data-ttu-id="f2226-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f2226-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f2226-175">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f2226-175">OUTPUTS</span></span>

### <span data-ttu-id="f2226-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="f2226-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="f2226-177">NOTES</span><span class="sxs-lookup"><span data-stu-id="f2226-177">NOTES</span></span>

## <span data-ttu-id="f2226-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2226-178">RELATED LINKS</span></span>
