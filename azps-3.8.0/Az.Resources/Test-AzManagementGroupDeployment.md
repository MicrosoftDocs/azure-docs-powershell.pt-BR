---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 81ee04b5248a95d686c2c135dfee0e73e6722bb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941704"
---
# <span data-ttu-id="349d3-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="349d3-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="349d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="349d3-102">SYNOPSIS</span></span>
<span data-ttu-id="349d3-103">Valida uma implantação em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="349d3-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="349d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="349d3-104">SYNTAX</span></span>

### <span data-ttu-id="349d3-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="349d3-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="349d3-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="349d3-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349d3-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="349d3-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349d3-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="349d3-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349d3-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="349d3-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349d3-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="349d3-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349d3-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="349d3-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349d3-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="349d3-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349d3-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="349d3-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349d3-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="349d3-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349d3-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="349d3-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="349d3-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="349d3-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="349d3-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="349d3-117">DESCRIPTION</span></span>
<span data-ttu-id="349d3-118">O cmdlet **Test-AzManagementGroupDeployment** determina se um modelo de implantação e seus valores de parâmetro são válidos em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="349d3-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="349d3-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="349d3-119">EXAMPLES</span></span>

### <span data-ttu-id="349d3-120">Exemplo 1: implantação de teste com um arquivo de modelo e um arquivo de parâmetro personalizado</span><span class="sxs-lookup"><span data-stu-id="349d3-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="349d3-121">Esse comando testa a implantação no grupo de gerenciamento "myMG" usando o arquivo de modelo e o arquivo de parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="349d3-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="349d3-122">Exemplo 2: implantação de teste com um objeto de modelo personalizado e um arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="349d3-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="349d3-123">Esse comando testa uma implantação no grupo de gerenciamento "myMG" usando uma Hashtable na memória criada a partir do arquivo de modelo específico e um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="349d3-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="349d3-124">OS</span><span class="sxs-lookup"><span data-stu-id="349d3-124">PARAMETERS</span></span>

### <span data-ttu-id="349d3-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="349d3-125">-ApiVersion</span></span>
<span data-ttu-id="349d3-126">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="349d3-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="349d3-127">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="349d3-127">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349d3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349d3-128">-DefaultProfile</span></span>
<span data-ttu-id="349d3-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="349d3-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349d3-130">-Local</span><span class="sxs-lookup"><span data-stu-id="349d3-130">-Location</span></span>
<span data-ttu-id="349d3-131">O local para armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="349d3-131">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349d3-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="349d3-132">-ManagementGroupId</span></span>
<span data-ttu-id="349d3-133">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="349d3-133">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349d3-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="349d3-134">-Pre</span></span>
<span data-ttu-id="349d3-135">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="349d3-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349d3-136">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="349d3-136">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="349d3-137">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="349d3-137">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="349d3-138">Essa verificação solicitaria que o usuário forneça um valor para os parâmetros ausentes, mas fornecer o-SkipTemplateParameterPrompt ignorará esse prompt e o erro será imediatamente se um parâmetro não fosse associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="349d3-138">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="349d3-139">Para scripts não interativos,-SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso não seja satisfeito todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="349d3-139">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349d3-140">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="349d3-140">-TemplateFile</span></span>
<span data-ttu-id="349d3-141">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="349d3-141">Local path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="349d3-142">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="349d3-142">-TemplateObject</span></span>
<span data-ttu-id="349d3-143">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="349d3-143">A hash table which represents the template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="349d3-144">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="349d3-144">-TemplateParameterFile</span></span>
<span data-ttu-id="349d3-145">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="349d3-145">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="349d3-146">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="349d3-146">-TemplateParameterObject</span></span>
<span data-ttu-id="349d3-147">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="349d3-147">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="349d3-148">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="349d3-148">-TemplateParameterUri</span></span>
<span data-ttu-id="349d3-149">URL para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="349d3-149">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="349d3-150">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="349d3-150">-TemplateUri</span></span>
<span data-ttu-id="349d3-151">URL para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="349d3-151">Uri to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="349d3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349d3-152">CommonParameters</span></span>
<span data-ttu-id="349d3-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="349d3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349d3-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="349d3-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349d3-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="349d3-155">INPUTS</span></span>

### <span data-ttu-id="349d3-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="349d3-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="349d3-157">System. String</span><span class="sxs-lookup"><span data-stu-id="349d3-157">System.String</span></span>

## <span data-ttu-id="349d3-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="349d3-158">OUTPUTS</span></span>

### <span data-ttu-id="349d3-159">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="349d3-159">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="349d3-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="349d3-160">NOTES</span></span>

## <span data-ttu-id="349d3-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="349d3-161">RELATED LINKS</span></span>
