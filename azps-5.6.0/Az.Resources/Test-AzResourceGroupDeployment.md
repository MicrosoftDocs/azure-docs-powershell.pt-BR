---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 0e0d4645901f60f9e290d197a47b133d6bf3db8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888443"
---
# <span data-ttu-id="84949-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84949-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="84949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84949-102">SYNOPSIS</span></span>
<span data-ttu-id="84949-103">Valida uma implantação de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="84949-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="84949-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="84949-104">SYNTAX</span></span>

### <span data-ttu-id="84949-105">ByTemplateFileWithNoParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="84949-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84949-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="84949-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84949-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="84949-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84949-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="84949-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84949-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="84949-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84949-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="84949-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84949-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="84949-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84949-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="84949-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84949-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="84949-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84949-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="84949-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84949-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="84949-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84949-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="84949-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84949-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="84949-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84949-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="84949-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84949-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="84949-119">ByTemplateSpecResourceId</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84949-120">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="84949-120">DESCRIPTION</span></span>
<span data-ttu-id="84949-121">O cmdlet **Test-AzResourceGroupDeployment** determina se um modelo de implantação do grupo de recursos do Azure e seus valores de parâmetro são válidos.</span><span class="sxs-lookup"><span data-stu-id="84949-121">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="84949-122">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84949-122">EXAMPLES</span></span>

### <span data-ttu-id="84949-123">Exemplo 1: Testar a implantação com um objeto de modelo personalizado e um arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="84949-123">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="84949-124">Este comando testa uma implantação no determinado grupo de recursos usando uma hashtable na memória criada a partir do arquivo de modelo determinado e de um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="84949-124">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="84949-125">Exemplo 2: Testar a implantação por meio de arquivo de modelo e arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="84949-125">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="84949-126">Este comando testa uma implantação no determinado grupo de recursos e recurso usando o arquivo de modelo fornecido e um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="84949-126">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="84949-127">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="84949-127">PARAMETERS</span></span>

### <span data-ttu-id="84949-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84949-128">-DefaultProfile</span></span>
<span data-ttu-id="84949-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="84949-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84949-130">-Mode</span><span class="sxs-lookup"><span data-stu-id="84949-130">-Mode</span></span>
<span data-ttu-id="84949-131">Especifica o modo de implantação.</span><span class="sxs-lookup"><span data-stu-id="84949-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="84949-132">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="84949-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84949-133">Incremental</span><span class="sxs-lookup"><span data-stu-id="84949-133">Incremental</span></span>
- <span data-ttu-id="84949-134">Concluído</span><span class="sxs-lookup"><span data-stu-id="84949-134">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84949-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="84949-135">-Pre</span></span>
<span data-ttu-id="84949-136">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="84949-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="84949-137">-QueryString</span><span class="sxs-lookup"><span data-stu-id="84949-137">-QueryString</span></span>
<span data-ttu-id="84949-138">A cadeia de caracteres de consulta (por exemplo, um token SAS) a ser usada com o parâmetro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="84949-138">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="84949-139">Seria usado no caso de modelos vinculados</span><span class="sxs-lookup"><span data-stu-id="84949-139">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="84949-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84949-140">-ResourceGroupName</span></span>
<span data-ttu-id="84949-141">Especifica o nome do grupo de recursos a ser testado.</span><span class="sxs-lookup"><span data-stu-id="84949-141">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="84949-142">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="84949-142">-RollBackDeploymentName</span></span>
<span data-ttu-id="84949-143">A replicação à implantação bem-sucedida com o nome dado no grupo de recursos não deve ser usada se -RollbackToLastDeployment for usado.</span><span class="sxs-lookup"><span data-stu-id="84949-143">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="84949-144">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="84949-144">-RollbackToLastDeployment</span></span>
<span data-ttu-id="84949-145">A replicação para a última implantação bem-sucedida no grupo de recursos não deve estar presente se -RollBackDeploymentName for usado.</span><span class="sxs-lookup"><span data-stu-id="84949-145">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="84949-146">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="84949-146">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="84949-147">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="84949-147">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="84949-148">Essa verificação solicitaria que o usuário fornecesse um valor para os parâmetros ausentes, mas o fornecimento de -SkipTemplateParameterPrompt ignorará esse prompt e o excluirá imediatamente se um parâmetro não tiver sido vinculado no modelo.</span><span class="sxs-lookup"><span data-stu-id="84949-148">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="84949-149">Para scripts não interativos, -SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso nem todos os parâmetros necessários sejam atendidos.</span><span class="sxs-lookup"><span data-stu-id="84949-149">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="84949-150">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="84949-150">-TemplateFile</span></span>
<span data-ttu-id="84949-151">Especifica o caminho completo de um arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="84949-151">Specifies the full path of a template file.</span></span> <span data-ttu-id="84949-152">Tipo de arquivo de modelo com suporte: json e bicep.</span><span class="sxs-lookup"><span data-stu-id="84949-152">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="84949-153">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="84949-153">-TemplateObject</span></span>
<span data-ttu-id="84949-154">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="84949-154">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="84949-155">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="84949-155">-TemplateParameterFile</span></span>
<span data-ttu-id="84949-156">Especifica o caminho completo de um arquivo JSON que contém os nomes e os valores dos parâmetros do modelo.</span><span class="sxs-lookup"><span data-stu-id="84949-156">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="84949-157">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="84949-157">-TemplateParameterObject</span></span>
<span data-ttu-id="84949-158">Especifica uma tabela de hash de nomes e valores de parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="84949-158">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="84949-159">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="84949-159">-TemplateParameterUri</span></span>
<span data-ttu-id="84949-160">Especifica o URI de um arquivo de parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="84949-160">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="84949-161">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="84949-161">-TemplateSpecId</span></span>
<span data-ttu-id="84949-162">ID do recurso do modeloSpec a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="84949-162">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="84949-163">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="84949-163">-TemplateUri</span></span>
<span data-ttu-id="84949-164">Especifica o URI de um arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="84949-164">Specifies the URI of a template file.</span></span>

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

### <span data-ttu-id="84949-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84949-165">CommonParameters</span></span>
<span data-ttu-id="84949-166">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84949-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84949-167">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84949-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84949-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84949-168">INPUTS</span></span>

### <span data-ttu-id="84949-169">System.String</span><span class="sxs-lookup"><span data-stu-id="84949-169">System.String</span></span>

### <span data-ttu-id="84949-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="84949-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="84949-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="84949-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="84949-172">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="84949-172">OUTPUTS</span></span>

### <span data-ttu-id="84949-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="84949-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="84949-174">NOTES</span><span class="sxs-lookup"><span data-stu-id="84949-174">NOTES</span></span>

## <span data-ttu-id="84949-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84949-175">RELATED LINKS</span></span>

[<span data-ttu-id="84949-176">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84949-176">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="84949-177">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84949-177">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="84949-178">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84949-178">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="84949-179">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84949-179">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


