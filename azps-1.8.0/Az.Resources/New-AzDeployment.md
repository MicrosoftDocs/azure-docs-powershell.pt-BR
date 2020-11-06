---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 2e18ec6f920a1de2c890e29e34b4f15f58f0cfc0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599394"
---
# <span data-ttu-id="d9fe7-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d9fe7-101">New-AzDeployment</span></span>

## <span data-ttu-id="d9fe7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="d9fe7-103">Criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="d9fe7-103">Create a deployment</span></span>

## <span data-ttu-id="d9fe7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9fe7-104">SYNTAX</span></span>

### <span data-ttu-id="d9fe7-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9fe7-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9fe7-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d9fe7-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9fe7-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d9fe7-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9fe7-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d9fe7-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9fe7-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d9fe7-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9fe7-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d9fe7-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9fe7-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d9fe7-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9fe7-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d9fe7-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9fe7-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d9fe7-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9fe7-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d9fe7-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9fe7-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d9fe7-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9fe7-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d9fe7-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9fe7-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9fe7-117">DESCRIPTION</span></span>
<span data-ttu-id="d9fe7-118">O cmdlet **New-AzDeployment** adiciona uma implantação ao escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="d9fe7-119">Isso inclui os recursos que a implantação requer.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="d9fe7-120">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="d9fe7-121">Um recurso pode residir em um grupo de recursos, como servidor de banco de dados, banco de dados, site, máquina virtual ou conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="d9fe7-122">Ou pode ser um recurso de nível de assinatura, como definição de função, definição de política, etc.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="d9fe7-123">Para adicionar recursos a um grupo de recursos, use o **New-AzResourceGroupDeployment** que cria uma implantação em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="d9fe7-124">O cmdlet **New-AzDeployment** cria uma implantação no escopo de assinatura atual, que implanta recursos de nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="d9fe7-125">Para adicionar uma implantação na assinatura, especifique o local e um modelo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="d9fe7-126">O local informa ao Azure Resource Manager onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="d9fe7-127">O modelo é uma cadeia de caracteres JSON que contém recursos individuais a serem implantados.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="d9fe7-128">O modelo inclui espaços reservados de parâmetro para recursos obrigatórios e valores de propriedade configuráveis, como nomes e tamanhos.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="d9fe7-129">Para usar um modelo personalizado para a implantação, especifique o parâmetro *TemplateFile* ou o parâmetro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="d9fe7-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="d9fe7-130">Cada modelo tem parâmetros para propriedades configuráveis.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="d9fe7-131">Para especificar valores para os parâmetros de modelo, especifique o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="d9fe7-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="d9fe7-132">Você também pode usar os parâmetros de modelo que são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="d9fe7-133">Para usar parâmetros dinâmicos, digite-os no prompt de comando ou digite um sinal de subtração (-) para indicar um parâmetro e use a tecla Tab para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="d9fe7-134">Os valores de parâmetro de modelo que você insere no prompt de comando prevalecem sobre os valores em um objeto ou arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="d9fe7-135">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9fe7-135">EXAMPLES</span></span>

### <span data-ttu-id="d9fe7-136">Exemplo 1: usar um modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="d9fe7-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="d9fe7-137">Esse comando cria uma nova implantação no escopo de assinatura atual usando um modelo personalizado e um arquivo de modelo no disco.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="d9fe7-138">O comando usa o parâmetro *TemplateFile* para especificar o modelo e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="d9fe7-139">Ele usa o parâmetro *TemplateVersion* para especificar a versão do modelo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="d9fe7-140">Exemplo 2: usar um objeto de modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="d9fe7-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="d9fe7-141">Esse comando cria uma nova implantação no escopo de assinatura atual usando um modelo personalizado e um arquivo de modelo no disco que foi convertido em uma Hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="d9fe7-142">Os primeiros dois comandos lêem o texto do arquivo de modelo no disco e o convertem em uma Hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="d9fe7-143">O último comando usa o parâmetro *templateobject* para especificar essa Hashtable e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="d9fe7-144">Ele usa o parâmetro *TemplateVersion* para especificar a versão do modelo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="d9fe7-145">OS</span><span class="sxs-lookup"><span data-stu-id="d9fe7-145">PARAMETERS</span></span>

### <span data-ttu-id="d9fe7-146">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d9fe7-146">-ApiVersion</span></span>
<span data-ttu-id="d9fe7-147">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-147">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d9fe7-148">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-148">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d9fe7-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9fe7-149">-AsJob</span></span>
<span data-ttu-id="d9fe7-150">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d9fe7-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9fe7-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9fe7-151">-DefaultProfile</span></span>
<span data-ttu-id="d9fe7-152">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9fe7-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="d9fe7-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="d9fe7-154">O nível de log de depuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="d9fe7-155">-Local</span><span class="sxs-lookup"><span data-stu-id="d9fe7-155">-Location</span></span>
<span data-ttu-id="d9fe7-156">O local para armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="d9fe7-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9fe7-157">-Name</span></span>
<span data-ttu-id="d9fe7-158">O nome da implantação que será criada.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-158">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="d9fe7-159">Só é válido quando um modelo é usado.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-159">Only valid when a template is used.</span></span>
<span data-ttu-id="d9fe7-160">Quando um modelo é usado, se o usuário não especifica um nome de implantação, use a hora atual, como "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="d9fe7-160">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

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

### <span data-ttu-id="d9fe7-161">-Pre</span><span class="sxs-lookup"><span data-stu-id="d9fe7-161">-Pre</span></span>
<span data-ttu-id="d9fe7-162">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-162">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d9fe7-163">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="d9fe7-163">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="d9fe7-164">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-164">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="d9fe7-165">Essa verificação solicitaria que o usuário forneça um valor para os parâmetros ausentes, mas fornecer o-SkipTemplateParameterPrompt ignorará esse prompt e o erro será imediatamente se um parâmetro não fosse associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-165">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="d9fe7-166">Para scripts não interativos,-SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso não seja satisfeito todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-166">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="d9fe7-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d9fe7-167">-TemplateFile</span></span>
<span data-ttu-id="d9fe7-168">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-168">Local path to the template file.</span></span>

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

### <span data-ttu-id="d9fe7-169">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="d9fe7-169">-TemplateObject</span></span>
<span data-ttu-id="d9fe7-170">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-170">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="d9fe7-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="d9fe7-171">-TemplateParameterFile</span></span>
<span data-ttu-id="d9fe7-172">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-172">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="d9fe7-173">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="d9fe7-173">-TemplateParameterObject</span></span>
<span data-ttu-id="d9fe7-174">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-174">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="d9fe7-175">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="d9fe7-175">-TemplateParameterUri</span></span>
<span data-ttu-id="d9fe7-176">URL para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-176">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="d9fe7-177">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="d9fe7-177">-TemplateUri</span></span>
<span data-ttu-id="d9fe7-178">URL para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-178">Uri to the template file.</span></span>

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

### <span data-ttu-id="d9fe7-179">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9fe7-179">-Confirm</span></span>
<span data-ttu-id="d9fe7-180">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9fe7-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9fe7-181">-WhatIf</span></span>
<span data-ttu-id="d9fe7-182">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9fe7-183">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9fe7-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9fe7-184">CommonParameters</span></span>
<span data-ttu-id="d9fe7-185">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9fe7-186">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9fe7-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9fe7-187">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9fe7-187">INPUTS</span></span>

### <span data-ttu-id="d9fe7-188">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d9fe7-188">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d9fe7-189">System. String</span><span class="sxs-lookup"><span data-stu-id="d9fe7-189">System.String</span></span>

## <span data-ttu-id="d9fe7-190">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9fe7-190">OUTPUTS</span></span>

### <span data-ttu-id="d9fe7-191">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="d9fe7-191">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d9fe7-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9fe7-192">NOTES</span></span>

## <span data-ttu-id="d9fe7-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9fe7-193">RELATED LINKS</span></span>
