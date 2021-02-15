---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5144dacb044523c2ad72d0a9c24aa43427f14f99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111401"
---
# <span data-ttu-id="acc67-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="acc67-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="acc67-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acc67-102">SYNOPSIS</span></span>
<span data-ttu-id="acc67-103">Valida uma implantação no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="acc67-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="acc67-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="acc67-104">SYNTAX</span></span>

### <span data-ttu-id="acc67-105">ByTemplateFileWithNoParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="acc67-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc67-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="acc67-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc67-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="acc67-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc67-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="acc67-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc67-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="acc67-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc67-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="acc67-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc67-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="acc67-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc67-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="acc67-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc67-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="acc67-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc67-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="acc67-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc67-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="acc67-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc67-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="acc67-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acc67-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="acc67-117">DESCRIPTION</span></span>
<span data-ttu-id="acc67-118">O cmdlet **Test-AzTenantDeployment** determina se um modelo de implantação e seus valores de parâmetro são válidos no escopo atual do locatário.</span><span class="sxs-lookup"><span data-stu-id="acc67-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="acc67-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="acc67-119">EXAMPLES</span></span>

### <span data-ttu-id="acc67-120">Exemplo 1: Testar a implantação com um modelo personalizado e um arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="acc67-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="acc67-121">Esse comando testa uma implantação no escopo do locatário atual usando o arquivo de modelo determinado e o arquivo de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="acc67-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="acc67-122">Exemplo 2: Testar a implantação com um objeto de modelo personalizado e um arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="acc67-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="acc67-123">Esse comando testa uma implantação no escopo do locatário atual usando uma tabela hashtable na memória criada a partir do arquivo de modelo determinado e um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="acc67-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="acc67-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acc67-124">PARAMETERS</span></span>

### <span data-ttu-id="acc67-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc67-125">-DefaultProfile</span></span>
<span data-ttu-id="acc67-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="acc67-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acc67-127">-Local</span><span class="sxs-lookup"><span data-stu-id="acc67-127">-Location</span></span>
<span data-ttu-id="acc67-128">O local para armazenar dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="acc67-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="acc67-129">-Pré-</span><span class="sxs-lookup"><span data-stu-id="acc67-129">-Pre</span></span>
<span data-ttu-id="acc67-130">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="acc67-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="acc67-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="acc67-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="acc67-132">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="acc67-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="acc67-133">Essa verificação solicitaria que o usuário fornecesse um valor para os parâmetros ausentes, mas fornecer o -SkipTemplateParameterPrompt ignorará esse prompt e um erro imediatamente se um parâmetro não tiver sido vinculado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="acc67-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="acc67-134">Para scripts não interativos, -SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso nem todos os parâmetros necessários sejam satisfeitos.</span><span class="sxs-lookup"><span data-stu-id="acc67-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="acc67-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="acc67-135">-TemplateFile</span></span>
<span data-ttu-id="acc67-136">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="acc67-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="acc67-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="acc67-137">-TemplateObject</span></span>
<span data-ttu-id="acc67-138">Uma tabela hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="acc67-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="acc67-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="acc67-139">-TemplateParameterFile</span></span>
<span data-ttu-id="acc67-140">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="acc67-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="acc67-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="acc67-141">-TemplateParameterObject</span></span>
<span data-ttu-id="acc67-142">Uma tabela hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="acc67-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="acc67-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="acc67-143">-TemplateParameterUri</span></span>
<span data-ttu-id="acc67-144">Uri para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="acc67-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="acc67-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="acc67-145">-TemplateUri</span></span>
<span data-ttu-id="acc67-146">Uri para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="acc67-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="acc67-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc67-147">CommonParameters</span></span>
<span data-ttu-id="acc67-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc67-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc67-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acc67-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc67-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="acc67-150">INPUTS</span></span>

### <span data-ttu-id="acc67-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="acc67-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="acc67-152">System.String</span><span class="sxs-lookup"><span data-stu-id="acc67-152">System.String</span></span>

## <span data-ttu-id="acc67-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="acc67-153">OUTPUTS</span></span>

### <span data-ttu-id="acc67-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="acc67-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="acc67-155">Notas</span><span class="sxs-lookup"><span data-stu-id="acc67-155">NOTES</span></span>

## <span data-ttu-id="acc67-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acc67-156">RELATED LINKS</span></span>
