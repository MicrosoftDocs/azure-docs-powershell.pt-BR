---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 51d0405ffbedf5ad5a708fdcf9184ef49dc6ecdb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785842"
---
# <span data-ttu-id="0a273-101">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="0a273-101">Test-AzureRmDeployment</span></span>

## <span data-ttu-id="0a273-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a273-102">SYNOPSIS</span></span>
<span data-ttu-id="0a273-103">Valida uma implantação.</span><span class="sxs-lookup"><span data-stu-id="0a273-103">Validates a deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a273-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a273-104">SYNTAX</span></span>

### <span data-ttu-id="0a273-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="0a273-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a273-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0a273-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a273-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0a273-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a273-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0a273-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a273-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0a273-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a273-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0a273-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a273-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0a273-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a273-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0a273-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a273-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a273-113">DESCRIPTION</span></span>
<span data-ttu-id="0a273-114">O cmdlet **Test-AzureRmDeployment** determina se um modelo de implantação e seus valores de parâmetro são válidos.</span><span class="sxs-lookup"><span data-stu-id="0a273-114">The **Test-AzureRmDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="0a273-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a273-115">EXAMPLES</span></span>

### <span data-ttu-id="0a273-116">Exemplo 1: implantação de teste com um arquivo de modelo e um arquivo de parâmetro personalizado</span><span class="sxs-lookup"><span data-stu-id="0a273-116">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\>Test-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="0a273-117">Esse comando testa a implantação no escopo de assinatura atual usando o arquivo de modelo e o arquivo de parâmetros fornecido.</span><span class="sxs-lookup"><span data-stu-id="0a273-117">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

## <span data-ttu-id="0a273-118">OS</span><span class="sxs-lookup"><span data-stu-id="0a273-118">PARAMETERS</span></span>

### <span data-ttu-id="0a273-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0a273-119">-ApiVersion</span></span>
<span data-ttu-id="0a273-120">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="0a273-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0a273-121">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="0a273-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0a273-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a273-122">-DefaultProfile</span></span>
<span data-ttu-id="0a273-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a273-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a273-124">-Local</span><span class="sxs-lookup"><span data-stu-id="0a273-124">-Location</span></span>
<span data-ttu-id="0a273-125">O local para armazenar os dados de implantação.</span><span class="sxs-lookup"><span data-stu-id="0a273-125">The location to store deployment data.</span></span>

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

### <span data-ttu-id="0a273-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="0a273-126">-Pre</span></span>
<span data-ttu-id="0a273-127">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="0a273-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0a273-128">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0a273-128">-TemplateFile</span></span>
<span data-ttu-id="0a273-129">Caminho local para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="0a273-129">Local path to the template file.</span></span>

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

### <span data-ttu-id="0a273-130">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0a273-130">-TemplateParameterFile</span></span>
<span data-ttu-id="0a273-131">Um arquivo que tem os parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="0a273-131">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="0a273-132">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="0a273-132">-TemplateParameterObject</span></span>
<span data-ttu-id="0a273-133">Uma tabela de hash que representa os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0a273-133">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="0a273-134">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="0a273-134">-TemplateParameterUri</span></span>
<span data-ttu-id="0a273-135">URL para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="0a273-135">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="0a273-136">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="0a273-136">-TemplateUri</span></span>
<span data-ttu-id="0a273-137">URL para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="0a273-137">Uri to the template file.</span></span>

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

### <span data-ttu-id="0a273-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a273-138">CommonParameters</span></span>
<span data-ttu-id="0a273-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a273-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a273-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a273-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a273-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a273-141">INPUTS</span></span>

### <span data-ttu-id="0a273-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0a273-142">System.String</span></span>
<span data-ttu-id="0a273-143">Microsoft. Azure. Management. ResourceManager. Models. Deploymentmode System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0a273-143">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode System.Collections.Hashtable</span></span>

## <span data-ttu-id="0a273-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a273-144">OUTPUTS</span></span>

### <span data-ttu-id="0a273-145">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="0a273-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="0a273-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a273-146">NOTES</span></span>

## <span data-ttu-id="0a273-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a273-147">RELATED LINKS</span></span>
