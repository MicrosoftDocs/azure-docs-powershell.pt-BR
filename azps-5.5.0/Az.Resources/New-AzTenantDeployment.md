---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: d2a54022768bd3751ed18713fdc123ef2ef9cbf1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118745"
---
# <span data-ttu-id="fe523-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="fe523-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="fe523-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe523-102">SYNOPSIS</span></span>
<span data-ttu-id="fe523-103">Criar uma implantação no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="fe523-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="fe523-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe523-104">SYNTAX</span></span>

### <span data-ttu-id="fe523-105">ByTemplateFileWithNoParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fe523-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe523-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="fe523-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe523-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="fe523-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe523-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="fe523-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe523-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="fe523-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe523-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="fe523-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe523-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="fe523-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe523-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="fe523-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe523-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="fe523-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe523-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="fe523-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe523-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="fe523-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe523-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="fe523-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe523-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="fe523-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe523-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="fe523-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe523-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="fe523-119">ByTemplateSpecResourceId</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe523-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe523-120">DESCRIPTION</span></span>
<span data-ttu-id="fe523-121">O **cmdlet New-AzTenantDeployment** adiciona uma implantação no escopo atual do locatário.</span><span class="sxs-lookup"><span data-stu-id="fe523-121">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="fe523-122">Para adicionar uma implantação no escopo do locatário, especifique o local e um modelo.</span><span class="sxs-lookup"><span data-stu-id="fe523-122">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="fe523-123">O local informa ao Gerenciador de Recursos do Azure onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="fe523-123">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="fe523-124">O modelo é uma cadeia de caracteres JSON que contém recursos individuais a serem implantados.</span><span class="sxs-lookup"><span data-stu-id="fe523-124">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="fe523-125">O modelo inclui os espaço reservados para parâmetros para recursos necessários e valores de propriedades configuráveis, como nomes e tamanhos.</span><span class="sxs-lookup"><span data-stu-id="fe523-125">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="fe523-126">Para usar um modelo personalizado para a implantação, especifique o parâmetro *TemplateFile* ou *o parâmetro TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="fe523-126">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="fe523-127">Cada modelo tem parâmetros para propriedades configuráveis.</span><span class="sxs-lookup"><span data-stu-id="fe523-127">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="fe523-128">Para especificar valores para os parâmetros de modelo, especifique o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="fe523-128">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="fe523-129">Como alternativa, você pode usar os parâmetros de modelo que são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="fe523-129">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="fe523-130">Para usar parâmetros dinâmicos, digite-os no prompt de comando ou digite um sinal de subtração (-) para indicar um parâmetro e use a tecla Tab para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fe523-130">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="fe523-131">Os valores de parâmetro de modelo que você inserir no prompt de comando têm precedência sobre os valores em um objeto ou arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="fe523-131">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="fe523-132">Para adicionar recursos a um grupo de recursos, use o **New-AzResourceGroupDeployment que** cria uma implantação em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe523-132">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="fe523-133">Para adicionar recursos a uma assinatura, use o **New-AzSubscriptionDeployment,** que cria uma implantação no escopo da assinatura, que implanta recursos de nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="fe523-133">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="fe523-134">Para adicionar recursos a um grupo de gerenciamento, use o **New-AzManagementGroupDeployment que** cria uma implantação em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fe523-134">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="fe523-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fe523-135">EXAMPLES</span></span>

### <span data-ttu-id="fe523-136">Exemplo 1: Usar um modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="fe523-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="fe523-137">Esse comando cria uma nova implantação no escopo do locatário atual usando um modelo personalizado e um arquivo de modelo no disco, com parâmetro de marcas definidas.</span><span class="sxs-lookup"><span data-stu-id="fe523-137">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="fe523-138">O comando usa o parâmetro *TemplateFile* para especificar o modelo e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fe523-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="fe523-139">Exemplo 2: Usar um objeto de modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="fe523-139">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="fe523-140">Esse comando cria uma nova implantação no locatário atual usando um modelo personalizado e um arquivo de modelo no disco que foi convertido em uma hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="fe523-140">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="fe523-141">Os dois primeiros comandos leem o texto do arquivo de modelo em disco e o convertem em uma hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="fe523-141">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="fe523-142">O último comando usa o parâmetro *TemplateObject* para especificar essa tabela hash e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fe523-142">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="fe523-143">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe523-143">PARAMETERS</span></span>

### <span data-ttu-id="fe523-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe523-144">-AsJob</span></span>
<span data-ttu-id="fe523-145">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fe523-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe523-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe523-146">-DefaultProfile</span></span>
<span data-ttu-id="fe523-147">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe523-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe523-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="fe523-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="fe523-149">O nível de log de depuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="fe523-149">The deployment debug log level.</span></span>

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

### <span data-ttu-id="fe523-150">-Local</span><span class="sxs-lookup"><span data-stu-id="fe523-150">-Location</span></span>
<span data-ttu-id="fe523-151">O local para armazenar dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="fe523-151">The location to store deployment data.</span></span>

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

### <span data-ttu-id="fe523-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe523-152">-Name</span></span>
<span data-ttu-id="fe523-153">O nome da implantação que ele vai criar.</span><span class="sxs-lookup"><span data-stu-id="fe523-153">The name of the deployment it's going to create.</span></span> <span data-ttu-id="fe523-154">Se não especificado, o padrão é o nome do arquivo de modelo quando um arquivo de modelo é fornecido; padrão para a hora atual quando um objeto de modelo é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="fe523-154">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="fe523-155">-Pré-</span><span class="sxs-lookup"><span data-stu-id="fe523-155">-Pre</span></span>
<span data-ttu-id="fe523-156">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="fe523-156">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fe523-157">-QueryString</span><span class="sxs-lookup"><span data-stu-id="fe523-157">-QueryString</span></span>
<span data-ttu-id="fe523-158">A cadeia de caracteres de consulta (por exemplo, um token SAS) a ser usado com o parâmetro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="fe523-158">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="fe523-159">Seria usado no caso de modelos vinculados</span><span class="sxs-lookup"><span data-stu-id="fe523-159">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="fe523-160">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="fe523-160">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="fe523-161">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="fe523-161">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="fe523-162">Essa verificação solicitaria que o usuário fornecesse um valor para os parâmetros ausentes, mas fornecer o -SkipTemplateParameterPrompt ignorará esse prompt e um erro imediatamente se um parâmetro não tiver sido vinculado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="fe523-162">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="fe523-163">Para scripts não interativos, -SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso nem todos os parâmetros necessários sejam satisfeitos.</span><span class="sxs-lookup"><span data-stu-id="fe523-163">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="fe523-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe523-164">-Tag</span></span>
<span data-ttu-id="fe523-165">As marcas a colocar na implantação.</span><span class="sxs-lookup"><span data-stu-id="fe523-165">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="fe523-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="fe523-166">-TemplateFile</span></span>
<span data-ttu-id="fe523-167">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="fe523-167">Local path to the template file.</span></span>

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

### <span data-ttu-id="fe523-168">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="fe523-168">-TemplateObject</span></span>
<span data-ttu-id="fe523-169">Uma tabela hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="fe523-169">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="fe523-170">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="fe523-170">-TemplateParameterFile</span></span>
<span data-ttu-id="fe523-171">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="fe523-171">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile, ByTemplateSpecResourceIdAndParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe523-172">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="fe523-172">-TemplateParameterObject</span></span>
<span data-ttu-id="fe523-173">Uma tabela hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fe523-173">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="fe523-174">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="fe523-174">-TemplateParameterUri</span></span>
<span data-ttu-id="fe523-175">Uri para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="fe523-175">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri, ByTemplateSpecResourceIdAndParamsUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe523-176">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="fe523-176">-TemplateSpecId</span></span>
<span data-ttu-id="fe523-177">ID do recurso do modeloSpec a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="fe523-177">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe523-178">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="fe523-178">-TemplateUri</span></span>
<span data-ttu-id="fe523-179">Uri para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="fe523-179">Uri to the template file.</span></span>

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

### <span data-ttu-id="fe523-180">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="fe523-180">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="fe523-181">Tipos de alteração de recursos separados por vírgulas a serem excluídos What-If resultados.</span><span class="sxs-lookup"><span data-stu-id="fe523-181">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="fe523-182">Aplicável quando a opção -WhatIf ou -Confirm estiver definida.</span><span class="sxs-lookup"><span data-stu-id="fe523-182">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="fe523-183">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="fe523-183">-WhatIfResultFormat</span></span>
<span data-ttu-id="fe523-184">O What-If de resultados.</span><span class="sxs-lookup"><span data-stu-id="fe523-184">The What-If result format.</span></span> <span data-ttu-id="fe523-185">Aplicável quando a opção -WhatIf ou -Confirm estiver definida.</span><span class="sxs-lookup"><span data-stu-id="fe523-185">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="fe523-186">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fe523-186">-Confirm</span></span>
<span data-ttu-id="fe523-187">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe523-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe523-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe523-188">-WhatIf</span></span>
<span data-ttu-id="fe523-189">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fe523-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe523-190">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe523-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe523-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe523-191">CommonParameters</span></span>
<span data-ttu-id="fe523-192">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe523-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe523-193">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe523-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe523-194">Entradas</span><span class="sxs-lookup"><span data-stu-id="fe523-194">INPUTS</span></span>

### <span data-ttu-id="fe523-195">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fe523-195">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fe523-196">System.String</span><span class="sxs-lookup"><span data-stu-id="fe523-196">System.String</span></span>

## <span data-ttu-id="fe523-197">Saídas</span><span class="sxs-lookup"><span data-stu-id="fe523-197">OUTPUTS</span></span>

### <span data-ttu-id="fe523-198">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="fe523-198">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="fe523-199">Notas</span><span class="sxs-lookup"><span data-stu-id="fe523-199">NOTES</span></span>

## <span data-ttu-id="fe523-200">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe523-200">RELATED LINKS</span></span>
