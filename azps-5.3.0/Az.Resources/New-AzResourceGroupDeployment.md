---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 916e2fea0e88a1409bc2586ab8b2e80b11ec1a70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427249"
---
# <span data-ttu-id="35392-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35392-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="35392-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35392-102">SYNOPSIS</span></span>
<span data-ttu-id="35392-103">Adiciona uma implantação do Azure a um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35392-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="35392-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35392-104">SYNTAX</span></span>

### <span data-ttu-id="35392-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="35392-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35392-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="35392-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35392-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="35392-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35392-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="35392-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35392-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="35392-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35392-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="35392-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35392-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="35392-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35392-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="35392-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35392-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="35392-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35392-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="35392-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35392-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="35392-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35392-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="35392-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35392-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35392-117">DESCRIPTION</span></span>
<span data-ttu-id="35392-118">O cmdlet **New-AzResourceGroupDeployment** adiciona uma implantação a um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="35392-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="35392-119">Isso inclui os recursos que a implantação requer.</span><span class="sxs-lookup"><span data-stu-id="35392-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="35392-120">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados, site, máquina virtual ou conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="35392-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="35392-121">Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade, como o site, o servidor de banco de dados e bancos de dados necessários para um site financeiro.</span><span class="sxs-lookup"><span data-stu-id="35392-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="35392-122">Uma implantação de grupo de recursos usa um modelo para adicionar recursos a um grupo de recursos e os publica para que eles estejam disponíveis no Azure.</span><span class="sxs-lookup"><span data-stu-id="35392-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="35392-123">Para adicionar recursos a um grupo de recursos sem usar um modelo, use o cmdlet New-AzResource.</span><span class="sxs-lookup"><span data-stu-id="35392-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="35392-124">Para adicionar uma implantação de grupo de recursos, especifique o nome de um grupo de recursos existente e um modelo de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35392-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="35392-125">Um modelo de grupo de recursos é uma cadeia de caracteres JSON que representa um grupo de recursos para um serviço complexo baseado em nuvem, como um portal da Web.</span><span class="sxs-lookup"><span data-stu-id="35392-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="35392-126">O modelo inclui espaços reservados de parâmetro para recursos obrigatórios e valores de propriedade configuráveis, como nomes e tamanhos.</span><span class="sxs-lookup"><span data-stu-id="35392-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="35392-127">Você pode encontrar muitos modelos na Galeria de modelos do Azure ou pode criar seus próprios modelos.</span><span class="sxs-lookup"><span data-stu-id="35392-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="35392-128">Para usar um modelo personalizado para criar um grupo de recursos, especifique o parâmetro *TemplateFile* ou o parâmetro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="35392-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="35392-129">Cada modelo tem parâmetros para propriedades configuráveis.</span><span class="sxs-lookup"><span data-stu-id="35392-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="35392-130">Para especificar valores para os parâmetros de modelo, especifique o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="35392-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="35392-131">Você também pode usar os parâmetros de modelo que são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="35392-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="35392-132">Para usar parâmetros dinâmicos, digite-os no prompt de comando ou digite um sinal de subtração (-) para indicar um parâmetro e use a tecla Tab para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="35392-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="35392-133">Os valores de parâmetro de modelo que você insere no prompt de comando prevalecem sobre os valores em um objeto ou arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="35392-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="35392-134">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35392-134">EXAMPLES</span></span>

### <span data-ttu-id="35392-135">Exemplo 1: usar um modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="35392-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="35392-136">Esse comando cria uma nova implantação usando um modelo personalizado e um arquivo de modelo no disco, com o parâmetro Tags definidas.</span><span class="sxs-lookup"><span data-stu-id="35392-136">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="35392-137">O comando usa o parâmetro *TemplateFile* para especificar o modelo e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="35392-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="35392-138">Exemplo 2: usar um objeto de modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="35392-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="35392-139">Esse comando cria uma nova implantação usando um arquivo de modelo e personalizado no disco que foi convertido em uma Hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="35392-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="35392-140">Os primeiros dois comandos lêem o texto do arquivo de modelo no disco e o convertem em uma Hashtable na memória.</span><span class="sxs-lookup"><span data-stu-id="35392-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="35392-141">O último comando usa o parâmetro *templateobject* para especificar a Hashtable e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="35392-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="35392-142">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="35392-142">Example 3</span></span>

<span data-ttu-id="35392-143">Adiciona uma implantação do Azure a um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35392-143">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="35392-144">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="35392-144">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

## <span data-ttu-id="35392-145">OS</span><span class="sxs-lookup"><span data-stu-id="35392-145">PARAMETERS</span></span>

### <span data-ttu-id="35392-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35392-146">-AsJob</span></span>
<span data-ttu-id="35392-147">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="35392-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35392-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35392-148">-DefaultProfile</span></span>
<span data-ttu-id="35392-149">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="35392-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35392-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="35392-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="35392-151">Especifica um nível de log de depuração.</span><span class="sxs-lookup"><span data-stu-id="35392-151">Specifies a debug log level.</span></span>
<span data-ttu-id="35392-152">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35392-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35392-153">RequestContent</span><span class="sxs-lookup"><span data-stu-id="35392-153">RequestContent</span></span>
- <span data-ttu-id="35392-154">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="35392-154">ResponseContent</span></span>
- <span data-ttu-id="35392-155">Todo</span><span class="sxs-lookup"><span data-stu-id="35392-155">All</span></span>
- <span data-ttu-id="35392-156">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="35392-156">None</span></span>

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

### <span data-ttu-id="35392-157">-Force</span><span class="sxs-lookup"><span data-stu-id="35392-157">-Force</span></span>
<span data-ttu-id="35392-158">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="35392-158">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35392-159">-Mode</span><span class="sxs-lookup"><span data-stu-id="35392-159">-Mode</span></span>
<span data-ttu-id="35392-160">Especifica o modo de implantação.</span><span class="sxs-lookup"><span data-stu-id="35392-160">Specifies the deployment mode.</span></span> <span data-ttu-id="35392-161">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35392-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35392-162">Concluir: no modo completo, o Gerenciador de recursos exclui recursos que existem no grupo de recursos, mas não estão especificados no modelo.</span><span class="sxs-lookup"><span data-stu-id="35392-162">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="35392-163">Incremental: no modo incremental, o Gerenciador de recursos deixa os recursos inalterados que existem no grupo de recursos, mas não estão especificados no modelo.</span><span class="sxs-lookup"><span data-stu-id="35392-163">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="35392-164">-Nome</span><span class="sxs-lookup"><span data-stu-id="35392-164">-Name</span></span>
<span data-ttu-id="35392-165">O nome da implantação que será criada.</span><span class="sxs-lookup"><span data-stu-id="35392-165">The name of the deployment it's going to create.</span></span> <span data-ttu-id="35392-166">Se não for especificado, o padrão será o nome do arquivo de modelo quando um arquivo de modelo for fornecido; o padrão é a hora atual quando um objeto de modelo é fornecido, por exemplo, "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="35392-166">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="35392-167">-Pre</span><span class="sxs-lookup"><span data-stu-id="35392-167">-Pre</span></span>
<span data-ttu-id="35392-168">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="35392-168">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="35392-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35392-169">-ResourceGroupName</span></span>
<span data-ttu-id="35392-170">Especifica o nome do grupo de recursos a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="35392-170">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="35392-171">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="35392-171">-RollBackDeploymentName</span></span>
<span data-ttu-id="35392-172">A reversão para a implantação bem-sucedida com o nome especificado no grupo de recursos não deve ser usada se-RollbackToLastDeployment for usado.</span><span class="sxs-lookup"><span data-stu-id="35392-172">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="35392-173">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="35392-173">-RollbackToLastDeployment</span></span>
<span data-ttu-id="35392-174">A reversão para a última implantação bem-sucedida no grupo de recursos não deve estar presente se-RollBackDeploymentName for usado.</span><span class="sxs-lookup"><span data-stu-id="35392-174">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="35392-175">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="35392-175">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="35392-176">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="35392-176">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="35392-177">Essa verificação solicitaria que o usuário forneça um valor para os parâmetros ausentes, mas fornecer o-SkipTemplateParameterPrompt ignorará esse prompt e o erro será imediatamente se um parâmetro não fosse associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="35392-177">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="35392-178">Para scripts não interativos,-SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso não seja satisfeito todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="35392-178">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="35392-179">-Marca</span><span class="sxs-lookup"><span data-stu-id="35392-179">-Tag</span></span>
<span data-ttu-id="35392-180">As marcas a serem colocadas na implantação.</span><span class="sxs-lookup"><span data-stu-id="35392-180">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="35392-181">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="35392-181">-TemplateFile</span></span>
<span data-ttu-id="35392-182">Especifica o caminho completo de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="35392-182">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="35392-183">Pode ser um modelo personalizado ou um modelo de galeria salvo como um arquivo JSON, como um criado usando o cmdlet **Save-AzResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="35392-183">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="35392-184">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="35392-184">-TemplateObject</span></span>
<span data-ttu-id="35392-185">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="35392-185">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="35392-186">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="35392-186">-TemplateParameterFile</span></span>
<span data-ttu-id="35392-187">Especifica o caminho completo de um arquivo JSON que contém os nomes e os valores dos parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="35392-187">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="35392-188">Se um modelo tem parâmetros, você deve especificar os valores de parâmetro com o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="35392-188">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="35392-189">Os parâmetros do modelo são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="35392-189">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="35392-190">Para usar os parâmetros dinâmicos, digite um sinal de subtração (-) para indicar um nome de parâmetro e use a tecla Tab para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="35392-190">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="35392-191">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="35392-191">-TemplateParameterObject</span></span>
<span data-ttu-id="35392-192">Especifica uma tabela de hash de nomes e valores de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="35392-192">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="35392-193">Para obter ajuda com tabelas de hash no Windows PowerShell, digite `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="35392-193">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="35392-194">Se um modelo tem parâmetros, você deve especificar valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="35392-194">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="35392-195">Os parâmetros do modelo são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="35392-195">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="35392-196">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="35392-196">-TemplateParameterUri</span></span>
<span data-ttu-id="35392-197">Especifica o URI de um arquivo de parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="35392-197">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="35392-198">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="35392-198">-TemplateUri</span></span>
<span data-ttu-id="35392-199">Especifica o URI de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="35392-199">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="35392-200">Esse arquivo pode ser um modelo personalizado ou um modelo de galeria salvo como um arquivo JSON, por exemplo, usando **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="35392-200">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="35392-201">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="35392-201">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="35392-202">Tipos de alteração de recursos separados por vírgula a serem excluídos dos resultados de What-If.</span><span class="sxs-lookup"><span data-stu-id="35392-202">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="35392-203">Aplicável quando a opção-WhatIf ou-Confirm está definida.</span><span class="sxs-lookup"><span data-stu-id="35392-203">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="35392-204">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="35392-204">-WhatIfResultFormat</span></span>
<span data-ttu-id="35392-205">O formato de resultado What-If.</span><span class="sxs-lookup"><span data-stu-id="35392-205">The What-If result format.</span></span>

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

### <span data-ttu-id="35392-206">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35392-206">-Confirm</span></span>
<span data-ttu-id="35392-207">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35392-207">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35392-208">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35392-208">-WhatIf</span></span>
<span data-ttu-id="35392-209">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35392-209">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35392-210">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35392-210">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35392-211">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35392-211">CommonParameters</span></span>
<span data-ttu-id="35392-212">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35392-212">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35392-213">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35392-213">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35392-214">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35392-214">INPUTS</span></span>

### <span data-ttu-id="35392-215">System. String</span><span class="sxs-lookup"><span data-stu-id="35392-215">System.String</span></span>

### <span data-ttu-id="35392-216">Microsoft. Azure. Management. ResourceManager. Models. Deploymentmode</span><span class="sxs-lookup"><span data-stu-id="35392-216">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="35392-217">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="35392-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="35392-218">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35392-218">OUTPUTS</span></span>

### <span data-ttu-id="35392-219">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35392-219">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="35392-220">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35392-220">NOTES</span></span>

## <span data-ttu-id="35392-221">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35392-221">RELATED LINKS</span></span>

[<span data-ttu-id="35392-222">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35392-222">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="35392-223">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="35392-223">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="35392-224">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="35392-224">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="35392-225">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35392-225">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="35392-226">Parar-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35392-226">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="35392-227">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35392-227">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)