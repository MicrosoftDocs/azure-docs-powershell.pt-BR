---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentWhatIfResult.md
ms.openlocfilehash: 8e25d83eda64bb9705829ff0a8b1dd40d6055953
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281903"
---
# <span data-ttu-id="7361c-101">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7361c-101">Get-AzTenantDeploymentWhatIfResult</span></span>

## <span data-ttu-id="7361c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7361c-102">SYNOPSIS</span></span>
<span data-ttu-id="7361c-103">Obtém um modelo ARM What-If resultado para uma implantação no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="7361c-103">Gets an ARM template What-If result for a deployment at tenant scope.</span></span> 

## <span data-ttu-id="7361c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7361c-104">SYNTAX</span></span>

### <span data-ttu-id="7361c-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="7361c-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7361c-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7361c-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7361c-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7361c-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7361c-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7361c-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7361c-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7361c-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7361c-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7361c-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7361c-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7361c-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7361c-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7361c-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7361c-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7361c-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7361c-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7361c-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7361c-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7361c-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7361c-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7361c-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7361c-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7361c-117">DESCRIPTION</span></span>
<span data-ttu-id="7361c-118">O cmdlet **Get-AzTenantDeploymentWhatIfResult** Obtém o modelo ARM What-If resultado para uma implantação de modelo no escopo do locatário especificado.</span><span class="sxs-lookup"><span data-stu-id="7361c-118">The **Get-AzTenantDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified tenant scope.</span></span> <span data-ttu-id="7361c-119">Ele retorna uma lista de alterações indicando quais recursos serão atualizados se a implantação for aplicada sem fazer alterações em recursos reais.</span><span class="sxs-lookup"><span data-stu-id="7361c-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="7361c-120">Para especificar o formato do resultado retornado, use o parâmetro *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="7361c-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="7361c-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7361c-121">EXAMPLES</span></span>

### <span data-ttu-id="7361c-122">Exemplo 1: obter um resultado de What-If no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="7361c-122">Example 1: Get a What-If result at tenant scope</span></span>
```powershell
PS C:\> Get-AzTenantDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="7361c-123">Esse comando obtém um resultado What-If em escopo do locatário usando um arquivo de modelo personalizado e um arquivo de parâmetro no disco.</span><span class="sxs-lookup"><span data-stu-id="7361c-123">This command gets a What-If result at tenant scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="7361c-124">O comando usa o parâmetro *Location* para especificar onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="7361c-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="7361c-125">O comando usa o parâmetro *TemplateFile* para especificar um arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="7361c-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="7361c-126">O comando usa o parâmetro *TemplateParameterFile* para especificar um arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="7361c-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="7361c-127">O comando usa o parâmetro *ResultFormat* para definir o resultado What-If para incluir cargas de recursos completas.</span><span class="sxs-lookup"><span data-stu-id="7361c-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="7361c-128">Exemplo 2: obter um resultado What-If no escopo do locatário com ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="7361c-128">Example 2: Get a What-If result at tenant scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzTenantDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="7361c-129">Esse comando obtém um resultado What-If em escopo do locatário usando um arquivo de modelo personalizado e um arquivo de parâmetro no disco.</span><span class="sxs-lookup"><span data-stu-id="7361c-129">This command gets a What-If result at tenant scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="7361c-130">O comando usa o parâmetro *Location* para especificar onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="7361c-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="7361c-131">O comando usa o parâmetro *TemplateFile* para especificar um arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="7361c-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="7361c-132">O comando usa o parâmetro *TemplateParameterFile* para especificar um arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="7361c-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="7361c-133">O comando usa o parâmetro *ResultFormat* para definir o resultado What-If para conter somente as IDs do recurso.</span><span class="sxs-lookup"><span data-stu-id="7361c-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="7361c-134">OS</span><span class="sxs-lookup"><span data-stu-id="7361c-134">PARAMETERS</span></span>

### <span data-ttu-id="7361c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7361c-135">-DefaultProfile</span></span>
<span data-ttu-id="7361c-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7361c-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7361c-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="7361c-137">-ExcludeChangeType</span></span>
<span data-ttu-id="7361c-138">Lista separada por vírgula dos tipos de alteração de recurso a serem excluídos dos resultados de What-If.</span><span class="sxs-lookup"><span data-stu-id="7361c-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="7361c-139">-Local</span><span class="sxs-lookup"><span data-stu-id="7361c-139">-Location</span></span>
<span data-ttu-id="7361c-140">O local para armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="7361c-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="7361c-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="7361c-141">-Name</span></span>
<span data-ttu-id="7361c-142">O nome da implantação que será criada.</span><span class="sxs-lookup"><span data-stu-id="7361c-142">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="7361c-143">Se não for especificado, o padrão será o nome do arquivo de modelo quando um arquivo de modelo for fornecido; o padrão é a hora atual quando um objeto de modelo é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="7361c-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="7361c-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="7361c-144">-Pre</span></span>
<span data-ttu-id="7361c-145">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="7361c-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7361c-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="7361c-146">-ResultFormat</span></span>
<span data-ttu-id="7361c-147">O formato de resultado What-If.</span><span class="sxs-lookup"><span data-stu-id="7361c-147">The What-If result format.</span></span>

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

### <span data-ttu-id="7361c-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="7361c-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="7361c-149">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="7361c-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="7361c-150">Essa verificação solicitaria que o usuário forneça um valor para os parâmetros ausentes, mas fornecer o-SkipTemplateParameterPrompt ignorará esse prompt e o erro será imediatamente se um parâmetro não fosse associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="7361c-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="7361c-151">Para scripts não interativos,-SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso não seja satisfeito todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="7361c-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="7361c-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="7361c-152">-TemplateFile</span></span>
<span data-ttu-id="7361c-153">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="7361c-153">Local path to the template file.</span></span>

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

### <span data-ttu-id="7361c-154">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="7361c-154">-TemplateObject</span></span>
<span data-ttu-id="7361c-155">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="7361c-155">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="7361c-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="7361c-156">-TemplateParameterFile</span></span>
<span data-ttu-id="7361c-157">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="7361c-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="7361c-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="7361c-158">-TemplateParameterObject</span></span>
<span data-ttu-id="7361c-159">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7361c-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="7361c-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="7361c-160">-TemplateParameterUri</span></span>
<span data-ttu-id="7361c-161">URL para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="7361c-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="7361c-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="7361c-162">-TemplateUri</span></span>
<span data-ttu-id="7361c-163">URL para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="7361c-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="7361c-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7361c-164">CommonParameters</span></span>
<span data-ttu-id="7361c-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7361c-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7361c-166">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7361c-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7361c-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7361c-167">INPUTS</span></span>

### <span data-ttu-id="7361c-168">System. String</span><span class="sxs-lookup"><span data-stu-id="7361c-168">System.String</span></span>

### <span data-ttu-id="7361c-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7361c-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7361c-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7361c-170">OUTPUTS</span></span>

### <span data-ttu-id="7361c-171">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. imdeployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="7361c-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="7361c-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7361c-172">NOTES</span></span>

## <span data-ttu-id="7361c-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7361c-173">RELATED LINKS</span></span>
