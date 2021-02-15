---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 9a1a183ac6a0fb896f6b3d901e8f429fdf225e26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111405"
---
# <span data-ttu-id="10cae-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="10cae-101">Test-AzDeployment</span></span>

## <span data-ttu-id="10cae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10cae-102">SYNOPSIS</span></span>
<span data-ttu-id="10cae-103">Valida uma implantação.</span><span class="sxs-lookup"><span data-stu-id="10cae-103">Validates a deployment.</span></span>

## <span data-ttu-id="10cae-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10cae-104">SYNTAX</span></span>

### <span data-ttu-id="10cae-105">ByTemplateFileWithNoParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="10cae-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cae-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="10cae-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cae-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="10cae-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cae-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="10cae-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cae-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="10cae-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cae-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="10cae-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cae-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="10cae-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cae-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="10cae-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cae-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="10cae-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cae-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="10cae-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cae-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="10cae-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10cae-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="10cae-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10cae-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="10cae-117">DESCRIPTION</span></span>
<span data-ttu-id="10cae-118">O **cmdlet Test-AzDeployment** determina se um modelo de implantação e seus valores de parâmetro são válidos.</span><span class="sxs-lookup"><span data-stu-id="10cae-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="10cae-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10cae-119">EXAMPLES</span></span>

### <span data-ttu-id="10cae-120">Exemplo 1: Testar a implantação com um modelo personalizado e um arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="10cae-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="10cae-121">Esse comando testa uma implantação no escopo da assinatura atual usando o arquivo de modelo determinado e o arquivo de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="10cae-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="10cae-122">Exemplo 2: Testar a implantação com um objeto de modelo personalizado e um arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="10cae-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="10cae-123">Esse comando testa uma implantação no escopo da assinatura atual usando uma tabela de hash na memória criada a partir do arquivo de modelo determinado e um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="10cae-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="10cae-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10cae-124">PARAMETERS</span></span>

### <span data-ttu-id="10cae-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10cae-125">-DefaultProfile</span></span>
<span data-ttu-id="10cae-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10cae-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10cae-127">-Local</span><span class="sxs-lookup"><span data-stu-id="10cae-127">-Location</span></span>
<span data-ttu-id="10cae-128">O local para armazenar dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="10cae-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="10cae-129">-Pré-</span><span class="sxs-lookup"><span data-stu-id="10cae-129">-Pre</span></span>
<span data-ttu-id="10cae-130">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="10cae-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="10cae-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="10cae-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="10cae-132">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="10cae-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="10cae-133">Essa verificação solicitaria que o usuário fornecesse um valor para os parâmetros ausentes, mas fornecer o -SkipTemplateParameterPrompt ignorará esse prompt e um erro imediatamente se um parâmetro não tiver sido vinculado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="10cae-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="10cae-134">Para scripts não interativos, -SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso nem todos os parâmetros necessários sejam satisfeitos.</span><span class="sxs-lookup"><span data-stu-id="10cae-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="10cae-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="10cae-135">-TemplateFile</span></span>
<span data-ttu-id="10cae-136">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="10cae-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="10cae-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="10cae-137">-TemplateObject</span></span>
<span data-ttu-id="10cae-138">Uma tabela hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="10cae-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="10cae-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="10cae-139">-TemplateParameterFile</span></span>
<span data-ttu-id="10cae-140">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="10cae-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="10cae-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="10cae-141">-TemplateParameterObject</span></span>
<span data-ttu-id="10cae-142">Uma tabela hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="10cae-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="10cae-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="10cae-143">-TemplateParameterUri</span></span>
<span data-ttu-id="10cae-144">Uri para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="10cae-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="10cae-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="10cae-145">-TemplateUri</span></span>
<span data-ttu-id="10cae-146">Uri para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="10cae-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="10cae-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10cae-147">CommonParameters</span></span>
<span data-ttu-id="10cae-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10cae-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10cae-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10cae-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10cae-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="10cae-150">INPUTS</span></span>

### <span data-ttu-id="10cae-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="10cae-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="10cae-152">System.String</span><span class="sxs-lookup"><span data-stu-id="10cae-152">System.String</span></span>

## <span data-ttu-id="10cae-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="10cae-153">OUTPUTS</span></span>

### <span data-ttu-id="10cae-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="10cae-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="10cae-155">Notas</span><span class="sxs-lookup"><span data-stu-id="10cae-155">NOTES</span></span>

## <span data-ttu-id="10cae-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10cae-156">RELATED LINKS</span></span>
