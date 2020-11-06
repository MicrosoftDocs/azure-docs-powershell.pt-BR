---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 514d1257d917dc1bbf20f93d05236af9f36bd832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428794"
---
# <span data-ttu-id="a1c10-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a1c10-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="a1c10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1c10-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c10-103">Adiciona uma implantação do Azure a um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1c10-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1c10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1c10-104">SYNTAX</span></span>

### <span data-ttu-id="a1c10-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1c10-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1c10-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a1c10-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1c10-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a1c10-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1c10-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a1c10-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1c10-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a1c10-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1c10-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a1c10-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1c10-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a1c10-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1c10-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a1c10-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1c10-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1c10-113">DESCRIPTION</span></span>
<span data-ttu-id="a1c10-114">O cmdlet **New-AzureRmResourceGroupDeployment** adiciona uma implantação a um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="a1c10-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="a1c10-115">Isso inclui os recursos que a implantação requer.</span><span class="sxs-lookup"><span data-stu-id="a1c10-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="a1c10-116">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados, site, máquina virtual ou conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a1c10-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="a1c10-117">Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade, como o site, o servidor de banco de dados e bancos de dados necessários para um site financeiro.</span><span class="sxs-lookup"><span data-stu-id="a1c10-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="a1c10-118">Uma implantação de grupo de recursos usa um modelo para adicionar recursos a um grupo de recursos e os publica para que eles estejam disponíveis no Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c10-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="a1c10-119">Para adicionar recursos a um grupo de recursos sem usar um modelo, use o cmdlet New-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="a1c10-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="a1c10-120">Para adicionar uma implantação de grupo de recursos, especifique o nome de um grupo de recursos existente e um modelo de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1c10-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="a1c10-121">Um modelo de grupo de recursos é uma cadeia de caracteres JSON que representa um grupo de recursos para um serviço complexo baseado em nuvem, como um portal da Web.</span><span class="sxs-lookup"><span data-stu-id="a1c10-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="a1c10-122">O modelo inclui espaços reservados de parâmetro para recursos obrigatórios e valores de propriedade configuráveis, como nomes e tamanhos.</span><span class="sxs-lookup"><span data-stu-id="a1c10-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="a1c10-123">Você pode encontrar muitos modelos na Galeria de modelos do Azure ou pode criar seus próprios modelos.</span><span class="sxs-lookup"><span data-stu-id="a1c10-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="a1c10-124">Você pode usar o cmdlet **Get-AzureRmResourceGroupGalleryTemplate** para localizar um modelo na galeria.</span><span class="sxs-lookup"><span data-stu-id="a1c10-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="a1c10-125">Para usar um modelo personalizado para criar um grupo de recursos, especifique o parâmetro *TemplateFile* ou o parâmetro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="a1c10-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="a1c10-126">Cada modelo tem parâmetros para propriedades configuráveis.</span><span class="sxs-lookup"><span data-stu-id="a1c10-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="a1c10-127">Para especificar valores para os parâmetros de modelo, especifique o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="a1c10-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="a1c10-128">Você também pode usar os parâmetros de modelo que são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="a1c10-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="a1c10-129">Para usar parâmetros dinâmicos, digite-os no prompt de comando ou digite um sinal de subtração (-) para indicar um parâmetro e use a tecla Tab para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a1c10-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="a1c10-130">Os valores de parâmetro de modelo que você insere no prompt de comando prevalecem sobre os valores em um objeto ou arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="a1c10-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="a1c10-131">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1c10-131">EXAMPLES</span></span>

### <span data-ttu-id="a1c10-132">Exemplo 1: usar um modelo personalizado e um arquivo de parâmetro para criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="a1c10-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="a1c10-133">Esse comando cria uma nova implantação usando um modelo personalizado e um arquivo de modelo no disco.</span><span class="sxs-lookup"><span data-stu-id="a1c10-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="a1c10-134">O comando usa o parâmetro *TemplateFile* para especificar o modelo e o parâmetro *TemplateParameterFile* para especificar um arquivo que contém parâmetros e valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a1c10-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="a1c10-135">Ele usa o parâmetro *TemplateVersion* para especificar a versão do modelo.</span><span class="sxs-lookup"><span data-stu-id="a1c10-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="a1c10-136">OS</span><span class="sxs-lookup"><span data-stu-id="a1c10-136">PARAMETERS</span></span>

### <span data-ttu-id="a1c10-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a1c10-137">-ApiVersion</span></span>
<span data-ttu-id="a1c10-138">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1c10-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a1c10-139">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="a1c10-139">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a1c10-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1c10-140">-AsJob</span></span>
<span data-ttu-id="a1c10-141">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a1c10-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1c10-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c10-142">-DefaultProfile</span></span>
<span data-ttu-id="a1c10-143">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a1c10-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1c10-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="a1c10-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="a1c10-145">Especifica um nível de log de depuração.</span><span class="sxs-lookup"><span data-stu-id="a1c10-145">Specifies a debug log level.</span></span>
<span data-ttu-id="a1c10-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a1c10-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1c10-147">RequestContent</span><span class="sxs-lookup"><span data-stu-id="a1c10-147">RequestContent</span></span>
- <span data-ttu-id="a1c10-148">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="a1c10-148">ResponseContent</span></span>
- <span data-ttu-id="a1c10-149">Todo</span><span class="sxs-lookup"><span data-stu-id="a1c10-149">All</span></span>
- <span data-ttu-id="a1c10-150">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a1c10-150">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c10-151">-Force</span><span class="sxs-lookup"><span data-stu-id="a1c10-151">-Force</span></span>
<span data-ttu-id="a1c10-152">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a1c10-152">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1c10-153">-Mode</span><span class="sxs-lookup"><span data-stu-id="a1c10-153">-Mode</span></span>
<span data-ttu-id="a1c10-154">Especifica o modo de implantação.</span><span class="sxs-lookup"><span data-stu-id="a1c10-154">Specifies the deployment mode.</span></span> <span data-ttu-id="a1c10-155">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a1c10-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1c10-156">Assuma</span><span class="sxs-lookup"><span data-stu-id="a1c10-156">Complete</span></span>
- <span data-ttu-id="a1c10-157">Adicionais</span><span class="sxs-lookup"><span data-stu-id="a1c10-157">Incremental</span></span>

<span data-ttu-id="a1c10-158">No modo completo, o Gerenciador de recursos exclui recursos que existem no grupo de recursos, mas que não estão especificados no modelo.</span><span class="sxs-lookup"><span data-stu-id="a1c10-158">In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="a1c10-159">No modo incremental, o Gerenciador de recursos deixa os recursos inalterados que existem no grupo de recursos, mas não estão especificados no modelo.</span><span class="sxs-lookup"><span data-stu-id="a1c10-159">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c10-160">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1c10-160">-Name</span></span>
<span data-ttu-id="a1c10-161">Especifica o nome da implantação do grupo de recursos a ser criada.</span><span class="sxs-lookup"><span data-stu-id="a1c10-161">Specifies the name of the resource group deployment to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c10-162">-Pre</span><span class="sxs-lookup"><span data-stu-id="a1c10-162">-Pre</span></span>
<span data-ttu-id="a1c10-163">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="a1c10-163">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a1c10-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c10-164">-ResourceGroupName</span></span>
<span data-ttu-id="a1c10-165">Especifica o nome do grupo de recursos a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="a1c10-165">Specifies the name of the resource group to deploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c10-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a1c10-166">-TemplateFile</span></span>
<span data-ttu-id="a1c10-167">Especifica o caminho completo de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="a1c10-167">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="a1c10-168">Pode ser um modelo personalizado ou um modelo de galeria salvo como um arquivo JSON, como um criado usando o cmdlet **Save-AzureRmResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="a1c10-168">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="a1c10-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a1c10-169">-TemplateParameterFile</span></span>
<span data-ttu-id="a1c10-170">Especifica o caminho completo de um arquivo JSON que contém os nomes e os valores dos parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="a1c10-170">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="a1c10-171">Se um modelo tem parâmetros, você deve especificar os valores de parâmetro com o parâmetro *TemplateParameterFile* ou o parâmetro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="a1c10-171">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="a1c10-172">Os parâmetros do modelo são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="a1c10-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="a1c10-173">Para usar os parâmetros dinâmicos, digite um sinal de subtração (-) para indicar um nome de parâmetro e use a tecla Tab para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a1c10-173">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="a1c10-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="a1c10-174">-TemplateParameterObject</span></span>
<span data-ttu-id="a1c10-175">Especifica uma tabela de hash de nomes e valores de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="a1c10-175">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="a1c10-176">Para obter ajuda com tabelas de hash no Windows PowerShell, digite `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="a1c10-176">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="a1c10-177">Se um modelo tem parâmetros, você deve especificar valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a1c10-177">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="a1c10-178">Os parâmetros do modelo são adicionados dinamicamente ao comando quando você especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="a1c10-178">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="a1c10-179">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="a1c10-179">-TemplateParameterUri</span></span>
<span data-ttu-id="a1c10-180">Especifica o URI de um arquivo de parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="a1c10-180">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="a1c10-181">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a1c10-181">-TemplateUri</span></span>
<span data-ttu-id="a1c10-182">Especifica o URI de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="a1c10-182">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="a1c10-183">Esse arquivo pode ser um modelo personalizado ou um modelo de galeria salvo como um arquivo JSON, por exemplo, usando **Save-AzureRmResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="a1c10-183">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="a1c10-184">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1c10-184">-Confirm</span></span>
<span data-ttu-id="a1c10-185">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1c10-185">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c10-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1c10-186">-WhatIf</span></span>
<span data-ttu-id="a1c10-187">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1c10-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1c10-188">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1c10-188">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c10-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c10-189">CommonParameters</span></span>
<span data-ttu-id="a1c10-190">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c10-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c10-191">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c10-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c10-192">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1c10-192">INPUTS</span></span>

### <span data-ttu-id="a1c10-193">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a1c10-193">None</span></span>

## <span data-ttu-id="a1c10-194">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1c10-194">OUTPUTS</span></span>

### <span data-ttu-id="a1c10-195">Microsoft. Azure. Commands. ResourceManager. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a1c10-195">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="a1c10-196">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1c10-196">NOTES</span></span>

## <span data-ttu-id="a1c10-197">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1c10-197">RELATED LINKS</span></span>

[<span data-ttu-id="a1c10-198">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a1c10-198">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a1c10-199">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a1c10-199">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="a1c10-200">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a1c10-200">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="a1c10-201">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a1c10-201">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a1c10-202">Parar-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a1c10-202">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a1c10-203">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a1c10-203">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


