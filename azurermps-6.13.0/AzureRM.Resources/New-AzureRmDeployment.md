---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmDeployment.md
ms.openlocfilehash: 3c28bc2a13bbcfdd496b8df01a757aa683a87802
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430039"
---
# <span data-ttu-id="744a3-101">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="744a3-101">New-AzureRmDeployment</span></span>

## <span data-ttu-id="744a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="744a3-102">SYNOPSIS</span></span>
<span data-ttu-id="744a3-103">Criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="744a3-103">Creat a deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="744a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="744a3-104">SYNTAX</span></span>

### <span data-ttu-id="744a3-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="744a3-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="744a3-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="744a3-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="744a3-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="744a3-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="744a3-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="744a3-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="744a3-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="744a3-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="744a3-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="744a3-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="744a3-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="744a3-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="744a3-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="744a3-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="744a3-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="744a3-113">DESCRIPTION</span></span>
<span data-ttu-id="744a3-114">O cmdlet **New-AzureRmDeployment** adiciona uma implantação ao escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="744a3-114">The **New-AzureRmDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="744a3-115">Isso inclui os recursos que a implantação requer.</span><span class="sxs-lookup"><span data-stu-id="744a3-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="744a3-116">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="744a3-116">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="744a3-117">Um recurso pode residir em um grupo de recursos, como servidor de banco de dados, banco de dados, site, máquina virtual ou conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="744a3-117">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span> <span data-ttu-id="744a3-118">Ou pode ser um recurso de nível de assinatura, como definição de função, definição de política, etc.</span><span class="sxs-lookup"><span data-stu-id="744a3-118">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="744a3-119">Para adicionar recursos a um grupo de recursos, use o **New-AzureRmDeployment** que cria uma implantação em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="744a3-119">To add resources to a resource group, use the **New-AzureRmDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="744a3-120">O cmdlet **New-AzureRmDeployment** cria uma implantação no escopo de assinatura atual, que implanta recursos de nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="744a3-120">The **New-AzureRmDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span> 

<span data-ttu-id="744a3-121">Para adicionar uma implantação na assinatura, especifique o local e um modelo.</span><span class="sxs-lookup"><span data-stu-id="744a3-121">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="744a3-122">O local informa ao Azure Resource Manager onde armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="744a3-122">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="744a3-123">O modelo é uma cadeia de caracteres JSON que contém recursos individuais a serem implantados.</span><span class="sxs-lookup"><span data-stu-id="744a3-123">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="744a3-124">O modelo inclui espaços reservados de parâmetro para recursos obrigatórios e valores de propriedade configuráveis, como nomes e tamanhos.</span><span class="sxs-lookup"><span data-stu-id="744a3-124">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="744a3-125">Para usar um modelo personalizado para a implantação, especifique o parâmetro *TemplateFile* ou o parâmetro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="744a3-125">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="744a3-126">Cada modelo tem parâmetros para propriedades configuráveis.</span><span class="sxs-lookup"><span data-stu-id="744a3-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="744a3-127">Para especificar valores para os parâmetros de modelo, especifique o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="744a3-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="744a3-128">Você também pode usar os parâmetros de modelo que são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="744a3-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="744a3-129">Para usar parâmetros dinâmicos, digite-os no prompt de comando ou digite um sinal de subtração (-) para indicar um parâmetro e use a tecla Tab para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="744a3-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="744a3-130">Os valores de parâmetro de modelo que você insere no prompt de comando prevalecem sobre os valores em um objeto ou arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="744a3-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="744a3-131">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="744a3-131">EXAMPLES</span></span>

### <span data-ttu-id="744a3-132">Exemplo 1: usar um modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="744a3-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="744a3-133">Esse comando cria uma nova implantação no escopo de assinatura atual usando um modelo personalizado e um arquivo de modelo no disco.</span><span class="sxs-lookup"><span data-stu-id="744a3-133">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="744a3-134">O comando usa o parâmetro *TemplateFile* para especificar o modelo e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="744a3-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="744a3-135">Ele usa o parâmetro *TemplateVersion* para especificar a versão do modelo.</span><span class="sxs-lookup"><span data-stu-id="744a3-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="744a3-136">OS</span><span class="sxs-lookup"><span data-stu-id="744a3-136">PARAMETERS</span></span>

### <span data-ttu-id="744a3-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="744a3-137">-ApiVersion</span></span>
<span data-ttu-id="744a3-138">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="744a3-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="744a3-139">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="744a3-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="744a3-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="744a3-140">-AsJob</span></span>
<span data-ttu-id="744a3-141">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="744a3-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="744a3-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744a3-142">-DefaultProfile</span></span>
<span data-ttu-id="744a3-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="744a3-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744a3-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="744a3-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="744a3-145">O nível de log de depuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="744a3-145">The deployment debug log level.</span></span>

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

### <span data-ttu-id="744a3-146">-Local</span><span class="sxs-lookup"><span data-stu-id="744a3-146">-Location</span></span>
<span data-ttu-id="744a3-147">O local para armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="744a3-147">The location to store deployment data.</span></span>

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

### <span data-ttu-id="744a3-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="744a3-148">-Name</span></span>
<span data-ttu-id="744a3-149">O nome da implantação que será criada.</span><span class="sxs-lookup"><span data-stu-id="744a3-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="744a3-150">Só é válido quando um modelo é usado.</span><span class="sxs-lookup"><span data-stu-id="744a3-150">Only valid when a template is used.</span></span>
<span data-ttu-id="744a3-151">Quando um modelo é usado, se o usuário não especifica um nome de implantação, use a hora atual, como "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="744a3-151">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744a3-152">-Pre</span><span class="sxs-lookup"><span data-stu-id="744a3-152">-Pre</span></span>
<span data-ttu-id="744a3-153">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="744a3-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="744a3-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="744a3-154">-TemplateFile</span></span>
<span data-ttu-id="744a3-155">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="744a3-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="744a3-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="744a3-156">-TemplateParameterFile</span></span>
<span data-ttu-id="744a3-157">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="744a3-157">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744a3-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="744a3-158">-TemplateParameterObject</span></span>
<span data-ttu-id="744a3-159">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="744a3-159">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744a3-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="744a3-160">-TemplateParameterUri</span></span>
<span data-ttu-id="744a3-161">URL para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="744a3-161">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744a3-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="744a3-162">-TemplateUri</span></span>
<span data-ttu-id="744a3-163">URL para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="744a3-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="744a3-164">-Confirme</span><span class="sxs-lookup"><span data-stu-id="744a3-164">-Confirm</span></span>
<span data-ttu-id="744a3-165">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="744a3-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744a3-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="744a3-166">-WhatIf</span></span>
<span data-ttu-id="744a3-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="744a3-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="744a3-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="744a3-168">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744a3-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744a3-169">CommonParameters</span></span>
<span data-ttu-id="744a3-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="744a3-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744a3-171">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="744a3-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744a3-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="744a3-172">INPUTS</span></span>

### <span data-ttu-id="744a3-173">System. String</span><span class="sxs-lookup"><span data-stu-id="744a3-173">System.String</span></span>
<span data-ttu-id="744a3-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="744a3-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="744a3-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="744a3-175">OUTPUTS</span></span>

### <span data-ttu-id="744a3-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="744a3-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="744a3-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="744a3-177">NOTES</span></span>

## <span data-ttu-id="744a3-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="744a3-178">RELATED LINKS</span></span>
