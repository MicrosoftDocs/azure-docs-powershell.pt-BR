---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: d3b9fce538512fdb55328d6c2e846c955bcfbb5d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113323"
---
# <span data-ttu-id="e9e84-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e9e84-101">New-AzDeployment</span></span>

## <span data-ttu-id="e9e84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9e84-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e84-103">Criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="e9e84-103">Create a deployment</span></span>

## <span data-ttu-id="e9e84-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9e84-104">SYNTAX</span></span>

### <span data-ttu-id="e9e84-105">ByTemplateFileWithNoParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e9e84-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e9e84-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e9e84-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e9e84-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e9e84-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e9e84-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e9e84-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="e9e84-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e9e84-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e9e84-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e9e84-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="e9e84-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e9e84-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e9e84-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e84-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="e9e84-119">ByTemplateSpecResourceId</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9e84-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9e84-120">DESCRIPTION</span></span>
<span data-ttu-id="e9e84-121">O **cmdlet New-AzDeployment** adiciona uma implantação no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e9e84-121">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="e9e84-122">Isso inclui os recursos necessários para a implantação.</span><span class="sxs-lookup"><span data-stu-id="e9e84-122">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="e9e84-123">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e9e84-123">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="e9e84-124">Um recurso pode residir em um grupo de recursos, como servidor de banco de dados, banco de dados, site, computador virtual ou conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e9e84-124">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="e9e84-125">Ou pode ser um recurso de nível de assinatura, como definição de função, definição de política etc.</span><span class="sxs-lookup"><span data-stu-id="e9e84-125">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="e9e84-126">Para adicionar recursos a um grupo de recursos, use o **New-AzResourceGroupDeployment que** cria uma implantação em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9e84-126">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="e9e84-127">O cmdlet **New-AzDeployment** cria uma implantação no escopo da assinatura atual, que implanta recursos de nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e9e84-127">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="e9e84-128">Para adicionar uma implantação à assinatura, especifique o local e um modelo.</span><span class="sxs-lookup"><span data-stu-id="e9e84-128">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="e9e84-129">O local informa ao Gerenciador de Recursos do Azure onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="e9e84-129">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="e9e84-130">O modelo é uma cadeia de caracteres JSON que contém recursos individuais a serem implantados.</span><span class="sxs-lookup"><span data-stu-id="e9e84-130">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="e9e84-131">O modelo inclui os espaço reservados para parâmetros para recursos necessários e valores de propriedades configuráveis, como nomes e tamanhos.</span><span class="sxs-lookup"><span data-stu-id="e9e84-131">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="e9e84-132">Para usar um modelo personalizado para a implantação, especifique o parâmetro *TemplateFile* ou *o parâmetro TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="e9e84-132">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="e9e84-133">Cada modelo tem parâmetros para propriedades configuráveis.</span><span class="sxs-lookup"><span data-stu-id="e9e84-133">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="e9e84-134">Para especificar valores para os parâmetros de modelo, especifique o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="e9e84-134">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="e9e84-135">Como alternativa, você pode usar os parâmetros de modelo que são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="e9e84-135">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="e9e84-136">Para usar parâmetros dinâmicos, digite-os no prompt de comando ou digite um sinal de subtração (-) para indicar um parâmetro e use a tecla Tab para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e9e84-136">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="e9e84-137">Os valores de parâmetro de modelo que você inserir no prompt de comando têm precedência sobre os valores em um objeto ou arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="e9e84-137">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="e9e84-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e9e84-138">EXAMPLES</span></span>

### <span data-ttu-id="e9e84-139">Exemplo 1: Usar um modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="e9e84-139">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="e9e84-140">Esse comando cria uma nova implantação no escopo da assinatura atual usando um modelo personalizado e um arquivo de modelo em disco, com parâmetro de marcas definidas.</span><span class="sxs-lookup"><span data-stu-id="e9e84-140">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="e9e84-141">O comando usa o parâmetro *TemplateFile* para especificar o modelo e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e9e84-141">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="e9e84-142">Ele usa o *parâmetro TemplateVersion* para especificar a versão do modelo.</span><span class="sxs-lookup"><span data-stu-id="e9e84-142">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="e9e84-143">Exemplo 2: Implantar um modelo armazenado em uma conta de armazenamento não pública usando um uri e um token SAS</span><span class="sxs-lookup"><span data-stu-id="e9e84-143">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="e9e84-144">Esse comando cria uma nova implantação usando o modelo no TemplateUri, que não é público e requer um parâmetro de token para acessar que seria fornecido usando o parâmetro QueryString.</span><span class="sxs-lookup"><span data-stu-id="e9e84-144">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="e9e84-145">Executar esse comando acessa efetivamente o modelo usando a https://example.com/example.json?foo URL.</span><span class="sxs-lookup"><span data-stu-id="e9e84-145">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="e9e84-146">Isso pode ser usado se você quiser usar um modelo em uma conta de armazenamento fornecendo o token SAS como o QueryString</span><span class="sxs-lookup"><span data-stu-id="e9e84-146">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="e9e84-147">Exemplo 3: Usar um objeto de modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="e9e84-147">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="e9e84-148">Esse comando cria uma nova implantação no escopo da assinatura atual usando um modelo personalizado e um arquivo de modelo no disco que foi convertido em uma tabela de hash na memória.</span><span class="sxs-lookup"><span data-stu-id="e9e84-148">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="e9e84-149">Os dois primeiros comandos leem o texto do arquivo de modelo em disco e o convertem em uma hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="e9e84-149">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="e9e84-150">O último comando usa o parâmetro *TemplateObject* para especificar essa tabela hash e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e9e84-150">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="e9e84-151">Ele usa o *parâmetro TemplateVersion* para especificar a versão do modelo.</span><span class="sxs-lookup"><span data-stu-id="e9e84-151">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="e9e84-152">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9e84-152">PARAMETERS</span></span>

### <span data-ttu-id="e9e84-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9e84-153">-AsJob</span></span>
<span data-ttu-id="e9e84-154">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e9e84-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9e84-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e84-155">-DefaultProfile</span></span>
<span data-ttu-id="e9e84-156">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e84-156">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9e84-157">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="e9e84-157">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="e9e84-158">O nível de log de depuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="e9e84-158">The deployment debug log level.</span></span>

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

### <span data-ttu-id="e9e84-159">-Local</span><span class="sxs-lookup"><span data-stu-id="e9e84-159">-Location</span></span>
<span data-ttu-id="e9e84-160">O local para armazenar dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="e9e84-160">The location to store deployment data.</span></span>

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

### <span data-ttu-id="e9e84-161">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9e84-161">-Name</span></span>
<span data-ttu-id="e9e84-162">O nome da implantação que ele vai criar.</span><span class="sxs-lookup"><span data-stu-id="e9e84-162">The name of the deployment it's going to create.</span></span> <span data-ttu-id="e9e84-163">Se não especificado, o padrão é o nome do arquivo de modelo quando um arquivo de modelo é fornecido; padrão para a hora atual quando um objeto de modelo é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="e9e84-163">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="e9e84-164">-Pré-</span><span class="sxs-lookup"><span data-stu-id="e9e84-164">-Pre</span></span>
<span data-ttu-id="e9e84-165">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e9e84-165">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e9e84-166">-QueryString</span><span class="sxs-lookup"><span data-stu-id="e9e84-166">-QueryString</span></span>
<span data-ttu-id="e9e84-167">A cadeia de caracteres de consulta (por exemplo, um token SAS) a ser usado com o parâmetro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="e9e84-167">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="e9e84-168">Seria usado no caso de modelos vinculados</span><span class="sxs-lookup"><span data-stu-id="e9e84-168">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="e9e84-169">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="e9e84-169">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="e9e84-170">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="e9e84-170">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="e9e84-171">Essa verificação solicitaria que o usuário fornecesse um valor para os parâmetros ausentes, mas fornecer o -SkipTemplateParameterPrompt ignorará esse prompt e um erro imediatamente se um parâmetro não tiver sido vinculado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="e9e84-171">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="e9e84-172">Para scripts não interativos, -SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso nem todos os parâmetros necessários sejam satisfeitos.</span><span class="sxs-lookup"><span data-stu-id="e9e84-172">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="e9e84-173">-Tag</span><span class="sxs-lookup"><span data-stu-id="e9e84-173">-Tag</span></span>
<span data-ttu-id="e9e84-174">As marcas a colocar na implantação.</span><span class="sxs-lookup"><span data-stu-id="e9e84-174">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="e9e84-175">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e9e84-175">-TemplateFile</span></span>
<span data-ttu-id="e9e84-176">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="e9e84-176">Local path to the template file.</span></span>

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

### <span data-ttu-id="e9e84-177">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="e9e84-177">-TemplateObject</span></span>
<span data-ttu-id="e9e84-178">Uma tabela hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="e9e84-178">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="e9e84-179">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e9e84-179">-TemplateParameterFile</span></span>
<span data-ttu-id="e9e84-180">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="e9e84-180">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="e9e84-181">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e9e84-181">-TemplateParameterObject</span></span>
<span data-ttu-id="e9e84-182">Uma tabela hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e9e84-182">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="e9e84-183">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e9e84-183">-TemplateParameterUri</span></span>
<span data-ttu-id="e9e84-184">Uri para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="e9e84-184">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="e9e84-185">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="e9e84-185">-TemplateSpecId</span></span>
<span data-ttu-id="e9e84-186">ID do recurso do modeloSpec a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="e9e84-186">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="e9e84-187">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e9e84-187">-TemplateUri</span></span>
<span data-ttu-id="e9e84-188">Uri para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="e9e84-188">Uri to the template file.</span></span>

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

### <span data-ttu-id="e9e84-189">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="e9e84-189">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="e9e84-190">Tipos de alteração de recursos separados por vírgulas a serem excluídos What-If resultados.</span><span class="sxs-lookup"><span data-stu-id="e9e84-190">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="e9e84-191">Aplicável quando a opção -WhatIf ou -Confirm estiver definida.</span><span class="sxs-lookup"><span data-stu-id="e9e84-191">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="e9e84-192">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="e9e84-192">-WhatIfResultFormat</span></span>
<span data-ttu-id="e9e84-193">O What-If de resultados.</span><span class="sxs-lookup"><span data-stu-id="e9e84-193">The What-If result format.</span></span>

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

### <span data-ttu-id="e9e84-194">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e9e84-194">-Confirm</span></span>
<span data-ttu-id="e9e84-195">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9e84-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9e84-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9e84-196">-WhatIf</span></span>
<span data-ttu-id="e9e84-197">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e9e84-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9e84-198">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9e84-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9e84-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e84-199">CommonParameters</span></span>
<span data-ttu-id="e9e84-200">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e84-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e84-201">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9e84-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e84-202">Entradas</span><span class="sxs-lookup"><span data-stu-id="e9e84-202">INPUTS</span></span>

### <span data-ttu-id="e9e84-203">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e9e84-203">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e9e84-204">System.String</span><span class="sxs-lookup"><span data-stu-id="e9e84-204">System.String</span></span>

## <span data-ttu-id="e9e84-205">Saídas</span><span class="sxs-lookup"><span data-stu-id="e9e84-205">OUTPUTS</span></span>

### <span data-ttu-id="e9e84-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="e9e84-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="e9e84-207">Notas</span><span class="sxs-lookup"><span data-stu-id="e9e84-207">NOTES</span></span>

## <span data-ttu-id="e9e84-208">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9e84-208">RELATED LINKS</span></span>
