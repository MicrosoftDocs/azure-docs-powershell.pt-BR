---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: 95aa46354fb0ea1f2a1883fe7d319acfda220526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118751"
---
# <span data-ttu-id="46256-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="46256-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="46256-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46256-102">SYNOPSIS</span></span>
<span data-ttu-id="46256-103">Criar uma implantação em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="46256-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="46256-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46256-104">SYNTAX</span></span>

### <span data-ttu-id="46256-105">ByTemplateFileWithNoParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="46256-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46256-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="46256-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46256-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="46256-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46256-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="46256-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46256-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="46256-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46256-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="46256-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46256-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="46256-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46256-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="46256-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46256-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="46256-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46256-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="46256-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46256-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="46256-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46256-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="46256-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46256-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="46256-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46256-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="46256-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46256-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="46256-119">ByTemplateSpecResourceId</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46256-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="46256-120">DESCRIPTION</span></span>
<span data-ttu-id="46256-121">O **cmdlet New-AzManagementGroupDeployment** adiciona uma implantação a um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="46256-121">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="46256-122">Para adicionar uma implantação a um grupo de gerenciamento, especifique o grupo de gerenciamento, o local e um modelo.</span><span class="sxs-lookup"><span data-stu-id="46256-122">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="46256-123">O local informa ao Gerenciador de Recursos do Azure onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="46256-123">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="46256-124">O modelo é uma cadeia de caracteres JSON que contém recursos individuais a serem implantados.</span><span class="sxs-lookup"><span data-stu-id="46256-124">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="46256-125">O modelo inclui os espaço reservados para parâmetros para recursos necessários e valores de propriedades configuráveis, como nomes e tamanhos.</span><span class="sxs-lookup"><span data-stu-id="46256-125">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="46256-126">Para usar um modelo personalizado para a implantação, especifique o parâmetro *TemplateFile* ou *o parâmetro TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="46256-126">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="46256-127">Cada modelo tem parâmetros para propriedades configuráveis.</span><span class="sxs-lookup"><span data-stu-id="46256-127">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="46256-128">Para especificar valores para os parâmetros de modelo, especifique o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="46256-128">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="46256-129">Como alternativa, você pode usar os parâmetros de modelo que são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="46256-129">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="46256-130">Para usar parâmetros dinâmicos, digite-os no prompt de comando ou digite um sinal de subtração (-) para indicar um parâmetro e use a tecla Tab para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="46256-130">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="46256-131">Os valores de parâmetro de modelo que você inserir no prompt de comando têm precedência sobre os valores em um objeto ou arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="46256-131">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="46256-132">Para adicionar recursos a um grupo de recursos, use o **New-AzResourceGroupDeployment que** cria uma implantação em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46256-132">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="46256-133">Para adicionar recursos a uma assinatura, use o **New-AzSubscriptionDeployment,** que cria uma implantação no escopo da assinatura, que implanta recursos de nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="46256-133">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="46256-134">Para adicionar recursos no escopo do locatário, use o **Novo-AzTenantDeployment que** cria uma implantação no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="46256-134">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="46256-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46256-135">EXAMPLES</span></span>

### <span data-ttu-id="46256-136">Exemplo 1: Usar um modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="46256-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="46256-137">Esse comando cria uma nova implantação no grupo de gerenciamento "myMG" usando um modelo personalizado e um arquivo de modelo em disco, com parâmetro de marcas definidas.</span><span class="sxs-lookup"><span data-stu-id="46256-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="46256-138">O comando usa o parâmetro *TemplateFile* para especificar o modelo e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="46256-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="46256-139">Exemplo 2: Implantar um modelo armazenado em uma conta de armazenamento não pública usando um uri e um token SAS</span><span class="sxs-lookup"><span data-stu-id="46256-139">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="46256-140">Esse comando cria uma nova implantação usando o modelo no TemplateUri, que não é público e requer um parâmetro de token para acessar que seria fornecido usando o parâmetro QueryString.</span><span class="sxs-lookup"><span data-stu-id="46256-140">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="46256-141">Executar esse comando acessa efetivamente o modelo usando a https://example.com/example.json?foo URL.</span><span class="sxs-lookup"><span data-stu-id="46256-141">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="46256-142">Isso pode ser usado se você quiser usar um modelo em uma conta de armazenamento fornecendo o token SAS como o QueryString</span><span class="sxs-lookup"><span data-stu-id="46256-142">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="46256-143">Exemplo 3: Usar um objeto de modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="46256-143">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="46256-144">Esse comando cria uma nova implantação no grupo de gerenciamento "myMG" usando um modelo personalizado e um arquivo de modelo no disco que foi convertido em uma hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="46256-144">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="46256-145">Os dois primeiros comandos leem o texto do arquivo de modelo em disco e o convertem em uma hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="46256-145">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="46256-146">O último comando usa o parâmetro *TemplateObject* para especificar essa tabela hash e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="46256-146">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="46256-147">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46256-147">PARAMETERS</span></span>

### <span data-ttu-id="46256-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46256-148">-AsJob</span></span>
<span data-ttu-id="46256-149">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="46256-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46256-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46256-150">-DefaultProfile</span></span>
<span data-ttu-id="46256-151">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46256-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46256-152">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="46256-152">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="46256-153">O nível de log de depuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="46256-153">The deployment debug log level.</span></span>

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

### <span data-ttu-id="46256-154">-Local</span><span class="sxs-lookup"><span data-stu-id="46256-154">-Location</span></span>
<span data-ttu-id="46256-155">O local para armazenar dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="46256-155">The location to store deployment data.</span></span>

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

### <span data-ttu-id="46256-156">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="46256-156">-ManagementGroupId</span></span>
<span data-ttu-id="46256-157">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="46256-157">The management group ID.</span></span>

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

### <span data-ttu-id="46256-158">-Nome</span><span class="sxs-lookup"><span data-stu-id="46256-158">-Name</span></span>
<span data-ttu-id="46256-159">O nome da implantação que ele vai criar.</span><span class="sxs-lookup"><span data-stu-id="46256-159">The name of the deployment it's going to create.</span></span> <span data-ttu-id="46256-160">Se não especificado, o padrão é o nome do arquivo de modelo quando um arquivo de modelo é fornecido; padrão para a hora atual quando um objeto de modelo é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="46256-160">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="46256-161">-Pré-</span><span class="sxs-lookup"><span data-stu-id="46256-161">-Pre</span></span>
<span data-ttu-id="46256-162">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="46256-162">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="46256-163">-QueryString</span><span class="sxs-lookup"><span data-stu-id="46256-163">-QueryString</span></span>
<span data-ttu-id="46256-164">A cadeia de caracteres de consulta (por exemplo, um token SAS) a ser usado com o parâmetro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="46256-164">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="46256-165">Seria usado no caso de modelos vinculados</span><span class="sxs-lookup"><span data-stu-id="46256-165">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="46256-166">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="46256-166">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="46256-167">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="46256-167">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="46256-168">Essa verificação solicitaria que o usuário fornecesse um valor para os parâmetros ausentes, mas fornecer o -SkipTemplateParameterPrompt ignorará esse prompt e um erro imediatamente se um parâmetro não tiver sido vinculado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="46256-168">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="46256-169">Para scripts não interativos, -SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso nem todos os parâmetros necessários sejam satisfeitos.</span><span class="sxs-lookup"><span data-stu-id="46256-169">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="46256-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="46256-170">-Tag</span></span>
<span data-ttu-id="46256-171">As marcas a colocar na implantação.</span><span class="sxs-lookup"><span data-stu-id="46256-171">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="46256-172">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="46256-172">-TemplateFile</span></span>
<span data-ttu-id="46256-173">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="46256-173">Local path to the template file.</span></span>

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

### <span data-ttu-id="46256-174">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="46256-174">-TemplateObject</span></span>
<span data-ttu-id="46256-175">Uma tabela hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="46256-175">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="46256-176">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="46256-176">-TemplateParameterFile</span></span>
<span data-ttu-id="46256-177">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="46256-177">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="46256-178">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="46256-178">-TemplateParameterObject</span></span>
<span data-ttu-id="46256-179">Uma tabela hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="46256-179">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="46256-180">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="46256-180">-TemplateParameterUri</span></span>
<span data-ttu-id="46256-181">Uri para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="46256-181">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="46256-182">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="46256-182">-TemplateSpecId</span></span>
<span data-ttu-id="46256-183">ID do recurso do modeloSpec a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="46256-183">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="46256-184">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="46256-184">-TemplateUri</span></span>
<span data-ttu-id="46256-185">Uri para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="46256-185">Uri to the template file.</span></span>

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

### <span data-ttu-id="46256-186">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="46256-186">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="46256-187">Tipos de alteração de recursos separados por vírgulas a serem excluídos What-If resultados.</span><span class="sxs-lookup"><span data-stu-id="46256-187">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="46256-188">Aplicável quando a opção -WhatIf ou -Confirm estiver definida.</span><span class="sxs-lookup"><span data-stu-id="46256-188">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="46256-189">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="46256-189">-WhatIfResultFormat</span></span>
<span data-ttu-id="46256-190">O What-If de resultados.</span><span class="sxs-lookup"><span data-stu-id="46256-190">The What-If result format.</span></span> <span data-ttu-id="46256-191">Aplicável quando a opção -WhatIf ou -Confirm estiver definida.</span><span class="sxs-lookup"><span data-stu-id="46256-191">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="46256-192">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="46256-192">-Confirm</span></span>
<span data-ttu-id="46256-193">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46256-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46256-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46256-194">-WhatIf</span></span>
<span data-ttu-id="46256-195">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="46256-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46256-196">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46256-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46256-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46256-197">CommonParameters</span></span>
<span data-ttu-id="46256-198">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46256-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46256-199">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46256-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46256-200">Entradas</span><span class="sxs-lookup"><span data-stu-id="46256-200">INPUTS</span></span>

### <span data-ttu-id="46256-201">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="46256-201">System.Collections.Hashtable</span></span>

### <span data-ttu-id="46256-202">System.String</span><span class="sxs-lookup"><span data-stu-id="46256-202">System.String</span></span>

## <span data-ttu-id="46256-203">Saídas</span><span class="sxs-lookup"><span data-stu-id="46256-203">OUTPUTS</span></span>

### <span data-ttu-id="46256-204">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="46256-204">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="46256-205">Notas</span><span class="sxs-lookup"><span data-stu-id="46256-205">NOTES</span></span>

## <span data-ttu-id="46256-206">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46256-206">RELATED LINKS</span></span>
