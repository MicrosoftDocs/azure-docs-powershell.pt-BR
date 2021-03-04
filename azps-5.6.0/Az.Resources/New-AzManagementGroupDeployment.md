---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: da2a2bc6d7c35f6d7f092123dce08496f491655b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892042"
---
# <span data-ttu-id="979fa-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="979fa-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="979fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="979fa-102">SYNOPSIS</span></span>
<span data-ttu-id="979fa-103">Criar uma implantação em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="979fa-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="979fa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="979fa-104">SYNTAX</span></span>

### <span data-ttu-id="979fa-105">ByTemplateFileWithNoParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="979fa-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="979fa-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="979fa-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979fa-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="979fa-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979fa-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="979fa-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979fa-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="979fa-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979fa-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="979fa-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979fa-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="979fa-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979fa-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="979fa-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979fa-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="979fa-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979fa-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="979fa-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979fa-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="979fa-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979fa-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="979fa-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979fa-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="979fa-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979fa-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="979fa-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="979fa-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="979fa-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="979fa-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="979fa-120">ByTemplateSpecResourceId</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="979fa-121">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="979fa-121">DESCRIPTION</span></span>
<span data-ttu-id="979fa-122">O cmdlet **New-AzManagementGroupDeployment** adiciona uma implantação em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="979fa-122">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="979fa-123">Para adicionar uma implantação em um grupo de gerenciamento, especifique o grupo de gerenciamento, o local e um modelo.</span><span class="sxs-lookup"><span data-stu-id="979fa-123">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="979fa-124">O local informa ao Gerente de Recursos do Azure onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="979fa-124">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="979fa-125">O modelo é uma cadeia de caracteres JSON que contém recursos individuais a serem implantados.</span><span class="sxs-lookup"><span data-stu-id="979fa-125">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="979fa-126">O modelo inclui os espaço reservados para parâmetros para recursos necessários e valores de propriedades configuráveis, como nomes e tamanhos.</span><span class="sxs-lookup"><span data-stu-id="979fa-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="979fa-127">Para usar um modelo personalizado para a implantação, especifique o parâmetro *TemplateFile* ou *o parâmetro TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="979fa-127">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="979fa-128">Cada modelo tem parâmetros para propriedades configuráveis.</span><span class="sxs-lookup"><span data-stu-id="979fa-128">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="979fa-129">Para especificar valores para os parâmetros de modelo, especifique o *parâmetro TemplateParameterFile* ou *o parâmetro TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="979fa-129">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="979fa-130">Como alternativa, você pode usar os parâmetros de modelo adicionados dinamicamente ao comando ao especificar um modelo.</span><span class="sxs-lookup"><span data-stu-id="979fa-130">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="979fa-131">Para usar parâmetros dinâmicos, digite-os no prompt de comando ou digite um sinal de menos (-) para indicar um parâmetro e use a tecla Tab para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="979fa-131">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="979fa-132">Os valores de parâmetro de modelo que você inserir no prompt de comando têm precedência sobre os valores em um objeto ou arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="979fa-132">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="979fa-133">Para adicionar recursos a um grupo de recursos, use **o New-AzResourceGroupDeployment** que cria uma implantação em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="979fa-133">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="979fa-134">Para adicionar recursos a uma assinatura, use o **New-AzSubscriptionDeployment** que cria uma implantação no escopo da assinatura, que implanta recursos de nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="979fa-134">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="979fa-135">Para adicionar recursos no escopo do locatário, use **o New-AzTenantDeployment** que cria uma implantação no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="979fa-135">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="979fa-136">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="979fa-136">EXAMPLES</span></span>

### <span data-ttu-id="979fa-137">Exemplo 1: usar um modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="979fa-137">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="979fa-138">Este comando cria uma nova implantação no grupo de gerenciamento "myMG" usando um modelo personalizado e um arquivo de modelo em disco, com parâmetro de marcas definidas.</span><span class="sxs-lookup"><span data-stu-id="979fa-138">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="979fa-139">O comando usa o *parâmetro TemplateFile* para especificar o modelo e o *parâmetro TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="979fa-139">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="979fa-140">Exemplo 2: Implantar um modelo armazenado em uma conta de armazenamento não pública usando um uri e um token SAS</span><span class="sxs-lookup"><span data-stu-id="979fa-140">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="979fa-141">Este comando cria uma nova implantação usando o modelo em TemplateUri que não é público e requer um parâmetro token para acessar o qual seria fornecido usando o parâmetro QueryString.</span><span class="sxs-lookup"><span data-stu-id="979fa-141">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="979fa-142">Executar esse comando acessa efetivamente o modelo usando a url https://example.com/example.json?foo .</span><span class="sxs-lookup"><span data-stu-id="979fa-142">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="979fa-143">Isso pode ser usado se você quiser usar um modelo em uma conta de armazenamento fornecendo o token SAS como o QueryString</span><span class="sxs-lookup"><span data-stu-id="979fa-143">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="979fa-144">Exemplo 3: usar um objeto de modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="979fa-144">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="979fa-145">Este comando cria uma nova implantação no grupo de gerenciamento "myMG" usando um modelo personalizado e um arquivo de modelo no disco que foi convertido em uma hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="979fa-145">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="979fa-146">Os dois primeiros comandos leem o texto do arquivo de modelo no disco e o convertem em uma hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="979fa-146">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="979fa-147">O último comando usa o *parâmetro TemplateObject* para especificar essa hashtable e o *parâmetro TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="979fa-147">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="979fa-148">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="979fa-148">PARAMETERS</span></span>

### <span data-ttu-id="979fa-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="979fa-149">-AsJob</span></span>
<span data-ttu-id="979fa-150">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="979fa-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="979fa-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="979fa-151">-DefaultProfile</span></span>
<span data-ttu-id="979fa-152">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="979fa-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="979fa-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="979fa-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="979fa-154">O nível de log de depuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="979fa-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="979fa-155">-Location</span><span class="sxs-lookup"><span data-stu-id="979fa-155">-Location</span></span>
<span data-ttu-id="979fa-156">O local para armazenar dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="979fa-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="979fa-157">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="979fa-157">-ManagementGroupId</span></span>
<span data-ttu-id="979fa-158">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="979fa-158">The management group ID.</span></span>

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

### <span data-ttu-id="979fa-159">-Name</span><span class="sxs-lookup"><span data-stu-id="979fa-159">-Name</span></span>
<span data-ttu-id="979fa-160">O nome da implantação que ele criará.</span><span class="sxs-lookup"><span data-stu-id="979fa-160">The name of the deployment it's going to create.</span></span> <span data-ttu-id="979fa-161">Se não for especificado, o padrão é o nome do arquivo de modelo quando um arquivo de modelo é fornecido; padrão para a hora atual em que um objeto template é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="979fa-161">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="979fa-162">-Pre</span><span class="sxs-lookup"><span data-stu-id="979fa-162">-Pre</span></span>
<span data-ttu-id="979fa-163">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="979fa-163">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="979fa-164">-QueryString</span><span class="sxs-lookup"><span data-stu-id="979fa-164">-QueryString</span></span>
<span data-ttu-id="979fa-165">A cadeia de caracteres de consulta (por exemplo, um token SAS) a ser usada com o parâmetro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="979fa-165">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="979fa-166">Seria usado no caso de modelos vinculados</span><span class="sxs-lookup"><span data-stu-id="979fa-166">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="979fa-167">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="979fa-167">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="979fa-168">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="979fa-168">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="979fa-169">Essa verificação solicitaria que o usuário fornecesse um valor para os parâmetros ausentes, mas o fornecimento de -SkipTemplateParameterPrompt ignorará esse prompt e o excluirá imediatamente se um parâmetro não tiver sido vinculado no modelo.</span><span class="sxs-lookup"><span data-stu-id="979fa-169">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="979fa-170">Para scripts não interativos, -SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso nem todos os parâmetros necessários sejam atendidos.</span><span class="sxs-lookup"><span data-stu-id="979fa-170">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="979fa-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="979fa-171">-Tag</span></span>
<span data-ttu-id="979fa-172">As marcas a ser colocadas na implantação.</span><span class="sxs-lookup"><span data-stu-id="979fa-172">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="979fa-173">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="979fa-173">-TemplateFile</span></span>
<span data-ttu-id="979fa-174">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="979fa-174">Local path to the template file.</span></span> <span data-ttu-id="979fa-175">Tipo de arquivo de modelo com suporte: json e bicep.</span><span class="sxs-lookup"><span data-stu-id="979fa-175">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="979fa-176">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="979fa-176">-TemplateObject</span></span>
<span data-ttu-id="979fa-177">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="979fa-177">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="979fa-178">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="979fa-178">-TemplateParameterFile</span></span>
<span data-ttu-id="979fa-179">Um arquivo que tem os parâmetros do modelo.</span><span class="sxs-lookup"><span data-stu-id="979fa-179">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="979fa-180">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="979fa-180">-TemplateParameterObject</span></span>
<span data-ttu-id="979fa-181">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="979fa-181">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="979fa-182">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="979fa-182">-TemplateParameterUri</span></span>
<span data-ttu-id="979fa-183">Uri para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="979fa-183">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="979fa-184">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="979fa-184">-TemplateSpecId</span></span>
<span data-ttu-id="979fa-185">ID do recurso do modeloSpec a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="979fa-185">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="979fa-186">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="979fa-186">-TemplateUri</span></span>
<span data-ttu-id="979fa-187">Uri para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="979fa-187">Uri to the template file.</span></span>

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

### <span data-ttu-id="979fa-188">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="979fa-188">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="979fa-189">Tipos de alteração de recursos separados por vírgulas a serem excluídos dos What-If resultados.</span><span class="sxs-lookup"><span data-stu-id="979fa-189">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="979fa-190">Aplicável quando a opção -WhatIf ou -Confirm estiver definida.</span><span class="sxs-lookup"><span data-stu-id="979fa-190">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="979fa-191">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="979fa-191">-WhatIfResultFormat</span></span>
<span data-ttu-id="979fa-192">O What-If de resultados.</span><span class="sxs-lookup"><span data-stu-id="979fa-192">The What-If result format.</span></span> <span data-ttu-id="979fa-193">Aplicável quando a opção -WhatIf ou -Confirm estiver definida.</span><span class="sxs-lookup"><span data-stu-id="979fa-193">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="979fa-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="979fa-194">-Confirm</span></span>
<span data-ttu-id="979fa-195">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="979fa-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="979fa-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="979fa-196">-WhatIf</span></span>
<span data-ttu-id="979fa-197">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="979fa-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="979fa-198">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="979fa-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="979fa-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="979fa-199">CommonParameters</span></span>
<span data-ttu-id="979fa-200">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="979fa-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="979fa-201">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="979fa-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="979fa-202">INPUTS</span><span class="sxs-lookup"><span data-stu-id="979fa-202">INPUTS</span></span>

### <span data-ttu-id="979fa-203">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="979fa-203">System.Collections.Hashtable</span></span>

### <span data-ttu-id="979fa-204">System.String</span><span class="sxs-lookup"><span data-stu-id="979fa-204">System.String</span></span>

## <span data-ttu-id="979fa-205">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="979fa-205">OUTPUTS</span></span>

### <span data-ttu-id="979fa-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="979fa-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="979fa-207">NOTES</span><span class="sxs-lookup"><span data-stu-id="979fa-207">NOTES</span></span>

## <span data-ttu-id="979fa-208">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="979fa-208">RELATED LINKS</span></span>
