---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: a04c19df84626fd08968e1950074306dfd7cf1ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262341"
---
# <span data-ttu-id="d74f7-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d74f7-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="d74f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d74f7-102">SYNOPSIS</span></span>
<span data-ttu-id="d74f7-103">Criar uma implantação em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d74f7-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="d74f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d74f7-104">SYNTAX</span></span>

### <span data-ttu-id="d74f7-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="d74f7-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74f7-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d74f7-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74f7-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d74f7-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d74f7-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d74f7-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d74f7-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d74f7-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d74f7-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d74f7-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d74f7-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d74f7-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d74f7-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d74f7-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d74f7-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d74f7-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d74f7-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d74f7-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d74f7-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d74f7-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74f7-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d74f7-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d74f7-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d74f7-117">DESCRIPTION</span></span>
<span data-ttu-id="d74f7-118">O cmdlet **New-AzManagementGroupDeployment** adiciona uma implantação em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d74f7-118">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="d74f7-119">Para adicionar uma implantação em um grupo de gerenciamento, especifique o grupo de gerenciamento, local e um modelo.</span><span class="sxs-lookup"><span data-stu-id="d74f7-119">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="d74f7-120">O local informa ao Azure Resource Manager onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="d74f7-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="d74f7-121">O modelo é uma cadeia de caracteres JSON que contém recursos individuais a serem implantados.</span><span class="sxs-lookup"><span data-stu-id="d74f7-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="d74f7-122">O modelo inclui espaços reservados de parâmetro para recursos obrigatórios e valores de propriedade configuráveis, como nomes e tamanhos.</span><span class="sxs-lookup"><span data-stu-id="d74f7-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="d74f7-123">Para usar um modelo personalizado para a implantação, especifique o parâmetro *TemplateFile* ou o parâmetro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="d74f7-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="d74f7-124">Cada modelo tem parâmetros para propriedades configuráveis.</span><span class="sxs-lookup"><span data-stu-id="d74f7-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="d74f7-125">Para especificar valores para os parâmetros de modelo, especifique o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="d74f7-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="d74f7-126">Você também pode usar os parâmetros de modelo que são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="d74f7-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="d74f7-127">Para usar parâmetros dinâmicos, digite-os no prompt de comando ou digite um sinal de subtração (-) para indicar um parâmetro e use a tecla Tab para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d74f7-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="d74f7-128">Os valores de parâmetro de modelo que você insere no prompt de comando prevalecem sobre os valores em um objeto ou arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="d74f7-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="d74f7-129">Para adicionar recursos a um grupo de recursos, use o **New-AzResourceGroupDeployment** que cria uma implantação em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d74f7-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="d74f7-130">Para adicionar recursos a uma assinatura, use o **New-AzSubscriptionDeployment** que cria uma implantação em escopo de assinatura, que implanta recursos de nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="d74f7-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="d74f7-131">Para adicionar recursos no escopo do locatário, use o **New-AzTenantDeployment** que cria uma implantação no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="d74f7-131">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="d74f7-132">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d74f7-132">EXAMPLES</span></span>

### <span data-ttu-id="d74f7-133">Exemplo 1: usar um modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="d74f7-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="d74f7-134">Esse comando cria uma nova implantação no grupo de gerenciamento "myMG" usando um modelo personalizado e um arquivo de modelo no disco, com o parâmetro Tags definidas.</span><span class="sxs-lookup"><span data-stu-id="d74f7-134">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="d74f7-135">O comando usa o parâmetro *TemplateFile* para especificar o modelo e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d74f7-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="d74f7-136">Exemplo 2: usar um objeto de modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="d74f7-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="d74f7-137">Esse comando cria uma nova implantação no grupo de gerenciamento "myMG" usando um modelo personalizado e um arquivo de modelo no disco que foi convertido em uma Hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="d74f7-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="d74f7-138">Os primeiros dois comandos lêem o texto do arquivo de modelo no disco e o convertem em uma Hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="d74f7-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="d74f7-139">O último comando usa o parâmetro *templateobject* para especificar essa Hashtable e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d74f7-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="d74f7-140">OS</span><span class="sxs-lookup"><span data-stu-id="d74f7-140">PARAMETERS</span></span>

### <span data-ttu-id="d74f7-141">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d74f7-141">-AsJob</span></span>
<span data-ttu-id="d74f7-142">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d74f7-142">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d74f7-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74f7-143">-DefaultProfile</span></span>
<span data-ttu-id="d74f7-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d74f7-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d74f7-145">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="d74f7-145">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="d74f7-146">O nível de log de depuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="d74f7-146">The deployment debug log level.</span></span>

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

### <span data-ttu-id="d74f7-147">-Local</span><span class="sxs-lookup"><span data-stu-id="d74f7-147">-Location</span></span>
<span data-ttu-id="d74f7-148">O local para armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="d74f7-148">The location to store deployment data.</span></span>

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

### <span data-ttu-id="d74f7-149">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d74f7-149">-ManagementGroupId</span></span>
<span data-ttu-id="d74f7-150">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d74f7-150">The management group ID.</span></span>

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

### <span data-ttu-id="d74f7-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="d74f7-151">-Name</span></span>
<span data-ttu-id="d74f7-152">O nome da implantação que será criada.</span><span class="sxs-lookup"><span data-stu-id="d74f7-152">The name of the deployment it's going to create.</span></span> <span data-ttu-id="d74f7-153">Se não for especificado, o padrão será o nome do arquivo de modelo quando um arquivo de modelo for fornecido; o padrão é a hora atual quando um objeto de modelo é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="d74f7-153">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="d74f7-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="d74f7-154">-Pre</span></span>
<span data-ttu-id="d74f7-155">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="d74f7-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d74f7-156">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="d74f7-156">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="d74f7-157">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="d74f7-157">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="d74f7-158">Essa verificação solicitaria que o usuário forneça um valor para os parâmetros ausentes, mas fornecer o-SkipTemplateParameterPrompt ignorará esse prompt e o erro será imediatamente se um parâmetro não fosse associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="d74f7-158">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="d74f7-159">Para scripts não interativos,-SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso não seja satisfeito todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="d74f7-159">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="d74f7-160">-Marca</span><span class="sxs-lookup"><span data-stu-id="d74f7-160">-Tag</span></span>
<span data-ttu-id="d74f7-161">As marcas a serem colocadas na implantação.</span><span class="sxs-lookup"><span data-stu-id="d74f7-161">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="d74f7-162">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d74f7-162">-TemplateFile</span></span>
<span data-ttu-id="d74f7-163">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="d74f7-163">Local path to the template file.</span></span>

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

### <span data-ttu-id="d74f7-164">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="d74f7-164">-TemplateObject</span></span>
<span data-ttu-id="d74f7-165">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="d74f7-165">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="d74f7-166">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="d74f7-166">-TemplateParameterFile</span></span>
<span data-ttu-id="d74f7-167">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="d74f7-167">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="d74f7-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="d74f7-168">-TemplateParameterObject</span></span>
<span data-ttu-id="d74f7-169">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d74f7-169">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="d74f7-170">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="d74f7-170">-TemplateParameterUri</span></span>
<span data-ttu-id="d74f7-171">URL para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="d74f7-171">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="d74f7-172">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="d74f7-172">-TemplateUri</span></span>
<span data-ttu-id="d74f7-173">URL para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="d74f7-173">Uri to the template file.</span></span>

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

### <span data-ttu-id="d74f7-174">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="d74f7-174">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="d74f7-175">Tipos de alteração de recursos separados por vírgula a serem excluídos dos resultados de What-If.</span><span class="sxs-lookup"><span data-stu-id="d74f7-175">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="d74f7-176">Aplicável quando a opção-WhatIf ou-Confirm está definida.</span><span class="sxs-lookup"><span data-stu-id="d74f7-176">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="d74f7-177">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="d74f7-177">-WhatIfResultFormat</span></span>
<span data-ttu-id="d74f7-178">O formato de resultado What-If.</span><span class="sxs-lookup"><span data-stu-id="d74f7-178">The What-If result format.</span></span> <span data-ttu-id="d74f7-179">Aplicável quando a opção-WhatIf ou-Confirm está definida.</span><span class="sxs-lookup"><span data-stu-id="d74f7-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="d74f7-180">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d74f7-180">-Confirm</span></span>
<span data-ttu-id="d74f7-181">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d74f7-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d74f7-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d74f7-182">-WhatIf</span></span>
<span data-ttu-id="d74f7-183">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d74f7-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d74f7-184">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d74f7-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d74f7-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74f7-185">CommonParameters</span></span>
<span data-ttu-id="d74f7-186">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d74f7-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74f7-187">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d74f7-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74f7-188">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d74f7-188">INPUTS</span></span>

### <span data-ttu-id="d74f7-189">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d74f7-189">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d74f7-190">System. String</span><span class="sxs-lookup"><span data-stu-id="d74f7-190">System.String</span></span>

## <span data-ttu-id="d74f7-191">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d74f7-191">OUTPUTS</span></span>

### <span data-ttu-id="d74f7-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="d74f7-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d74f7-193">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d74f7-193">NOTES</span></span>

## <span data-ttu-id="d74f7-194">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d74f7-194">RELATED LINKS</span></span>
