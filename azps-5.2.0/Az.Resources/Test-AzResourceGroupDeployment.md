---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260226"
---
# <span data-ttu-id="227c8-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="227c8-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="227c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="227c8-102">SYNOPSIS</span></span>
<span data-ttu-id="227c8-103">Valida uma implantação de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="227c8-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="227c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="227c8-104">SYNTAX</span></span>

### <span data-ttu-id="227c8-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="227c8-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="227c8-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="227c8-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="227c8-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="227c8-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="227c8-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="227c8-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="227c8-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="227c8-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="227c8-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="227c8-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="227c8-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="227c8-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="227c8-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="227c8-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="227c8-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="227c8-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="227c8-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="227c8-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="227c8-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="227c8-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="227c8-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="227c8-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="227c8-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="227c8-117">DESCRIPTION</span></span>
<span data-ttu-id="227c8-118">O cmdlet **Test-AzResourceGroupDeployment** determina se um modelo de implantação do grupo de recursos do Azure e seus valores de parâmetro são válidos.</span><span class="sxs-lookup"><span data-stu-id="227c8-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="227c8-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="227c8-119">EXAMPLES</span></span>

### <span data-ttu-id="227c8-120">Exemplo 1: implantação de teste com um objeto de modelo personalizado e um arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="227c8-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="227c8-121">Esse comando testa uma implantação no grupo de recursos específico usando a Hashtable na memória criada a partir do arquivo de modelo específico e um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="227c8-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="227c8-122">Exemplo 2: implantação de teste via arquivo de modelo e arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="227c8-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="227c8-123">Esse comando testa a implantação no grupo de recursos e no recurso fornecido usando o arquivo de modelo fornecido e um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="227c8-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="227c8-124">OS</span><span class="sxs-lookup"><span data-stu-id="227c8-124">PARAMETERS</span></span>

### <span data-ttu-id="227c8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="227c8-125">-DefaultProfile</span></span>
<span data-ttu-id="227c8-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="227c8-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="227c8-127">-Mode</span><span class="sxs-lookup"><span data-stu-id="227c8-127">-Mode</span></span>
<span data-ttu-id="227c8-128">Especifica o modo de implantação.</span><span class="sxs-lookup"><span data-stu-id="227c8-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="227c8-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="227c8-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="227c8-130">Adicionais</span><span class="sxs-lookup"><span data-stu-id="227c8-130">Incremental</span></span>
- <span data-ttu-id="227c8-131">Assuma</span><span class="sxs-lookup"><span data-stu-id="227c8-131">Complete</span></span>

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

### <span data-ttu-id="227c8-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="227c8-132">-Pre</span></span>
<span data-ttu-id="227c8-133">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="227c8-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="227c8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="227c8-134">-ResourceGroupName</span></span>
<span data-ttu-id="227c8-135">Especifica o nome do grupo de recursos para testar.</span><span class="sxs-lookup"><span data-stu-id="227c8-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="227c8-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="227c8-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="227c8-137">A reversão para a implantação bem-sucedida com o nome especificado no grupo de recursos não deve ser usada se-RollbackToLastDeployment for usado.</span><span class="sxs-lookup"><span data-stu-id="227c8-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="227c8-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="227c8-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="227c8-139">A reversão para a última implantação bem-sucedida no grupo de recursos não deve estar presente se-RollBackDeploymentName for usado.</span><span class="sxs-lookup"><span data-stu-id="227c8-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="227c8-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="227c8-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="227c8-141">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="227c8-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="227c8-142">Essa verificação solicitaria que o usuário forneça um valor para os parâmetros ausentes, mas fornecer o-SkipTemplateParameterPrompt ignorará esse prompt e o erro será imediatamente se um parâmetro não fosse associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="227c8-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="227c8-143">Para scripts não interativos,-SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso não seja satisfeito todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="227c8-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="227c8-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="227c8-144">-TemplateFile</span></span>
<span data-ttu-id="227c8-145">Especifica o caminho completo de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="227c8-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="227c8-146">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="227c8-146">-TemplateObject</span></span>
<span data-ttu-id="227c8-147">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="227c8-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="227c8-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="227c8-148">-TemplateParameterFile</span></span>
<span data-ttu-id="227c8-149">Especifica o caminho completo de um arquivo JSON que contém os nomes e os valores dos parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="227c8-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="227c8-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="227c8-150">-TemplateParameterObject</span></span>
<span data-ttu-id="227c8-151">Especifica uma tabela de hash de nomes e valores de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="227c8-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="227c8-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="227c8-152">-TemplateParameterUri</span></span>
<span data-ttu-id="227c8-153">Especifica o URI de um arquivo de parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="227c8-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="227c8-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="227c8-154">-TemplateUri</span></span>
<span data-ttu-id="227c8-155">Especifica o URI de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="227c8-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="227c8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="227c8-156">CommonParameters</span></span>
<span data-ttu-id="227c8-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="227c8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="227c8-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="227c8-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="227c8-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="227c8-159">INPUTS</span></span>

### <span data-ttu-id="227c8-160">System. String</span><span class="sxs-lookup"><span data-stu-id="227c8-160">System.String</span></span>

### <span data-ttu-id="227c8-161">Microsoft. Azure. Management. ResourceManager. Models. Deploymentmode</span><span class="sxs-lookup"><span data-stu-id="227c8-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="227c8-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="227c8-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="227c8-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="227c8-163">OUTPUTS</span></span>

### <span data-ttu-id="227c8-164">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="227c8-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="227c8-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="227c8-165">NOTES</span></span>

## <span data-ttu-id="227c8-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="227c8-166">RELATED LINKS</span></span>

[<span data-ttu-id="227c8-167">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="227c8-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="227c8-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="227c8-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="227c8-169">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="227c8-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="227c8-170">Parar-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="227c8-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


