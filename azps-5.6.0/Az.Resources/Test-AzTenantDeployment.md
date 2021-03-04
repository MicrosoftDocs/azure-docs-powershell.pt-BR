---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5c440c6f150993b947a0db2162ef0fd664e73220
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886399"
---
# <span data-ttu-id="8c19e-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8c19e-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="8c19e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c19e-102">SYNOPSIS</span></span>
<span data-ttu-id="8c19e-103">Valida uma implantação no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="8c19e-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="8c19e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8c19e-104">SYNTAX</span></span>

### <span data-ttu-id="8c19e-105">ByTemplateFileWithNoParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8c19e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c19e-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8c19e-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c19e-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8c19e-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c19e-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8c19e-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c19e-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8c19e-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c19e-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8c19e-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c19e-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8c19e-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c19e-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="8c19e-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c19e-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8c19e-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c19e-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8c19e-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c19e-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8c19e-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c19e-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="8c19e-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c19e-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8c19e-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c19e-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8c19e-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c19e-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="8c19e-119">ByTemplateSpecResourceId</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c19e-120">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8c19e-120">DESCRIPTION</span></span>
<span data-ttu-id="8c19e-121">O cmdlet **Test-AzTenantDeployment** determina se um modelo de implantação e seus valores de parâmetro são válidos no escopo de locatário atual.</span><span class="sxs-lookup"><span data-stu-id="8c19e-121">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="8c19e-122">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c19e-122">EXAMPLES</span></span>

### <span data-ttu-id="8c19e-123">Exemplo 1: Testar a implantação com um modelo personalizado e um arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c19e-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="8c19e-124">Este comando testa uma implantação no escopo de locatário atual usando o arquivo de modelo determinado e o arquivo de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8c19e-124">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="8c19e-125">Exemplo 2: Testar a implantação com um objeto de modelo personalizado e um arquivo de parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c19e-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="8c19e-126">Este comando testa uma implantação no escopo de locatário atual usando uma hashtable na memória criada a partir do arquivo de modelo determinado e de um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8c19e-126">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="8c19e-127">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8c19e-127">PARAMETERS</span></span>

### <span data-ttu-id="8c19e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c19e-128">-DefaultProfile</span></span>
<span data-ttu-id="8c19e-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c19e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c19e-130">-Location</span><span class="sxs-lookup"><span data-stu-id="8c19e-130">-Location</span></span>
<span data-ttu-id="8c19e-131">O local para armazenar dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="8c19e-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="8c19e-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="8c19e-132">-Pre</span></span>
<span data-ttu-id="8c19e-133">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8c19e-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8c19e-134">-QueryString</span><span class="sxs-lookup"><span data-stu-id="8c19e-134">-QueryString</span></span>
<span data-ttu-id="8c19e-135">A cadeia de caracteres de consulta (por exemplo, um token SAS) a ser usada com o parâmetro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="8c19e-135">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="8c19e-136">Seria usado no caso de modelos vinculados</span><span class="sxs-lookup"><span data-stu-id="8c19e-136">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="8c19e-137">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="8c19e-137">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="8c19e-138">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="8c19e-138">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="8c19e-139">Essa verificação solicitaria que o usuário fornecesse um valor para os parâmetros ausentes, mas o fornecimento de -SkipTemplateParameterPrompt ignorará esse prompt e o excluirá imediatamente se um parâmetro não tiver sido vinculado no modelo.</span><span class="sxs-lookup"><span data-stu-id="8c19e-139">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="8c19e-140">Para scripts não interativos, -SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso nem todos os parâmetros necessários sejam atendidos.</span><span class="sxs-lookup"><span data-stu-id="8c19e-140">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="8c19e-141">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8c19e-141">-TemplateFile</span></span>
<span data-ttu-id="8c19e-142">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="8c19e-142">Local path to the template file.</span></span> <span data-ttu-id="8c19e-143">Tipo de arquivo de modelo com suporte: json e bicep.</span><span class="sxs-lookup"><span data-stu-id="8c19e-143">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="8c19e-144">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="8c19e-144">-TemplateObject</span></span>
<span data-ttu-id="8c19e-145">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="8c19e-145">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="8c19e-146">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8c19e-146">-TemplateParameterFile</span></span>
<span data-ttu-id="8c19e-147">Um arquivo que tem os parâmetros do modelo.</span><span class="sxs-lookup"><span data-stu-id="8c19e-147">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="8c19e-148">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="8c19e-148">-TemplateParameterObject</span></span>
<span data-ttu-id="8c19e-149">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8c19e-149">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="8c19e-150">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="8c19e-150">-TemplateParameterUri</span></span>
<span data-ttu-id="8c19e-151">Uri para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="8c19e-151">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="8c19e-152">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="8c19e-152">-TemplateSpecId</span></span>
<span data-ttu-id="8c19e-153">ID do recurso do modeloSpec a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="8c19e-153">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="8c19e-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="8c19e-154">-TemplateUri</span></span>
<span data-ttu-id="8c19e-155">Uri para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="8c19e-155">Uri to the template file.</span></span>

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

### <span data-ttu-id="8c19e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c19e-156">CommonParameters</span></span>
<span data-ttu-id="8c19e-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c19e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c19e-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c19e-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c19e-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c19e-159">INPUTS</span></span>

### <span data-ttu-id="8c19e-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8c19e-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8c19e-161">System.String</span><span class="sxs-lookup"><span data-stu-id="8c19e-161">System.String</span></span>

## <span data-ttu-id="8c19e-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8c19e-162">OUTPUTS</span></span>

### <span data-ttu-id="8c19e-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="8c19e-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="8c19e-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="8c19e-164">NOTES</span></span>

## <span data-ttu-id="8c19e-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c19e-165">RELATED LINKS</span></span>
