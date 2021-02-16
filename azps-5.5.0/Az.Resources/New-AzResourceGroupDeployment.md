---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 3e704885c4ce2df0aee2a9b890f768983f93d7bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113317"
---
# <span data-ttu-id="0b97a-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0b97a-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="0b97a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b97a-102">SYNOPSIS</span></span>
<span data-ttu-id="0b97a-103">Adiciona uma implantação do Azure a um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b97a-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="0b97a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b97a-104">SYNTAX</span></span>

### <span data-ttu-id="0b97a-105">ByTemplateFileWithNoParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0b97a-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b97a-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0b97a-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b97a-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0b97a-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b97a-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0b97a-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b97a-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0b97a-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b97a-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0b97a-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b97a-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0b97a-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b97a-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="0b97a-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b97a-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0b97a-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b97a-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0b97a-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b97a-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0b97a-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b97a-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="0b97a-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b97a-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0b97a-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b97a-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0b97a-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b97a-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="0b97a-119">ByTemplateSpecResourceId</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b97a-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b97a-120">DESCRIPTION</span></span>
<span data-ttu-id="0b97a-121">O cmdlet **New-AzResourceGroupDeployment** adiciona uma implantação a um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="0b97a-121">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="0b97a-122">Isso inclui os recursos necessários para a implantação.</span><span class="sxs-lookup"><span data-stu-id="0b97a-122">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="0b97a-123">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, um banco de dados, um site, uma máquina virtual ou uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b97a-123">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="0b97a-124">Um grupo de recursos do Azure é um conjunto de recursos do Azure implantados como uma unidade, como o site, o servidor de banco de dados e os bancos de dados necessários para um site financeiro.</span><span class="sxs-lookup"><span data-stu-id="0b97a-124">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="0b97a-125">Uma implantação de grupo de recursos usa um modelo para adicionar recursos a um grupo de recursos e os publica para que eles sejam disponibilizados no Azure.</span><span class="sxs-lookup"><span data-stu-id="0b97a-125">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="0b97a-126">Para adicionar recursos a um grupo de recursos sem usar um modelo, use New-AzResource cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b97a-126">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="0b97a-127">Para adicionar uma implantação de grupo de recursos, especifique o nome de um grupo de recursos existente e um modelo de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b97a-127">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="0b97a-128">Um modelo de grupo de recursos é uma cadeia de caracteres JSON que representa um grupo de recursos para um serviço complexo baseado em nuvem, como um portal da Web.</span><span class="sxs-lookup"><span data-stu-id="0b97a-128">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="0b97a-129">O modelo inclui os espaço reservados para parâmetros para recursos necessários e valores de propriedades configuráveis, como nomes e tamanhos.</span><span class="sxs-lookup"><span data-stu-id="0b97a-129">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="0b97a-130">Você pode encontrar muitos modelos na galeria de modelos do Azure ou pode criar seus próprios modelos.</span><span class="sxs-lookup"><span data-stu-id="0b97a-130">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="0b97a-131">Para usar um modelo personalizado para criar um grupo de recursos, especifique o parâmetro *TemplateFile* ou *o parâmetro TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="0b97a-131">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="0b97a-132">Cada modelo tem parâmetros para propriedades configuráveis.</span><span class="sxs-lookup"><span data-stu-id="0b97a-132">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="0b97a-133">Para especificar valores para os parâmetros de modelo, especifique o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="0b97a-133">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="0b97a-134">Como alternativa, você pode usar os parâmetros de modelo que são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="0b97a-134">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="0b97a-135">Para usar parâmetros dinâmicos, digite-os no prompt de comando ou digite um sinal de subtração (-) para indicar um parâmetro e use a tecla Tab para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0b97a-135">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="0b97a-136">Os valores de parâmetro de modelo que você inserir no prompt de comando têm precedência sobre os valores em um objeto ou arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="0b97a-136">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="0b97a-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b97a-137">EXAMPLES</span></span>

### <span data-ttu-id="0b97a-138">Exemplo 1: Usar um modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="0b97a-138">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="0b97a-139">Esse comando cria uma nova implantação usando um modelo personalizado e um arquivo de modelo em disco, com parâmetro de marcas definido.</span><span class="sxs-lookup"><span data-stu-id="0b97a-139">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="0b97a-140">O comando usa o parâmetro *TemplateFile* para especificar o modelo e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0b97a-140">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="0b97a-141">Exemplo 2: Usar um objeto de modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="0b97a-141">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="0b97a-142">Esse comando cria uma nova implantação usando um arquivo personalizado e um arquivo de modelo no disco que foi convertido em uma hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="0b97a-142">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="0b97a-143">Os dois primeiros comandos leem o texto do arquivo de modelo em disco e o convertem em uma hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="0b97a-143">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="0b97a-144">O último comando usa o parâmetro *TemplateObject* para especificar a tabela hash e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0b97a-144">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="0b97a-145">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0b97a-145">Example 3</span></span>

<span data-ttu-id="0b97a-146">Adiciona uma implantação do Azure a um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b97a-146">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="0b97a-147">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="0b97a-147">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

### <span data-ttu-id="0b97a-148">Exemplo 4: Implantar um modelo armazenado em uma conta de armazenamento não pública usando um uri e um token SAS</span><span class="sxs-lookup"><span data-stu-id="0b97a-148">Example 4: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "RGName" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="0b97a-149">Esse comando cria uma nova implantação usando o modelo no TemplateUri, que não é público e requer um parâmetro de token para acessar que seria fornecido usando o parâmetro QueryString.</span><span class="sxs-lookup"><span data-stu-id="0b97a-149">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="0b97a-150">Executar esse comando acessa efetivamente o modelo usando a https://example.com/example.json?foo URL.</span><span class="sxs-lookup"><span data-stu-id="0b97a-150">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="0b97a-151">Isso pode ser usado se você quiser usar um modelo em uma conta de armazenamento fornecendo o token SAS como o QueryString</span><span class="sxs-lookup"><span data-stu-id="0b97a-151">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>
## <span data-ttu-id="0b97a-152">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b97a-152">PARAMETERS</span></span>

### <span data-ttu-id="0b97a-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b97a-153">-AsJob</span></span>
<span data-ttu-id="0b97a-154">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0b97a-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b97a-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b97a-155">-DefaultProfile</span></span>
<span data-ttu-id="0b97a-156">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0b97a-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b97a-157">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="0b97a-157">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="0b97a-158">Especifica um nível de log de depuração.</span><span class="sxs-lookup"><span data-stu-id="0b97a-158">Specifies a debug log level.</span></span>
<span data-ttu-id="0b97a-159">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0b97a-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b97a-160">RequestContent</span><span class="sxs-lookup"><span data-stu-id="0b97a-160">RequestContent</span></span>
- <span data-ttu-id="0b97a-161">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="0b97a-161">ResponseContent</span></span>
- <span data-ttu-id="0b97a-162">Todos</span><span class="sxs-lookup"><span data-stu-id="0b97a-162">All</span></span>
- <span data-ttu-id="0b97a-163">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0b97a-163">None</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestContent, ResponseContent, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b97a-164">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0b97a-164">-Force</span></span>
<span data-ttu-id="0b97a-165">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0b97a-165">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0b97a-166">-Modo</span><span class="sxs-lookup"><span data-stu-id="0b97a-166">-Mode</span></span>
<span data-ttu-id="0b97a-167">Especifica o modo de implantação.</span><span class="sxs-lookup"><span data-stu-id="0b97a-167">Specifies the deployment mode.</span></span> <span data-ttu-id="0b97a-168">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0b97a-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b97a-169">Concluído: No modo completo, o Gerenciador de Recursos exclui recursos que existem no grupo de recursos, mas não são especificados no modelo.</span><span class="sxs-lookup"><span data-stu-id="0b97a-169">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="0b97a-170">Incremental: No modo incremental, o Gerenciador de Recursos deixa os recursos inalterados que existem no grupo de recursos, mas não são especificados no modelo.</span><span class="sxs-lookup"><span data-stu-id="0b97a-170">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b97a-171">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b97a-171">-Name</span></span>
<span data-ttu-id="0b97a-172">O nome da implantação que ele vai criar.</span><span class="sxs-lookup"><span data-stu-id="0b97a-172">The name of the deployment it's going to create.</span></span> <span data-ttu-id="0b97a-173">Se não especificado, o padrão é o nome do arquivo de modelo quando um arquivo de modelo é fornecido; padrão para a hora atual quando um objeto de modelo é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="0b97a-173">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="0b97a-174">-Pré-</span><span class="sxs-lookup"><span data-stu-id="0b97a-174">-Pre</span></span>
<span data-ttu-id="0b97a-175">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="0b97a-175">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0b97a-176">-QueryString</span><span class="sxs-lookup"><span data-stu-id="0b97a-176">-QueryString</span></span>
<span data-ttu-id="0b97a-177">A cadeia de caracteres de consulta (por exemplo, um token SAS) a ser usado com o parâmetro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="0b97a-177">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="0b97a-178">Seria usado no caso de modelos vinculados</span><span class="sxs-lookup"><span data-stu-id="0b97a-178">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="0b97a-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b97a-179">-ResourceGroupName</span></span>
<span data-ttu-id="0b97a-180">Especifica o nome do grupo de recursos a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="0b97a-180">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="0b97a-181">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="0b97a-181">-RollBackDeploymentName</span></span>
<span data-ttu-id="0b97a-182">A reação à implantação bem-sucedida com o nome determinado no grupo de recursos não deve ser usada se -RollbackToLastDeployment for usado.</span><span class="sxs-lookup"><span data-stu-id="0b97a-182">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b97a-183">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="0b97a-183">-RollbackToLastDeployment</span></span>
<span data-ttu-id="0b97a-184">A reação à última implantação bem-sucedida no grupo de recursos não deverá estar presente se -RollBackDeploymentName for usado.</span><span class="sxs-lookup"><span data-stu-id="0b97a-184">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="0b97a-185">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="0b97a-185">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="0b97a-186">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="0b97a-186">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="0b97a-187">Essa verificação solicitaria que o usuário fornecesse um valor para os parâmetros ausentes, mas fornecer o -SkipTemplateParameterPrompt ignorará esse prompt e um erro imediatamente se um parâmetro não tiver sido vinculado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="0b97a-187">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="0b97a-188">Para scripts não interativos, -SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso nem todos os parâmetros necessários sejam satisfeitos.</span><span class="sxs-lookup"><span data-stu-id="0b97a-188">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="0b97a-189">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b97a-189">-Tag</span></span>
<span data-ttu-id="0b97a-190">As marcas a colocar na implantação.</span><span class="sxs-lookup"><span data-stu-id="0b97a-190">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="0b97a-191">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0b97a-191">-TemplateFile</span></span>
<span data-ttu-id="0b97a-192">Especifica o caminho completo de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="0b97a-192">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="0b97a-193">Pode ser um modelo personalizado ou um modelo de galeria que é salvo como um arquivo JSON, como um criado usando o cmdlet **Save-AzResourceGroupGalleryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="0b97a-193">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="0b97a-194">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="0b97a-194">-TemplateObject</span></span>
<span data-ttu-id="0b97a-195">Uma tabela hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="0b97a-195">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="0b97a-196">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0b97a-196">-TemplateParameterFile</span></span>
<span data-ttu-id="0b97a-197">Especifica o caminho completo de um arquivo JSON que contém os nomes e os valores dos parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="0b97a-197">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="0b97a-198">Se um modelo tiver parâmetros, você deverá especificar os valores de parâmetro com o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="0b97a-198">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="0b97a-199">Os parâmetros de modelo são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="0b97a-199">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="0b97a-200">Para usar os parâmetros dinâmicos, digite um sinal de subtração (-) para indicar um nome de parâmetro e use a tecla Tab para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0b97a-200">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="0b97a-201">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="0b97a-201">-TemplateParameterObject</span></span>
<span data-ttu-id="0b97a-202">Especifica uma tabela hash de nomes e valores de parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="0b97a-202">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="0b97a-203">Para ajuda com tabelas hash no Windows PowerShell, `Get-Help about_Hash_Tables` digite.</span><span class="sxs-lookup"><span data-stu-id="0b97a-203">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="0b97a-204">Se um modelo tiver parâmetros, você deverá especificar valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0b97a-204">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="0b97a-205">Os parâmetros de modelo são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="0b97a-205">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="0b97a-206">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="0b97a-206">-TemplateParameterUri</span></span>
<span data-ttu-id="0b97a-207">Especifica o URI de um arquivo de parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="0b97a-207">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="0b97a-208">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="0b97a-208">-TemplateSpecId</span></span>
<span data-ttu-id="0b97a-209">ID do recurso do modeloSpec a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="0b97a-209">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="0b97a-210">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="0b97a-210">-TemplateUri</span></span>
<span data-ttu-id="0b97a-211">Especifica o URI de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="0b97a-211">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="0b97a-212">Esse arquivo pode ser um modelo personalizado ou um modelo de galeria que é salvo como um arquivo JSON, por exemplo, usando **Save-AzResourceGroupGalleryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="0b97a-212">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="0b97a-213">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="0b97a-213">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="0b97a-214">Tipos de alteração de recursos separados por vírgulas a serem excluídos What-If resultados.</span><span class="sxs-lookup"><span data-stu-id="0b97a-214">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="0b97a-215">Aplicável quando a opção -WhatIf ou -Confirm estiver definida.</span><span class="sxs-lookup"><span data-stu-id="0b97a-215">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="0b97a-216">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="0b97a-216">-WhatIfResultFormat</span></span>
<span data-ttu-id="0b97a-217">O What-If de resultados.</span><span class="sxs-lookup"><span data-stu-id="0b97a-217">The What-If result format.</span></span>

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

### <span data-ttu-id="0b97a-218">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0b97a-218">-Confirm</span></span>
<span data-ttu-id="0b97a-219">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b97a-219">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b97a-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b97a-220">-WhatIf</span></span>
<span data-ttu-id="0b97a-221">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0b97a-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b97a-222">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b97a-222">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b97a-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b97a-223">CommonParameters</span></span>
<span data-ttu-id="0b97a-224">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b97a-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b97a-225">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b97a-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b97a-226">Entradas</span><span class="sxs-lookup"><span data-stu-id="0b97a-226">INPUTS</span></span>

### <span data-ttu-id="0b97a-227">System.String</span><span class="sxs-lookup"><span data-stu-id="0b97a-227">System.String</span></span>

### <span data-ttu-id="0b97a-228">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="0b97a-228">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="0b97a-229">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b97a-229">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b97a-230">Saídas</span><span class="sxs-lookup"><span data-stu-id="0b97a-230">OUTPUTS</span></span>

### <span data-ttu-id="0b97a-231">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0b97a-231">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="0b97a-232">Notas</span><span class="sxs-lookup"><span data-stu-id="0b97a-232">NOTES</span></span>

## <span data-ttu-id="0b97a-233">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b97a-233">RELATED LINKS</span></span>

[<span data-ttu-id="0b97a-234">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0b97a-234">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="0b97a-235">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="0b97a-235">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="0b97a-236">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b97a-236">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="0b97a-237">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0b97a-237">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="0b97a-238">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0b97a-238">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="0b97a-239">Teste-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0b97a-239">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)