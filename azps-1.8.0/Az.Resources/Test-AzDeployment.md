---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 182cf4d60cf2b81f5a465f9ffad5d862b09e3787
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599298"
---
# <span data-ttu-id="2b760-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="2b760-101">Test-AzDeployment</span></span>

## <span data-ttu-id="2b760-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b760-102">SYNOPSIS</span></span>
<span data-ttu-id="2b760-103">Valida uma implantação.</span><span class="sxs-lookup"><span data-stu-id="2b760-103">Validates a deployment.</span></span>

## <span data-ttu-id="2b760-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b760-104">SYNTAX</span></span>

### <span data-ttu-id="2b760-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="2b760-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b760-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2b760-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b760-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2b760-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b760-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2b760-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b760-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2b760-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b760-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2b760-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b760-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2b760-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b760-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2b760-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b760-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2b760-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b760-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2b760-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b760-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2b760-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b760-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2b760-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b760-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b760-117">DESCRIPTION</span></span>
<span data-ttu-id="2b760-118">O cmdlet **Test-AzDeployment** determina se um modelo de implantação e seus valores de parâmetro são válidos.</span><span class="sxs-lookup"><span data-stu-id="2b760-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="2b760-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b760-119">EXAMPLES</span></span>

### <span data-ttu-id="2b760-120">Exemplo 1: implantação de teste com um arquivo de modelo e um arquivo de parâmetro personalizado</span><span class="sxs-lookup"><span data-stu-id="2b760-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="2b760-121">Esse comando testa a implantação no escopo de assinatura atual usando o arquivo de modelo e o arquivo de parâmetros fornecido.</span><span class="sxs-lookup"><span data-stu-id="2b760-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="2b760-122">Exemplo 2: implantação de teste com um objeto de modelo personalizado e um arquivo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b760-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="2b760-123">Esse comando testa a implantação no escopo de assinatura atual usando a Hashtable em memória criada a partir do arquivo de modelo específico e de um arquivo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2b760-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="2b760-124">OS</span><span class="sxs-lookup"><span data-stu-id="2b760-124">PARAMETERS</span></span>

### <span data-ttu-id="2b760-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2b760-125">-ApiVersion</span></span>
<span data-ttu-id="2b760-126">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="2b760-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2b760-127">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="2b760-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2b760-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b760-128">-DefaultProfile</span></span>
<span data-ttu-id="2b760-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b760-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b760-130">-Local</span><span class="sxs-lookup"><span data-stu-id="2b760-130">-Location</span></span>
<span data-ttu-id="2b760-131">O local para armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="2b760-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="2b760-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="2b760-132">-Pre</span></span>
<span data-ttu-id="2b760-133">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="2b760-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2b760-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="2b760-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="2b760-135">Ignora o processamento de parâmetro dinâmico do PowerShell que verifica se o parâmetro de modelo fornecido contém todos os parâmetros necessários usados pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="2b760-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="2b760-136">Essa verificação solicitaria que o usuário forneça um valor para os parâmetros ausentes, mas fornecer o-SkipTemplateParameterPrompt ignorará esse prompt e o erro será imediatamente se um parâmetro não fosse associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="2b760-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="2b760-137">Para scripts não interativos,-SkipTemplateParameterPrompt pode ser fornecido para fornecer uma mensagem de erro melhor caso não seja satisfeito todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="2b760-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="2b760-138">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2b760-138">-TemplateFile</span></span>
<span data-ttu-id="2b760-139">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="2b760-139">Local path to the template file.</span></span>

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

### <span data-ttu-id="2b760-140">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="2b760-140">-TemplateObject</span></span>
<span data-ttu-id="2b760-141">Uma tabela de hash que representa o modelo.</span><span class="sxs-lookup"><span data-stu-id="2b760-141">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="2b760-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2b760-142">-TemplateParameterFile</span></span>
<span data-ttu-id="2b760-143">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="2b760-143">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="2b760-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2b760-144">-TemplateParameterObject</span></span>
<span data-ttu-id="2b760-145">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2b760-145">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="2b760-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2b760-146">-TemplateParameterUri</span></span>
<span data-ttu-id="2b760-147">URL para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="2b760-147">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="2b760-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2b760-148">-TemplateUri</span></span>
<span data-ttu-id="2b760-149">URL para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="2b760-149">Uri to the template file.</span></span>

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

### <span data-ttu-id="2b760-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b760-150">CommonParameters</span></span>
<span data-ttu-id="2b760-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b760-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b760-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b760-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b760-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b760-153">INPUTS</span></span>

### <span data-ttu-id="2b760-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2b760-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2b760-155">System. String</span><span class="sxs-lookup"><span data-stu-id="2b760-155">System.String</span></span>

## <span data-ttu-id="2b760-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b760-156">OUTPUTS</span></span>

### <span data-ttu-id="2b760-157">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="2b760-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="2b760-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b760-158">NOTES</span></span>

## <span data-ttu-id="2b760-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b760-159">RELATED LINKS</span></span>
