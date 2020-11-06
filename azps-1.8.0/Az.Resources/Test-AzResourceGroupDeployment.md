---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 01d7aa0cb0b363dac8e19e5b38796c43523d6296
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599297"
---
# <span data-ttu-id="71d87-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71d87-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="71d87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71d87-102">SYNOPSIS</span></span>
<span data-ttu-id="71d87-103">Valida uma implantação de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71d87-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="71d87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71d87-104">SYNTAX</span></span>

### <span data-ttu-id="71d87-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="71d87-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71d87-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="71d87-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71d87-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="71d87-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71d87-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="71d87-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71d87-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="71d87-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71d87-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="71d87-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71d87-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="71d87-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71d87-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="71d87-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71d87-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="71d87-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71d87-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="71d87-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71d87-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="71d87-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71d87-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="71d87-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71d87-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71d87-117">DESCRIPTION</span></span>
<span data-ttu-id="71d87-118">O cmdlet **Test-AzResourceGroupDeployment** determina se um modelo de implantação do grupo de recursos do Azure e seus valores de parâmetro são válidos.</span><span class="sxs-lookup"><span data-stu-id="71d87-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="71d87-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71d87-119">EXAMPLES</span></span>

### <span data-ttu-id="71d87-120">Exemplo 1: implantação de teste com um objeto de modelo personalizado e um arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="71d87-120">Example 1: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="71d87-121">Esse comando testa uma implantação no grupo de recursos específico usando a Hashtable na memória criada a partir do arquivo de modelo específico e um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="71d87-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="71d87-122">OS</span><span class="sxs-lookup"><span data-stu-id="71d87-122">PARAMETERS</span></span>

### <span data-ttu-id="71d87-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="71d87-123">-ApiVersion</span></span>
<span data-ttu-id="71d87-124">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="71d87-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="71d87-125">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="71d87-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="71d87-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d87-126">-DefaultProfile</span></span>
<span data-ttu-id="71d87-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="71d87-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71d87-128">-Mode</span><span class="sxs-lookup"><span data-stu-id="71d87-128">-Mode</span></span>
<span data-ttu-id="71d87-129">Especifica o modo de implantação.</span><span class="sxs-lookup"><span data-stu-id="71d87-129">Specifies the deployment mode.</span></span>
<span data-ttu-id="71d87-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="71d87-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71d87-131">Adicionais</span><span class="sxs-lookup"><span data-stu-id="71d87-131">Incremental</span></span>
- <span data-ttu-id="71d87-132">Assuma</span><span class="sxs-lookup"><span data-stu-id="71d87-132">Complete</span></span>

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

### <span data-ttu-id="71d87-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="71d87-133">-Pre</span></span>
<span data-ttu-id="71d87-134">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="71d87-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="71d87-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71d87-135">-ResourceGroupName</span></span>
<span data-ttu-id="71d87-136">Especifica o nome do grupo de recursos para testar.</span><span class="sxs-lookup"><span data-stu-id="71d87-136">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="71d87-137">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="71d87-137">-RollBackDeploymentName</span></span>
<span data-ttu-id="71d87-138">A reversão para a implantação bem-sucedida com o nome especificado no grupo de recursos não deve ser usada se-RollbackToLastDeployment for usado.</span><span class="sxs-lookup"><span data-stu-id="71d87-138">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="71d87-139">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="71d87-139">-RollbackToLastDeployment</span></span>
<span data-ttu-id="71d87-140">A reversão para a última implantação bem-sucedida no grupo de recursos não deve estar presente se-RollBackDeploymentName for usado.</span><span class="sxs-lookup"><span data-stu-id="71d87-140">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="71d87-141">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="71d87-141">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="71d87-142">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="71d87-142">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="71d87-143">Essa verificação solicitaria que o usuário forneça um valor para os parâmetros ausentes, mas fornecer o-SkipTemplateParameterPrompt ignorará esse prompt e o erro será imediatamente se um parâmetro não fosse associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="71d87-143">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="71d87-144">Para scripts não interativos,-SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso não seja satisfeito todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="71d87-144">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="71d87-145">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="71d87-145">-TemplateFile</span></span>
<span data-ttu-id="71d87-146">Especifica o caminho completo de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="71d87-146">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="71d87-147">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="71d87-147">-TemplateObject</span></span>
<span data-ttu-id="71d87-148">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="71d87-148">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="71d87-149">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="71d87-149">-TemplateParameterFile</span></span>
<span data-ttu-id="71d87-150">Especifica o caminho completo de um arquivo JSON que contém os nomes e os valores dos parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="71d87-150">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="71d87-151">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="71d87-151">-TemplateParameterObject</span></span>
<span data-ttu-id="71d87-152">Especifica uma tabela de hash de nomes e valores de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="71d87-152">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="71d87-153">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="71d87-153">-TemplateParameterUri</span></span>
<span data-ttu-id="71d87-154">Especifica o URI de um arquivo de parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="71d87-154">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="71d87-155">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="71d87-155">-TemplateUri</span></span>
<span data-ttu-id="71d87-156">Especifica o URI de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="71d87-156">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="71d87-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d87-157">CommonParameters</span></span>
<span data-ttu-id="71d87-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71d87-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d87-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71d87-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d87-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71d87-160">INPUTS</span></span>

### <span data-ttu-id="71d87-161">System. String</span><span class="sxs-lookup"><span data-stu-id="71d87-161">System.String</span></span>

### <span data-ttu-id="71d87-162">Microsoft. Azure. Management. ResourceManager. Models. Deploymentmode</span><span class="sxs-lookup"><span data-stu-id="71d87-162">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="71d87-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="71d87-163">System.Collections.Hashtable</span></span>

## <span data-ttu-id="71d87-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71d87-164">OUTPUTS</span></span>

### <span data-ttu-id="71d87-165">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="71d87-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="71d87-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71d87-166">NOTES</span></span>

## <span data-ttu-id="71d87-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71d87-167">RELATED LINKS</span></span>

[<span data-ttu-id="71d87-168">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71d87-168">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="71d87-169">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71d87-169">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="71d87-170">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71d87-170">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="71d87-171">Parar-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71d87-171">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


