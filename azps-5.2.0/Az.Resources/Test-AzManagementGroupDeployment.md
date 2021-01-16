---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263673"
---
# <span data-ttu-id="95e26-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="95e26-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="95e26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95e26-102">SYNOPSIS</span></span>
<span data-ttu-id="95e26-103">Valida uma implantação em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="95e26-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="95e26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95e26-104">SYNTAX</span></span>

### <span data-ttu-id="95e26-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="95e26-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95e26-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="95e26-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95e26-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="95e26-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95e26-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="95e26-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95e26-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="95e26-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95e26-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="95e26-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95e26-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="95e26-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95e26-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="95e26-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95e26-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="95e26-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95e26-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="95e26-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95e26-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="95e26-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95e26-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="95e26-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95e26-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95e26-117">DESCRIPTION</span></span>
<span data-ttu-id="95e26-118">O cmdlet **Test-AzManagementGroupDeployment** determina se um modelo de implantação e seus valores de parâmetro são válidos em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="95e26-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="95e26-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95e26-119">EXAMPLES</span></span>

### <span data-ttu-id="95e26-120">Exemplo 1: implantação de teste com um arquivo de modelo e um arquivo de parâmetro personalizado</span><span class="sxs-lookup"><span data-stu-id="95e26-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="95e26-121">Esse comando testa a implantação no grupo de gerenciamento "myMG" usando o arquivo de modelo e o arquivo de parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="95e26-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="95e26-122">Exemplo 2: implantação de teste com um objeto de modelo personalizado e um arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="95e26-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="95e26-123">Esse comando testa uma implantação no grupo de gerenciamento "myMG" usando uma Hashtable na memória criada a partir do arquivo de modelo específico e um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="95e26-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="95e26-124">OS</span><span class="sxs-lookup"><span data-stu-id="95e26-124">PARAMETERS</span></span>

### <span data-ttu-id="95e26-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e26-125">-DefaultProfile</span></span>
<span data-ttu-id="95e26-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95e26-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95e26-127">-Local</span><span class="sxs-lookup"><span data-stu-id="95e26-127">-Location</span></span>
<span data-ttu-id="95e26-128">O local para armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="95e26-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="95e26-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="95e26-129">-ManagementGroupId</span></span>
<span data-ttu-id="95e26-130">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="95e26-130">The management group id.</span></span>

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

### <span data-ttu-id="95e26-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="95e26-131">-Pre</span></span>
<span data-ttu-id="95e26-132">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="95e26-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="95e26-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="95e26-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="95e26-134">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="95e26-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="95e26-135">Essa verificação solicitaria que o usuário forneça um valor para os parâmetros ausentes, mas fornecer o-SkipTemplateParameterPrompt ignorará esse prompt e o erro será imediatamente se um parâmetro não fosse associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="95e26-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="95e26-136">Para scripts não interativos,-SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso não seja satisfeito todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="95e26-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="95e26-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="95e26-137">-TemplateFile</span></span>
<span data-ttu-id="95e26-138">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="95e26-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="95e26-139">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="95e26-139">-TemplateObject</span></span>
<span data-ttu-id="95e26-140">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="95e26-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="95e26-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="95e26-141">-TemplateParameterFile</span></span>
<span data-ttu-id="95e26-142">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="95e26-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="95e26-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="95e26-143">-TemplateParameterObject</span></span>
<span data-ttu-id="95e26-144">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="95e26-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="95e26-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="95e26-145">-TemplateParameterUri</span></span>
<span data-ttu-id="95e26-146">URL para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="95e26-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="95e26-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="95e26-147">-TemplateUri</span></span>
<span data-ttu-id="95e26-148">URL para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="95e26-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="95e26-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e26-149">CommonParameters</span></span>
<span data-ttu-id="95e26-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95e26-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e26-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95e26-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e26-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95e26-152">INPUTS</span></span>

### <span data-ttu-id="95e26-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="95e26-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="95e26-154">System. String</span><span class="sxs-lookup"><span data-stu-id="95e26-154">System.String</span></span>

## <span data-ttu-id="95e26-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95e26-155">OUTPUTS</span></span>

### <span data-ttu-id="95e26-156">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="95e26-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="95e26-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95e26-157">NOTES</span></span>

## <span data-ttu-id="95e26-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95e26-158">RELATED LINKS</span></span>
