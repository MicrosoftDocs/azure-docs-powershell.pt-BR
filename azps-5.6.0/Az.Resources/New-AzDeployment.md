---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 42f68065fb5a1785d0f9a243d0165bc72125743d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885521"
---
# <span data-ttu-id="1e2c2-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1e2c2-101">New-AzDeployment</span></span>

## <span data-ttu-id="1e2c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2c2-103">Criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="1e2c2-103">Create a deployment</span></span>

## <span data-ttu-id="1e2c2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1e2c2-104">SYNTAX</span></span>

### <span data-ttu-id="1e2c2-105">ByTemplateFileWithNoParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1e2c2-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e2c2-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e2c2-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e2c2-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="1e2c2-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e2c2-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e2c2-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e2c2-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="1e2c2-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1e2c2-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1e2c2-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1e2c2-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="1e2c2-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1e2c2-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1e2c2-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e2c2-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="1e2c2-120">ByTemplateSpecResourceId</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e2c2-121">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1e2c2-121">DESCRIPTION</span></span>
<span data-ttu-id="1e2c2-122">O cmdlet **New-AzDeployment** adiciona uma implantação no escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-122">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="1e2c2-123">Isso inclui os recursos necessários para a implantação.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-123">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="1e2c2-124">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-124">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="1e2c2-125">Um recurso pode residir em um grupo de recursos, como servidor de banco de dados, banco de dados, site, máquina virtual ou conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-125">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="1e2c2-126">Ou pode ser um recurso de nível de assinatura, como definição de função, definição de política, etc.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-126">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="1e2c2-127">Para adicionar recursos a um grupo de recursos, use **o New-AzResourceGroupDeployment** que cria uma implantação em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-127">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="1e2c2-128">O cmdlet **New-AzDeployment** cria uma implantação no escopo de assinatura atual, que implanta recursos de nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-128">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="1e2c2-129">Para adicionar uma implantação na assinatura, especifique o local e um modelo.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-129">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="1e2c2-130">O local informa ao Gerente de Recursos do Azure onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-130">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="1e2c2-131">O modelo é uma cadeia de caracteres JSON que contém recursos individuais a serem implantados.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-131">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="1e2c2-132">O modelo inclui os espaço reservados para parâmetros para recursos necessários e valores de propriedades configuráveis, como nomes e tamanhos.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-132">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="1e2c2-133">Para usar um modelo personalizado para a implantação, especifique o parâmetro *TemplateFile* ou *o parâmetro TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="1e2c2-133">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="1e2c2-134">Cada modelo tem parâmetros para propriedades configuráveis.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-134">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="1e2c2-135">Para especificar valores para os parâmetros de modelo, especifique o *parâmetro TemplateParameterFile* ou *o parâmetro TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="1e2c2-135">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="1e2c2-136">Como alternativa, você pode usar os parâmetros de modelo adicionados dinamicamente ao comando ao especificar um modelo.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-136">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="1e2c2-137">Para usar parâmetros dinâmicos, digite-os no prompt de comando ou digite um sinal de menos (-) para indicar um parâmetro e use a tecla Tab para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-137">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="1e2c2-138">Os valores de parâmetro de modelo que você inserir no prompt de comando têm precedência sobre os valores em um objeto ou arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-138">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="1e2c2-139">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e2c2-139">EXAMPLES</span></span>

### <span data-ttu-id="1e2c2-140">Exemplo 1: usar um modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="1e2c2-140">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="1e2c2-141">Este comando cria uma nova implantação no escopo de assinatura atual usando um modelo personalizado e um arquivo de modelo em disco, com parâmetro de marcas definidas.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="1e2c2-142">O comando usa o *parâmetro TemplateFile* para especificar o modelo e o *parâmetro TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-142">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="1e2c2-143">Ele usa o *parâmetro TemplateVersion* para especificar a versão do modelo.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-143">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="1e2c2-144">Exemplo 2: Implantar um modelo armazenado em uma conta de armazenamento não pública usando um uri e um token SAS</span><span class="sxs-lookup"><span data-stu-id="1e2c2-144">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="1e2c2-145">Este comando cria uma nova implantação usando o modelo em TemplateUri que não é público e requer um parâmetro token para acessar o qual seria fornecido usando o parâmetro QueryString.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-145">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="1e2c2-146">Executar esse comando acessa efetivamente o modelo usando a url https://example.com/example.json?foo .</span><span class="sxs-lookup"><span data-stu-id="1e2c2-146">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="1e2c2-147">Isso pode ser usado se você quiser usar um modelo em uma conta de armazenamento fornecendo o token SAS como o QueryString</span><span class="sxs-lookup"><span data-stu-id="1e2c2-147">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="1e2c2-148">Exemplo 3: usar um objeto de modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="1e2c2-148">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="1e2c2-149">Este comando cria uma nova implantação no escopo de assinatura atual usando um modelo personalizado e um arquivo de modelo em disco que foi convertido em uma hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-149">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="1e2c2-150">Os dois primeiros comandos leem o texto do arquivo de modelo no disco e o convertem em uma hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-150">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="1e2c2-151">O último comando usa o *parâmetro TemplateObject* para especificar essa hashtable e o *parâmetro TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-151">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="1e2c2-152">Ele usa o *parâmetro TemplateVersion* para especificar a versão do modelo.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-152">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="1e2c2-153">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1e2c2-153">PARAMETERS</span></span>

### <span data-ttu-id="1e2c2-154">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e2c2-154">-AsJob</span></span>
<span data-ttu-id="1e2c2-155">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1e2c2-155">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e2c2-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e2c2-156">-DefaultProfile</span></span>
<span data-ttu-id="1e2c2-157">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e2c2-158">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="1e2c2-158">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="1e2c2-159">O nível de log de depuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-159">The deployment debug log level.</span></span>

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

### <span data-ttu-id="1e2c2-160">-Location</span><span class="sxs-lookup"><span data-stu-id="1e2c2-160">-Location</span></span>
<span data-ttu-id="1e2c2-161">O local para armazenar dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-161">The location to store deployment data.</span></span>

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

### <span data-ttu-id="1e2c2-162">-Name</span><span class="sxs-lookup"><span data-stu-id="1e2c2-162">-Name</span></span>
<span data-ttu-id="1e2c2-163">O nome da implantação que ele criará.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-163">The name of the deployment it's going to create.</span></span> <span data-ttu-id="1e2c2-164">Se não for especificado, o padrão é o nome do arquivo de modelo quando um arquivo de modelo é fornecido; padrão para a hora atual em que um objeto template é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="1e2c2-164">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="1e2c2-165">-Pre</span><span class="sxs-lookup"><span data-stu-id="1e2c2-165">-Pre</span></span>
<span data-ttu-id="1e2c2-166">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-166">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1e2c2-167">-QueryString</span><span class="sxs-lookup"><span data-stu-id="1e2c2-167">-QueryString</span></span>
<span data-ttu-id="1e2c2-168">A cadeia de caracteres de consulta (por exemplo, um token SAS) a ser usada com o parâmetro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-168">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="1e2c2-169">Seria usado no caso de modelos vinculados</span><span class="sxs-lookup"><span data-stu-id="1e2c2-169">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="1e2c2-170">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="1e2c2-170">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="1e2c2-171">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-171">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="1e2c2-172">Essa verificação solicitaria que o usuário fornecesse um valor para os parâmetros ausentes, mas o fornecimento de -SkipTemplateParameterPrompt ignorará esse prompt e o excluirá imediatamente se um parâmetro não tiver sido vinculado no modelo.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-172">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="1e2c2-173">Para scripts não interativos, -SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso nem todos os parâmetros necessários sejam atendidos.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-173">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="1e2c2-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="1e2c2-174">-Tag</span></span>
<span data-ttu-id="1e2c2-175">As marcas a ser colocadas na implantação.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-175">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="1e2c2-176">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1e2c2-176">-TemplateFile</span></span>
<span data-ttu-id="1e2c2-177">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-177">Local path to the template file.</span></span> <span data-ttu-id="1e2c2-178">Tipo de arquivo de modelo com suporte: json e bicep.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-178">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="1e2c2-179">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="1e2c2-179">-TemplateObject</span></span>
<span data-ttu-id="1e2c2-180">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-180">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="1e2c2-181">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e2c2-181">-TemplateParameterFile</span></span>
<span data-ttu-id="1e2c2-182">Um arquivo que tem os parâmetros do modelo.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-182">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="1e2c2-183">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e2c2-183">-TemplateParameterObject</span></span>
<span data-ttu-id="1e2c2-184">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-184">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject, ByTemplateSpecResourceIdAndParamsObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2c2-185">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="1e2c2-185">-TemplateParameterUri</span></span>
<span data-ttu-id="1e2c2-186">Uri para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-186">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="1e2c2-187">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="1e2c2-187">-TemplateSpecId</span></span>
<span data-ttu-id="1e2c2-188">ID do recurso do modeloSpec a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-188">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParamsObject, ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2c2-189">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="1e2c2-189">-TemplateUri</span></span>
<span data-ttu-id="1e2c2-190">Uri para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-190">Uri to the template file.</span></span>

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

### <span data-ttu-id="1e2c2-191">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="1e2c2-191">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="1e2c2-192">Tipos de alteração de recursos separados por vírgulas a serem excluídos dos What-If resultados.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-192">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="1e2c2-193">Aplicável quando a opção -WhatIf ou -Confirm estiver definida.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-193">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="1e2c2-194">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="1e2c2-194">-WhatIfResultFormat</span></span>
<span data-ttu-id="1e2c2-195">O What-If de resultados.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-195">The What-If result format.</span></span>

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

### <span data-ttu-id="1e2c2-196">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e2c2-196">-Confirm</span></span>
<span data-ttu-id="1e2c2-197">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e2c2-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e2c2-198">-WhatIf</span></span>
<span data-ttu-id="1e2c2-199">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e2c2-200">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e2c2-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2c2-201">CommonParameters</span></span>
<span data-ttu-id="1e2c2-202">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e2c2-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2c2-203">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e2c2-203">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2c2-204">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e2c2-204">INPUTS</span></span>

### <span data-ttu-id="1e2c2-205">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e2c2-205">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1e2c2-206">System.String</span><span class="sxs-lookup"><span data-stu-id="1e2c2-206">System.String</span></span>

## <span data-ttu-id="1e2c2-207">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1e2c2-207">OUTPUTS</span></span>

### <span data-ttu-id="1e2c2-208">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="1e2c2-208">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1e2c2-209">NOTES</span><span class="sxs-lookup"><span data-stu-id="1e2c2-209">NOTES</span></span>

## <span data-ttu-id="1e2c2-210">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e2c2-210">RELATED LINKS</span></span>
