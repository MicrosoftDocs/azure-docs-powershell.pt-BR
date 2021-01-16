---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: ad5979d65565107ac071bcaac94bc178b8c36d1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262344"
---
# <span data-ttu-id="0184d-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0184d-101">New-AzDeployment</span></span>

## <span data-ttu-id="0184d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0184d-102">SYNOPSIS</span></span>
<span data-ttu-id="0184d-103">Criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="0184d-103">Create a deployment</span></span>

## <span data-ttu-id="0184d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0184d-104">SYNTAX</span></span>

### <span data-ttu-id="0184d-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="0184d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0184d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0184d-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0184d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0184d-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0184d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0184d-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0184d-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0184d-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0184d-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0184d-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0184d-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0184d-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0184d-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0184d-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0184d-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0184d-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0184d-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0184d-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0184d-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0184d-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0184d-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0184d-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0184d-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0184d-117">DESCRIPTION</span></span>
<span data-ttu-id="0184d-118">O cmdlet **New-AzDeployment** adiciona uma implantação ao escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0184d-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="0184d-119">Isso inclui os recursos que a implantação requer.</span><span class="sxs-lookup"><span data-stu-id="0184d-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="0184d-120">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0184d-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="0184d-121">Um recurso pode residir em um grupo de recursos, como servidor de banco de dados, banco de dados, site, máquina virtual ou conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0184d-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="0184d-122">Ou pode ser um recurso de nível de assinatura, como definição de função, definição de política, etc.</span><span class="sxs-lookup"><span data-stu-id="0184d-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="0184d-123">Para adicionar recursos a um grupo de recursos, use o **New-AzResourceGroupDeployment** que cria uma implantação em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0184d-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="0184d-124">O cmdlet **New-AzDeployment** cria uma implantação no escopo de assinatura atual, que implanta recursos de nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="0184d-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="0184d-125">Para adicionar uma implantação na assinatura, especifique o local e um modelo.</span><span class="sxs-lookup"><span data-stu-id="0184d-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="0184d-126">O local informa ao Azure Resource Manager onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="0184d-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="0184d-127">O modelo é uma cadeia de caracteres JSON que contém recursos individuais a serem implantados.</span><span class="sxs-lookup"><span data-stu-id="0184d-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="0184d-128">O modelo inclui espaços reservados de parâmetro para recursos obrigatórios e valores de propriedade configuráveis, como nomes e tamanhos.</span><span class="sxs-lookup"><span data-stu-id="0184d-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="0184d-129">Para usar um modelo personalizado para a implantação, especifique o parâmetro *TemplateFile* ou o parâmetro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="0184d-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="0184d-130">Cada modelo tem parâmetros para propriedades configuráveis.</span><span class="sxs-lookup"><span data-stu-id="0184d-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="0184d-131">Para especificar valores para os parâmetros de modelo, especifique o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="0184d-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="0184d-132">Você também pode usar os parâmetros de modelo que são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="0184d-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="0184d-133">Para usar parâmetros dinâmicos, digite-os no prompt de comando ou digite um sinal de subtração (-) para indicar um parâmetro e use a tecla Tab para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0184d-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="0184d-134">Os valores de parâmetro de modelo que você insere no prompt de comando prevalecem sobre os valores em um objeto ou arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="0184d-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="0184d-135">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0184d-135">EXAMPLES</span></span>

### <span data-ttu-id="0184d-136">Exemplo 1: usar um modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="0184d-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="0184d-137">Esse comando cria uma nova implantação no escopo de assinatura atual usando um modelo personalizado e um arquivo de modelo no disco, com o parâmetro Tags definidas.</span><span class="sxs-lookup"><span data-stu-id="0184d-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="0184d-138">O comando usa o parâmetro *TemplateFile* para especificar o modelo e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0184d-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="0184d-139">Ele usa o parâmetro *TemplateVersion* para especificar a versão do modelo.</span><span class="sxs-lookup"><span data-stu-id="0184d-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="0184d-140">Exemplo 2: usar um objeto de modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="0184d-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="0184d-141">Esse comando cria uma nova implantação no escopo de assinatura atual usando um modelo personalizado e um arquivo de modelo no disco que foi convertido em uma Hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="0184d-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="0184d-142">Os primeiros dois comandos lêem o texto do arquivo de modelo no disco e o convertem em uma Hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="0184d-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="0184d-143">O último comando usa o parâmetro *templateobject* para especificar essa Hashtable e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0184d-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="0184d-144">Ele usa o parâmetro *TemplateVersion* para especificar a versão do modelo.</span><span class="sxs-lookup"><span data-stu-id="0184d-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="0184d-145">OS</span><span class="sxs-lookup"><span data-stu-id="0184d-145">PARAMETERS</span></span>

### <span data-ttu-id="0184d-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0184d-146">-AsJob</span></span>
<span data-ttu-id="0184d-147">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0184d-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0184d-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0184d-148">-DefaultProfile</span></span>
<span data-ttu-id="0184d-149">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0184d-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0184d-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="0184d-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="0184d-151">O nível de log de depuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="0184d-151">The deployment debug log level.</span></span>

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

### <span data-ttu-id="0184d-152">-Local</span><span class="sxs-lookup"><span data-stu-id="0184d-152">-Location</span></span>
<span data-ttu-id="0184d-153">O local para armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="0184d-153">The location to store deployment data.</span></span>

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

### <span data-ttu-id="0184d-154">-Nome</span><span class="sxs-lookup"><span data-stu-id="0184d-154">-Name</span></span>
<span data-ttu-id="0184d-155">O nome da implantação que será criada.</span><span class="sxs-lookup"><span data-stu-id="0184d-155">The name of the deployment it's going to create.</span></span> <span data-ttu-id="0184d-156">Se não for especificado, o padrão será o nome do arquivo de modelo quando um arquivo de modelo for fornecido; o padrão é a hora atual quando um objeto de modelo é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="0184d-156">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="0184d-157">-Pre</span><span class="sxs-lookup"><span data-stu-id="0184d-157">-Pre</span></span>
<span data-ttu-id="0184d-158">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="0184d-158">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0184d-159">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="0184d-159">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="0184d-160">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="0184d-160">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="0184d-161">Essa verificação solicitaria que o usuário forneça um valor para os parâmetros ausentes, mas fornecer o-SkipTemplateParameterPrompt ignorará esse prompt e o erro será imediatamente se um parâmetro não fosse associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="0184d-161">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="0184d-162">Para scripts não interativos,-SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso não seja satisfeito todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0184d-162">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="0184d-163">-Marca</span><span class="sxs-lookup"><span data-stu-id="0184d-163">-Tag</span></span>
<span data-ttu-id="0184d-164">As marcas a serem colocadas na implantação.</span><span class="sxs-lookup"><span data-stu-id="0184d-164">The tags to put on the deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0184d-165">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0184d-165">-TemplateFile</span></span>
<span data-ttu-id="0184d-166">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="0184d-166">Local path to the template file.</span></span>

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

### <span data-ttu-id="0184d-167">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="0184d-167">-TemplateObject</span></span>
<span data-ttu-id="0184d-168">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="0184d-168">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="0184d-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0184d-169">-TemplateParameterFile</span></span>
<span data-ttu-id="0184d-170">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="0184d-170">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="0184d-171">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="0184d-171">-TemplateParameterObject</span></span>
<span data-ttu-id="0184d-172">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0184d-172">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="0184d-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="0184d-173">-TemplateParameterUri</span></span>
<span data-ttu-id="0184d-174">URL para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="0184d-174">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="0184d-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="0184d-175">-TemplateUri</span></span>
<span data-ttu-id="0184d-176">URL para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="0184d-176">Uri to the template file.</span></span>

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

### <span data-ttu-id="0184d-177">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="0184d-177">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="0184d-178">Tipos de alteração de recursos separados por vírgula a serem excluídos dos resultados de What-If.</span><span class="sxs-lookup"><span data-stu-id="0184d-178">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="0184d-179">Aplicável quando a opção-WhatIf ou-Confirm está definida.</span><span class="sxs-lookup"><span data-stu-id="0184d-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="0184d-180">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="0184d-180">-WhatIfResultFormat</span></span>
<span data-ttu-id="0184d-181">O formato de resultado What-If.</span><span class="sxs-lookup"><span data-stu-id="0184d-181">The What-If result format.</span></span>

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

### <span data-ttu-id="0184d-182">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0184d-182">-Confirm</span></span>
<span data-ttu-id="0184d-183">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0184d-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0184d-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0184d-184">-WhatIf</span></span>
<span data-ttu-id="0184d-185">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0184d-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0184d-186">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0184d-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0184d-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0184d-187">CommonParameters</span></span>
<span data-ttu-id="0184d-188">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0184d-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0184d-189">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0184d-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0184d-190">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0184d-190">INPUTS</span></span>

### <span data-ttu-id="0184d-191">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0184d-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0184d-192">System. String</span><span class="sxs-lookup"><span data-stu-id="0184d-192">System.String</span></span>

## <span data-ttu-id="0184d-193">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0184d-193">OUTPUTS</span></span>

### <span data-ttu-id="0184d-194">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="0184d-194">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0184d-195">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0184d-195">NOTES</span></span>

## <span data-ttu-id="0184d-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0184d-196">RELATED LINKS</span></span>
