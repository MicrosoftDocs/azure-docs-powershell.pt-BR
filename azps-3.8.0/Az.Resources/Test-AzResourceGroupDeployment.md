---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 97a16dcebe2730fef1d770fe8cbbf54d5488b49a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941703"
---
# <span data-ttu-id="8639f-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8639f-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="8639f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8639f-102">SYNOPSIS</span></span>
<span data-ttu-id="8639f-103">Valida uma implantação de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8639f-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="8639f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8639f-104">SYNTAX</span></span>

### <span data-ttu-id="8639f-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="8639f-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8639f-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8639f-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8639f-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8639f-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8639f-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8639f-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8639f-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8639f-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8639f-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8639f-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8639f-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8639f-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8639f-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8639f-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8639f-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8639f-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8639f-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8639f-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8639f-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8639f-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8639f-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8639f-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8639f-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8639f-117">DESCRIPTION</span></span>
<span data-ttu-id="8639f-118">O cmdlet **Test-AzResourceGroupDeployment** determina se um modelo de implantação do grupo de recursos do Azure e seus valores de parâmetro são válidos.</span><span class="sxs-lookup"><span data-stu-id="8639f-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="8639f-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8639f-119">EXAMPLES</span></span>

### <span data-ttu-id="8639f-120">Exemplo 1: implantação de teste com um objeto de modelo personalizado e um arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="8639f-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="8639f-121">Esse comando testa uma implantação no grupo de recursos específico usando a Hashtable na memória criada a partir do arquivo de modelo específico e um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8639f-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="8639f-122">Exemplo 2: implantação de teste via arquivo de modelo e objeto de parâmetro</span><span class="sxs-lookup"><span data-stu-id="8639f-122">Example 2: Test deployment via template file and parameter object</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name testDeployment1 -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="8639f-123">Esse comando testa a implantação no grupo de recursos e no recurso fornecido usando o arquivo de modelo fornecido e um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8639f-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="8639f-124">OS</span><span class="sxs-lookup"><span data-stu-id="8639f-124">PARAMETERS</span></span>

### <span data-ttu-id="8639f-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8639f-125">-ApiVersion</span></span>
<span data-ttu-id="8639f-126">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8639f-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8639f-127">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="8639f-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8639f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8639f-128">-DefaultProfile</span></span>
<span data-ttu-id="8639f-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8639f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8639f-130">-Mode</span><span class="sxs-lookup"><span data-stu-id="8639f-130">-Mode</span></span>
<span data-ttu-id="8639f-131">Especifica o modo de implantação.</span><span class="sxs-lookup"><span data-stu-id="8639f-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="8639f-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8639f-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8639f-133">Adicionais</span><span class="sxs-lookup"><span data-stu-id="8639f-133">Incremental</span></span>
- <span data-ttu-id="8639f-134">Assuma</span><span class="sxs-lookup"><span data-stu-id="8639f-134">Complete</span></span>

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

### <span data-ttu-id="8639f-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="8639f-135">-Pre</span></span>
<span data-ttu-id="8639f-136">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8639f-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8639f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8639f-137">-ResourceGroupName</span></span>
<span data-ttu-id="8639f-138">Especifica o nome do grupo de recursos para testar.</span><span class="sxs-lookup"><span data-stu-id="8639f-138">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="8639f-139">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="8639f-139">-RollBackDeploymentName</span></span>
<span data-ttu-id="8639f-140">A reversão para a implantação bem-sucedida com o nome especificado no grupo de recursos não deve ser usada se-RollbackToLastDeployment for usado.</span><span class="sxs-lookup"><span data-stu-id="8639f-140">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="8639f-141">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="8639f-141">-RollbackToLastDeployment</span></span>
<span data-ttu-id="8639f-142">A reversão para a última implantação bem-sucedida no grupo de recursos não deve estar presente se-RollBackDeploymentName for usado.</span><span class="sxs-lookup"><span data-stu-id="8639f-142">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="8639f-143">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="8639f-143">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="8639f-144">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="8639f-144">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="8639f-145">Essa verificação solicitaria que o usuário forneça um valor para os parâmetros ausentes, mas fornecer o-SkipTemplateParameterPrompt ignorará esse prompt e o erro será imediatamente se um parâmetro não fosse associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="8639f-145">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="8639f-146">Para scripts não interativos,-SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso não seja satisfeito todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8639f-146">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="8639f-147">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8639f-147">-TemplateFile</span></span>
<span data-ttu-id="8639f-148">Especifica o caminho completo de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="8639f-148">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="8639f-149">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="8639f-149">-TemplateObject</span></span>
<span data-ttu-id="8639f-150">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="8639f-150">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="8639f-151">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8639f-151">-TemplateParameterFile</span></span>
<span data-ttu-id="8639f-152">Especifica o caminho completo de um arquivo JSON que contém os nomes e os valores dos parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="8639f-152">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="8639f-153">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="8639f-153">-TemplateParameterObject</span></span>
<span data-ttu-id="8639f-154">Especifica uma tabela de hash de nomes e valores de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="8639f-154">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="8639f-155">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="8639f-155">-TemplateParameterUri</span></span>
<span data-ttu-id="8639f-156">Especifica o URI de um arquivo de parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="8639f-156">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="8639f-157">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="8639f-157">-TemplateUri</span></span>
<span data-ttu-id="8639f-158">Especifica o URI de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="8639f-158">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="8639f-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8639f-159">CommonParameters</span></span>
<span data-ttu-id="8639f-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8639f-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8639f-161">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8639f-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8639f-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8639f-162">INPUTS</span></span>

### <span data-ttu-id="8639f-163">System. String</span><span class="sxs-lookup"><span data-stu-id="8639f-163">System.String</span></span>

### <span data-ttu-id="8639f-164">Microsoft. Azure. Management. ResourceManager. Models. Deploymentmode</span><span class="sxs-lookup"><span data-stu-id="8639f-164">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="8639f-165">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8639f-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8639f-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8639f-166">OUTPUTS</span></span>

### <span data-ttu-id="8639f-167">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="8639f-167">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="8639f-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8639f-168">NOTES</span></span>

## <span data-ttu-id="8639f-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8639f-169">RELATED LINKS</span></span>

[<span data-ttu-id="8639f-170">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8639f-170">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="8639f-171">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8639f-171">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="8639f-172">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8639f-172">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="8639f-173">Parar-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8639f-173">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


